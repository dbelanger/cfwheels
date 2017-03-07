```coldfusion
setTableNamePrefix(prefix)
```
```coldfusion
// In `models/User.cfc`, add a prefix to the default table name of `tbl`
<cffunction name="init">
    setTableNamePrefix("tbl")>
</cffunction>
```