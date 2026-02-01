# To-Do List (Vazifalar ro'yxati) - Texnik Topshiriq

## 1. LOYIHA HAQIDA UMUMIY MA'LUMOT

**Loyiha nomi:** To-Do List (Vazifalar ro'yxati)  
**Maqsad:** Shaxsiy foydalanish uchun kundalik vazifalarni boshqarish tizimi  
**Platforma:** Web ilovasi (Desktop va mobil moslashuvchan)

## 2. ASOSIY FUNKSIYALAR

### 2.1 Vazifalar bilan ishlash
- Yangi vazifa qo'shish (sarlavha, tavsif, muddat)
- Vazifani tahrirlash
- Vazifani o'chirish
- Vazifani bajarilgan deb belgilash
- Vazifalarni tartiblash (sana, muhimlik, alfabit bo'yicha)

### 2.2 Kategoriyalar va teglar
- Vazifalarni kategoriyalarga ajratish (Ish, Shaxsiy, Shopping va h.k.)
- Rang kodlash tizimi
- Kategoriyalar yaratish va boshqarish

### 2.3 Prioritet darajalari
- Yuqori (High) - qizil
- O'rta (Medium) - sariq
- Past (Low) - yashil

### 2.4 Muddat (Deadline)
- Sana va vaqt belgilash
- Eslatma (notification) tizimi
- Kechikkan vazifalarni ajratib ko'rsatish

### 2.5 Qidiruv va filtrlash
- Vazifalarni qidirish
- Holati bo'yicha filtrlash (Barcha, Faol, Bajarilgan)
- Kategoriya bo'yicha filtrlash
- Prioritet bo'yicha filtrlash

## 3. TEXNIK TALABLAR

### 3.1 Frontend
**Tavsiya etiladigan texnologiyalar:**
- **Variant 1 (Sodda):** HTML, CSS, Vanilla JavaScript
- **Variant 2 (Zamonaviy):** React.js yoki Vue.js
- **Styling:** Tailwind CSS yoki Bootstrap

### 3.2 Ma'lumotlar saqlash
**Variant 1 (Sodda):** LocalStorage - brauzerda saqlash  
**Variant 2 (Ilg'or):** Backend yaratish
- Node.js + Express
- MongoDB yoki PostgreSQL
- RESTful API

### 3.3 Dizayn talablari
- Zamonaviy va minimalistik interfeys
- Responsive dizayn (mobil va desktop)
- Qorong'u va yorug' rejim (Dark/Light mode)
- Ikki tillik interfeys: O'zbek va Ingliz

## 4. INTERFEYS TUZILMASI

### 4.1 Asosiy ekran elementlari
```
┌─────────────────────────────────────────┐
│  Logo    [Yangi vazifa +]   [Qidiruv]  │
├─────────────────────────────────────────┤
│ Sidebar:          │ Vazifalar ro'yxati │
│ - Bugun           │ ┌──────────────────┐│
│ - Haftada         │ │ □ Vazifa 1       ││
│ - Barcha          │ │   [Edit] [Del]   ││
│ - Kategoriyalar   │ ├──────────────────┤│
│                   │ │ □ Vazifa 2       ││
│                   │ │   [Edit] [Del]   ││
│                   │ └──────────────────┘│
└─────────────────────────────────────────┘
```

### 4.2 Vazifa kartasi ko'rinishi
- Checkbox (bajarilganligini belgilash)
- Sarlavha (bold)
- Tavsif (kichikroq shrift)
- Kategoriya belgisi (rangli tag)
- Muddat (agar mavjud bo'lsa)
- Prioritet indikatori
- Tahrirlash va o'chirish tugmalari

## 5. FOYDALANUVCHI OQIMI (User Flow)

1. Foydalanuvchi ilovaga kiradi
2. Mavjud vazifalar ro'yxatini ko'radi
3. "+" tugmasini bosib yangi vazifa qo'shadi
4. Modal oyna ochiladi (sarlavha, tavsif, kategoriya, prioritet, muddat)
5. "Saqlash" tugmasini bosadi
6. Yangi vazifa ro'yxatda paydo bo'ladi
7. Vazifa checkbox orqali bajarilgan deb belgilanadi
8. Bajarilgan vazifalar chiziqcha bilan ko'rsatiladi yoki alohida bo'limga o'tadi

## 6. RIVOJLANTIRISH BOSQICHLARI

### Bosqich 1: MVP (Minimal Viable Product) - 1 hafta
- Asosiy CRUD operatsiyalari
- LocalStorage bilan saqlash
- Oddiy dizayn

### Bosqich 2: Funksionallikni kengaytirish - 1 hafta
- Kategoriyalar
- Prioritetlar
- Muddat va eslatmalar
- Qidiruv va filtrlash

### Bosqich 3: Yaxshilash - 1 hafta
- Dark mode
- Ikki tillik
- Animatsiyalar
- Responsive dizayn

### Bosqich 4: Qo'shimcha xususiyatlar (ixtiyoriy)
- Backend integratsiyasi
- Foydalanuvchi autentifikatsiyasi
- Cloud sync
- Mobil ilova versiyasi

## 7. TEXNIK ARXITEKTURA (LocalStorage versiyasi)

### 7.1 Ma'lumotlar strukturasi
```javascript
{
  id: "unique-id",
  title: "Vazifa nomi",
  description: "Batafsil tavsif",
  category: "Ish",
  priority: "high",
  deadline: "2026-02-05T10:00:00",
  completed: false,
  createdAt: "2026-02-01T14:30:00"
}
```

### 7.2 Asosiy funksiyalar
- `addTask()` - vazifa qo'shish
- `editTask(id)` - vazifa tahrirlash
- `deleteTask(id)` - vazifa o'chirish
- `toggleComplete(id)` - holatni o'zgartirish
- `filterTasks(criteria)` - filtrlash
- `searchTasks(query)` - qidiruv

## 8. XAVFSIZLIK VA SAMARADORLIK

- Input validatsiya
- XSS himoyasi
- LocalStorage limitlarini nazorat qilish
- Kod optimizatsiyasi
- Lazy loading (katta ro'yxatlar uchun)

## 9. TEST QILISH

- Barcha funksiyalarni manual test qilish
- Turli brauzerlarda test (Chrome, Firefox, Safari)
- Mobil qurilmalarda test
- LocalStorage to'lishi holatini test qilish

## 10. DEPLOY

**Bepul hosting variantlari:**
- GitHub Pages
- Netlify
- Vercel
- Firebase Hosting

---

**Qo'shimcha tavsiyalar:**
- Birinchi navbatda sodda versiyani tugatib, keyin funksionallikni kengaytiring
- Har bir funksiyani alohida commit qiling (Git version control)
- Kodingizni izohlar bilan yozing
- UI/UX dizaynga e'tibor bering

Ushbu texnik topshiriq asosida loyihani bosqichma-bosqich amalga oshirishingiz mumkin. Qaysi texnologiyalar to'plamidan foydalanmoqchisiz?
