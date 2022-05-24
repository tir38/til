# Android Readings

_Links get added to this list, but rarely removed. So some of this information may become data and may even become 'no longer best practices'. Always check the date on articles to see how relevant they are._

## Good Habits
*I'm not a great programmer; I'm just a good programmer with great habits.* - Kent Beck

There are some things that I regularly need to come back to and refresh myself on.

### Software Dev Soft Skills
* [How to Write a Git Commit Message](http://chris.beams.io/posts/git-commit/)
* [Don't Re-estimate Stories](https://www.mountaingoatsoftware.com/blog/to-re-estimate-or-not-that-is-the-question)
* [How to squash commits with CL rebase](http://gitready.com/advanced/2009/02/10/squashing-commits-with-rebase.html)
* [Git workflow model](http://nvie.com/posts/a-successful-git-branching-model/)
* [git merge vs git rebase](https://www.atlassian.com/git/tutorials/merging-vs-rebasing)
* [Data model mapping between architecture layers](https://overflow.buffer.com/2017/12/21/even-map-though-data-model-mapping-android-apps/)

### Testing
* [Don't Mock What You Don't Own](https://blog.8thlight.com/eric-smith/2011/10/27/thats-not-yours.html)
* [Proper Naming of Test Doubles](https://blog.8thlight.com/uncle-bob/2014/05/14/TheLittleMocker.html)
* [Principles of Test Automation](http://xunitpatterns.com/Principles%20of%20Test%20Automation.html#Use%20the%20Front%20Door%20First) (useful beyond the "automation" part)
* [Avoid Nested Mocks](https://www.destroyallsoftware.com/blog/2014/test-isolation-is-about-avoiding-mocks)

### Style Guides
* [The best Android style guide](https://github.com/bufferapp/android-guidelines/blob/master/project_style_guidelines.md)

### Android Studio Tips
* [50 Android Studio tips](https://medium.com/@mmbialas/50-android-studio-tips-tricks-resources-you-should-be-familiar-with-as-an-android-developer-af86e7cf56d2#.zdg2tg99u)

### Crash Early; Crash Often
* [Why your app should crash](https://jeroenmols.com/blog/2017/03/08/appcrash/)
* [Instagram Design Philosophy](https://instagram-engineering.com/instagram-android-four-years-later-927c166b0201)

>Almost all complex business logic happens server-side, where it is easier to fix bugs and add new features. We rely on the server to be perfect, enforced through continuous integration testing, and dispense with null-checking or data-consistency checking on the client. Because of this, the app crashes when there is malformed data, rather than remain in a weird state. Our automated crash reporting triggers alarms and an investigation, and we can fix the bug. It is much easier to fix a crash, with an attached stack trace, than to debug a weird state issue based on a user’s report.

* [Square's Crash Fast approach](https://vimeo.com/145042944)

### Design Patterns
* [Functional Core / Imperetive Shell](https://github.com/kbilsted/Functional-core-imperative-shell/blob/master/README.md)

## Reading List

### Android (hairball)
* [RxJava2Debug](https://github.com/akaita/RxJava2Debug)
* https://blog.stylingandroid.com/the-trouble-with-clickablespan/
* https://code.tutsplus.com/tutorials/introduction-to-android-architecture--cms-28749
* http://blog.danlew.net/2017/08/02/why-not-rxlifecycle
* https://rongi.github.io/kotlin-blog/rxjava/rx/2017/08/01/error-handling-in-rxjava.html
* https://medium.com/@Pinterest_Engineering/the-case-against-kotlin-2c574cb87953
* https://www.bignerdranch.com/blog/bluetooth-low-energy-part-1/
* https://blog.stylingandroid.com/architecture-components-summary/
* https://medium.com/@skaliakoudas/decreasing-build-times-by-decreasing-gradle-memory-requirements-7fcafc6d98ea
* https://jeroenmols.com/blog/2017/06/14/androidstudio3/ (gradle's  `api` vs `implementation`)
* [The Importance of Thread Priority video](https://www.youtube.com/watch?v=NwFXVsM15Co)
* https://proandroiddev.com/solid-android-analytics-with-rxjava2-6270ce8c26f9
* [Time Libs in Android, pt1](https://blog.stylingandroid.com/time-for-non-time-lords-part-1)
* [Understanding the performance benefits of ConstraintLayout](https://android-developers.googleblog.com/2017/08/understanding-performance-benefits-of.html)
* [Bluetooth attribute caching problems](https://punchthrough.com/blog/posts/attribute-caching-in-ble-advantages-and-pitfalls)
* [Instant Apps SDK 1.1](https://android-developers.googleblog.com/2017/10/introducing-android-instant-apps-sdk-11.html)
* [Random Musings on the Android 8.1 Developer Preview 1](https://commonsware.com/blog/2017/10/25/random-musings-android-8p1-developer-preview-1.html)
* [Exploring Background Execution Limits on Android Oreo](https://medium.com/exploring-android/exploring-background-execution-limits-on-android-oreo-ab384762a66c)
* [Improving performance with background data prefetching](https://engineering.instagram.com/improving-performance-with-background-data-prefetching-b191acb39898)
* [Practical Data Structures Guide for Android developers](https://blog.mindorks.com/practical-data-structures-guide-for-android-developers-73fdec190802)
* [Android tools options for layout editor, pt 1](https://blog.stylingandroid.com/tool-time-part-1-2/)
* [Android tools options for layout editor, pt 2](https://blog.stylingandroid.com/tool-time-part-2/)
* [Improve cold start times](https://redfin.engineering/how-we-improved-our-android-app-cold-start-time-by-28-a722e231314a)
* [Renaming build.gradle files for each module](http://www.developerphil.com/renaming-your-gradle-build-files/)
* [Performance drawbacks of Vector Images](https://medium.com/upday-devs/optimizing-the-performance-of-vector-drawables-680a4c456286)
* [Window fitting VIDEO](https://www.youtube.com/watch?reload=9&v=_mGDMVRO3iE)
* [Google I/O 2018 app animations](https://medium.com/androiddevelopers/animating-on-a-schedule-8a90d812ae4)
* [Google I/O 2018 app architecture](https://medium.com/androiddevelopers/google-i-o-2018-app-architecture-and-testing-f546e37fc7eb)
* [droidcon NYC 2017 - Optimizing Dagger on Android](https://www.youtube.com/watch?v=PBrhRvhF00k)
* [Introduction to MotionLayout, pt1](https://medium.com/google-developers/introduction-to-motionlayout-part-i-29208674b10d)
* [Udacity's experience with ReactNative](https://engineering.udacity.com/react-native-a-retrospective-from-the-mobile-engineering-team-at-udacity-89975d6a8102)
* [Retrofit uses Proxies](https://proandroiddev.com/how-does-retrofit-work-6ecad1bb683b)
* [Styles, Themes, Text Appearnce, and attributes](https://medium.com/androiddevelopers/whats-your-text-s-appearance-f3a1729192d)
* [Android's Java 8 Support](http://jakewharton.com/androids-java-8-support/)
* [Android's Java 9, 10, 11, and 12 Support](http://jakewharton.com/androids-java-9-10-11-and-12-support/)
* [Digging into D8 and R8](https://www.youtube.com/watch?v=99H7COwhIpI)
* [Why I Will Not Use Architecture Navigation Component](https://proandroiddev.com/why-i-will-not-use-architecture-navigation-component-97d2ad596b36)
* [Exploring Android Thread Priority](https://link.medium.com/Klt0byNn7Q)


### Android P changes
* [Changes to @hide](https://commonsware.com/blog/2018/01/18/think-hard-about-hide.html)
* [Precomputed text in recycylerview](https://medium.com/androiddevelopers/prefetch-text-layout-in-recyclerview-4acf9103f438)

### Android Accessibility
* [Making you App Switch Access Compatible](https://riggaroo.co.za/android-accessibility-switch-access)

### CI
* [Parallel workflows in Bitrise](https://medium.com/@bitrise/start-multiple-builds-with-the-same-trigger-on-bitrise-1d46ca847b9e)

### Compose
* [Compose from First Principles](http://intelligiblebabble.com/compose-from-first-principles/)
* [A Jetpack Compose by any other name](https://jakewharton.com/a-jetpack-compose-by-any-other-name/) (history of Compose project and origins on name)
* [Migrating to Compose](https://compose.academy/blog/migrating_to_compose_-_composeview) (helpful in understanding how to migrate a single view to use composeUi and still use that view inside an existing android.view hierarchy)

### General Software
* https://testing.googleblog.com/2017/07/code-health-to-comment-or-not-to-comment.html
* [The Harmful Consequences of Postel's Maxim](https://tools.ietf.org/html/draft-thomson-postel-was-wrong-01)
* [Don't make objects that end with 'er'.](http://objology.blogspot.com/2011/09/one-of-best-bits-of-programming-advice.html)
* [Your Coding Conventions Are Hurting You](http://www.carlopescio.com/2011/04/your-coding-conventions-are-hurting-you.html) (follow up to "Don't make objects that end with 'er'.")
* [Better commit messages](https://medium.com/square-corner-blog/how-square-writes-commit-messages-8e92fcbf77c9)

### Process
* https://www.linkedin.com/pulse/20140715230840-3372859-agile-basics-estimating-the-unknown
* https://www.leadingagile.com/2015/07/estimating-placeholder-stories-is-a-bad-practice/
* https://medium.com/bynder-tech/12-common-mistakes-made-when-using-story-points-f0bb9212d2f7
* [Too many comments in your code review](http://testing.googleblog.com/2017/06/code-health-too-many-comments-on-your.html)

### Testing (inc. Android Testing)
* https://android-developers.googleblog.com/2017/07/android-testing-support-library-10-is.html
* https://www.bignerdranch.com/blog/mockito-2-updates-and-issues/
* https://github.com/testdouble/contributing-tests/wiki/London-school-TDD
* https://github.com/testdouble/contributing-tests/wiki/Don%27t-mock-what-you-don%27t-own
* [Cleanly create test data](https://testing.googleblog.com/2018/02/testing-on-toilet-cleanly-create-test.html)
* [To comment or not to comment](http://testing.googleblog.com/2017/07/code-health-to-comment-or-not-to-comment.html)
* [Android Test Orchestrator, how to](https://medium.com/stepstone-tech/android-test-orchestrator-unmasked-83b8879928fa)
* [Using ADB Enhanced to test diff device situations](https://ashishb.net/tech/introducing-adb-enhanced-a-swiss-army-knife-for-android-development/)
* [Good Android Test strategy at Azimo](https://medium.com/azimolabs/automated-testing-will-set-your-engineering-team-free-a89467c40731)
* [Verified Fakes, explained](https://pythonspeed.com/articles/verified-fakes/)



