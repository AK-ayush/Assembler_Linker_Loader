/////////////////////////////////////////
/										/	
/    	Assembler_Linker_Loader			/
/										/ 	
/////////////////////////////////////////	

Discription:
			This is a simulation of the assembler, 
			linker and loader implemented in operating System.
			All simple or complicated programs of each languages
			must pass through these and finally converted to 
			Machine readable instrcutions which are actually 
			computed by CPU.
Mechanism :
			Input to the assembler is program written in simple 'C' type
			language( not 'C' exactly). Assembler parse this program file
			and convert them to assembly code(8085) which is input to the 
			linker. Linker connect those variables and functions which are 
			in different files and used somewhere else , and generate a new 
			file which contain the assembly code of program but variables 
			and functions are linked wich is input to loader. Loader takes 
			argument as memorylocation at which the code should be loaded, 
			then just change the jump and branch instructions accordingly 
			and generates a new file which contains the linked assembly code
			and ready to loaded at perticuler memory location. 

How to use:
			Open the terminal of your linux machine and change directory 
			to directory at which the Assembler_linker_loader is present.
			and type :
			$cd Assembler_linker_loader
			$python run.py

			an file dialog will be open to select the program files as input,
			to choose multiple files, press CTRL and select those files after
			this click open then assembling starts and generate files 
			
			after pass 1 : "file_name.pre"
			after pass 2 : "file_name.pre.s"

			and "file_name.pre.s" input to linker which linked the variable 
			and functions among different files and generate a file:

			"file_name.linked.8085"

			which actually input to the loader. Loader take input as a specific 
			memory location on terminal and change those instructions which are
			using absolute memory location. Loader generates the finle file:

			"file_name.loaded.8085"   


--> I have tested it on ubuntu 14.04 and it works well so will be on most 
Linux machines but for windows file dialog box part causes the problem because
that code is only for linux machines, so not sure about windows.


/********************/
/	THANK YOU 		 /	
/********************/