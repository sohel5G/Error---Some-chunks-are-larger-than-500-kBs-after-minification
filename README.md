# Error---Some-chunks-are-larger-than-500-kBs-after-minification
 Some chunks are larger than 500 kBs after minification. Consider: - Using dynamic import() to code-split the application - Use build.rollupOptions.output.manualChunks to improve chunking: https://rollupjs.org/configuration-options/#output-manualchunks - Adjust chunk size limit for this warning via build.chunkSizeWarningLimit.
