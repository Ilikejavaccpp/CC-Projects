# CC-Projects

[TOC]

my c/c++ projects here. DO NOT EDIT unless downloaded / cloned

<hr>



## How to Clone / Download

Simply just open <a href="https://github.com">Github</a> and go to <a href="https://github.com/Ilikejavaccpp/CC-Projects">my (this current) repository.</a> and simply click on the code thingy that looks like 
> <> Code
<h3 style="align: center; text-align: center;">OR</h3>
Simply open up your terminal and type in the following command

> sh
>&gt; mkdir <b>&lt;dir&gt;</b><i> *</i>
>&gt; cd <b>&lt;dir&gt;</b>
>&gt; git clone https://github.com/Ilikejavaccpp/CC-Projects/

if on Windows (using either Command Prompt or Windows Powershell)
</br>

> bash
>&dollar; mkdir <b>&lt;dir&gt;</b> <i> *</i>
>&dollar; cd <b>&lt;dir&gt;</b>
>&dollar; git clone https://github.com/Ilikejavaccpp/CC-Projects/

if on Linux/MacOS (Konsole or whatever)
</br>
Then, on <strong>all</strong> OS inside <b>&lt;dir&gt;</b>, simply build

> sh
> cd CC-Projects/C-gui/<t># should be inside your <b>&lt;dir&gt;</b></t>
> cmake -S . -B build/
> cd build/ && make

<hr>
</br>
* <i>Where </i><b>&lt;dir&gt;</b><i> is a replacement for your directory (folder) name.</i>

<hr>

## Once Cloned / Downloaded

<p>
Once you have cloned (downloaded) the repo, you now have full access to do what u want with it. <u>It is simply a journey of somebody learning <a href="https://learnopengl.com/">OpenGL</a></u> .
</p>
<p>
</t>You may also edit the <a href="https://github.com/Ilikejavaccpp/CC-Projects.git">.gitignore</a> file provided in the</p>

> C-gui/

or (remove the below)
> C-gui/lib/glfw/.gitignore
C-gui/lib/raylib/.gitignore

<hr>

## File Structure

The file structure is (C-gui is where all it is for OpenGl,Raylib for C; which is the main focus)
> C-gui/
> |__ build/ (untracked)
> |__ include/
> |__ lib/
> |__ src/
|---^|__ main.c
> |__ [M] CMakeLists.txt
> |__ [g] .gitignore
> |__ ..
|---^|__ [i] README.md (this document)
> |__ .gitignore