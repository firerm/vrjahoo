# VR180 Web Player
A web-based video player for 180 degree, 3D video.

Got an immersive video you want people to see with the Apple Vision Pro or Meta Quest headsets? You could build an app and deal with corporate policies and rejections. You can put it on YouTube but it will be limited to 4k and Meta headsets. Or, now, you can use this web player and put it on your website.

## How to use it
Add the player script `<script type="module" src="vr180-player.js"></script>` before the closing body tag and use this HTML snippet: 
```
<div id="player-container">
	<div id="video-info" style="display: none;"><!-- You can put whatever you like in this div. It's only shown when VR is available. -->
		<video id="vrVideo" controls crossOrigin="anonymous" playsinline webkit-playsinline>
			<source src="REPLACE_THIS.mp4" type="video/mp4">`
		</video>
		<button id="enterVrBtn">Enter VR</button>
	</div>
</div>
```
When VR is available, the page will display a button (and anything else you include inside `<div id="video-info">`) to begin the immersive experience. 

<img src="https://github.com/user-attachments/assets/05db6208-6d42-48fa-a0da-55de41f35e6d" width=50%>

*Example Button*

Once the video is playing, you can bring up video controls. When the video is over, you'll automatically exit the experience.

![vr180-web-player](https://github.com/user-attachments/assets/ac86dba9-add9-462e-9590-26abc5f20912)

## Video Format
**The player only supports 2:1, side-by-side video using either H.264 or HEVC in an mp4 file by default.** It does not support over-under. MV-HEVC (Apple spatial video) files are converted at runtime using ffmpeg.wasm so they can play in the same player.

## Features
Tapping anywhere will bring up the controls. Without interaction they will go away in 10 seconds. Tapping outside of the controls will close them right away.
- Play/Pause
- Rewind 15 seconds
- Skip 15 seconds
- Mute/Unmute
- Seek
- Exit VR

## Future
I'm not a developer. I used Google's Gemini to help create this and give me the ability to post immersive videos on my website. I'm unlikely to be able to help you if you run into problems, want to customize this, or add new features. I'm releasing this with the [unlicense](https://unlicense.org/) so you're free to do anything at all with it. That said, if you have ideas or want to contribute code, I'd love to [hear](mailto:hello@michaelverdi.com) from you.

## Demo
**Test it out in a headset!**
Open [https://exp.michaelverdi.com/vr180web](https://exp.michaelverdi.com/vr180web) in browser on your headset and then click the Enter VR button.
