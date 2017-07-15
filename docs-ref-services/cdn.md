---
title: Azure CDN modules for Node.js
description: Reference for Azure CDN modules for Node.js
keywords: Azure,SDK,API,CDN, Node.js
author: tomarcher
ms.author: tarcher
manager: douge
ms.date: 07/06/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: nodejs
ms.service: CDN
---

# Azure CDN packages for Node.js

## Overview
The Azure Content Delivery Network (CDN) offers developers a global solution for delivering high-bandwidth content that is hosted in Azure or any other location. Using the CDN, you can cache publicly available objects loaded from Azure blob storage, a web application, virtual machine, application folder, or other HTTP/HTTPS location. The CDN cache can be held at strategic locations to provide maximum bandwidth for delivering content to users. The CDN is typically used for delivering static content such as images, style sheets, documents, files, client-side scripts, and HTML pages.

## Management Package
### Install npm module
```bash
npm install azure-arm-cdn
```

### Example
```javascript
const msRestAzure = require('ms-rest-azure');
const cdnManagementClient = require('azure-arm-cdn');

const subscriptionId = 'your-subscription-id';
let cdnClient;

msRestAzure.interactiveLogin((err, credentials) => {
  cdnClient = new cdnManagementClient(credentials, subscriptionId);
  cdnClient.profiles
    .list()
    .then(profilesList => console.log('Retrieved profiles list: ', profilesList));
});
```

### Samples

Explore more [sample Node.js code](https://azure.microsoft.com/resources/samples/?platform=nodejs) you can use in your apps.