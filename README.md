# Brain Dump

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

### Style Guides
* [The best Android style guide](https://github.com/bufferapp/android-guidelines/blob/master/project_style_guidelines.md)

### Android Studio Tips
* [50 Android Studio tips](https://medium.com/@mmbialas/50-android-studio-tips-tricks-resources-you-should-be-familiar-with-as-an-android-developer-af86e7cf56d2#.zdg2tg99u)

### Crash Early; Crash Often
* [Why your app should crash](https://jeroenmols.com/blog/2017/03/08/appcrash/)
* [Instagram Design Philosophy](https://instagram-engineering.com/instagram-android-four-years-later-927c166b0201)

>Almost all complex business logic happens server-side, where it is easier to fix bugs and add new features. We rely on the server to be perfect, enforced through continuous integration testing, and dispense with null-checking or data-consistency checking on the client. Because of this, the app crashes when there is malformed data, rather than remain in a weird state. Our automated crash reporting triggers alarms and an investigation, and we can fix the bug. It is much easier to fix a crash, with an attached stack trace, than to debug a weird state issue based on a user’s report.


## Today I Learned:

A running list of things that I've learned or had to re-learn. Lately I've been doing more [reading](READ_LIST.md) than learning individual tricks:

* **05/30/2018** You can define RecyclerView's LayoutManager in xml [here](https://stackoverflow.com/a/35680716)

* **10/11/2017** If we set `START_STICKY` then system will restart service when resources are available (which means immediatly if user force kills app). Read more [here](https://stackoverflow.com/q/15452935)

* **8/27/2017** We can make Observables blocking with `toBlocking()` for RxJava1 and `forBlockingX()` for RxJava2. Read more [here](https://stackoverflow.com/questions/28081821/rxjava-how-to-set-observer-to-block).

* **8/7/2017** `protected` fields are still exposed to entire package. i.e. `package private` is *more* restrictive than `protected`. How did I not know this?

* **5/17/2017** You don't need to do math on Window height/width to determine orientation. Just `getResources().getConfiguration().orientation`. [read more](https://developer.android.com/reference/android/content/res/Configuration.html#orientation)

* **2/10/2017** RecyclerView has a `smoothScrollToPosition` in addition to `scrollToPosition`

* **12/7/2016** RxJava has a `distinct` and `distinctUntilChanged` operators that won't emit duplicate items [read more](http://rxmarbles.com/#distinctUntilChanged)

* **11/7/2016** Junit4's `@BeforeClass` and `@AfterClass` methods have to be `static`. [read more](http://selftechy.com/2011/05/17/junit4-before-vs-beforeclass-after-vs-afterclass)

* **10/13/2016** Views can dump out a bitmap version of themselves by "hijacking" the existing draw(Canvas method) method. This method is normally used by parent views to draw a view by providing a canvas for the view. Instead we supply our own Canvas that has an empty (but properly sized) Bitmap. This bitmap will then be used by the view to draw a pixelated version of itself. Read more [here](http://stackoverflow.com/a/3036736).

* **9/6/2016** Using Dagger, we don't *have* to use the module to provide all sub-dependencies. We can just use `@Binds` (instead of `@Provides`) [read more](https://medium.com/android-news/inject-interfaces-without-providing-in-dagger-2-618cce9b1e29#.ozol1agh5)

* **9/2/2016** FragmentTransactions can be committed after onSavedInstanceState if you are willing to lose state when activity is killed via [commitAllowingStateLoss( )](https://developer.android.com/reference/android/app/FragmentTransaction.html#commitAllowingStateLoss(%29)

* **8/9/2016** That size and capacity are different in array lists [details](http://stackoverflow.com/questions/8896758/initial-size-for-the-arraylist)

* **7/11/2016** When specifying url in intent filter, scheme is mandatory *"If a scheme is not specified for the intent filter, all the other URI attributes are ignored."* [docs](https://developer.android.com/guide/topics/manifest/data-element.html#scheme)

* **7/7/2016** [`PhoneNumberFormattingTextWatcher`](https://developer.android.com/reference/android/telephony/PhoneNumberFormattingTextWatcher.html) is a thing.

* **7/5/2016** The default interpolator on `ObjectAnimator` is ` AccelerateDecelerateInterpolator` not (as I expected) `LinearInterpolator`. This results in really janky animation when repeating.

* **6/17/2016** Travis will not supply secret env vars for builds coming from pull requests from upstream forks. This means that if other people create a pull request against your repository, they can't see your secret env vars. [read more](https://docs.travis-ci.com/user/pull-requests#Security-Restrictions-when-testing-Pull-Requests)

* **6/9/2016** In Android Studio when refactoring code out into new method, it will detect other occurrences of that code and replace with new method call.

* **5/19/2016** Rx's Obervable.subscribe() has overload for multiple functions. This means that you don't have to pass in an Observer which implements three methods (onNext, onError, and onComplete). By passing in a three-method object, you can't lambda-ify. However with the overloaded subscribe() method, it takes in single-method objects (i.e. function objects) as parameters. [link](http://reactivex.io/RxJava/javadoc/rx/Observable.html#subscribe(rx.functions.Action1,%20rx.functions.Action1,%20rx.functions.Action0%29). This means you can lambda-ify.

* **5/16/2016** `TextUtils.join` for creating character-delimited strings; [link](https://developer.android.com/reference/android/text/TextUtils.html#join(java.lang.CharSequence, java.lang.Object[]))

* **5/10/2016** - TextView has `letterSpacing` attribute for custom kerning (on API 21+) [link](http://developer.android.com/reference/android/widget/TextView.html#attr_android:letterSpacing)

* **5/5/2016** - TextView support seamless shadows with `android:shadowColor`, `android:shadowDx`, `android:shadowDy`, and `android:shadowRadius`. [link](http://developer.android.com/reference/android/widget/TextView.html#attr_android:shadowColor)

* **5/4/2016** - `Stroke` has `dashGap` and `dashWidth` for making dashed line drawable shapes. [link](http://developer.android.com/guide/topics/resources/drawable-resource.html#stroke-element)

* **4/27/2016** sacrificial architecture [link](http://martinfowler.com/bliki/SacrificialArchitecture.html). specifically this quote:

	>Indeed one of the best things to do with an early version of a system is to explore what the best modular structure should be so that you can build on that knowledge for the replacement

* **4/25/2016** `ellipsize="middle"` is an attribute/value on TextView that will automagically remove elements in the middle to ensure text fits [docs](http://developer.android.com/reference/android/widget/TextView.html#attr_android:ellipsize)

* **12/21/2015** `$?` is a special bash variable that's the exit code of the previous command	[link](http://www.thegeekstuff.com/2010/03/bash-shell-exit-status/)

* **12/10/2015**	Travis will run scripts in individual bash processes. [link](https://docs.travis-ci.com/user/ci-environment/#Group-membership)

* **10/9/2015**	Genymotion doesn't support ARM translation out of the box. [link](http://stackoverflow.com/a/24572239)

* **10/6/2015**	`onCreateNative()` and `onDestroyNative()` pattern for passing stuff down to JNI library at the start of an Activity (and cleanup)

* **10/5/2015** Timber is awesome; always use it

* **9/8/2015**	InstantiationException is a thing: [link](http://docs.oracle.com/javase/7/docs/api/java/lang/InstantiationException.html)

* **8/24/2015**	in Android Studio we can see running threads in debug without having to use breakpoint with "Restore 'Threads' view"	

* **8/20/2015**	adjustResize vs adjustPan; [read more](http://developer.android.com/guide/topics/manifest/activity-element.html)

* **7/31/2015**	GSON can serialize directly to/from enum; [read more](http://stackoverflow.com/questions/9064433/gson-non-case-sensitive-enum-deserialization/18343576#18343576)

* **7/22/2015**	we can recreate back stack in pending intent [read more](http://stackoverflow.com/a/13294352)

* **7/16/2015**	`setUserVisibleHint()` is called when view pager puts fragment on screen

* **6/19/2015**	`compareTo` takes in a generic	

* **6/19/2015**	in java, you can cast a null object without exception	[read more](http://stackoverflow.com/questions/18723596/no-exception-while-type-casting-with-a-null-in-java)

* **6/19/2015**	Butterknife has an @onEditorAction annotation	[read more](https://jakewharton.github.io/butterknife/javadoc/butterknife/OnEditorAction.html)

* **6/14/2015**	`apply()` to shared pref is async; `commit()` is sync and returns success boolean	

* **6/10/2015**	`parentActivityName` was introduced in API 16, this is one of the reasons we set minSDK = 16 in version 2 of the book [read more](http://developer.android.com/guide/topics/manifest/activity-element.html#parent)

* **6/9/2015**	LinearLayout.LayoutParams constructor takes in layout weight as a float, so we can specify layout weight as float in xml	[link](http://developer.android.com/reference/android/widget/LinearLayout.LayoutParams.html#LinearLayout.LayoutParams(int, int, float%29)

* **5/15/2015**	 we can have our location request piggy back another request (and only get locations when another app requests a location) via the [PRIORITY_NO_POWER flag](https://developer.android.com/reference/com/google/android/gms/location/LocationRequest.html#PRIORITY_NO_POWER)

* **5/15/2015**	we can set "uses feature" for location (and course and fine resolution)	[read more](http://developer.android.com/guide/topics/manifest/uses-feature-element.html#features-reference)

* **5/14/2015**	we can intercept recycler view's `onMeasure` to set custom span [link](http://blog.sqisland.com/2014/12/recyclerview-autofit-grid.html)

* **5/14/2015** 	I never knew *why* we set `attachToRoot` to be false inside layout inflater. Its because layout inflater doesn't' know that something else might handle attachment (e.g. a fragment). Read more [here](http://stackoverflow.com/a/12567640).

* **5/13/2015**	we can rely on the system backup to backup our app. Read more [here](http://developer.android.com/google/backup/index.html)

* **5/11/2015**	`onActivityResult` doesn't call up to super. So we don't have to worry about conflicts from inheriting `REQUEST_CODES`

* 5/1/2015	ints in java are 32 bit signed, in swift/objC they are 64 bit signed	
* 5/1/2015	you can long press on a notification and see which app posted it and link to application's notification screen	

* 4/28/2015	cool plugin to generate butterknife annotations	https://github.com/avast/android-butterknife-zelezny

* 4/28/2015	All the widgets that I traditionally think of having enabled state (i.e buttons/ edit texts) actually inherit the setEnabled() method from View. So any View object can be set to enabled or disabled	http://developer.android.com/reference/android/view/View.html#setEnabled(boolean)

* 4/28/2015	TextView and EditText have android:digits attribute which will limit text to only digits	http://developer.android.com/reference/android/widget/TextView.html#attr_android:digits

* 4/26/2015	we don't need to use MaterialDialog support lib anymore	http://android-developers.blogspot.co.uk/2015/04/android-support-library-221.html

* 4/26/2015	ActionBarActivity is now deprecated and called AppCompatActivity	http://android-developers.blogspot.co.uk/2015/04/android-support-library-221.html

* 4/21/2015	applicationID vs packageID	http://tools.android.com/tech-docs/new-build-system/applicationid-vs-packagename

* 4/17/2015	git blame from CLI	

* 4/16/2015	IntentService handles intents on background thread, out of the box	
* 4/16/2015	we have to manually shut down HandlerThread	
* 4/14/2015	RecyclerView.Adapter.getItemViewType()  and why this is important	
* 4/14/2015	static interface is the same thing as a "regular" interface; the static modifier does nothing	

* 4/14/2015	AndroidStudio can automatically create a landscape version of a layout .xml file from within the graphical layout editor	

* 4/13/2015	"%s" is a valid string formatter; you don't need to use $1%s

* 4/13/2015	if three widgets live inside a LinearLayout and the second one is "match parent" and first and third widgets are "wrap content"  then you'll see the first and second widgets but not the third. it will get collapsed to zero	