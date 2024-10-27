# pmake

## Who its for:

THIS UTILITY IS MAINLY MEANT TO BE USED IN COMBINATION WITH GNU EMACS.

THIS UTILITY IS MAINLY MEANT FOR LINUX USERS, HOWEVER IT IS POSSIBLE TO GET IT TO WORK USING MSYS2 ON WINDOWS.

THIS UTILITY IS MAINLY MEANT FOR GENERATING C PROJECT FOLDERS, BUT THE SOURCE CODE SHOULD BE EASY TO CONFIGURE FOR YOUR LANGUAGE OF CHOICE.

THIS UTILITY HAS BIAS TOWARDS GCC, HOWEVER IT SHOULD BE EASY TO ALTER THE SOURCE CODE TO PREPARE THE MAKEFILE FOR THE COMPILER OF YOUR CHOICE.

## Soft dependencies:

- GNU C COMPILER (You can swap it for any C compiler in the source code by changing the CC variable in the printf function in S1. Alternatively, you could go for a different language entirely since gtags supports several other languages.)

- GNU EMACS (I havent really designed this script for other editors, but you are free to hack it for your own use case. I tried to document the code to make it easier.)

## Dependencies:

* GNU BASH (https://www.gnu.org/software/bash/)

* GNU MAKE (https://www.gnu.org/software/make/)

* GLOBAL (https://www.gnu.org/software/global/)

## USAGE EXAMPLE
- So, I wanted to show my self setting up an SDL project as an example. So I downloaded the source here for SDL2 [SDL2](https://github.com/libsdl-org/SDL/releases/tag/release-2.30.8 "SDL2")

- In order to get all the includes and libs in one directory to make the process easier, I created a new directory in my home folder named il and a subdirectory named SDL2, and I ran ./configure --prefix=$HOME/il/SDL2 in order to gaslight the makefile into thinking thats where it should throw all the files in after running make install.

- After running all those commands, i navigated to $HOME/il/SDL2 and ran PWD to get the absolute path of this place, and then i used this to feed into pmake. It asks me what the include path will be, so i give it /home/sudotouchgrass/il/SDL2/include and when asked where the libs are i give it /home/sudotouchgrass/il/SDL2/lib and then the script does its work.

