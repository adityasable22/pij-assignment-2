

Command line arguments: The main method takes an array of strings as input, which represents the command line arguments passed to the program. The args array can be used to access these arguments within the program. function: public static void main(String[] args) { // Code to access command line arguments }

Scanner : The Scanner class is used to get input from the user. The System.in object is used as the input stream for the Scanner object. You can use various next methods of the Scanner class to get different types of input from the user. function: import java.util.Scanner; Scanner sc = new Scanner(System.in);

BufferedReader: The BufferedReader class is used to read characters from the input stream. The System.in object is wrapped in an InputStreamReader object, which is then used to create a BufferedReader object. You can use the readLine method of the BufferedReader class to get a line of input from the user as a string. function : import java.io.BufferedReader; import java.io.InputStreamReader; BufferedReader br = new BufferedReader(new InputStreamReader(System.in));

DataInputStream: The DataInputStream class is used to read primitive data types from the input stream. The System.in object is used to create a DataInputStream object, which can be used to read input from the user in a variety of formats. function: import java.io.DataInputStream; import java.io.InputStream;

DataInputStream dis = new DataInputStream(System.in); The Console class provides methods for reading characters, lines, and password-based input from the console. The System.console method is used to get the console object, which can then be used to get input from the user. function: import java.io.Console; Console console = System.console();
