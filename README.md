# 💲 ShopNexus – Full Stack Ecommerce App

ShopNexus is a full-stack **E-Commerce App** built using **Flutter (Frontend)** and **Node.js + MongoDB (Backend)**.
It provides a complete e-commerce experience, with real-time product management, payments, analytics, and more.

---

## 🚀 Features

### 👤 User App

* 🔐 **Login & Signup** with email/password
* ♻️ **Persisted Auth State** using Provider
* 🔍 **Search Products** and by category
* ⭐ **Rate Products** and view average rating
* 🛒 **Add to Cart** and manage cart items
* 💳 **Buy Products** with **Apple Pay** & **Google Pay**
* 🏠 **Manage Addresses** — Add, Update, Delete, and set Default
* 📦 **Order History** — View and track your orders
* 🌟 **Deal of the Day** section
* ⚙️ **Settings** — Amazon Pay, miniTV, Funzone, Sign Out
* 🔐 **Secure Authentication** with JWT

### 🧑‍💼 Admin Panel

* 🏧 **Add New Products**
* 📦 **View & Delete Products**
* 📊 **View Orders** and **Change Status**
* 💰 **View Total & Category Earnings**
* 📈 **Earnings Graph** using `charts_flutter`

---

## 🧪 Tech Stack

### 🖥️ Frontend (Flutter)

| Package            | Purpose                          |
| ------------------ | -------------------------------- |
| provider           | State management                 |
| http               | API communication                |
| shared_preferences | Local auth storage               |
| badges             | Cart badge counter               |
| carousel_slider    | Product image carousel           |
| dotted_border      | Border design for product upload |
| file_picker        | Select product images            |
| cloudinary_public  | Upload images to Cloudinary      |
| flutter_rating_bar | Product ratings                  |
| pay                | Google Pay / Apple Pay           |
| intl               | Currency/date formatting         |
| charts_flutter     | Graphs for Admin dashboard       |
| webview_flutter    | Embedded web views               |
| cupertino_icons    | iOS-like icons                   |

### ⚙️ Backend (Node.js + MongoDB)

| Package      | Purpose                  |
| ------------ | ------------------------ |
| express      | Web server framework     |
| mongoose     | MongoDB object modeling  |
| bcryptjs     | Password hashing         |
| jsonwebtoken | JWT-based authentication |
| http         | Server setup             |

---

## 🧠 Prerequisites

* ✅ Flutter SDK installed → [Install Flutter](https://docs.flutter.dev/get-started/install)
* ✅ Node.js (v14 or higher)
* ✅ MongoDB Atlas account → [Create Here](https://cloud.mongodb.com/)
* ✅ Cloudinary account → [Create Here](https://cloudinary.com/)

---

## ⚙️ Backend Setup

1. Navigate to the server folder:

   ```bash
   cd server
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Open `index.js` and replace with your MongoDB connection string:

   ```js
   const DB = "mongodb+srv://<username>:<password>@cluster.mongodb.net/shopnexus";
   ```

4. Run the backend:

   ```bash
   npm run dev   # for live reload
   ```

   or

   ```bash
   npm start     # single run
   ```

5. Server runs by default at **[http://localhost:3000](http://localhost:3000)**

---

## 📱 Frontend Setup (Flutter)

1. Clone this repo:

   ```bash
   git clone https://github.com/vishal28d/shopnexus.git
   ```

2. Navigate to project folder:

   ```bash
   cd shopnexus
   ```

3. Install dependencies:

   ```bash
   flutter pub get
   ```

4. Update environment configurations:

   * In `lib/features/admin/services/admin_services.dart`
     Replace with your **Cloudinary Credentials**:

     ```dart
     const cloudName = "YOUR_CLOUD_NAME";
     const uploadPreset = "YOUR_UPLOAD_PRESET";
     ```
   * In `lib/constants/global_variables.dart`
     Replace with your **local IP Address**:

     ```dart
     String uri = 'http://<your_local_ip>:3000';
     ```

5. Run the app:

   ```bash
   flutter run
   ```

6. Build APK:

   ```bash
   flutter build apk --split-per-abi
   ```

---

## 🗾 Folder Structure

```
shopnexus/
│
├── lib/
│   ├── features/
│   │   ├── auth/
│   │   ├── home/
│   │   ├── cart/
│   │   ├── account/
│   │   ├── admin/
│   │   └── orders/
│   ├── common/
│   ├── constants/
│   └── main.dart
│
├── server/
│   ├── models/
│   ├── routes/
│   ├── middlewares/
│   └── index.js
│
├── assets/
├── pubspec.yaml
├── package.json
└── README.md
```

---

## 🔑 Environment Variables

### 🧉 Cloudinary (Frontend)

```bash
CLOUD_NAME=your_cloud_name
UPLOAD_PRESET=your_upload_preset
```

### ☁️ MongoDB (Backend)

```bash
DB_URL=mongodb+srv://<username>:<password>@cluster.mongodb.net/shopnexus
JWT_SECRET=your_secret_key
PORT=3000
```

---

## 📊 Admin Dashboard

View your total and category-wise earnings directly in the admin panel.
Visualized using **charts_flutter** graphs.

---

## 🔐 Authentication Flow

1. User signs up or logs in
2. JWT token is generated and saved with `shared_preferences`
3. Auth state is managed by Provider
4. Server validates each request with the token

---

## 🧩 Requirements Recap

* ✅ Cloudinary account (for product images)
* ✅ MongoDB cluster (for database)
* ✅ Flutter SDK installed
* ✅ Node.js installed

---

## 🤝 Contributing

Contributions are welcome!
Please open an issue or submit a pull request to propose changes.

---

## 👨‍🔧 Author

**Vishal Maurya**
🔗 [GitHub – vishal28d](https://github.com/vishal28d)

---

## 📜 License

This project is open-source and available under the [MIT License](LICENSE).

---

### ⭐ Support

If you found this project helpful, please give it a ⭐ on GitHub — it motivates continued development!

---

**ShopNexus – Built with Flutter ❤️ & Node.js **
