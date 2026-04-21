Tool name: Link Peeker
One-sentence purpose: Shows the final destination URL of any link before you click it.
Core behavior: When the user holds the mouse button down on any link, the extension resolves all redirects and displays the final URL in a small tooltip near the cursor. Releasing the mouse dismisses the tooltip.
Stack: Chrome MV3 extension
Needs Cloudflare Worker proxy: no
AI model calls: no
If yes, what for: 
Free vs Pro split: free only
If freemium, describe split: 
Known edge cases or constraints: Some links are JavaScript-driven and have no real href. If resolution fails or times out after 3 seconds, show "Could not resolve" instead of hanging.
