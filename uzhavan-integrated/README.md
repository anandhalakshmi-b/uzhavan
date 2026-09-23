# 🌾 AgriConnect · SIH 2026

> Direct Markets. Fair Prices. Better Futures.  
> **Smart India Hackathon 2026 · PS-26132**

AgriConnect is a comprehensive agricultural web application built with **React**, **Tailwind CSS**, and **Firebase** (Firestore & Authentication) that unifies real-time mandi price discovery with direct buyer-seller matching, high-value specialty produce, and smart farm management.

---

## 🚀 Quick Start

1. **Install Dependencies**:
   ```bash
   npm install
   ```

2. **Run Development Server**:
   ```bash
   npm run dev
   ```
   Open [http://localhost:5173](http://localhost:5173) in your browser.

3. **Build for Production**:
   ```bash
   npm run build
   ```

---

## 🔥 Firebase Setup (Backend)

The app comes equipped with a **Hybrid Firebase Architecture**:
- **Offline / Local Fallback**: If no Firebase credentials are provided, the app runs completely in-memory and in `localStorage` with reactive updates.
- **Live Firestore & Auth**: To connect your live Firebase project, create or edit `.env` with your project keys:

```env
VITE_FIREBASE_API_KEY=your_api_key_here
VITE_FIREBASE_AUTH_DOMAIN=your_project_id.firebaseapp.com
VITE_FIREBASE_PROJECT_ID=your_project_id
VITE_FIREBASE_STORAGE_BUCKET=your_project_id.appspot.com
VITE_FIREBASE_MESSAGING_SENDER_ID=your_messaging_sender_id
VITE_FIREBASE_APP_ID=your_app_id
```

### Firestore Collections Used:
- `produce_listings`: Marketplace produce uploaded by farmers
- `orders`: Direct buy, bidding, and subscription orders
- `farmer_listings`: Farmer inventory and sales status
- `chat_history`: Multilingual AI assistant interactions

---

## 🌟 Key Features

1. **Price Discovery (`/prices`)**:
   - Interactive historical price trend chart comparing Mandi vs. Platform vs. MSP (Recharts)
   - Dynamic AI Advisory recommendation for each crop
   - Searchable live mandi table with arrival volume and price variance
2. **Digital Marketplace (`/marketplace`)**:
   - Direct buy modal with dynamic price total calculation
   - Price negotiation & bidding modal
   - Filter by All Produce vs. Organic Only
3. **Farmer Dashboard (`/dashboard`)**:
   - Farm sales metrics, income uplift (+18%), and active listings
   - Monthly earnings visualization
   - "New Produce Listing" modal with harvest date, grade, and organic badges
   - Real-time orders tracking table
4. **Specialty & Niche Produce (`/specialty`)**:
   - Exotic & gourmet crops (Microgreens, Gourmet Mushrooms, Bok Choy, Avocado)
   - Cold-chain assurance & shelf life metrics
   - Recurring weekly subscription tiers (Starter, Restaurant, Wholesale)
5. **Multilingual Support**:
   - Seamless instant switching across **English**, **Hindi (हिन्दी)**, and **Tamil (தமிழ்)**
6. **AgriConnect AI Voice Assistant**:
   - Speech-to-text voice recognition (Web Speech API)
   - Crop price inquiries, listing instructions, and government scheme advisories
