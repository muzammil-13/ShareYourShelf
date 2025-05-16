# 📚 ShareYourShelf – Give Books, Grow Futures

**ShareYourShelf** is a lightweight web app that lets students and families **donate or request used school books** — reducing educational costs, preventing book waste, and supporting underprivileged learners.

This project was inspired by a humble public WhatsApp message — now built as a digital movement to make sharing simple.

---

## 🌟 Features

- 📝 List books with Board, Class, Subjects, and Contact Info
- 🔍 Search & filter book listings by Board and Class
- 📞 Contact donors directly via WhatsApp
- 🚀 Fast, mobile-friendly UI with no login required

---

## 🛠️ Tech Stack

| Layer        | Tech                  |
|--------------|------------------------|
| Frontend     | React (Vite) + Tailwind CSS |
| Backend/DB   | Firebase Firestore     |
| Hosting      | Vercel or Netlify      |
| Messaging    | WhatsApp Deep Links    |

---

## 📦 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/shareyourshelf.git
cd shareyourshelf
````

### 2. Install Dependencies

```bash
npm install
```

### 3. Setup Firebase

* Create a Firebase project
* Enable Firestore in test mode
* Copy your Firebase config into `.env.local`:

```env
VITE_FIREBASE_API_KEY=your_key
VITE_FIREBASE_AUTH_DOMAIN=your_domain
VITE_FIREBASE_PROJECT_ID=your_project_id
VITE_FIREBASE_STORAGE_BUCKET=your_bucket
VITE_FIREBASE_MESSAGING_SENDER_ID=your_sender_id
VITE_FIREBASE_APP_ID=your_app_id
```

### 4. Start Development Server

```bash
npm run dev
```

---

## 📁 Project Structure

```
src/
├── components/       # Reusable components (BookCard, Navbar)
├── pages/            # Routes: Home, Donate, Search
├── firebase/         # Firebase config
├── App.jsx           # App router
├── main.jsx          # Vite entry point
```

---

## 📊 Firestore Schema

**Collection: `books`**

```json
{
  "name": "Ayesha Khan",
  "board": "CBSE",
  "class": "10",
  "subjects": ["Maths", "Science"],
  "condition": "Good",
  "contact": "91XXXXXXXXXX",
  "pincode": "673XXX",
  "timestamp": "serverTimestamp"
}
```

---

## 🔗 WhatsApp Deep Link Format

```js
const phone = "91XXXXXXXXXX";
const message = "Hi! I'm interested in the books you listed on ShareYourShelf.";
const url = `https://wa.me/${phone}?text=${encodeURIComponent(message)}`;
```

---

## 🌱 Roadmap

### Phase 1 – MVP

* [] Donate Book form (write to Firestore)
* [] View/Search Book listings
* [] WhatsApp contact integration
* [ ] Deploy public version on Vercel

### Phase 2 – Community Features

* [ ] Add LocalStorage-based "My Listings"
* [ ] Pincode-based nearby filtering
* [ ] Uniforms, guides, and stationary
* [ ] Bulk upload for schools/NGOs

---

## 🙌 Contribute

We welcome your ideas, designs, and code. Feel free to fork, build, and PR:

```bash
git checkout -b feature/your-feature-name
```

---

## 📜 License

This project is open source under the [MIT License](LICENSE).

---

## ✍️ Creator Note

> ShareYourShelf is built to solve a simple but overlooked problem — helping families exchange books with dignity and ease.
> Built by [Muzammil Ibrahim](https://github.com/muzammil-13) with the vision of tech-for-good.
> Let's turn books into bridges. 📖🤝

```
