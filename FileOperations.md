
				## **File Class and its basic methods** ##

For File Handling there are 3 main steps:
	1. Open File
	2. Read/Write/Append File
	3. Close File
 
* **File Open Operation**
	`file1 = File.open("Sample.txt")`

* **File Read Operation**
	```	
	data= file1.read
	puts "Reading sample.txt in one hop "
	puts data

	puts "\nReading Sample2.txt line by line"
	file2 = File.open("Sample2.txt")
	File.foreach(file2) do |line|
		puts line
		puts "Seperater"
	end
	```
* **File Write Operation**
	```	
	f1= File.open("Writing.txt","w") 
	f1.write("This file is written by a Ruby Program")
	```
* **File append Operation**
	```	
	file_handle= File.open("Writing.txt","a")
	file_handle.write("\nThis text is appended by Ruby program")
	```
* **File Close Operation**
	```	
	file_handle= File.open("Writing.txt","W")
	file_handle.close
	```
* **Other basic file operations**

	* File.rename(old_nm,new_nm) - renames the given file
		`File.rename("Writing","WritingPad")`
	
	* File.size(file_nm)- returns file size in bytes
		`puts "Sample2.txt  Size: #{File.size("Sample2.txt")} bytes"`

	* File.exist? - check existance of file and return true or false
		`puts "Login file exists" if File.exist?("login.rb")`
		`puts "Sample file exists" if File.exist?("Sample.txt")

	* File.dirname(file_nm) - returns path of file upto its directory name
		`puts "Location of Sample2.txt is #{File.dirname("/ruby_training/Sample2.txt")}"`
	
	* File.basename(file_nm) - return only name of the file from whole path
		`puts "Basename of file /ruby_training/Sample2.txt is #{File.basename("/ruby_training/Sample2.txt")}"`

	* File.atime(file_nm) - returns recent append time for given file
		`puts "WritingPad was recently appended on #{File.atime("Writing.txt")}"	#returns last append time`

	* File.delete(file_nm) - deletes given file from memory
		`if File.delete("Garbage.txt")`
			`puts "Garbage.txt is deleted"`
		'end'


