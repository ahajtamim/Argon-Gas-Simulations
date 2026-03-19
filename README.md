ffmpeg -i Media/argon_2d.mp4 -vf "fps=15,scale=800:-1:flags=lanczos,palettegen" palette.png
ffmpeg -i Media/argon_2d.mp4 -i palette.png -filter_complex "fps=15,scale=800:-1:flags=lanczos[x];[x][1:v]paletteuse" argon_2d.gif

<video src="Media/argon_3d.mp4" controls autoplay loop muted width="600"></video>