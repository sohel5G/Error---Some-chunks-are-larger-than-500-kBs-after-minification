# Error---Some-chunks-are-larger-than-500-kBs-after-minification


 ## Common error : 
```javascript
 (!) Some chunks are larger than 500 kBs after minification. Consider:
- Using dynamic import() to code-split the application
- Use build.rollupOptions.output.manualChunks to improve chunking: https://rollupjs.org/configuration-options/#output-manualchunks
- Adjust chunk size limit for this warning via build.chunkSizeWarningLimit.
```

## Solution 

Add the below code in > vite.config.js
  ```javascript
  build: {
    chunkSizeWarningLimit: 2000, // Set your preferred limit in kB
  }
```
  

 ## So original file will look like this 
```javascript
import { defineConfig } from 'vite'
import react from '@vitejs/plugin-react'

// https://vitejs.dev/config/
export default defineConfig({
  plugins: [react()],
  build: {
    chunkSizeWarningLimit: 2000, // Set your preferred limit in kB
  }
})
```
