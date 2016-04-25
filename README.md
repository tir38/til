#Brain Dump

##Good Habits
*I'm not a great programmer; I'm just a good programmer with great habits.* - Kent Beck

There are some things that I regularly need to come back to and refresh myself on.

### Software Dev Soft Skills
* [How to Write a Git Commit Message](http://chris.beams.io/posts/git-commit/)
* [Don't Re-estimate Stories](https://www.mountaingoatsoftware.com/blog/to-re-estimate-or-not-that-is-the-question)

### Testing

* [Don't Mock What You Don't Own](https://blog.8thlight.com/eric-smith/2011/10/27/thats-not-yours.html)
* [Proper Naming of Test Doubles](https://blog.8thlight.com/uncle-bob/2014/05/14/TheLittleMocker.html)
* [Principles of Test Automation](http://xunitpatterns.com/Principles%20of%20Test%20Automation.html#Use%20the%20Front%20Door%20First) (useful beyond the "automation" part)

##Today I Learned:

A running list of things that I've learned or had to re-learn:

* **4/25/2016** `ellipsize="middle"` is an attribute/value on TextView that will automagically remove elements in the middle to ensure text fits [docs](http://developer.android.com/reference/android/widget/TextView.html#attr_android:ellipsize)

* **12/21/2015** `$?` is a special bash variable that's the exit code of the previous command	[link](http://www.thegeekstuff.com/2010/03/bash-shell-exit-status/)

* 12/10/2015	travis will run scripts in individual bash processes	https://docs.travis-ci.com/user/ci-environment/#Group-membership

* 10/9/2015	Genymotion doesn't support ARM translation out of the box	http://stackoverflow.com/a/24572239

* 10/6/2015	onCreateNative() and onDestroyNative() pattern for passing stuff down to JNI library at the start of an Activity (and cleanup)

* 10/5/2015	Timber is awesome; always use it	

* 9/8/2015	InstantiationException is a thing	http://docs.oracle.com/javase/7/docs/api/java/lang/InstantiationException.html

* 8/24/2015	in AS we can see running threads in debug without having to use breakpoint with "Restore 'Threads' view"	

* 8/20/2015	adjustResize vs adjustPan	http://developer.android.com/guide/topics/manifest/activity-element.html

* 7/31/2015	GSON can serialize directly to/from enum	http://stackoverflow.com/questions/9064433/gson-non-case-sensitive-enum-deserialization/18343576#18343576

* 7/22/2015	we can recreate back stack in pending intent	http://stackoverflow.com/a/13294352

* 7/16/2015	setUserVisibleHint() is called when view pager puts fragment on screen	

* 6/19/2015	compareTo takes in a generic	

* 6/19/2015	in java, you can cast a null object without exception	http://stackoverflow.com/questions/18723596/no-exception-while-type-casting-with-a-null-in-java

* 6/19/2015	Butterknife has an @onEditorAction annotation	https://jakewharton.github.io/butterknife/javadoc/butterknife/OnEditorAction.html

* 6/14/2015	apply() to shared pref is async; commit() is sync and returns success boolean	
* 6/10/2015	parentActivityName was introduced in API 16, this is one of the reasons we set minSDK = 16 in version 2 of the book	http://developer.android.com/guide/topics/manifest/activity-element.html#parent

* 6/9/2015	LinearLayout.LayoutParams constuctor takes in layout weight as a float, so we can specify layout weight as float in xml	http://developer.android.com/reference/android/widget/LinearLayout.LayoutParams.html#LinearLayout.LayoutParams(int, int, float)

* 5/15/2015	we can have our location request piggy back another request (and only get locations when another app requests a location) via the PRIORITY_NO_POWER flag	https://developer.android.com/reference/com/google/android/gms/location/LocationRequest.html#PRIORITY_NO_POWER

* 5/15/2015	we can set "uses feature" for location (and course and fine resolution)	http://developer.android.com/guide/topics/manifest/uses-feature-element.html#features-reference

* 5/14/2015	we can intercept recycler view's onMeasure to set custom span	http://blog.sqisland.com/2014/12/recyclerview-autofit-grid.html

* 5/14/2015	I never knew **why* we set attachToRoot to be false in side layout inflater. Its because layout inflater doesnt' know that something else might handle attachement (e.g. a fragment)	http://stackoverflow.com/a/12567640

* 5/13/2015	we can rely on the system backup to backup our app	http://developer.android.com/google/backup/index.html

* 5/11/2015	onActivityResult doesn't call up to super. So we don't have to worry about conflicts from inheriting REQUEST_CODES	

* 5/1/2015	ints in java are 32 bit signed, in swift/objC they are 64 bit signed	
* 5/1/2015	you can long press on a notification and see which app posted it and link to application's notification screen	

* 4/28/2015	cool plugin to generate butterknife annontations	https://github.com/avast/android-butterknife-zelezny

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

* 4/13/2015	if three wigets live insde a LinearLayout and the second one is "match parent" and first and third widgets are "wrap content"  then you'll see the first and second wigets but not the third. it will get collapsed to zero	