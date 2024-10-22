# 💊 Smart Pill Reminder System

![Android](https://img.shields.io/badge/Android-3DDC84?style=for-the-badge&logo=android&logoColor=white)
![Kotlin](https://img.shields.io/badge/Kotlin-0095D5?style=for-the-badge&logo=kotlin&logoColor=white)
![ESP8266](https://img.shields.io/badge/ESP8266-00979D?style=for-the-badge&logo=arduino&logoColor=white)
![GitHub last commit](https://img.shields.io/github/last-commit/ideepaknishadd/pill-reminder)
![GitHub issues](https://img.shields.io/github/issues/ideepaknishadd/pill-reminder)
![License](https://img.shields.io/badge/License-MIT-blue.svg?style=for-the-badge)

<div align="center">
  <img src="/api/placeholder/200/200" alt="App Logo" width="200"/>
  
  *Smart medication management for modern healthcare*
</div>

> **Important Notice:** This is a private repository. While project information and statistics are shared publicly, the source code is maintained privately for security and intellectual property reasons.

## 📱 Project Overview

The Smart Pill Reminder System is a sophisticated Android application that bridges the gap between digital reminders and physical medication management. This innovative system combines a modern mobile interface with IoT capabilities through ESP8266 integration, ensuring reliable medication adherence and enhanced healthcare outcomes.

### 🌟 Key Features

- **Intuitive Medication Management**
  - Create and manage multiple medication reminders
  - Customizable time schedules and descriptions
  - Toggle reminders active/inactive
  - 24-hour format support
  - Real-time updates and synchronization

- **Smart Device Connectivity**
  - Seamless WiFi-based device pairing
  - Robust UDP protocol implementation
  - Real-time data synchronization
  - Intelligent connection state management
  - Automatic reconnection handling

- **Modern User Interface**
  - Material Design implementation
  - Fluid animations and transitions
  - Pull-to-refresh functionality
  - Intuitive empty state handling
  - Clear connection status indicators

## 📱 App Screenshots

<div align="center">

### Main Interface
<div style="display: flex; justify-content: space-between;">
  <img src="/api/placeholder/200/400" alt="Home Screen" width="200"/>
  <img src="/api/placeholder/200/400" alt="Reminder List" width="200"/>
  <img src="/api/placeholder/200/400" alt="Add Reminder" width="200"/>
</div>

### Device Connection
<div style="display: flex; justify-content: space-between;">
  <img src="/api/placeholder/200/400" alt="Connection Screen" width="200"/>
  <img src="/api/placeholder/200/400" alt="Sync Status" width="200"/>
  <img src="/api/placeholder/200/400" alt="Success State" width="200"/>
</div>

### Management Features
<div style="display: flex; justify-content: space-between;">
  <img src="/api/placeholder/200/400" alt="Edit Screen" width="200"/>
  <img src="/api/placeholder/200/400" alt="Delete Dialog" width="200"/>
  <img src="/api/placeholder/200/400" alt="Settings" width="200"/>
</div>

</div>

## 🛠️ Technical Architecture

### Core Components

#### 1. Activity Layer
```kotlin
class PillReminderHomeActivity : AppCompatActivity {
    // Handles:
    // - UI initialization
    // - Reminder list management
    // - Network connectivity
    // - User interactions
}
```

#### 2. Data Layer
```kotlin
data class PillReminderDataModel(
    val time: String?,
    val timeIn24Hour: String?,
    val description: String?,
    var isSwitchChecked: Boolean
)
```

#### 3. Database Layer
```kotlin
class PillReminderDBHandler(context: Context) : SQLiteOpenHelper {
    // Manages:
    // - SQLite operations
    // - CRUD functionality
    // - Data persistence
}
```

### Network Protocol

#### Communication Format
```
TIME_DATA:time1,time2,time3...
```

#### Commands
- `PING`: Connection establishment
- `PONG`: Connection acknowledgment
- `DISCONNECT`: Connection termination
- `TIME_DATA`: Schedule synchronization

## 🔧 Implementation Details

### 1. Reminder Management
- **Database Operations**
  - SQLite implementation for local storage
  - Custom DBHandler for CRUD operations
  - Transaction management
  - Data integrity checks

- **UI Components**
  - RecyclerView with custom adapter
  - Custom dialog fragments
  - Data Binding implementation
  - SwipeRefreshLayout integration

### 2. Network Communication
- **UDP Socket Implementation**
  - Default port: 8266
  - ESP8266 AP Mode (192.168.4.1)
  - Connection state validation
  - Error handling mechanisms

- **Data Synchronization**
  - Real-time schedule updates
  - Batch timing transmission
  - Connection maintenance
  - Automatic retry logic

### 3. User Interface
- **Material Design Components**
  - Custom dialogs and fragments
  - Interactive status indicators
  - Progress animations
  - Error state handling

## 📋 System Requirements

- Android 5.0 (API Level 21) or higher
- WiFi-enabled device
- Compatible ESP8266 hardware unit
- Internet connectivity for updates

## 🎯 Usage Guide

1. **Initial Setup**
   - Install the application
   - Enable WiFi connectivity
   - Connect to ESP8266 network
   - Initialize device pairing

2. **Reminder Management**
   - Create new reminders via "+" button
   - Set time and description
   - Toggle reminder status
   - Edit/delete as needed

3. **Device Synchronization**
   - Ensure WiFi connection
   - Select desired reminders
   - Initiate synchronization
   - Verify successful transmission

## 🔐 Privacy & Security

This project maintains a balanced approach to open-source collaboration while protecting intellectual property:

- **Public Components:**
  - This README documentation
  - Project statistics and activity
  - Issue tracking
  - Feature announcements

- **Private Components:**
  - Source code
  - Implementation details
  - Configuration files
  - Development history

## 🚀 Future Enhancements

1. **Planned Features**
   - Cloud backup integration
   - Multi-device support
   - Advanced scheduling patterns
   - Medication tracking analytics
   - User profiles system

2. **Technical Roadmap**
   - MVVM architecture migration
   - Kotlin Coroutines integration
   - Jetpack Compose UI
   - Comprehensive testing
   - CI/CD implementation

## 👨‍💻 Developer Information

- **Developer**: Deepak Nishad
- **GitHub**: [github.com/ideepaknishadd](https://github.com/ideepaknishadd)
- **Contact**: +916351387915
- **Email**: ideepaknishadd@gmail.com

## 🤝 Contributing

While the source code is private, we welcome:
- Feature suggestions
- Bug reports
- Documentation improvements
- General feedback

## 🙏 Acknowledgments

- Android Development Community
- ESP8266 Development Team
- Material Design Guidelines
- Open-source contributors

---
<div align="center">
*Note: This is a private repository. While project information and statistics are shared publicly, the source code is maintained privately for security and intellectual property reasons.*

Engineered with ❤️ by Deepak Nishad

</div>