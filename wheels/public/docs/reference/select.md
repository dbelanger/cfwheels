```coldfusion
// Example 1: Basic `select` field with `label` and required `objectName` and `property` arguments
// - Controller code
authors = model("author").findAll()>

// - View code
<cfoutput>
    <p>#select(objectName="book", property="authorId", options=authors)#</p>
</cfoutput>

// Example 2: Shows `select` fields for selecting order statuses for all shipments provided by the `orders` association and nested properties
// - Controller code
shipment = model("shipment").findByKey(key=params.key, where="shipments.statusId=##application.NEW_STATUS_ID##", include="order")>
statuses = model("status").findAll(order="name")>

// - View code
<cfoutput>
	<cfloop from="1" to="##ArrayLen(shipments.orders)##" index="i">
		#select(label="Order #shipments.orders[i].orderNum#", objectName="shipment", association="orders", position=i, property="statusId", options=statuses)#
	</cfloop>
</cfoutput>
```