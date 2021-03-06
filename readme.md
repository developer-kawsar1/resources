
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
5. Private route
```hs 
<Route path='/orders' 
   element={
          <RequireAuth>
            <Orders></Orders>
          </RequireAuth>
        }>
</Route>


```
6. Require Auth
```hs 
import { getAuth } from 'firebase/auth';
import React from 'react';
import { useAuthState } from 'react-firebase-hooks/auth';
import { Navigate, useLocation } from 'react-router-dom';
import app from '../../firebase.init';

const auth = getAuth(app);

const RequireAuth = ({children}) => {
    const [user,loading] = useAuthState(auth);
    const location = useLocation();
       if(loading){
        return <Loading></Loading>
    }
    if(!user){
        return <Navigate to="/login" state={{ from: location }} replace />;
    }
    return children;
};

export default RequireAuth;
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
3. Msin css file এর মধ্যে ডাইরেক্টিভ এড করা 

```hs
@tailwind base;
@tailwind components;
@tailwind utilities;
```

# Daisy ui
1. Install
```hs
npm i daisyui

```

2.Then add daisyUI to  tailwind.config.js files:
```hs
module.exports = {
  //...
  plugins: [require("daisyui")],
}
```

# Edit daisy color 
1.Add Daisy ui object item after plugins object
```hs
module.exports = {
  content: ["./src/**/*.{html,js}"],
  theme: {
    extend: {},
  },
  plugins: [require("daisyui")],
  daisyui: {
    themes: [
      {
        mytheme: {
          primary: "#0FCFEC",
          secondary: "#19D3AE",
          accent: "#3A4256",
          neutral: "#3d4451",
          "base-100": "#ffffff",
        },
      },
      "dark",
      "cupcake",
    ],
  },
}

```




# React firebase hook

1.google login import
```
import { useCreateUserWithEmailAndPassword, useSignInWithGoogle, useUpdateProfile } from 'react-firebase-hooks/auth';
```
2.google login hook
```hs
const [signInWithGoogle, gUser, gLoading, gError] = useSignInWithGoogle(auth);
```
 
# Fontawesome 5 

```hs
  <link
            rel="stylesheet"
            href="https://pro.fontawesome.com/releases/v5.10.0/css/all.css"
            integrity="sha384-AYmEC3Yw5cVb3ZcuHtOA93w35dYTsvhLPVnYs9eStHfGJvOvKxVfELGroGkvsg+p"
            crossorigin="anonymous"
        />
```
