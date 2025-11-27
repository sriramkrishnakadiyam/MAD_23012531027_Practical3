Android Intent Demonstration App – Simple Explanation
Aim

This Android app shows how to use Implicit and Explicit Intents to perform common actions on a phone. From the main screen, the user can:

Make a call to a number they enter

Open any URL in a browser

View the call log

Open the gallery

Set or view alarms

Open the camera

Go to a Login screen (another activity in the app)

What This App Teaches
1. Intents

Intents let Android apps request actions from other apps or components.

2. Types of Intents

Explicit Intent:
Used to open another activity in the same app
(e.g., Intent(this, LoginActivity::class.java))

Implicit Intent:
Used to ask the system to find any app that can do an action
(e.g., open a URL, call a number, open the camera)

3. Common Intent Actions Used

ACTION_DIAL → Open the dialer

ACTION_VIEW → Open URLs or images

ACTION_IMAGE_CAPTURE → Open the camera

ACTION_SET_ALARM → Set an alarm

4. setData() and setType()

setData(Uri) → Tell the intent what data to act on
(Example: tel: for phone numbers, http: for websites)

setType() → Specify the type of data
(Example: "image/*" for viewing images)

UI Components Used

Button → Trigger actions

EditText → Input fields for phone number and URL

ConstraintLayout → Main layout

CoordinatorLayout → Used in some XML for scrolling/behaviors

Starting Activities

startActivity(intent) is used to launch either:

another screen in the app (explicit intent), or

another app (implicit intent)

Handling Missing Apps

Before using an implicit intent, the app checks if a suitable app exists.
If not, it shows a Toast instead of crashing.

Permissions (Basic Idea)

Some actions may require permissions (like CALL_PHONE), but most actions here rely on external apps (browser, camera, gallery), so runtime permissions are usually not needed.

Project Files

MainActivity.kt – Has all the buttons and intent demos

LoginActivity.kt – Opened using an explicit intent

RegisterActivity.kt – Part of login/registration

XML Layouts – UI for each activity

AndroidManifest.xml – Activity declarations and optional permissions
**Demonstration Screenshots

![image alt]()
