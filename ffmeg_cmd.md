**Step 1: Generate a High-Quality Palette**

ffmpeg -i D:\\Git\_Repositories\\Optimizers\\animation\_Smooth\_Valley.mp4 -vf "fps=30,scale=800:-1:flags=lanczos,palettegen" palette.png



ffmpeg -i D:\\Git\_Repositories\\Optimizers\\animation\_Narrow\_Valley.mp4 -vf "fps=30,scale=800:-1:flags=lanczos,palettegen" palette.png



ffmpeg -i D:\\Git\_Repositories\\Optimizers\\animation\_Peaks\_and\_Valleys.mp4 -vf "fps=30,scale=800:-1:flags=lanczos,palettegen" palette.png



ffmpeg -i D:\\Git\_Repositories\\Optimizers\\animation\_Saddle\_Point.mp4 -vf "fps=30,scale=800:-1:flags=lanczos,palettegen" palette.png







**Step 2: Create the GIF with the Palette**

ffmpeg -i D:\\Git\_Repositories\\Optimizers\\animation\_Smooth\_Valley.mp4 -i palette.png -lavfi "fps=30,scale=800:-1:flags=lanczos\[x];\[x]\[1:v]paletteuse" D:\\Git\_Repositories\\Optimizers\\images\\SmoothValley.gif



ffmpeg -i D:\\Git\_Repositories\\Optimizers\\animation\_Narrow\_Valley.mp4 -i palette.png -lavfi "fps=30,scale=800:-1:flags=lanczos\[x];\[x]\[1:v]paletteuse" D:\\Git\_Repositories\\Optimizers\\images\\NarrowValley.gif



ffmpeg -i D:\\Git\_Repositories\\Optimizers\\animation\_Peaks\_and\_Valleys.mp4 -i palette.png -lavfi "fps=30,scale=800:-1:flags=lanczos\[x];\[x]\[1:v]paletteuse" D:\\Git\_Repositories\\Optimizers\\images\\PeaksandValleys.gif



ffmpeg -i D:\\Git\_Repositories\\Optimizers\\animation\_Saddle\_Point.mp4 -i palette.png -lavfi "fps=30,scale=800:-1:flags=lanczos\[x];\[x]\[1:v]paletteuse" D:\\Git\_Repositories\\Optimizers\\images\\SaddlePoint.gif

