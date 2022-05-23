## 1.8.0

- Bump minimum Flutter version to 3.0.

- Bump minimum Dart version to 2.17.

- Improve documentation

- Make it possible to disable logging using `FlutterDownloader.initialize(debug: false)`

## 1.7.4

- fix bug SSL on Android
- merged PRs: [#635](https://github.com/fluttercommunity/flutter_downloader/pull/635), [#637](https://github.com/fluttercommunity/flutter_downloader/pull/637)

## 1.7.3

- fix bug [#614](https://github.com/fluttercommunity/flutter_downloader/issues/614)

## 1.7.2

- fix bug on Android
- upgrade Android dependencies (WorkerManager 2.7.1)

## 1.7.1

- Android: fix bug notification stuck in processing
- fix bug resume download on Android
- upgrade Android dependencies (WorkerManager 2.7.0-rc01)

## 1.7.0

- iOS: fix bug missing update download progress
- support Android 11 (ScopedStorage, PackageVisibility)

## 1.6.1

- Update `pubspec` to new format
- Upgrade `AndroidWorkManager` to v2.4.0
- fix bug on Android: `getContentLength`
- upgrade Android dependencies (WorkerManager 2.5.0)

## 1.6.0

- add `debug` (optional) parameter in `initialize()` method that supports disable logging to console
- Stable version of nullsafety

## 1.6.0-nullsafety.0

- iOS: fix bug on `remove` method
- Fix bugs
- Migrate to nullsafety

## 1.5.2

- add `timeCreated` in `DownloadTask` model
- iOS: fix bug MissingPluginException
- Android: fix bug notification stuck in processing

## 1.5.1

- Android: fix bug `ensureInitializationComplete must be called after startInitialization`
- clarify integration documents
- iOS: fix bug missing update download progress

## 1.5.0

- migrate to Android v2 embedding.
- Update `pubspec` to new format
- Upgrade `AndroidWorkManager` to v2.4.0

## 1.4.4

- fix bug stuck in Flutter v12.13
- fix bug on casting int to long value
- add `debug` (optional) parameter in `initialize()` method that supports disable logging to console

## 1.4.3

- update document
- assert and make sure FlutterDownloader initialized one time.
- iOS: fix bug on `remove` method

## 1.4.2

- correct document and example codes about communication with background isolate
- add `timeCreated` in `DownloadTask` model
- iOS: fix bug MissingPluginException

## 1.4.1

- assert the initialization of FlutterDownloader
- Android: fix bug `ensureInitializationComplete must be called after startInitialization`
- clarify integration documents

## 1.4.0

- **BREAKING CHANGES**: the plugin has been refactored to support update download events with background isolate. In order to support background execution in Dart, the `callback`, that receives events from platform codes, now must be a static or top-level function. There's also an additional native configuration required on both of iOS and Android. See README for detail.
- Android: upgrade `WorkManager` to v2.2.0.
- Fix bug `SecurityException` when saving image/videos to internal storage in Android
- Fix bug cannot save videos in Android.
- migrate to Android v2 embedding.

## 1.3.4

- Android: fix bugs
- fix bug stuck in Flutter v12.13
- fix bug on casting int to long value

## 1.3.3

- Android: hot-fix unregister `BroadcastReceiver` in case using `FlutterFragmentActivity`
- update document
- assert and make sure FlutterDownloader initialized one time.

## 1.3.2

- Android: support `FlutterFragmentActivity`, fix bug downloaded image/video files not shown in Gallery application, improved HTTP redirection implementation, fix bug cannot open apk file in some cases
- correct document and example codes about communication with background isolate

## 1.3.1

- Android: support HTTP redirection
- iOS: correct getting file name from HTTP response
- assert the initialization of FlutterDownloader

## 1.3.0

- Fix bug in iOS: from iOS 8, absolute path to app's sandbox changes every time you relaunch the app, hence `savedDir` path is needed to truncate the changing part before saving it to DB and recreate the absolute path every time it loaded from DB. Currently, the plugin only supports save files in `NSDocumentDirectory`.
- Fix bug is iOS: setting wrong status of task in case that the application is terminated
- Android: upgrade dependencies
- **BREAKING CHANGES**: the plugin has been refactored to support update download events with background isolate. In order to support background execution in Dart, the `callback`, that receives events from platform codes, now must be a static or top-level function. There's also an additional native configuration required on both of iOS and Android. See README for detail.
- Android: upgrade `WorkManager` to v2.2.0.
- Fix bug `SecurityException` when saving image/videos to internal storage in Android
- Fix bug cannot save videos in Android.

## 1.2.2

- Android: upgrade `WorkManager` to version 2.0.0 (AndroidX)
- Android: fix bugs

## 1.2.1

- Android: upgrade `WorkManager` to version 1.0.0-beta05
- Android: migrate to AndroidX
- Android: hot-fix unregister `BroadcastReceiver` in case using `FlutterFragmentActivity`

## 1.2.0

- Android: upgrade `WorkManager` to version 1.0.0-beta03
- fix bugs
- Android: support `FlutterFragmentActivity`, fix bug downloaded image/video files not shown in Gallery application, improved HTTP redirection implementation, fix bug cannot open apk file in some cases

## 1.1.9

- add `remove()` feature to delete task (in DB) and downloaded file as well (optional).
- support clean up callback by setting callback as `null` in `registerCallback()`
- Android: upgrade `WorkManager` to version 1.0.0-beta01
- Android: support HTTP redirection
- iOS: correct getting file name from HTTP response

## 1.1.8

- Android: fix bug NullPointerException of `saveFilePath`
- Fix bug in iOS: from iOS 8, absolute path to app's sandbox changes every time you relaunch the app, hence `savedDir` path is needed to truncate the changing part before saving it to DB and recreate the absolute path every time it loaded from DB. Currently, the plugin only supports save files in `NSDocumentDirectory`.
- Fix bug is iOS: setting wrong status of task in case that the application is terminated
- Android: upgrade dependencies

## 1.1.7

- Android: fix typo error
- iOS: catch HTTP status code in case of error
- Android: upgrade `WorkManager` to version 2.0.0 (AndroidX)

## 1.1.6

- correct `README` instruction
- Android: upgrade `WorkManager` to version 1.0.0-beta05
- Android: migrate to AndroidX

## 1.1.5

- Android: upgrade `WorkManager` library to version v1.0.0-alpha11
- **BREAKING CHANGE**: `initialize()` is removed (to deal with the change of the initialization of `WorkManager` in v1.0.0-alpha11). The plugin initializes itself with default configurations. If you would like to change the default configuration, you can follows the instruction in `README.md`
- Android: upgrade `WorkManager` to version 1.0.0-beta03
- fix bugs

## 1.1.4

- fix bug related to `filename`
- add `remove()` feature to delete task (in DB) and downloaded file as well (optional).
- support clean up callback by setting callback as `null` in `registerCallback()`
- Android: upgrade `WorkManager` to version 1.0.0-beta01

## 1.1.3

- Android: re-config dependencies
- Android: fix bug NullPointerException of `saveFilePath`

## 1.1.2

- Android: upgrade WorkManager to v1.0.0-alpha10
- Android: fix typo error
- iOS: catch HTTP status code in case of error

## 1.1.1

- Android: upgrade compile sdk version to 28
- correct `README` instruction

## 1.1.0

- Fixed Flutter Community badge.
- Android: upgrade `WorkManager` library to version v1.0.0-alpha11
- **BREAKING CHANGE**: `initialize()` is removed (to deal with the change of the initialization of `WorkManager` in v1.0.0-alpha11). The plugin initializes itself with default configurations. If you would like to change the default configuration, you can follows the instruction in `README.md`

## 1.0.6

- Moved package to [Flutter Community](https://github.com/fluttercommunity)
- fix bug related to `filename`

## 1.0.5

- **NEW** features: initialize, loadTasksWithRawQuery, pause, resume, retry, open
- **IMPORTANT**: the plugin must be initialized by `initialize()` at first
- **BREAKING CHANGE**: `clickToOpenDownloadedFile` now renames to `openFileFromNotification` (to prevent confusing from `open` feature). Static property `maximumConcurrentTask` has been removed, this configuration now moves into `initialize()` method.
- full support SQLite on both Android and iOS side, the plugin now itself manages its states persistently and exposes `loadTasksWithRawQuery` api that helps developers to load tasks from SQLite database with customized conditions
- support localizing Android notification messages with `messages` parameter of `initialize()` method
- full support opening and previewing downloaded file with `open()` method
- (iOS integration) no need to override `application:handleEventsForBackgroundURLSession:completionHandler:` manually anymore, the plugin now itself takes responsibility for handling it
- Android: re-config dependencies

## 1.0.4

- fix bugs: SQLite leak
- new feature: support configuration of the maximum of concurrent download tasks
- upgrade WorkManager to v1.0.0-alpha08
- Android: upgrade WorkManager to v1.0.0-alpha10

## 1.0.3

- add: handle click on notification to open downloaded file (for Android)
- Android: upgrade compile sdk version to 28

## 1.0.2

- re-config to support Dart2
- Fixed Flutter Community badge.

## 1.0.1

- upgrade WorkManager to v1.0.0-alpha06
- fix bug: disable sound on notifications
- Moved package to [Flutter Community](https://github.com/fluttercommunity)

## 1.0.0

- upgrade WorkManager to v1.0.0-alpha04
- **NEW** features: initialize, loadTasksWithRawQuery, pause, resume, retry, open
- **IMPORTANT**: the plugin must be initialized by `initialize()` at first
- **BREAKING CHANGE**: `clickToOpenDownloadedFile` now renames to `openFileFromNotification` (to prevent confusing from `open` feature). Static property `maximumConcurrentTask` has been removed, this configuration now moves into `initialize()` method.
- full support SQLite on both Android and iOS side, the plugin now itself manages its states persistently and exposes `loadTasksWithRawQuery` api that helps developers to load tasks from SQLite database with customized conditions
- support localizing Android notification messages with `messages` parameter of `initialize()` method
- full support opening and previewing downloaded file with `open()` method
- (iOS integration) no need to override `application:handleEventsForBackgroundURLSession:completionHandler:` manually anymore, the plugin now itself takes responsibility for handling it

## 0.1.1

- upgrade WorkManager to v1.0.0-alpha03
- change default value of `showNotification` to `true` (it makes sense on Android 8.0 and above, it helps our tasks not to be killed by system when the app goes to background)
- fix bugs: SQLite leak
- new feature: support configuration of the maximum of concurrent download tasks
- upgrade WorkManager to v1.0.0-alpha08

## 0.1.0

- update metadata
- add: handle click on notification to open downloaded file (for Android)

## 0.0.9

- fix bug: Worker finished with FAILURE on Android API 26 and above
- re-config to support Dart2

## 0.0.8

- support HTTP headers
- upgrade WorkManager to v1.0.0-alpha06
- fix bug: disable sound on notifications

## 0.0.7

- correct README document
- upgrade WorkManager to v1.0.0-alpha04

## 0.0.6

- upgrade WorkManager to v1.0.0-alpha03
- change default value of `showNotification` to `true` (it makes sense on Android 8.0 and above, it helps our tasks not to be killed by system when the app goes to background)

## 0.0.5

- update metadata

## 0.0.4

- fix bug: Worker finished with FAILURE on Android API 26 and above

## 0.0.3

- support HTTP headers

## 0.0.2

- correct README document

## 0.0.1

- initial release.
