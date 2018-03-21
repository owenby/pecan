# Pecan
Pecan is a bar for macOS.  It was built to be highly configurable and — by default — reports the current workspace, network bandwidth, date, battery percentage and time.

![Screenshot 1](/screenshots/3.jpg)

![Screenshot 2](/screenshots/4.jpg)

![Screenshot 3](/screenshots/1.jpg)

![Screenshot 4](/screenshots/2.jpg)

## Instructions

Pecan requires [Übersicht](http://tracesof.net/uebersicht/).  Once Übersicht is installed, you can clone this repository to where your Übersicht bars are placed.

```
git clone https://github.com/zzzeyez/Pecan.git $HOME/Library/Application\ Support/Übersicht/widgets/Pecan
```

If Übersicht is running, then the bar should appear.

## Optional features
  
#### Network bandwidth

Current download and upload speeds may be shown in the 2nd-to-left element via Ifstat.  If Ifstat is not found, then the current wifi network will be displayed instead.  To install Ifstat via Homebrew:

```
brew install ifstat
```
  
#### Workspaces

Current workspace ID can be shown on the left element if [ChunkWM](https://github.com/koekeishiya/chunkwm) is installed, otherwise an Apple symbol will be shown instead.  To install ChunkWM:
  
```
brew tap crisidev/homebrew-chunkwm
brew install chunkwm
````

## Customization
Pecan is, by default, styled like shown in the top screenshot.  However, Because Pecan is styled using CSS3 variables, the top lines of `style.css` can easily be editted to change properties like opacity, alignment, padding, colors and more.  If you are using this bar with Wal, then you should be editting `scss/style.scss` instead.

#### Wal

Pecan can pull a color palette generated by Wal using Sassc.  I have included a script, `wal-set`, that will perform this.
 
To install Sassc:

```
brew install sassc
```
  
And then you must change the username at the top of `scss/style.scss` to that of your own:

```
sed -i -e "s/zzzeyez/$USER/g" ~/Library/Application\ Support/Übersicht/widgets/Pecan/scss/style.scss
```
  
Now you can run the script to use Wal's palettes:

```
bash ~/Library/Application\ Support/Übersicht/widgets/Pecan/wal-set
```

