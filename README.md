# Fork from https://github.com/wkh237/react-native-fetch-blob
- **Fix android upload assign default value to content-type**. Seem latest release dose not merge [#425](https://github.com/wkh237/react-native-fetch-blob/issues/425)

- (Android) **Enhance the actionViewIntent** handle the file from latest android document pick standand - [SAF](https://developer.android.com/guide/topics/providers/document-provider.html). All documents are returned as 'content://xxxx'. We can get the filestream and save a new copy for temporary read.

- (Android) **Add cleanExternalCache function** for clean up context.getExternalCacheDir() folder since normalizePath(saveExternal) will save the copy mentioned above into the folder.

For S3: 
```
if((mheaders.containsKey("Content-Type".toLowerCase()) ||
mheaders.containsKey("Content-Type")) &&
cType.isEmpty()){
//NOTE AWS S3 special handle
}
}
```
