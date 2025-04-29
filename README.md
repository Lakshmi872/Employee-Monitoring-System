# Employee-Monitoring-System
Overview
The Employee Monitoring System is a comprehensive tool designed to track and monitor employee productivity, attendance, and activities during work hours. This system allows managers to gain insights into team performance, manage workloads, and ensure compliance with company policies. It helps businesses optimize workflows, identify areas of improvement, and foster a more efficient and transparent work environment.

USNs-for testing JSSATEB:1JS21EI026, 1JS21EI021

Features
Real-Time Monitoring
Live Screen Sharing
Capture and stream the employee’s screen in real-time using ImageGrab and PIL, allowing administrators to visually monitor current activity.

Webcam Feed Preview (Optional)
Receive webcam frames from employee systems and view them via the Admin dashboard using cv2 and numpy.

🧠 Intelligent System Design
Efficient Image Compression & Streaming
Images are serialized and compressed using io, PIL, and struct for optimal transmission over sockets.

Multithreaded Communication
The Admin system handles multiple employee connections concurrently using threading, maintaining responsiveness and scalability.

Robust Socket-Based Networking
Real-time, bidirectional communication is established via TCP sockets (socket), ensuring reliable data transfer.

📊 Logging & Productivity Insights
Timestamped Activity Logs
Screenshots and webcam images are logged with precise datetime stamps, useful for tracking activity over time.

Session Duration Monitoring
Use time and datetime to compute active working hours or periods of inactivity.

Idle Time Detection (extendable)
Analyze repeated frames to detect inactivity or lack of input from the employee's end.

🖥️ Intuitive User Interface
Admin Control Dashboard
Built with tkinter and ttk, the Admin GUI provides:

Live stream viewing

Connected employee list

Start/stop controls

Employee Interface
Lightweight tkinter GUI for launching the monitoring client, including status indicators and error alerts via messagebox.

📁 File & Data Handling
Optional Screenshot Archiving
Admin can save screen captures locally with timestamps for future reference or compliance review.

Lightweight Memory Usage
Byte stream processing (io.BytesIO) ensures efficient RAM usage even with frequent image transfers.

🔒 Security & Reliability (extendable)
Offline Mode (Future Enhancement)
Queue screenshots and send them when the connection is reestablished.

Face Detection Support (Optional)
Integrate OpenCV-based face recognition to confirm physical presence during sessions.

Technologies & Libraries Used
Admin Component
tkinter – GUI development

ttk – Themed tkinter widgets

socket, threading – Networking and multithreading

struct, io – Data serialization and I/O

PIL (Pillow) – Image processing

numpy – Array and image data handling

cv2 (OpenCV) – Webcam image capture and video processing

json – Configuration and data handling

os, datetime – File and time management

Employee Component
tkinter, messagebox – GUI and message alerts

socket, threading – Network communication

time, datetime – Logging and timestamps

PIL (Pillow) – Image handling

io, struct – Stream and byte conversion

ImageGrab, Image – Screen capture functionality (from PIL)



