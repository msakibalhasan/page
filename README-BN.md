# VelvetWish Birthday Studio — বাংলা গাইড

এই ZIP-এ আছে একটি ব্যবসার/প্যাকেজ দেখানোর ওয়েবসাইট এবং তিনটি আলাদা Birthday Surprise template।

## প্যাকেজ ও মূল্য
- **Little Wish / Basic — ৳৩৯৯:** খাম খোলা, শুভেচ্ছা, ব্যক্তিগত বার্তা, ৩টি ছবি, কনফেটি।
- **Signature Story / Popular — ৳৬৯৯:** ৭ ধাপ, ডিজিটাল টাইপোগ্রাফি রিভিল, ৮টি ছবি, মেমোরি গ্যালারি, চিঠি, কেক, লাইভ ঘড়ি, ঐচ্ছিক গান।
- **Velvet Luxe / Luxury — ৳১,১৯৯:** PIN স্ক্রিন (ঐচ্ছিক), তীর-হার্ট-BIRTHDAY cinematic reveal, ১২টি ছবি, মেমোরি, চিঠি, গোল্ড পার্টিকল ও ফিনালে।

তিনটি ডিজাইন/লেআউট ইচ্ছাকৃতভাবে আলাদা: Basic হলো উষ্ণ কাগজ-খাম, Popular হলো ডার্ক ডিজিটাল কোড-রিভিল, Luxury হলো সিনেমাটিক বারগান্ডি-গোল্ড।

## কোন ফাইল এডিট করলেই হবে?
প্রত্যেক প্যাকেজের `config.js` ফাইল এডিট করো। সাধারণত HTML/CSS/মূল JS বদলাতে হবে না।
- `recipientName`: যার জন্মদিন
- `senderName`: যে উপহার দিচ্ছে
- `birthdayDate`: `YYYY-MM-DDTHH:MM:SS` ফরম্যাট
- `message`: ব্যক্তিগত বার্তা
- `pinEnabled` এবং `pin`: Luxury-এর ডেমো PIN gate
- `musicEnabled`: গান চালু/বন্ধ

## শুধু ছবি বদলানোর নিয়ম
প্রত্যেক template-এর `images` ফোল্ডারে নিজের ছবি কপি করে **একই ফাইলের নাম** রাখো:
- Basic: `photo-1.jpg`, `photo-2.jpg`, `photo-3.jpg`
- Popular: `photo-1.jpg` থেকে `photo-8.jpg`
- Luxury: `photo-1.jpg` থেকে `photo-12.jpg`

ছবির নাম একই রাখলে HTML বা JS বদলাতে হবে না। `.jpg`-এর বদলে PNG ব্যবহার করলে ফাইলের নামও `photo-1.jpg` রাখবে না—তখন `config.js`-এর `imageExtension`-কে `png` করো। (সেরা ফলের জন্য JPG, portrait ছবি এবং 1–3 MB-এর মধ্যে রাখো।)

## গান
প্যাকেজের `music` ফোল্ডারে `birthday.mp3` রাখো। তারপর `config.js`-এ `musicEnabled: true` করো। মোবাইলে ব্রাউজার সাধারণত প্রথম tap-এর আগে অটো-প্লে ব্লক করে; তাই মিউজিক বাটন ব্যবহার করতে হবে।

## লোকাল প্রিভিউ
ফোল্ডার থেকে `index.html` খুলে দেখা যায়। কিছু ব্রাউজারে `file://` থেকে অডিও/ছবি আচরণ আলাদা হতে পারে; চূড়ান্ত পরীক্ষা localhost বা অনলাইন hosting-এ করো।

## অনলাইনে প্রকাশ ও QR
1. GitHub-এ নতুন repository তৈরি করো।
2. ZIP extract করে ভেতরের সব ফাইল repository-তে upload করো।
3. Settings → Pages → Deploy from a branch → `main` এবং `/ (root)` বেছে Save করো।
4. সাইট live হলে package URL কপি করো। আলাদা template-ও publish করতে চাইলে root site-সহ পুরো folder structure upload করো; যেমন `https://USERNAME.github.io/REPOSITORY/templates/popular/`।
5. QR তৈরির আগে URL ফোনে খুলে পরীক্ষা করো। তারপর `https://www.qrcode-monkey.com/`-এ URL বসিয়ে QR বানাও এবং অন্য ফোন দিয়ে স্ক্যান পরীক্ষা করো।

## গুরুত্বপূর্ণ সীমাবদ্ধতা/স্বচ্ছতা
- QR code নিজে এই ZIP-এ তৈরি করা হয়নি, কারণ QR-এ দিতে হলে আগে live URL প্রয়োজন।
- PIN screen হলো surprise-এর access gate, নিরাপদ/এনক্রিপ্টেড গোপনীয়তা নয়; config.js-এ PIN দেখা যায়।
- লাইভ countdown-এর জন্য `birthdayDate` ঠিকভাবে সেট করো। উদাহরণ: `2026-10-24T00:00:00`.
- প্যাকেজের মূল্য ও ফিচার ওয়েবসাইটে দেখানো হয়েছে। অতিরিক্ত কাজ, custom domain/hosting বা পরিবর্তনের খরচ থাকলে অর্ডারের আগে ক্রেতাকে পরিষ্কারভাবে জানাবে।


## এই আপডেটের পরিবর্তন
- Basic Little Wish এখন ৪টি আলাদা ধাপে চলে: Intro → Letter → Memories → Final Wish।
- Luxury এখন একসঙ্গে লম্বা পেজ নয়; প্রতিটি বাটনে পরের আলাদা স্ক্রিন/চ্যাপ্টার আসে: PIN/Entry → Heart & Birthday Reveal → Gallery → Letter → Finale।
- মূল VelvetWish হোমপেজে তিনটি প্যাকেজের live iframe preview এবং full preview link যোগ করা হয়েছে।
- Popular প্যাকেজের ডিজাইন/ফ্লো অপরিবর্তিত রাখা হয়েছে।


## Luxury প্যাকেজের আপডেট
- Luxury-র Finale পেজের class ঠিক করা হয়েছে। এখন Letter-এর পর UNVEIL YOUR WISH চাপলে শেষ পেজ দেখাবে; আগে এই পেজটি navigation list-এ ছিল না বলে blank মনে হচ্ছিল।
- Luxury CSS-এ ফোনের ছোট স্ক্রিন, safe-area, বাটনের টাচ সাইজ, গ্যালারির দুই-কলাম লেআউট এবং ছোট স্ক্রিনের typography ঠিক করা হয়েছে।
- ফোনে পরীক্ষা করতে Chrome-এ সাইট খুলে প্রতিটি ধাপ ট্যাপ করবে; লাইভ সাইটে আপডেট দেখতে সংশোধিত ফাইলগুলো আবার hosting-এ আপলোড করতে হবে।
