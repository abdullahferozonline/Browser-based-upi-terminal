🔐 SecurePay — Premium UPI QR Payment Terminal

<p align="center"><img src="https://readme-typing-svg.demolab.com?font=Inter&weight=800&size=30&duration=3000&pause=900&color=7180FF&center=true&vCenter=true&width=750&lines=SecurePay;Premium+UPI+QR+Terminal;Fast.+Clean.+Animated.;Built+with+Python+%2B+Flask" alt="SecurePay animated title"></p><p align="center"><img src="https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge&logo=python&logoColor=white">
<img src="https://img.shields.io/badge/Flask-Web%20App-000000?style=for-the-badge&logo=flask&logoColor=white">
<img src="https://img.shields.io/badge/UPI-Payment-6C63FF?style=for-the-badge">
<img src="https://img.shields.io/badge/Mobile-First-22C55E?style=for-the-badge">
<img src="https://img.shields.io/badge/License-MIT-111827?style=for-the-badge"></p><p align="center"><b>A beautiful, animated, mobile-first UPI QR payment terminal built with Python and Flask.</b>

</p>---

✨ What is SecurePay?

SecurePay is a lightweight UPI QR payment terminal designed to make accepting payments feel more like using a modern banking/POS application than a basic QR generator.

Enter an amount → generate a UPI QR → let the customer scan → the QR session automatically locks after five minutes.

The entire application is contained in a single Python file:

secureqr.py

No frontend build system.

No React installation.

No Node.js requirement.

No database requirement.

Just Python, Flask and QR generation.

---

🎬 The Experience

                 ┌──────────────────────────┐
                 │       SECUREPAY          │
                 │    PREMIUM UPI TERMINAL  │
                 └────────────┬─────────────┘
                              │
                              ▼
                  ┌─────────────────────┐
                  │   ENTER AMOUNT      │
                  │                     │
                  │       ₹500          │
                  │                     │
                  │  50  100  200  500  │
                  │                     │
                  │   1  2  3            │
                  │   4  5  6            │
                  │   7  8  9            │
                  │   .  0  ⌫            │
                  └──────────┬──────────┘
                             │
                             ▼
                  ┌─────────────────────┐
                  │      QR ACTIVE      │
                  │                     │
                  │     ┌─────────┐     │
                  │     │         │     │
                  │     │   QR    │     │
                  │     │         │     │
                  │     └─────────┘     │
                  │                     │
                  │       ₹500          │
                  │       04:32          │
                  │                     │
                  │    🔒 LOCK QR       │
                  └──────────┬──────────┘
                             │
                       5 minutes
                             │
                             ▼
                  ┌─────────────────────┐
                  │      🔒 LOCKED      │
                  │                     │
                  │  Generate a fresh   │
                  │       payment       │
                  └─────────────────────┘

---

🚀 Features

💳 UPI QR Payments

Generate standard UPI payment QR codes containing:

- UPI ID
- Merchant/shop name
- Payment amount
- INR currency

Example:

upi://pay?
pa=example@upi
&pn=YourShopName
&am=500.00
&cu=INR

---

🔢 Built-in Payment Keypad

SecurePay includes its own mobile-friendly numeric keypad.

Features:

- "0–9"
- Decimal point
- Backspace
- Quick amount buttons
- Amount validation
- Mobile-first layout

Quick amounts:

₹50
₹100
₹200
₹500

---

🎨 Premium Animated UI

SecurePay isn't designed like a basic HTML form.

The interface includes:

- Glassmorphism cards
- Animated background lighting
- Floating ambient effects
- Smooth page transitions
- QR entrance animation
- Animated QR glow
- Button shine animation
- Micro-interactions
- Animated status indicator
- Smooth countdown ring
- Expiry animation
- Responsive mobile layout

---

⏱️ Five-Minute QR Session

Every generated QR receives a five-minute application session.

The UI displays:

05:00
04:59
04:58
...
00:01
00:00

The circular progress indicator follows the countdown.

The timer changes state during the final 30 seconds.

When the session expires, SecurePay switches to:

🔒 QR LOCKED

---

🔒 Manual QR Lock

The merchant can immediately terminate the displayed session:

🔒 Lock QR Now

No page refresh is required.

---

📋 Copy UPI ID

The application provides a quick action to copy the configured UPI ID.

---

📤 Share Payment Information

On supported mobile browsers, SecurePay can use the device's native sharing interface.

---

📱 Mobile First

The UI is optimized for phone screens.

It works particularly well as a local terminal opened from:

Chrome
Firefox
Android WebView-compatible browsers

---

🧠 Server-Side Sessions

Each QR generation receives a random session identifier.

Example:

session_id
    ↓
random secure token
    ↓
5-minute expiry
    ↓
automatic cleanup

The server keeps track of active sessions in memory.

---

🛠️ Technology Stack

Technology| Purpose
Python| Application backend
Flask| Local web server
qrcode| QR generation
Pillow| QR image rendering
HTML| Interface
CSS| UI + animations
JavaScript| Interactions + timer
UPI URI| Payment data

---

📁 Project Structure

The project intentionally stays simple:

SecurePay/
│
├── secureqr.py
│
└── README.md

That's it.

The frontend is embedded directly inside "secureqr.py".

This makes the project extremely easy to copy, test and deploy.

---

📲 Run SecurePay on Android with Termux

1. Install Termux

Install Termux from a trusted source such as F-Droid or the official Termux project distribution.

After installation, open Termux.

---

2. Update packages

pkg update -y
pkg upgrade -y

---

3. Install Python

pkg install python -y

Check:

python --version

You should see something similar to:

Python 3.x.x

---

4. Install the required Python packages

pip install flask qrcode pillow

Verify:

python -c "import flask, qrcode, PIL; print('Dependencies OK')"

Expected:

Dependencies OK

---

📥 Download the Repository

Once this project is published on GitHub:

git clone https://github.com/YOUR-USERNAME/SecurePay.git

Enter the directory:

cd SecurePay

Check the files:

ls

You should see:

README.md
secureqr.py

---

▶️ Start SecurePay

Run:

python secureqr.py

You should see:

=============================================
          SECUREPAY PREMIUM UPI
=============================================

Shop : YourShopName
UPI  : example@upi
Open : http://127.0.0.1:5010
QR display session: 5 minutes

Press CTRL+C to stop

Open your Android browser and visit:

http://127.0.0.1:5010

🎉 SecurePay is now running.

---

⚙️ Configure Your Own Shop

Open the Python file:

nano secureqr.py

Find:

SHOP_NAME = "YourShopName"
UPI_ID = "example@upi"

Replace them with your own values:

SHOP_NAME = "My Shop"
UPI_ID = "myshop@upi"

Save:

CTRL + O
ENTER
CTRL + X

Then restart:

python secureqr.py

---

🔍 Test the Python File Before Running

This is useful when modifying the project.

Run:

python -m py_compile secureqr.py

If there is no output:

✅ Syntax OK

Then:

python secureqr.py

---

🌐 Access From Another Device

By default SecurePay listens on:

0.0.0.0:5010

This means it can potentially be accessed from another device on the same local network.

Find your Android device's local IP:

ip addr

Look for an address similar to:

192.168.1.25

Then another device on the same network may access:

http://192.168.1.25:5010

⚠️ Important

Only expose the application to networks you trust.

Do not expose a payment terminal directly to the public internet without adding proper authentication, HTTPS, production session storage and other security controls.

---

🧪 Troubleshooting

Port 5010 already in use

You may see:

Address already in use
Port 5010 is in use by another program.

Find the running Python processes:

ps -ef | grep python

You may see:

python secureqr.py

Find the PID and terminate it:

kill PID

If necessary:

kill -9 PID

Then restart:

python secureqr.py

---

Check Port 5010

ss -ltnp | grep ':5010'

If SecurePay is running, you should see the port listening.

---

Dependency Error

If you get:

ModuleNotFoundError: No module named 'flask'

Run:

pip install flask

For QR errors:

pip install qrcode pillow

Or simply:

pip install flask qrcode pillow

---

🎨 UI Architecture

SecurePay's interface is divided into three primary states:

┌──────────────────────┐
│ PAYMENT GENERATOR    │
│                      │
│ Amount + keypad      │
└──────────┬───────────┘
           │
           │ Generate
           ▼
┌──────────────────────┐
│ ACTIVE QR            │
│                      │
│ QR + amount          │
│ countdown            │
│ copy/share           │
└──────────┬───────────┘
           │
           │ Lock / Expire
           ▼
┌──────────────────────┐
│ LOCKED               │
│                      │
│ Generate new payment │
└──────────────────────┘

This keeps the user experience simple while allowing the interface to feel much more dynamic.

---

🎞️ Motion System

The interface uses CSS animations for:

Background floating effects
        ↓
Logo motion
        ↓
Screen transition
        ↓
Button shine
        ↓
QR entrance
        ↓
QR glow
        ↓
Countdown ring
        ↓
Expiry transition

The result is a UI that feels alive without requiring a frontend framework.

---

🔐 Security Notes

SecurePay generates a standard UPI payment URI.

The five-minute session controls the SecurePay application's displayed QR session.

It does not make a screenshot or previously copied static UPI QR cryptographically invalid after five minutes.

For example, if someone photographs a QR while it is displayed, the photograph may still contain the payment information.

For a real production payment system, additional controls would be required, such as:

- Server-side payment verification
- Authentication
- HTTPS
- Persistent session storage
- Payment status callbacks/webhooks
- Transaction reconciliation
- Rate limiting
- Audit logging
- Proper production deployment

SecurePay is therefore best understood as a local UPI QR payment terminal/demo application, not a replacement for a regulated payment processor.

---

🧑‍💻 Development

Clone:

git clone https://github.com/YOUR-USERNAME/SecurePay.git
cd SecurePay

Install:

pip install -r requirements.txt

If the repository does not contain "requirements.txt", install manually:

pip install flask qrcode pillow

Run:

python secureqr.py

---

📦 Recommended requirements.txt

Create:

nano requirements.txt

Add:

Flask
qrcode
Pillow

Then anyone can install everything with:

pip install -r requirements.txt

---

🚀 One-Command Setup

For a fresh Termux installation:

pkg update -y && \
pkg install python git -y && \
git clone https://github.com/YOUR-USERNAME/SecurePay.git && \
cd SecurePay && \
pip install -r requirements.txt && \
python secureqr.py

Then open:

http://127.0.0.1:5010

---

📸 Demo

Add your own screenshots or screen recording here:

docs/
├── home.png
├── keypad.png
├── qr.png
├── locked.png
└── demo.gif

Then display them in the README:

<p align="center">
  <img src="docs/demo.gif" width="330">
</p>

A short screen recording converted to "demo.gif" makes the repository immediately show off the animations.

---

🎥 Suggested Demo Sequence

For the best GitHub showcase, record this:

1. Open SecurePay
        ↓
2. Animated landing screen
        ↓
3. Tap ₹500
        ↓
4. Press Generate Secure QR
        ↓
5. QR animation appears
        ↓
6. Countdown starts at 05:00
        ↓
7. Tap Copy UPI ID
        ↓
8. Tap Lock QR
        ↓
9. QR disappears
        ↓
10. Locked animation
        ↓
11. Generate New Payment

Keep the recording around 10–20 seconds.

---

🏆 Why SecurePay?

SecurePay focuses on a simple idea:

«A payment terminal doesn't have to look boring.»

It combines:

Python
+
Flask
+
UPI
+
QR generation
+
Mobile UI
+
Animations
+
Session management
=
SecurePay

---

🗺️ Roadmap

Current

- [x] UPI QR generation
- [x] Amount entry
- [x] Built-in keypad
- [x] Quick amount buttons
- [x] Animated UI
- [x] QR animation
- [x] Five-minute session
- [x] Circular countdown
- [x] Manual lock
- [x] Copy UPI
- [x] Share payment information
- [x] Mobile responsive design
- [x] Server-side session tracking

Future

- [ ] Persistent transaction history
- [ ] Payment verification
- [ ] PIN-protected settings
- [ ] Merchant dashboard
- [ ] Multiple payment profiles
- [ ] Printable QR mode
- [ ] Dark/light themes
- [ ] Custom merchant branding
- [ ] PWA installation
- [ ] Production database
- [ ] Authentication
- [ ] HTTPS deployment

---

🤝 Contributing

Contributions are welcome.

Fork the repository:

git clone https://github.com/YOUR-USERNAME/SecurePay.git

Create a branch:

git checkout -b feature/my-feature

Make your changes.

Commit:

git add .
git commit -m "Add my feature"

Push:

git push origin feature/my-feature

Then open a Pull Request.

---

📄 License

This project is released under the MIT License.

See:

LICENSE

for details.

---

⭐ Support the Project

If you find SecurePay useful:

⭐ Star the repository

🍴 Fork the project

🐛 Report issues

💡 Suggest features

🤝 Contribute improvements

---

<p align="center"><img src="https://readme-typing-svg.demolab.com?font=Inter&weight=700&size=18&duration=3500&pause=1000&color=7180FF&center=true&vCenter=true&width=650&lines=Built+with+Python+%E2%9D%A4%EF%B8%8F;Designed+for+mobile;Made+to+look+beautiful;SecurePay+%E2%80%94+Premium+UPI+QR+Terminal" alt="Animated footer"></p><p align="center"><b>SecurePay</b> • Premium UPI QR Terminal

<br>Made with Python + Flask

</p>
