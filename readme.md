# React + Vite + Tailwind CSS + React Router Setup Guide

This guide will help you set up a React project using **Vite**, **Tailwind CSS**, and **React Router**.

---

## Step 1: Create a New React App with Vite
   
   1. Go to [https://react.dev](https://react.dev)
   2.  Navigate to:
      - `Learn` → `Installation` → `From Scratch` → `Vite`
   3. Run the following command in **your desired folder**:
   
      ```bash
      npm create vite@latest ./
      ```
      **⚠️ The ./ is important — it tells Vite to initialize the project in the current directory**
   
 4.If you accidentally ran it in the wrong folder, navigate using:

  ```
  cd your-folder-name
  ```
 5. After setup, check your React version in package.json. <sub>we are using V19 during our course</sub>
 6. You will only be editing files inside the src/ folder.
 7. Install React and all dependencies using command
  ```bash
   npm install
   ```
 8. Start Development server using
  ```bash

   npm run dev

   ``` 
   
## Step 2: Install and Set Up Tailwind CSS

   1. Go to [https://tailwindcss.com/] (https://tailwindcss.com/)
   2.  Navigate to:
      - `Docs` → `Installation` → `Using Vite` + `Follow the given steps till step 4`
        
   *Or* or directly: https://tailwindcss.com/docs/installation/using-vite and follow till step 4
   
      **⚠️ Do not do the step 5 as it is not related to Vite using React**
   
   ### Commands to run:
   
   ```bash
   
   npm install tailwindcss @tailwindcss/vite
   ```
   
   and after vite.config and index.css run 
   
   ```bash
   
   npm run dev
   ```
   to start the development server and test using writing any tailwind class to src/app.jsx file and see changes
   
   **Just to show files should look post installing Tailwind.**
   
   1. vite.config.js
   ```javascript
   import { defineConfig } from 'vite'
   import react from '@vitejs/plugin-react'
   import tailwindcss from '@tailwindcss/vite'
   
   // https://vite.dev/config/
   export default defineConfig({
     plugins: [
       react(),
       tailwindcss(),
     ],
   })
   ```
   2. src/index.css
   
   ```css
   @import "tailwindcss";
   
   ```
   
   ***Thats all Changes required in files for installing tailwind Css in React***
   
## Step 3: Install React Router for routing inside our react application:
  1. Go to Link: https://reactrouter.com/start/declarative/installation
 
   ***OR***
   
  1.  go to https://reactrouter.com and navigate: `Docs`->`Delarative`-> `Installation`
  2. Next install React Router from npm:
    ```bash
      npm i react-router
    ```
  4. Make your main.jsx look like this
      ```jsx
     
      import { StrictMode } from 'react'
      import { createRoot } from 'react-dom/client'
      import './index.css'
      import { BrowserRouter, Routes, Route } from "react-router";
      import App from './App.jsx'
      
      createRoot(document.getElementById('root')).render(
        <StrictMode>
        <BrowserRouter>
          <Routes>
            <Route path="/" element={<App />} />
          </Routes>
        </BrowserRouter>
        </StrictMode>,
  
        ) 
      ```

     
