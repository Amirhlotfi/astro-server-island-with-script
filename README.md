# astro-server-island-with-script
Demonstrating unexpected behavior when using scripts in an Astro server island. 
The script within the island is executed before the server island is fetched. Additionally, the entire .astro file is being shipped to the client when there is a script tag in the server island.

## Steps to reproduce
1. Run npm install.
2. Run npm run dev.
3. Navigate to http://localhost:4321.
4. Click "Celebrate! (Using Astro component)" and "Celebrate! (Using server island)" to observe the differences.
5. Open the "Sources" tab in the browser's developer tools and notice that the entire .astro file is available to the client.