
# [Dark colors code](https://developer-kawsar1.github.io/colors/)

রিয়েক্ট প্রজেক্ট তৈরি

```hs
 npx create-react-app appname
```
# Router
1. রিয়েক্ট রাউটার ইন্সটল

```hs
npm install react-router-dom@6

```
2. index.js ফাইলে
```hs
    <BrowserRouter>
      <App />
    </BrowserRouter>
```
index.js ফাইলে Import করতে হবে 
```hs
import { BrowserRouter } from "react-router-dom";
```

3. App.js ফাইলে রাউট সেট করা
```hs
<Routes>
        <Route path="/" element={<Home />} />
        <Route path="about" element={<About />} />
 </Routes>
```
App.js ফাইলে import করতে হবে 
```hs
import { Routes, Route } from "react-router-dom";
```
4. মেনুতে দেখানো 
```hs
<Link to="/">Home</Link>
 <Link to="about">About</Link>
```

# tailwinnd css
1. Install and create tailwind cinfig js file
```hs
npm install -D tailwindcss
npx tailwindcss init
```
2. Edit tailwind config js file
```hs
module.exports = {
  content: ["./src/**/*.{html,js}"],
  theme: {
    extend: {},
  },
  plugins: [],
}
```


