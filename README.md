
![CC Graphics 2024_ TEX](https://github.com/csae-coders-corner/Compiling-.tex-files-to-.docx/assets/148211163/a8d46ef0-a6e4-4c69-b07d-018486c27a2b)

# Compiling-.tex-files-to-.docx
Working with LaTeX is super convenient, but the downside is that it can make teamwork a challenge. That is especially true if a team includes individuals from fields in which LaTeX is not the default text editing language. In this post, I will walk you through a way to compile your .tex into a .docx. 
Just as a warning, step 1 is the most tedious step if you are not familiar with command prompts, but fortunately, you just need to run it once. When that’s done, you will never (hopefully ever) have to worry about step 1 again.

## STEP 1: Installing Pandcoc
**Mac OS**
1.	Make sure you have .tex compiler installed. If you don’t, go here or here.
2.	Open the terminal:
Press command+spacebar to launch Spotlight, then type terminal and press enter.

4.	If you don’t already have it installed, install Homebrew :
`/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`

6.	In the command line, install the compiling tool:
`brew install pandoc`

8.	If you want to also compile the bibliography, install the bibliography tool:
`brew install pandoc-citeproc`

**Windows OS**
1.	Make sure you have (.tex compiler) installed. If you don’t, go here.
2.	Open the terminal:
Press windows+r and type cmd then press ctrl+shift+enter (that will allow you to open the terminal as admin).

3.	If you don’t already have Chocolatey installed, then install it with this command line (make sure you correct the line break that might occur when you copy/paste this command):

```
@"%SystemRoot%\System32\WindowsPowerShell\v1.0\powershell.exe" -NoProfile -InputFormat None -ExecutionPolicy Bypass -Command "iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))" && SET "PATH=%PATH%;%ALLUSERSPROFILE%\chocolatey\bin"
```
If it doesn’t work, go here for more information on why it doesn’t work.

4.	In the command line, install the compiling tool:
choco install pandoc

## STEP 2: Compiling your .tex into a .docx
If you are a windows user and your files are located in a different drive, first specify the correct drive. Here is an example for the “D:” drive:
```
D: 
cd temp
```

1.	You first need to specify the directory in which all your files that will compile are located with the change directory command:
`cd “path”`
For Mac OS something like: `cd “user/Documents/Texfolder”`
For Windows OS something like: `cd ‘‘C:\user\Texfolder\’’` 

2.	Then to compile it into a word document you write (note that here texfile.tex is pre-existing and wordfile.docx is the created file):
`pandoc texfile.tex -o wordfile.docx`

3.	Adding the bibliography:
`pandoc texfile.tex -o wordfile.docx –bibliography references.bib`


Pandoc allows for way more conversions. Go to [https://pandoc.org/demos.html](https://pandoc.org/demos.html) for more!


**Binta Zahra Diop, DPhil Candidate in Economics, St Hugh's College, Oxford, 04 November 2019**
