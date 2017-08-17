# Fork from https://github.com/wkh237/react-native-fetch-blob
- Temporary fix the issue about android upload AWS S3 content type default value. Seem latest release dose not merge [#425](https://github.com/wkh237/react-native-fetch-blob/issues/425)
- Enhance the actionViewIntent handle the file from latest android document pick standand - [SAF](https://developer.android.com/guide/topics/providers/document-provider.html). All documents are returned as 'content://xxxx'. The way we can get the file is open the filestream and save a new copy for temporary read.
- Add clean function for clean up context.getCacheDir() folder since normalizePath() will save the copy in it.
