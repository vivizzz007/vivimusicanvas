# vivimusicanvas

Implementing a new way to get beautiful custom canvas videos for the ViviMusic app!

This repository acts as the central hub for mapping custom `.mp4` videos to specific songs or albums within ViviMusic. It is powered by Vercel, meaning any changes you push to this repository are instantly deployed and served via a lightning-fast global CDN. 

## How to add a new Canvas

If you find a cool visualizer or music video and want to display it in the background of ViviMusic whenever a specific song plays, follow these steps:

### 1. Upload your Video
Upload your `.mp4` file into either the `Song/` or `Album/` directories within this repository. 
*Example: `Song/dracula_visualizer.mp4`*

### 2. Update `canvas.json`
Open the `canvas.json` file located in the root of the repository. You will add a new block to the `"items"` array mapping the exact song name and artist to your new video URL.

Make sure your URL points to your deployed Vercel domain!

**Example:**
```json
{
  "items": [
    {
      "song": "Song Title",
      "artist": "Artist Name",
      "url": "https://vivimusicanvas.vercel.app/Song/your_video.mp4"
    }
  ]
}
```

### 3. Commit and Push
Once you have uploaded your video and updated `canvas.json`, simply commit your changes and push them to GitHub. 

```bash
git add .
git commit -m "feat: added canvas for Song Title"
git push
```

That's it! Vercel will automatically redeploy your changes. The next time you play that song in ViviMusic, your custom video will automatically be fetched and looped in the background!
