# saturation
Saturation control for xrandr

## Building

For Ubuntu, `libxrandr-dev` and `libdrm-dev` need to be installed, then you 
can run make and it will compile an executable called `cmddemo`

    chmod +x cmdemo cmsaturation.pl

Then copy it to somewhere in your path. `~/.local/bin` is a common one, I have 
`~/bin` on my path due to this being a long time ago standard place to set 
`GOBIN` for `go install`.

run `xrandr` and it will show you your currently connected displays. 

	root@bravobravo:/home/loki/color-demo-app# xrandr
	Screen 0: minimum 320 x 200, current 4480 x 1440, maximum 16384 x 16384
	eDP connected primary 1920x1080+2560+240 (normal left inverted right x axis y axis) 344mm x 194mm
	   1920x1080    144.00*+ 120.02    96.00    72.00    60.01    50.01    48.00    48.00  
	   1680x1050    144.00  
	   1280x1024    144.00  
	   1440x900     144.00  
	   1280x800     144.00  
	   1280x720     144.00  
	   1024x768     144.00  
	   800x600      144.00  
	   640x480      144.00  
	HDMI-A-1-0 connected 2560x1440+0+0 (normal left inverted right x axis y axis) 527mm x 296mm
	   2560x1440     59.95 +  74.78* 
	   1920x1200     59.95  
	   1920x1080     60.00    60.00    50.00    59.94  
	   1600x1200     60.00  
	   1680x1050     59.88  
	   1280x1024     75.02    60.02  
	   1440x900      59.90  
	   1366x768      59.79  
	   1280x800      59.91  
	   1152x864      75.00  
	   1280x720      60.00    50.00    59.94  
	   1024x768      75.03    70.07    60.00  
	   832x624       74.55  
	   800x600       72.19    75.00    60.32  
	   720x576       50.00  
	   720x480       60.00    59.94  
	   640x480       75.00    72.81    60.00    59.94  
	   720x400       70.08  

Then you can call `cmsaturation.pl eDP 1.6` for example, which will crank up 
the color saturation of your laptop's inbuilt panel. This was my purpose for 
doing it as the default color transform setting on the 144hz panel is very 
unsaturated.