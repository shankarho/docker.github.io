---
description: Explains how to use the Aliyun OSS storage driver
keywords: registry, service, driver, images, storage, OSS, aliyun
title: Aliyun OSS storage driver
---

An implementation of the `storagedriver.StorageDriver` interface which uses
[Aliyun OSS](https://www.alibabacloud.com/product/oss) for object storage.

## Parameters

<table>
  <thead>
    <tr>
      <th>Parameter</th>
      <th>Required</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <code>accesskeyid</code>
      </td>
      <td>
      yes
      </td>
      <td>
      Your access key ID.
      </td>
    </tr>
    <tr>
      <td>
        <code>accesskeysecret</code>
      </td>
      <td>
      yes
      </td>
      <td>
      Your access key secret.
      </td>
    </tr>
    <tr>
      <td>
        <code>region</code>
      </td>
      <td>
      yes
      </td>
      <td> The name of the OSS region in which you would like to store objects (for example <code>oss-cn-beijing</code>). For a list of regions, you can look at <a href="https://www.alibabacloud.com/help/doc-detail/31837.htm">the official documentation</a>.
      </td>
    </tr>
    <tr>
      <td>
        <code>endpoint</code>
      </td>
      <td>
      no
      </td>
      <td>
      An endpoint which defaults to <code>[bucket].[region].aliyuncs.com</code> or <code>[bucket].[region]-internal.aliyuncs.com</code> (when <code>internal=true</code>). You can change the default endpoint by changing this value.
      </td>
    </tr>
    <tr>
      <td>
        <code>internal</code>
      </td>
      <td>
      no
      </td>
      <td> An internal endpoint or the public endpoint for OSS access. The default is false.
      For a list of regions, you can look at <a href="https://www.alibabacloud.com/help/doc-detail/31837.htm">the official documentation</a>.
      </td>
    </tr>
    <tr>
      <td>
        <code>bucket</code>
      </td>
      <td>
      yes
      </td>
      <td> The name of your OSS bucket where you wish to store objects (needs to already be created prior to driver initialization).
      </td>
    </tr>
    <tr>
      <td>
        <code>encrypt</code>
      </td>
      <td>
      no
      </td>
      <td> Specifies whether you would like your data encrypted on the server side. Defaults to false if not specified.
      </td>
    </tr>
    <tr>
      <td>
        <code>secure</code>
      </td>
      <td>
      no
      </td>
      <td> Specifies whether to transfer data to the bucket over ssl or not. If you omit this value, <code>true</code> is used.
      </td>
    </tr>
    <tr>
      <td>
        <code>chunksize</code>
      </td>
      <td>
      no
      </td>
      <td> The default part size for multipart uploads (performed by WriteStream) to OSS. The default is 10 MB. Keep in mind that the minimum part size for OSS is 5MB. You might experience better performance for larger chunk sizes depending on the speed of your connection to OSS.
      </td>
    </tr>
    <tr>
      <td>
        <code>rootdirectory</code>
      </td>
      <td>
      no
      </td>
      <td> The root directory tree in which to store all registry files. Defaults to an empty string (bucket root).
      </td>
    </tr>
  </tbody>
</table>
