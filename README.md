# 🔗 UPI Deep Link Tester

A simple browser-based tool to test UPI deep links for **Google Pay (GPay)**, **PhonePe**, and **Paytm** on both Android and iOS — built for Razorpay UPI integration testing.

## 🚀 Live Demo

👉 [Open Tester](https://your-username.github.io/upi-tester/)

---

## 📱 Features

- Toggle between **Android** (Intent URLs) and **iOS** (URL Schemes)
- Fill in payment details — VPA, amount, payee name, transaction note & reference ID
- One-tap launch for GPay, PhonePe, and Paytm
- Live deep link URL preview
- Copy generated URL to clipboard

---

## 🧪 How to Use

1. Open the page on your **mobile device**
2. Fill in your merchant **UPI VPA** (e.g. `merchant@razorpay`)
3. Enter an **amount** and optional transaction details
4. Select your platform — **Android** or **iOS**
5. Tap an app button to launch the UPI deep link

> ⚠️ Deep links only work on a real mobile device with the UPI apps installed. Intent URLs will not work in a desktop browser.

---

## 🔗 Deep Link Formats

### Android (Intent URLs)
| App | Intent URL |
|-----|-----------|
| GPay | `intent://upi/pay?...#Intent;scheme=tez;package=com.google.android.apps.npe;end` |
| PhonePe | `intent://pay?...#Intent;scheme=phonepe;package=com.phonepe.app;end` |
| Paytm | `intent://pay?...#Intent;scheme=paytmmp;package=net.one97.paytm;end` |

### iOS (URL Schemes)
| App | URL Scheme |
|-----|-----------|
| GPay | `tez://upi/pay?...` |
| PhonePe | `phonepe://pay?...` |
| Paytm | `paytmmp://pay?...` |

---

## 🔑 UPI Query Parameters

| Parameter | Description | Example |
|-----------|-------------|---------|
| `pa` | Payee VPA | `merchant@razorpay` |
| `pn` | Payee Name | `My Store` |
| `am` | Amount | `499.00` |
| `cu` | Currency | `INR` |
| `tn` | Transaction Note | `Order #1234` |
| `tr` | Transaction Reference ID | `TXN123456` |
| `mc` | Merchant Category Code | `5411` |

---

## 🍎 iOS Setup (for Native App Integration)

Add the following to your `Info.plist` to allow querying installed UPI apps:

```xml
<key>LSApplicationQueriesSchemes</key>
<array>
  <string>tez</string>
  <string>phonepe</string>
  <string>paytmmp</string>
</array>
```

---

## 🛠️ Built With

- Plain HTML, CSS & JavaScript — no dependencies
- Razorpay UPI deep link specification

---

## 📚 References

- [Razorpay UPI Integration Docs](https://razorpay.com/docs/)
- [NPCI UPI Deep Link Spec](https://www.npci.org.in/what-we-do/upi/product-overview)

---

## 📄 License

MIT — free to use and modify for your projects.