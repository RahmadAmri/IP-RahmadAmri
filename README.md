# IP-HCK83

Individual Project:

App Idea: "SportMate – AI Personal Sports Companion"

✅ Overview Aplikasi
SportMate adalah aplikasi web berbasis React yang berfungsi sebagai asisten pribadi bagi penggemar olahraga. Aplikasi ini membantu pengguna menemukan olahraga yang cocok berdasarkan kebiasaan, cuaca, dan lokasi; memberikan rekomendasi latihan dan nutrisi berbasis AI; serta menyediakan fitur pelacakan kegiatan olahraga harian.
SportMate menggunakan teknologi AI (OpenAI) untuk memberikan saran personal, serta memanfaatkan data dari API olahraga pihak ketiga (misalnya API cuaca, lokasi gym, atau RapidAPI untuk jadwal pertandingan olahraga) untuk meningkatkan pengalaman pengguna.

🧩 Fitur Utama

1. Sport Recommendation AI
   - Menggunakan OpenAI untuk menyarankan jenis olahraga yang cocok berdasarkan preferensi pengguna, cuaca, dan waktu luang.
   - Contoh prompt: “I have 1 hour every evening and a weak knee. What sport should I try?”
2. Daily Fitness & Nutrition Plan Generator
   - AI membuat rencana harian latihan dan nutrisi berdasarkan tujuan pengguna (misalnya: kurus, otot, sehat).
3. Live Weather Integration
   - Menggunakan 3rd Party API (e.g., OpenWeatherMap API) untuk menampilkan cuaca hari ini dan memberikan saran apakah olahraga outdoor cocok dilakukan.
4. Nearby Sports Facilities
   - Integrasi dengan Google Maps API atau RapidAPI untuk mencari tempat olahraga terdekat (gym, lapangan, dll).
5. Progress Tracker
   - Input manual atau otomatis (pakai chart) aktivitas harian dan kemajuan (berbasis Redux state).
6. Chatbot Motivator (AI)
   - Chatbot AI dengan mood tracking: memberi semangat, tips, dan mengingatkan target mingguan.
7. Social Media Sign-In
   - Autentikasi pengguna via Login.

📦 Teknologi dan Arsitektur
🖥️ Client

- React + Vite
- React Router
- Redux (state management)
- Tailwind CSS (optional for fast UI)
  🖥️ Server
- Express.js + REST API
- CRUD minimal untuk: User, Preferences, Progress
  ☁️ 3rd Party API
- OpenAI API: Recommendation + Chatbot
- OpenWeatherMap API (or other weather API via RapidAPI)
- Google Maps API / Location API: Nearby places
- Social Media Sign-In: Google OAuth2
  🧠 AI Implementation (Minimum 2)
- OpenAI for sport & fitness recommendations
- Chatbot Motivator with Conversational AI

🚀 Alasan Memilih Ide Ini

- Mudah dikembangkan karena fitur bisa dibangun bertahap (fokus utama: rekomendasi + tracker).
- Menarik secara UX – banyak orang tertarik pada kebugaran, cocok jadi portofolio.
- Memenuhi semua syarat: AI, 3rd Party API, Redux, Client-Server architecture, Git Workflow, dsb.

🔒 Contoh Arsitektur Folder (Client)
css
CopyEdit
src/
├── components/
├── pages/
├── features/ (Redux slices)
├── services/ (API call utils)
├── App.jsx
├── main.jsx
└── routes.jsx

- Buat wireframe/mockup
- Struktur API dan skema MongoDB
- Sample prompt untuk fitur AI-nya
- Deploy ke Vercel + Render setup User ├── id (PK) ├── name ├── email ├── password └── googleId (nullable for OAuth) │ │ 1 │ └───< hasMany UserPreferences ├── id (PK) ├── userId (FK) ├── preferredSports ├── fitnessGoal ├── injuries (nullable) └── availableTime │ │ 1 │ └───< hasMany ProgressLog ├── id (PK) ├── userId (FK) ├── date ├── sport ├── duration (minutes) ├── caloriesBurned └── notes (nullable) │ │ 1 │ └───< hasMany RecommendationHistory ├── id (PK) ├── userId (FK) ├── inputPrompt ├── aiResponse ├── createdAt
-
