HTML-Only Security Cam (WebRTC)

What this is
------------
Two static HTML pages (camera.html and viewer.html) that establish a peer-to-peer
WebRTC connection using manual copy/paste for signaling. No Node.js, no backend.
Great for simple remote checks when both sides have reasonable NAT traversal.
On very strict networks you may need a TURN server (not included).

Quick Start
-----------
1) Host these files over HTTPS (recommended) or open camera.html on localhost.
   - Easiest: GitHub Pages, Netlify, or any static file host.
2) On the computer with the webcam:
   - Open camera.html
   - Click "Start camera"
   - Click "Create Offer" and copy the JSON Offer
3) On your phone:
   - Open viewer.html (must be HTTPS for best compatibility)
   - Paste the Offer
   - Click "Create Answer" and copy the JSON Answer
4) Back on the camera page:
   - Paste the Answer
   - Click "Apply Answer"

Tips
----
- Keep the camera tab active and prevent the computer from sleeping.
- If the video doesn't appear on iPhone, tap the video or the play control once.
- If it won't connect across certain networks, you likely need a TURN relay.
  You can add your own TURN server credentials inside each HTML file (search for "TURN").
