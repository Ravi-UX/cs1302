# ce06 Interfaces (ADTs)

![Approved for: Fall 2020](https://img.shields.io/badge/Approved%20for-Fall%202020-blueviolet)

This class exercise is designed to get you acquainted with Interfaces in Java.
When a seasoned programmer or potential employer asks you if you know 
Object-Oriented Programming (OOP), they do not mean, "do you know classes and objects?" 
That's basic enough that it's assumed! Instead, they mean, "do you know the pillars of OOP?"
The pillars of OOP are interfaces, inheritance, and polymorphism. In this exercise, we continue 
the exploration of interfaces and interface-based polymorphism that you started with the 
posted readings/videos. 

## Prerequisite Knowledge

* A basic understanding of creating and implementing interfaces in Java.
* [CSCI 1302 Interfaces Tutorial](https://github.com/cs1302uga/cs1302-tutorials/blob/master/interfaces/interfaces.md)

## Course-Specific Learning Outcomes

* **LO2.e:** (Partial) Utilize existing generic methods, interfaces, and classes in a software solution.
* **LO3.b:** Create class, interface, method, and inline documentation that satisfies a 
set of requirements.
* **LO3.c:** Generate user-facing API documentation for a software solution.
* **L04.b:** Utilize interface-based polymorphism in a software solution.

## Questions

In your notes, clearly answer the following questions. These instructions assume that you are 
logged into the Odin server. 

**NOTE:** If a step requires you to enter in a command, please provide in your notes the full 
command that you typed to make the related action happen. If context is necessary (e.g., the 
command depends on your present working directory), then please note that context as well.

## Exercise Steps

### Checkpoint 1 Steps - Getting Started

1. Use Git to clone the repository for this exercise onto Odin into a subdirectory called `cs1302-ce06`:

   ```
   $ git clone https://github.com/cs1302uga/cs1302-ce06.git
   ```

1. Change into the `cs1302-ce06` directory that was just created and look around. There should be
   multiple Java files contained within the directory structure. To see a listing of all of the 
   files under the `src` subdirectory, use the `find` command as follows:
   
   ```
   $ find src
   ```
   
   For each Java file under the `src` subdirectory, fill out a row in a table similar to the 
   following in your notes:

   **Note:** If a class is not an interface and does not implement an interface, write `NA` in the second
   column. Also, the "Depends On" column should list any Java types in the `cs1302.ce06` package that the file
   is dependent upon. 

   | Name of the Java file | Interface or Implementing Class? | Fully Qualified Name (FQN) | Depends On |
   |-----------------------|----------------------------------|----------------------------|------------|
   |-----------------------|----------------------------------|----------------------------|------------|
   |-----------------------|----------------------------------|----------------------------|------------|
   |-----------------------|----------------------------------|----------------------------|------------|

1. List the abstract methods found in the `Driveable` interface.

1. Generate the API documentation website for all of the code in the `cs1302` package. 
   Host the documentation on Odin using `cs1302-ce06-doc` as the name for your symbolic link.
   What is the URL to your hosted website?
   
1. Look at the `speedUp` method in the `Car.java` file. Compare the Javadoc comment for the
   method in that file to the documentation listed for that method in the API documentation
   website. What do you notice? How is this possible?

<hr/>

![CP](https://img.shields.io/badge/Just%20Finished%20Checkpoint-1-success?style=for-the-badge)

<hr/>

### Checkpoint 2 Steps

1. Make sure that you are still in the `cs1302-ce06` directory. Compile `Drivable.java` and place the compiled
   code under the preexisting `bin` directory. To see a listing of all of the files under the `bin` subdirectory, 
   use the `find` command as follows:
   
   ```
   $ find bin
   ```
   
   Notice that interfaces are compiled the same way as classes. In your notes, write down the path for the
   `Drivable.class` file that the compiler generated based on the output of `find`.
   
1. Compile `Car.java`. Remember to set the classpath appropriately so `javac` can locate dependencies. 

   *Uh-oh*. (╯°□°）╯︵ ┻━┻ 

   * What compile-time error was generated? Note: the expected error is not "package does not exist" or 
   "cannot find symbol". If you received one of these errors, check your compilation line.
   * **Tricky** Why did you receive this error? Hint: check spelling and capitalization.
   
   Modify `Car.java` to fix the error and recompile. ┬─┬ノ( º _ ºノ)
   
1. Compile and execute `Driver.java`. It should run properly once `Car.java` is compiled. For now, we only
   have a single class (`Car.java`) that implements `Drivable`. Notice that the `test` method in `Driver.java`
   takes an argument of type `Car`. For now this is okay--just observe what is going on.
   
1. Think of two different types of things in real life that are capable of being driven. If you're working in a
   group, have each group member come up with two. In your notes, include the items from your list as well as your 
   favorite among the ones generated by your group. Pick one of the choices and note it as best--play nice.

1. Add a class to the `cs1302.ce06.impl` package that represents your best drivable type. That type should
   be something that is capable of being driven (speeding up and slowing down) and therefore a perfect 
   candidate for a class that implements the actions in the `Drivable` interface. Make sure that your 
   class properly implements the interface. Also make sure that your class compiles. Here is a small 
   list of things you should do:
   
   1. Properly implement the interface. 
   1. Add appropriate Javadoc comments and update your API documentation website. 
   1. Compile your class.
   1. Run your program through `checkstyle` to make sure it follows the style guidelines.
   
   What is the command that you used to compile your class? 
   
1. Update `Driver.java` to test your new class. Modify the existing `test` method (don't overload the method 
   by creating a separate method with the same name) so it can be used to 
   test `Car` objects and objects of the new type that you just created (what do `Car` objects and objects
   of your new type have in common?). You should not change the name of the method, its return type, or the 
   number of parameters. However, you may modify other parts of the method signature as well as the method's 
   body, as needed. Be sure to update the Javadoc comments in the `Driver` class where necessary. 
   In your notes, summarize the changes you made.
   
1. Regenerate the API documentation website for all of the code in the `cs1302` package using
   the Javadoc tool. You should not need to recreate the symbolic link, assuming it still exists from
   a prior step. Show the instructor or PLA the Javadoc webpage for the new class you created
   and documented _as well as_ the driver class.

<hr/>

![CP](https://img.shields.io/badge/Just%20Finished%20Checkpoint-2-success?style=for-the-badge)

<hr/>

### Checkpoint 3 Steps

1. Add an abstract method `stop` to the `Drivable` interface, including appropriate Javadoc comments
   for _what_ the method should do. Recompile the interface _as well_ as any code that depends on 
   the interface.  Did any compilation problems occur?  If so, where and why?

1. Without further modifying the code in the interface, fix the errors observed in the previous step. 
   If you find yourself writing additional methods in any of the other Java source code files, then 
   be sure to include appropriate Javadoc comments. For each affected file, list the commands you used 
   to verify that you fixed the errors. Repeat this step, as needed, until the code compiles.

1. Regenerate the API documentation website for all of the code in the `cs1302` package. Since you
   added a method to the interface in a previous step, you will likely want to share that information
   with other developers. What is the direct URL to the API documentation for the `stop` method you
   wrote, so that you can share it with ~~friends and family~~ other developers?

1. Run the 1302 `checkstyle` program on all `.java` files. If errors are reported, look up each error 
   message in the [Style Guide](https://github.com/cs1302uga/cs1302-styleguide), fix the error, and 
   repeat until no style errors remain.
   
1. Take a minute to notice your `stop` method in the various places that it appears in the API 
   documentation website that you regenerated in the previous step.

1. Do not type the following command:

   ```
   $ nc towel.blinkenlights.nl 23
   ```
   
   The `nc` command provided above is not related to the exercise. 
   If you type it in, then you may end up wasting time.
   The command connects you to a highly addictive form of entertainment provided Sten S. Stans, 
   an elite Dutch Unix engineer.
   
<hr/>

![CP](https://img.shields.io/badge/Just%20Finished%20Checkpoint-3-success?style=for-the-badge)

<hr/>


### Submission Steps

**Each student needs to individually submit their own work.**

1. Create a plain text file called `SUBMISSION.md` directly inside the `cs1302-ce06`
   directory with the following information.

   1. Your name and UGA ID number;
   1. Collaborator names, if any; and
   1. The full link to the website generated in this exercise.
   
   Here is an example of the contents of `SUBMISSION.md`.
   
   ```
   1. Sally Smith (811-000-999)
   2. Collaborators: Joe Allen, Stacie Mack
   3. https://webwork.cs.uga.edu/~user/cs1302-ce06-doc
   ```

1. Change directories to the parent of `cs1302-ce06` (e.g., `cd ..` from `cs1302-ce06`). If you would like
   to make a backup tar file, the instructions are in the submissions steps for [ce02](https://github.com/cs1302uga/cs1302-ce02).
   We won't repeat those steps here and you can view them as optional.
   
1. Use the `submit` command to submit this exercise to `csci-1302`:
   
   ```
   $ submit cs1302-ce06 csci-1302
   ```
   
   Read the output of the submit command very carefully. If there is an error while submitting, then it will displayed 
   in that output. Additionally, if successful, the submit command creates a new receipt file in the directory you 
   submitted. The receipt file begins with rec and contains a detailed list of all files that were successfully submitted. 
   Look through the contents of the rec file and always remember to keep that file in case there is an issue with your submission.

   **Note:** You must be on Odin to submit.

<hr/>

![CP](https://img.shields.io/badge/Just%20Finished-Submission-success?style=for-the-badge)

<hr/>

[![License: CC BY-NC-ND 4.0](https://img.shields.io/badge/License-CC%20BY--NC--ND%204.0-lightgrey.svg)](http://creativecommons.org/licenses/by-nc-nd/4.0/)

<small>
Copyright &copy; Michael E. Cotterell, Brad Barnes, and the University of Georgia.
This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-nd/4.0/">Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International License</a> to students and the public.
The content and opinions expressed on this Web page do not necessarily reflect the views of nor are they endorsed by the University of Georgia or the University System of Georgia.
</small>
