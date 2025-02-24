# Import and parse a text file

<h1>Introduction</h1>
Security logs are often stored in text files. To analyze the security logs in these files, security analysts have to import and parse these files. Python has some functions that come in handy for these tasks, allowing analysts to efficiently access information from text files.

In this lab, you'll practice using functions and other syntax in Python to import and parse text files.

<h1>Scenario</h1>
In this lab, you're working as a security analyst. You're responsible for preparing a security log file for analysis and creating a text file with IP addresses that are allowed to access restricted information.

<h1>Task 1</h1>
In this task, you'll import a security log text file and store it as a string to prepare it for analysis.

In Python, a with statement is often used in file handling to open a file and then automatically close the file after reading it.

You're given a variable named import_file that contains the name of the log file that you want to import. Start by writing the first line of the with statement in the following code cell. Use the open() function, setting the second parameter to "r". Note that running this code will produce an error because it will only contain the first line of the with statement; you'll complete this with statement in the task after this. Be sure to replace the ### YOUR CODE HERE ### with your own code.

![image](https://github.com/user-attachments/assets/26a043d4-83ea-4f53-a259-7fcc4073926c)

<h1>Task 2</h1>
Now, you'll use the .read() method to read the imported file, and you'll store the result in a variable named text. Afterwards, display the text and explore what it contains by running the cell. Be sure to replace the ### YOUR CODE HERE ### with your own code before you run the following cell.

![image](https://github.com/user-attachments/assets/2930ef30-1f64-4615-b7fd-018331288267)

![image](https://github.com/user-attachments/assets/31be164b-2553-4ec5-b744-c8d297c3cb56)

<h1>Task 3</h1>
The output in the previous step is one big string. In this task, you'll explore how you can split the string that contains the entire imported log file into a list of strings, one string per line.

Use the .split() method to perform this split and then display the result. Be sure to replace the ### YOUR CODE HERE ### with your own code before you run the following cell.

Note that displaying .split() doesn’t change what is stored in the text variable. Variable reassignment would be necessary if you want to store the result after splitting.

![image](https://github.com/user-attachments/assets/17cc2563-7728-4817-b0c3-c0227f519b4b)

![image](https://github.com/user-attachments/assets/634ad589-582c-459d-9cfd-966117a5f82f)

<h1>Question 1</h1>
What do you notice about the output before and after using the .split() method?

Before using the .split() method, the output is one long string containing all of the lines from the log file. After using the .split() method, the output is a list of strings; each string corresponds to a line from the log file.

<h1>Task 4</h1>
There is a missing entry in the log file. You'll need to account for that by appending it to the log file. You're given the missing entry stored in a variable named missing_entry.

Use the .write() method and the parameter "a" in the open() function. Be sure to replace each ### YOUR CODE HERE ### with your own code before you run the following cell.

After the portion of the code that writes to the file, another with statement uses the .read() method to read the updated file into the text variable and then display it.

![image](https://github.com/user-attachments/assets/0dc74138-172a-4724-90ce-fc1dc009aeb8)

![image](https://github.com/user-attachments/assets/4c41acb5-99c1-461d-8773-5b4b5fccce1d)

<h1>Question 2</h1>
What do you notice about the position of the entry that was added to the log file?

The additional entry was added to the end of the log file, so it appears in the last line of the output.

<h1>Task 5</h1>
The next task you're responsible for is creating a text file. This text file should include a list of IP addresses that are allowed to access restricted information. Documenting this in a text file will help you communicate your findings to your security team.

Start by creating a variable named import_file that stores the name of the file, which should be "allow_list.txt".

You're also given a variable named ip_addresses that stores a string containing the IP addresses that are allowed.

Run the code to display the two variables and explore what they contain. Be sure to replace the ### YOUR CODE HERE ### with your own code before you run the following cell.

![image](https://github.com/user-attachments/assets/7a777cf8-97ed-4d8c-8726-e1e1205e63a5)

![image](https://github.com/user-attachments/assets/e5f46c49-551e-4976-a2a5-060a660d53b4)

<h1>Task 6</h1>
Your next goal is to create a with statement in order to write the IP addresses to the text file you created in the previous step.

You'll first open the file using the "w" parameter. Then, you'll write the IP addresses to the file. Be sure to replace each ### YOUR CODE HERE ### with your own code before you run the following cell. Note that the code cell will contain a with statement that writes to a file but does not display information to the screen, so running it will not produce an output.

![image](https://github.com/user-attachments/assets/e9066740-6cdf-424a-bc46-583d22f816bd)

<h1>Task 7</h1>
In this final step, you'll complete the code you've been writing up to this point. You'll add code to read the file containing IP addresses.

Complete a with statement that reads the text file and stores it in a new variable called text.

Afterwards, display the contents of text and run the cell to explore the result. Be sure to replace each ### YOUR CODE HERE ### with your own code before you run the following cell.

![image](https://github.com/user-attachments/assets/354fcc88-c81c-47e3-a889-8a6c127f20a0)

![image](https://github.com/user-attachments/assets/4ede14e0-9e22-47ec-9c33-1a59f5506ef7)

<h1>Conclusion</h1>
What are your key takeaways from this lab?

- Python has functions and syntax that help you import and parse text files.
- The with statement allows you to efficiently handle files.
- The open() function allows you to import or open a file. It takes in the name of the file as the first parameter and a string that indicates the purpose of opening the file as the second parameter.
- Specify "r" as the second parameter if you're opening the file for reading purposes.
- Specify "a" as the second parameter if you're opening the file for appending purposes.
- Specify "w" as the second parameter if you're opening the file for writing purposes.
- The .read() method allows you to read in a file.
- The .write() method allows you to append or write to a file.
- The .split() method in Python allows you to convert a string to a list.
