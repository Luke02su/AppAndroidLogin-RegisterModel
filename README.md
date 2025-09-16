# Login & Register Model App 🔐📲

[![Kotlin](https://img.shields.io/badge/Language-Kotlin-orange?logo=kotlin)](https://kotlinlang.org/)  
[![Android Studio](https://img.shields.io/badge/IDE-Android_Studio-brightgreen?logo=android-studio)](https://developer.android.com/studio)  
[![Firebase](https://img.shields.io/badge/Firebase-FFCA28?logo=firebase&logoColor=white)](https://firebase.google.com/docs/auth)  
[![License](https://img.shields.io/badge/License-MIT-blue)](LICENSE)  

---

## Project 🎯
This Android app provides a **Login & Register Model App** using **Firebase Authentication (Email/Password)**. It includes Login Screen, Register Screen, and Home Dashboard. The app is designed with a **modern, responsive UI**, interactive clickable links, custom drawables, and reusable components. Perfect for learning authentication flows and Android UI best practices.

---

## App Layout 🎨

### Login Screen
- Email and Password input fields with **icons**, **padding**, and **rounded corners**.  
- **Sign In button**: blue (#2196F3), full-width, elevated (8dp), corner radius (10dp).  
- **Clickable "Sign up" link** to navigate to Register screen.  

### Register Screen
- Similar styling to Login screen.  
- **Sign Up button** with same design.  
- **Clickable "Sign in" link** to navigate to Login screen.  
- Firebase handles **account creation and validation**.  

### Home Screen
- Placeholder dashboard for post-login content.  
- Fully **responsive**.  
- Ready to add **navigation drawer, tabs, or app features**.  

<p align="center">
   <img width="300" height="600" alt="Login Screen" src="https://github.com/user-attachments/assets/815c2afd-a0bf-43d4-96d4-4e7ed9f6174c" />
   <img width="300" height="600" alt="Register Screen" src="https://github.com/user-attachments/assets/c2250948-9c00-478d-9653-5e4e6bffc553" />
   <img width="300" height="600" alt="Home Screen" src="https://github.com/user-attachments/assets/98736a01-f73c-4bb0-9603-00928882e5a8" />
</p>

---

## Features ✨
| Feature | Description |
|---------|-------------|
| Login/Register | Email/password authentication using Firebase |
| Input Validation | Check for empty fields, correct email format |
| Toast Messages | Descriptive feedback for success/error |
| Clickable Links | Navigate between Login/Register screens |
| Custom Drawables | Rounded corners, 1dp stroke (#A9A9A9), 10dp padding |
| Styled Buttons | Blue (#2196F3), white text, elevation, corner radius |
| Responsive | Works on phones and tablets |
| Exported Login Activity | App entry point ready for deep linking |
| Modular Design | Easy to maintain and expand |
| Home Screen | Placeholder for navigation drawer, profile info, or tabs |

---

## Firebase Integration 🔐
- **Email/Password Authentication**  
- **User creation, login, and error handling**  
- Ready for future expansion:
- - Remember login
  - Password reset  
  - Email verification  
  - Social OAuth login (Google, Facebook, etc.)  

**Code register example**
```kotlin
auth.createUserWithEmailAndPassword(email, password)
    .addOnCompleteListener { task ->
        if (task.isSuccessful) {
            Toast.makeText(this, "Registered successfully!", Toast.LENGTH_SHORT).show()
            startActivity(Intent(this, Login::class.java))
            finish()
        } else {
            Toast.makeText(this, "Error: ${task.exception?.message}", Toast.LENGTH_SHORT).show()
        }
    }
```

**Code login example**
```kotlin
auth.signInWithEmailAndPassword(email, password)
    .addOnCompleteListener { task ->
        if (task.isSuccessful) {
            Toast.makeText(this, "Login successfully!", Toast.LENGTH_SHORT).show()
            val intent = Intent(this, Home::class.java)
            startActivity(intent)
            finish()
        } else {
            Toast.makeText(this, "Erro: ${task.exception?.message}", Toast.LENGTH_LONG).show()
        }
    }
```

---

## Technologies Used 🤖🍏
- **Programming Language:** Kotlin  
- **Development Environment:** Android Studio  
- **Firebase Authentication:** Email/Password login  
- **UI Components:** ConstraintLayout, LinearLayout, TextView, EditText, Button  
- **Custom Drawables:** Rounded rectangle with stroke and padding, and icons 24x24 .svg of email and password
- **Target Platform:** Android Mobile Devices  

---

## Best Practices ✅
- Modular and maintainable activity structure  
- Reusable XML styles for EditText and Buttons  
- Input validation for security and UX  
- Edge-to-edge layout for modern immersive design  
- Responsive and adaptive to different screen sizes  
- Clickable spans for interactive links  

---

## Code Author 💻👨‍💻
```kotlin
fun main() {
    println("Code by Lucas Samuel Dias!")
    println("Welcome to the User Registration Model!")
}

