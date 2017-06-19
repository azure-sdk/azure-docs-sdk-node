---
title: Azure App Service libraries for Node.js
description: Deploy, manage, and scale web apps, APIs, and mobile apps running in Azure App Service from your Node.js code
keywords: Azure, Node, SDK, API, web apps , mobile , nodejs, javascript
author: tomarcher
ms.author: tarcher
manager: douge
ms.date: 06/19/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: nodejs
ms.service: appservice
---

# Azure Storage Node.js modules

## Overview

Use the Azure Storage client module to:

- Read and write objects and files from [Azure Blob storage](https://docs.microsoft.com/azure/storage/storage-nodejs-how-to-use-blob-storage)
- Send and receive messages between cloud-connected applications with [Azure Queue storage](https://docs.microsoft.com/azure/storage/storage-nodejs-how-to-use-queues)
- Read and write large structured data with [Azure Table storage](https://docs.microsoft.com/azure/storage/storage-nodejs-how-to-use-table-storage) 

Create, update, and manage Azure Storage accounts and query and regenerate access keys from your Node.js apps with the management libraries.

## Install modules with npm

Use npm to install the Azure storage client or management modules.

### Client 

```
npm install azure-storage
```   

### Management

```
npm install azure-arm-storage
```   

## Example

Write a local file *data.txt* to an existing blob storage container.

```javascript
var azure = require('azure-storage');
var blobService = azure.createBlobService(storageConnectionString);
 
blobService.createBlockBlobFromLocalFile('mycontainer', 'taskblob', 'data.txt', function(error, result, response) {
  if (!error) {
    // file uploaded
  }
});
```

## Samples

[!INCLUDE [node-storage-samples](../docs-ref-conceptual/includes/storage-samples.md)]

Explore more [sample Node.js code](https://azure.microsoft.com/resources/samples/?platform=nodejs) you can use in your apps.