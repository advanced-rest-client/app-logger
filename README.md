
`<app-logger>` A logger for web components. Allows to print messages and save them into the datastore

It listening for `app-log` events and logs evens when the event occure.
The event detail object may have `level` property which describes log level of the message.
It should also contain `message` property with the message to log.

See `level` property documentation for logging level details.

This element works with `<arc-database>` element and fires an event with the log details
to store log data into the database. By default the database name is `logs`. It can be owerriten
by setting the `store` property.
This behavior can be switched off by setting `noDatabase` attribute.

Note that this element will not check for database insert errors and basically it will not react
on any error during database insert. Also it will not check if the `<arc-database>` element
exists in the documenmt. This will just fire an event and allow other elements to take care of it.

### Example
```
<app-logger level="info"></app-logger>
```

