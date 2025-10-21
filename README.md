# CS360_ProjectThree_Journal
### Francisco Sousa  

## CS 360 Module Eight Journal – Project Three: Inventory Tracker App

### App Summary and Goals
The Inventory Tracker App was built to help users record, monitor, and update their inventory items efficiently while learning how to combine user authentication, persistent data storage, and SMS notifications in Android Studio. The goal was to create a functional mobile application that demonstrates full CRUD operations in SQLite, login and registration logic, and conditional SMS alerts for low stock. It was designed for users who need a simple but reliable way to track items locally, even without internet connectivity.

---

### User Needs and UI Design
The app includes four main screens:  
- **LoginActivity:** Allows users to sign in or register with secure credentials using a new two-step “Register” toggle we implemented.  
- **InventoryActivity:** Displays the database contents in a grid view and supports updating, deleting, and refreshing items dynamically.  
- **AddItemActivity:** Provides text fields for entering item names and quantities.  
- **SmsPermissionActivity:** Requests SMS permission and handles both granted and denied outcomes gracefully.  

The UI follows **Material Design 3** standards (Google, 2023), with clear labels, accessible button sizes, and consistent spacing. By keeping the interface minimal and using color contrast consistent with Android’s design system, users can easily navigate and perform key actions without confusion. The two-step registration update was particularly successful—it clarified how to create a new account, reducing user error during testing.

---

### Coding Approach and Strategies
I began by coding the **DatabaseHelper.java** class to handle all user and inventory operations. Following Java best practices (IBM Developer, n.d.), I structured the code with concise, modular functions—one for each CRUD operation. Each Activity class was linked to the database through this helper to keep the logic centralized and reusable.  
For the login workflow, I added validation checks and null-safe input handling to prevent crashes. The app uses clear naming conventions, comments, and inline documentation to maintain readability, matching professional standards.  

The **SmsManager** feature was implemented with conditional logic so the app continues functioning even when permissions are denied (Android, 2015). These techniques can be reused in future apps where modular coding and structured permission handling are required.

---

### Testing and Debugging
Testing was completed using the **Android Emulator (API 34)**. I verified functionality by simulating both permission outcomes for SMS (granted and denied), creating new users, and testing CRUD operations on the inventory database.  
Throughout debugging, I fixed issues such as:  
- Package-path mismatch errors in `DatabaseHelper.java`.  
- Null pointer exceptions for empty login fields.  
- Deprecation warnings for `SmsManager.getDefault()`, updated to `getSystemService(SmsManager.class)`.  

Testing revealed the importance of iterative validation—small changes were built and tested frequently to ensure stability. This approach led to a fully functional, error-free APK.

---

### Innovation and Problem Solving
One key innovation was introducing the **two-step Register mode** inside the same Login screen. Initially, the Create Account button did not clearly differentiate registration from login. By toggling between “Create Account” and “Register,” the UI became more intuitive.  
Another area of innovation was building a permission system that allows the app to function normally even when the SMS feature is unavailable. These design choices improved user experience and ensured the app met project requirements for reliability.

---

### Demonstrated Strengths
I was particularly successful in implementing and debugging the **SQLite database integration**. Every CRUD operation—insert, update, delete, and read—was tested and verified through a live grid display. This part of the project demonstrated strong understanding of data persistence, modular class design, and user-driven interaction.  

The app also showcases effective use of **Material Design** principles (Google, 2023) and Java coding standards (IBM Developer, n.d.). Following modular and data-driven design principles similar to those found in Dash framework documentation (Dash Documentation & User Guide | Plotly, n.d.) and MongoDB data structuring practices (Giamas, 2022) helped ensure long-term maintainability.

---

### References
Android. (2015). *Permissions Overview | Android Developers.* Android Developers. https://developer.android.com/guide/topics/permissions/overview  
Dash Documentation & User Guide | Plotly. (n.d.). *Dash.plotly.com.* https://dash.plotly.com/  
Giamas, A. (2022). *Mastering MongoDB 6.x.* Packt Publishing Ltd.  
Google. (2023). *Material Design.* Material Design. https://m3.material.io/  
IBM Developer. (n.d.). *Developer.ibm.com.* https://developer.ibm.com/tutorials/j-perry-writing-good-java-code/  

---

**Repository Contents:**  
- `CS360_7-2_Project_3_Inventory_App_Francisco_Sousa.zip` – Completed Android Studio project.  
- `CS360_InventoryApp_LaunchPlan_Francisco_Sousa.docx` – Final launch plan document.  
- `README.md` – Journal reflection (this file).  
