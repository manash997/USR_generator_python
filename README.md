# USR_generator_python
This is the program to generate USR from a sentence
To run this program save both the files in your directory where the USR setup exists
1)Create a folder named "txt_files"
txt_files:It is the folder where the input file and all the intermediate program outputs will be stored
2)Run the command "python3 complete_usr.py" on shell
3)Enter the filename where a single simple sentence is stored.If file is not in current directory,then provide full-path along with filename
4)Enter the desired filename where the final generated USR output will be stored.a path+filename can also be specified.
-The program calls check_punctuation() function where the it is modified according to required punctuation(fullstop,space before final symbol etc.)
-parser,wx,pruner called
-final USR program called
5)Check output in output file specified.

