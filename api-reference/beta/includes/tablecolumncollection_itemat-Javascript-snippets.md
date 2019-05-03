
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const workbookTableColumn = {
  index: {
  }
};

let res = await client.api('/me/drive/items/{id}/workbook/tables/{id|name}/columns/ItemAt')
	.version('beta')
	.post({workbookTableColumn : workbookTableColumn});

```