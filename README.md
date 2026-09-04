# PawAI
# 🐾 PawAI — Pet AI Frontend

> **Your Pet. Our AI. Better Care.**

PawAI is an AI-powered pet companion application designed to help pet parents understand their pets through **video, audio, image analysis, pet history, weekly reports, and an AI chatbot**.

This repository contains the frontend UI/UX prototype for the PawAI application.

---

## 🎯 Project Goal

The goal of the frontend is to provide a **modern, premium, responsive and user-friendly Pet AI experience**.

The application should feel like a real production-level AI product rather than a basic college-project interface.

### Core Features

* Pet profile creation
* User authentication
* Pet photo upload
* Camera/video capture
* Audio upload/recording
* Image/video upload
* AI pet behavior analysis
* AI-generated result
* Text-to-speech result
* Analysis history
* History management
* Pet profile dashboard
* Weekly pet report
* Settings & personalization
* Pet AI chatbot — PawBot
* Responsive design
* Light/Dark theme

---

# 📱 Main Pages

## 1. Create Account

File:

`01-create-account.html`

### Includes

* Pet profile picture upload
* Pet name
* Breed
* Age
* Gender
* Email
* User ID
* Password
* Confirm password
* Terms & Privacy
* Create Account button

### Important

The profile picture should be the **pet's photo, not the user's photo**.

---

## 2. Login

File:

`02-login.html`

### Includes

* Username / Email
* Password
* Show/Hide password
* Remember me
* Forgot Password UI
* Login button
* Social login UI
* Create Account link

### Note

Forgot Password is currently **UI only**.

OTP/backend integration is not required at this stage.

---

# 3. Home / AI Analysis

File:

`03-home.html`

This is the main application dashboard.

### Main Features

### Camera

User should be able to:

* Open camera
* Record pet video
* Stop recording
* Preview video
* Re-record
* Submit for analysis

### Audio

User should be able to:

* Record audio
* Upload audio
* Preview audio
* Remove/retry

### Gallery

User should be able to:

* Upload image
* Upload video
* Preview selected media
* Remove/retry

### AI Processing

After submitting media, show:

```text
Uploading
↓
Processing
↓
Detecting
↓
Understanding
↓
Generating Result
```

Use a visually polished AI processing animation.

### AI Result

Display:

* AI-generated sentence
* Analysis type
* Date/time
* Confidence score, if available
* Pet media preview
* Speaker button

### Actions

* Save
* Ask PawBot
* Analyze Again

---

# 4. My Account / Pet Profile

File:

`04-account.html`

This should behave like a **Pet Profile Dashboard**.

### Pet Information

* Pet photo
* Pet name
* Breed
* Age
* Gender
* Weight
* Other information

### Statistics

Show:

* Total analyses
* Videos
* Audio
* Images

### Analysis History

Each history item should contain:

* Media thumbnail
* Analysis result
* Date/time
* Analysis type
* Speaker button
* View details
* Delete

### History Controls

* Erase All History
* Turn Off History
* Change Profile Photo

### Other Options

* Edit Pet Information
* Change Password
* Privacy & Data
* Help & Support
* Logout

---

# 📊 Weekly Pet Report

The account/report section should eventually include a **Weekly Report Dashboard**.

The report should summarize the pet's activity and AI observations during the week.

### Weekly Report should include

* Overall wellness score
* Activity
* Sleep
* Water intake
* Food/feeding observations
* Mood/behavior observations
* AI insights
* Comparison with previous week
* Weekly highlights

Example:

```text
Weekly Report — Bruno

Wellness Score       93/100
Activity             ↑ 25%
Sleep                ↑ 1.1 hrs
Water Intake         ↑ 20%
Food Intake          ↑ 8%

Weekly Highlights
✓ Activity improved
✓ Sleep quality improved
✓ Water intake was good

AI Insight
"Bruno appears healthy and active this week."
```

### Report Actions

* View detailed report
* Compare weeks
* Download report UI
* Share report UI
* Ask PawBot about report

> Actual health/wellness values must come from the backend/AI system. The frontend should only display received data.

---

# 5. Settings

File:

`05-settings.html`

### Appearance

* Light Theme
* Dark Theme
* System Theme
* Font Size
* UI Density

### Accessibility

* Larger Text
* High Contrast
* Reduce Animations

### Notifications

* Analysis Complete
* Chatbot Messages
* General Updates

### Privacy

* Save Analysis History
* Clear Uploaded Media
* Data Permissions

### Security

* Change Password
* Active Sessions
* Logout from All Devices

### About

* App Version
* Privacy Policy
* Terms & Conditions
* Help & Support
* Contact Us

---

# 6. PawBot — Pet AI Chatbot

File:

`06-chatbot.html`

PawBot is the application's **Pet AI Assistant**.

### Chat Features

* User messages
* AI messages
* Typing indicator
* Loading state
* Error state
* Speaker button
* Copy response
* Image attachment
* Video attachment
* Voice input
* Send message

### Suggested Questions

Examples:

```text
Why is my pet doing this?
Food suggestions
Is this behavior normal?
When should I see a vet?
Explain my last analysis
```

### Important

PawBot should be context-aware.

If possible, it should receive:

* Pet profile
* Breed
* Age
* Previous analysis
* Weekly report
* Relevant history

This will make the chatbot feel like a **personal pet assistant** instead of a generic chatbot.

---

# 🧩 Reusable Components

Frontend should use reusable components instead of creating every element separately.

Recommended components:

```text
Button
Input
Select
Toggle
Modal
Toast
Navbar
Sidebar
BottomNavigation
PetProfileCard
PetAvatar
MediaUpload
CameraButton
AudioPlayer
AnalysisCard
HistoryCard
WeeklyReportCard
Chart
ProgressBar
ChatBubble
ChatInput
LoadingState
EmptyState
ErrorState
ConfirmationModal
```

---

# 🎨 Design System

### Primary Style

* Soft pink / rose
* White cards
* Light backgrounds
* Rounded corners
* Soft shadows
* Clean typography
* Pet-friendly illustrations
* Minimal but premium UI

### Typography

Recommended:

* Inter
* Manrope
* DM Sans
* Plus Jakarta Sans

### Icons

Use one consistent icon library.

Recommended:

* Lucide
* Phosphor

Do not mix multiple icon styles unnecessarily.

---

# 📱 Responsive Requirements

The application must work properly on:

* Mobile
* Tablet
* Laptop
* Desktop

Mobile should have:

```text
Home
History
PawBot
Account
```

as bottom navigation.

Desktop can use a sidebar navigation.

---

# ⚡ UI States

Every important feature must have proper states.

### Normal

Default UI

### Loading

Skeleton/spinner/progress

### Processing

AI analysis animation

### Success

Success message/animation

### Error

Clear error + Retry

### Empty

Helpful empty-state message + CTA

### Disabled

Disabled controls when necessary

---

# 🔌 Backend Integration

The current HTML pages are UI prototypes.

Backend/API integration will be required for:

### Authentication

```text
POST /register
POST /login
POST /forgot-password
```

### Pet Profile

```text
GET /pet
PUT /pet
POST /pet/photo
```

### Media

```text
POST /upload
POST /analysis
GET /analysis/:id
```

### History

```text
GET /history
DELETE /history
PUT /history/settings
```

### Weekly Report

```text
GET /reports/weekly
GET /reports/weekly/:date
```

### Chatbot

```text
POST /chat
GET /chat/history
```

> Endpoint names are placeholders. Final API contracts should be decided with the backend team.

---

# 🔐 Security & Privacy

Do not store sensitive credentials directly in frontend code.

Authentication tokens should be handled securely.

Uploaded pet media should not be permanently stored on the client unless explicitly required.

The frontend should clearly communicate:

* Data privacy
* History settings
* Media deletion
* Account security

---

# 🚀 Development Flow

Recommended order:

```text
1. Finalize Figma/UI
        ↓
2. Create Design System
        ↓
3. Create Reusable Components
        ↓
4. Build Authentication
        ↓
5. Build Pet Profile
        ↓
6. Build Home + Media Upload
        ↓
7. Build AI Result
        ↓
8. Build History
        ↓
9. Build Weekly Report
        ↓
10. Build Settings
        ↓
11. Build PawBot
        ↓
12. Connect Backend APIs
        ↓
13. Testing
        ↓
14. Responsive Testing
        ↓
15. Final UI Polish
```

---

# ✅ Definition of Done

Frontend will be considered complete when:

* All major screens are implemented
* Navigation works between screens
* Forms have validation
* Camera/upload UI works
* Loading/processing states exist
* AI result UI is implemented
* Speaker UI is implemented
* History UI is implemented
* Weekly Report UI is implemented
* Settings work on frontend
* PawBot UI is complete
* Responsive layout works
* Light/Dark theme works
* Empty/error/success states are handled
* Backend APIs are connected
* No major console errors exist
* UI is consistent across the application

---

## 🐾 Product Vision

PawAI should feel like:

> **A personal AI companion for understanding and caring for your pet.**

The final interface should be **simple for the pet parent, visually premium, emotionally friendly, and technically scalable.**

