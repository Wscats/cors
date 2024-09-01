# Open Browser Preview

<a href="https://marketplace.visualstudio.com/items?itemName=Wscats.cors-browser"><img name: Lint
on:
  push:
    branches: [main]
  pull_request:

concurrency:
  group: ${{ github.workflow }}-${{ github.head_ref || github.run_id }}
  cancel-in-progress: ${{ github.event_name == 'pull_request' }}

permissions:
  actions: write
  contents: read
  pull-requests: read

jobs:
  determine_jobs:
    name: Determine jobs to run
    runs-on: ubuntu-latest
    permissions:
      contents: read
      pull-requests: write
    steps:
      - name: Checkout
        uses: actions/checkout@v3

      - name: CI related changes
        id: ci
        uses: technote-space/get-diff-action@v6
        with:
          PATTERNS: |
            .github/actions/**
            .github/workflows/lint.yml

      - name: Rust related changes
        id: rust
        uses: technote-space/get-diff-action@v6
        with:
          PATTERNS: |
            pnpm-lock.yaml
            package.json
            Cargo.**
            crates/**
            shim/**
            xtask/**
            .cargo/**
            rust-toolchain
            !**.md
            !**.mdx

      - name: Formatting related changes
        id: format
        uses: technote-space/get-diff-action@v6
        with:
          PATTERNS: |
            **/*.{yml,yaml,md,mdx,js,jsx,ts,tsx,json,toml,css}

    outputs:
      rust: ${{ steps.ci.outputs.diff != '' || steps.rust.outputs.diff != '' }}
      format: ${{ steps.ci.outputs.diff != '' || steps.format.outputs.diff != '' }}

  rust_lint:
    needs: [determine_jobs]
    if: needs.determine_jobs.outputs.rust == 'true'
    name: Rust lints
    runs-on:
      - "self-hosted"
      - "linux"
      - "x64"
      - "metal"
    steps:
      - name: Checkout
        uses: actions/checkout@v3

      - name: Setup Rust
        uses: ./.github/actions/setup-rust
        with:
          github-token: "${{ secrets.GITHUB_TOKEN }}"

      - name: Run cargo fmt check
        run: |
          cargo fmt --check

      - name: Check Cargo.toml formatting (taplo)
        run: npx @taplo/cli@0.5.2 format --check

      - name: Check licenses
        uses: EmbarkStudios/cargo-deny-action@v1
        with:
          command: check licenses

          function checkWinner(){
  
    var firstSlot = slotMac1.getBoundingClientRect(),
        secondSlot = slotMac2.getBoundingClientRect(),
        lastSlot = slotMac3.getBoundingClientRect(),
        loserModal = document.querySelector('.loser-modal'),
        winnerModal = document.querySelector('.winner-modal'),
  
      r1 = document.elementFromPoint(firstSlot.x+(firstSlot.width/2),firstSlot.y+(firstSlot.height/2+10)),
      r2 = document.elementFromPoint(secondSlot.x+(secondSlot.width/2),secondSlot.y+(secondSlot.height/2+10)),
      r3 = document.elementFromPoint(lastSlot.x+(lastSlot.width/2),lastSlot.y+(lastSlot.height/2+10));
    
    setTimeout(() => {
      if (r1.parentElement.textContent == r2.parentElement.textContent && r1.parentElement.textContent == r3.parentElement.textContent && rnd <= totalWRates) {
        winnerModal.innerHTML = `
        <div class="modal-title" >Tebrikler</div>
        <div class="modal-subtitle">%20 indirim kazandınız.</div>
        <div class="wis-code">F53DWE</div>
      `;
        winnerModal.style.display = 'flex';
      } else {
        loserModal.innerHTML = `
        <div class="modal-title" >Üzgünüm Kazanamadın</div>
        <button class="try-again-btn">Yeniden Dene</button>
      `;
        loserModal.style.display = 'flex';
        var againBtn = document.querySelector('.try-again-btn');
        if(gameCount > 0){
          gameCount--;
          againBtn.addEventListener('click', function () {
            rnd = randomInt(0, 100);
  
            loserModal.style.display = 'none';
  
            slotMac1.style = '';
            slotMac2.style = '';
            slotMac3.style = '';
            slotMac1.style = '';
            slotMac2.style = '';
            slotMac3.style = '';
            spin();
            wisText.innerHTML = "<span class='wis-starter-txt'> You can spin "+gameCount+" more times.</span>"
          });
        }else{
          againBtn.textContent = 'Tüm Hakların Bitti';
          againBtn.disabled = true;
        }
      }
    }, 400);
  }
          
  format_lint:
    name: Formatting
    runs-on:
      - "self-hosted"
      - "linux"
      - "x64"
      - "metal"
    needs: determine_jobs
    if: needs.determine_jobs.outputs.format == 'true'
    env:
      TURBO_TOKEN: ${{ secrets.TURBO_TOKEN }}
      TURBO_TEAM: ${{ vars.TURBO_TEAM }}
      TURBO_REMOTE_ONLY: true
    steps:
      - name: Checkout
        uses: actions/checkout@v3

      - name: "Setup Node"
        uses: ./.github/actions/setup-node
        with:
          extra-flags: --no-optional
          node-version: "20"

      - name: Install Global Turbo
        uses: ./.github/actions/install-global-turbo

      - name: Lint
        run: |
          turbo run lint --env-mode=strict

  cleanup:
    name: Cleanup
    needs:
      - rust_lint
      - format_lint
    if: always()
    uses: ./.github/workflows/pr-clean-caches.yml
    secrets: inherit
      init();
  spin();
    /*Start Spin*/
    leverBall.addEventListener('click',function(){
    leverBall.classList.add('downBall');
    leverBar.classList.add ('downBar');
    slotMac1.classList.add('animation1');
    slotMac2.classList.add('animation2');
    slotMac3.classList.add('animation3');
  });
src="https://img.shields.io/badge/Download-+-orange" alt="Download" /></a>
<a href="https://marketplace.visualstudio.com/items?itemName=Wscats.cors-browser"><img src="https://img.shields.io/badge/Macketplace-v0.0X-brightgreen" alt="Macketplace" /></a>
<a href="https://github.com/Wscats/browser-preview"><img src="https://img.shields.io/badge/Github Page-Wscats-yellow" alt="Github Page" /></a>
<a href="https://github.com/Wscats"><img src="https://img.shields.io/badge/Author-Eno Yao-blueviolet" alt="Eno Yao" /></a>

Preview file in your default browser.

# Context Menu

Select `Preview In Default Browser` in context menu, preview file in browser↓

<!-- ![DEMO](./assets/2.gif) -->
![2](https://user-images.githubusercontent.com/17243165/100516702-a106ee80-31c0-11eb-8d85-89b1567810bb.gif)


# Command

1. Press `Ctrl+Shift+P` to open the command list.
2. Select `Preview In Default Browser`.

# Keybindings

1. Press `Ctrl+F1` in win or `Cmd+F1` in mac.

If you think it's useful, you can leave us a [message and like it](https://marketplace.visualstudio.com/items?itemName=Wscats.cors-browser&ssr=false#review-details), Your support is our driving force😀

# License

Open Browser Preview is released under the [MIT](http://opensource.org/licenses/MIT).
