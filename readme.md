
# [Dark colors code](https://developer-kawsar1.github.io/colors/)

রিয়েক্ট প্রজেক্ট তৈরি

```hs
 npx create-react-app appname
```
রিয়েক্ট রাউটার ইন্সটল

```hs
npm install react-router-dom@6

```
index.js ফাইলে
```hs
    <BrowserRouter>
      <App />
    </BrowserRouter>
```
index.js ফাইলে Import করতে হবে 
```hs
import { BrowserRouter } from "react-router-dom";
```

App.js ফাইলে 
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
