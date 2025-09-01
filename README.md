# 🌡️ Human Body Thermal Pattern Detection for Cardiac Risk Alerts

## Project Overview

This project is a Python-based thermal monitoring system designed to detect abnormal human body thermal patterns indicative of fever, cold limbs, asymmetry, or potential cardiac risks. The system automatically analyzes thermal images and sends real-time alerts via Telegram and Email.

It is ideal for early health monitoring, research, or a demonstration of interdisciplinary integration of AI, computer vision, and IoT-like alert mechanisms.

---

## Features

### 1. Automatic Thermal Image Processing
- Processes all images in the `sample_images/` folder automatically.
- Detects abnormal patterns using a custom `detect_abnormality()` function.
- Highlights detection results on Streamlit interface.

### 2. User-Friendly Interface
- Built with Streamlit, providing a clean and interactive dashboard.
- Allows manual image upload or automatic batch processing.
- Displays detection status as Normal or Alert with details.

### 3. Multi-Channel Alerts
- Telegram Alerts: Sends instant messages to a pre-configured Telegram bot or group.
- Email Alerts: Sends detailed email notifications using Gmail SMTP credentials.
- Console Alerts: Prints alert messages to the console for local monitoring.
- Sound Alerts: Plays a beep sound for immediate attention.

### 4. Environment Configuration
- All credentials (Email, Telegram) are securely stored in a `.env` file.
- SMTP server and port are configurable for flexibility.

### 5. Future Real-Time Expansion
- Once a thermal camera is available, the system can be extended to real-time monitoring.
- Alerts will be sent instantly per frame with optional cooldown to prevent spamming.
- Can integrate with multiple cameras or dashboards for continuous monitoring.

---

## Technologies Used
- Python 3.10+
- OpenCV – Image processing and frame capture
- NumPy – Image array manipulation
- Streamlit – Web interface
- SMTP / smtplib – Email alerts
- Telegram Bot API – Instant notifications
- dotenv – Environment variable management

---

## Setup Instructions

1. Clone the repository:
```bash
git clone <your-repo-url>
cd Cardiac_thermal_app
````

2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Configure `.env` file with your credentials:

```env
EMAIL_USER=your_email@gmail.com
EMAIL_PASS="your_app_password"
EMAIL_RECEIVER=receiver_email@gmail.com
TELEGRAM_BOT_TOKEN=your_bot_token
TELEGRAM_CHAT_ID=your_chat_id
SMTP_SERVER=smtp.gmail.com
SMTP_PORT=587
```

4. Run the Streamlit app:

```bash
streamlit run app.py
```

5. Upload images or let the app process images from `sample_images/`. Alerts will be triggered automatically if abnormalities are detected.

---

## Future Enhancements

* Real-time camera integration for continuous thermal monitoring.
* Annotated thermal image outputs with detected regions.
* Historical data logging and dashboards for trend analysis.
* Multi-user monitoring for hospitals or care centers.

---

## Use Cases

* Early detection of fever or abnormal body temperature.
* Monitoring cardiac risk indicators via thermal patterns.
* Educational and demonstration purposes for AI + CV + IoT integration.
* Prototype for patient monitoring systems or smart healthcare solutions.

---

## License

This project is open-source and available under the MIT License. Please credit the authors if reused or modified.

```
