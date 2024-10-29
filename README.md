# astro-server-island-with-script
Demonstrating unexpected behavior when using scripts in an Astro server island, as the script in the island is executed before the server island is fetched.\
Additionally, the entire .astro file is being shipped to the client when there is a script tag in the server island. This is not the case if the server island does not contain a script tag.

## Steps to reproduce
1. Run npm install.
2. Run npm run dev.
3. Navigate to http://localhost:4321.
4. Click "Celebrate! (Using Astro component)" and "Celebrate! (Using server island)" to observe the difference.
5. Open the "Sources" tab in the browser's developer tools and notice that the entire .astro file is available to the client. 
