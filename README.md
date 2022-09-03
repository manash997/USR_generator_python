Pre-requisites:The USR program takes as input,the output from parser,morph-analyzer and utf8_wx generator.
install the three first with python 2.7.
(1) Install iscnlp parser 
	Please follow the instructions given in the [https://bitbucket.org/iscnlp/] repository.
	First, install the tokenizer, then the pos-tagger, and then the parser. (Run all the commands in home itself)
	
	Read the readme given in all three and run the code given in terminal.
	In pos-tagger and parser,
		Run the dependencies code after installing them with given codes.
		
	After installing,
		Keep your input file in parser folder and run command
			isc-parser -i <input_file_name> > <output_file_name> 
		in terminal and your parser output will be saved in your output file.
			eg, 
				isc-parser -i inp > oup


(2) Install Morph
	Download the given file [ilmt-morph-ner-from-api-0.2.zip] and extract it in parser folder.
	Now open ilmt folder and put .py files in parser folder OR change the path of morph command in [makenewusr.sh file].
	Download the given file [dictionary-scrapper.py] and put in parser folder.
	Run following commands in terminal in parser folder.
		sudo apt install python2.7
		sudo apt-get install python-requests
		
	Download get-pip.py and copy it in parser folder.
	Run following commands in terminal in parser folder.
		sudo python2.7 get-pip.py 
		sudo pip2.7 install requests
		
	Keep your input file in parser folder and run following command
		python2.7 getMorphPruneAndNER.py -i <input_filename> -o <ouput_filename>
	in terminal and your morph output will be saved in your output file.
			eg,
				python2.7 getMorphPruneAndNER.py -i test -o testoup


(3) Install utf8_wx
	copy this file in parser folder.
	run command 
		sudo bash install-project.sh			

4)TAM dictionary in a tsv format is also needed in current folder :filename- TAM-num-per-details.tsv.wx


1)Save the file in the directory,where the USR set-up is installed
2)Open the file and in the following lines,provide relevant path:
line 7:path of parser-output.txt
line 8:path of prune-output.txt
line 9:path of wx.txt
line 125:Change "TAM-num-per-details.tsv (2).wx" to the current name of your TAM dictionary file

3)generate output of parser,prune and wx using your old program
4)After that,run this python script using "python3 generate_usr.py" on command line.
5)The output of the program is generated on command line,you can redirect it to an empty file accordingly.for eg "python3 generate_usr.py > hello.txt" generates the output in an empty file called hello.txt.

