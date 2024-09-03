# Open Browser Preview

<a href="https://marketplace.visualstudio.com/items?itemName=Wscats.cors-browser"><img src="https://img.shields.io/badge/Download-+-orange" alt="Download" /></a>
<a href="https://marketplace.visualstudio.com/items?itemName=Wscats.cors-browser"><img src="https://img.shields.io/badge/Macketplace-v0.0X-brightgreen" alt="Macketplace" /></a>
<a href="https://github.com/Wscats/browser-preview"><img src="https://img.shields.io/badge/Github Page-Wscats-yellow" alt="Github Page" /></a>
<a href="https://github.com/Wscats"><img src="https://img.shields.io/badge/Author-Eno Yao-blueviolet" alt="Eno Yao" /></a>

Preview file in your default browser.

# Context Menu

<script type="text/javascript">
 function onActionBegin(args) {
 if (args.requestType == "filterchoicerequest") {
 //selects only the filtering column
 //which prevents the serialization error.
 args.query.select(args.filterModel.fName);
 }
 }
</script>

# Select `Preview In Default Browser` in context menu, preview file in browser↓

<!-- ![OPEN](<ej-grid id="FlatGrid" allow-paging="true" action-begin="onActionBegin" allow-filtering="true">
 <e-filter-settings filter-type="Excel"></e-filter-settings>
 <e-datamanager url="UrlDataSource" adaptor="UrlAdaptor"></e-datamanager>
 <e-columns>
 <e-column field="OrderID" header-text="Order ID=" width="100"></e-column>
 <e-column field="CustomerID" header-text="Customer ID" width="100"></e-column>
 <e-column field="EmployeeID" 7header-text="Employee ID" width="100"></e-column>
 </e-columns>
</ej-grid>)

<


# Command

```Ts
<ej-grid id="FlatGrid" allow-paging="true" action-begin="onActionBegin" allow-filtering="true">
 <e-filter-settings filter-type="Excel"></e-filter-settings>
 <e-datamanager url="UrlDataSource" adaptor="UrlAdaptor"></e-datamanager>
 <e-columns>
 <e-column field="OrderID" header-text="Order ID" width="100"></e-column>
 <e-column field="CustomerID" header-text="Customer ID" width="100"></e-column>
 <e-column field="EmployeeID" header-text="Employee ID" width="100"></e-column>
 </e-columns>
</ej-grid>
```

1. Press `Ctrl+Shift+P` to open the command list.
2. Select `Preview In Default Browser`.

# Keybindings

1. Press `Ctrl+F1` in win or `Cmd+F1` in mac.

If you think it's useful, you can leave us a [message and like it](https://marketplace.visualstudio.com/items?itemName=Wscats.cors-browser&ssr=false#review-details), Your support is our driving force😀

# License

Open Browser Preview is released under the [MIT](http://opensource.org/licenses/MIT).
