Download Link: https://assignmentchef.com/product/solved-lab-exercise-11-problems
<br>
<ol>

 <li>Write C++ programs</li>

 <li>Compile C++ programs</li>

 <li>Implement programs that use object composition.</li>

</ol>

<h1><a id="user-content-additional-reading" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_11#additional-reading" aria-hidden="true"></a>Additional Reading</h1>

This lab exercise requires an understanding of some concepts to solve the problems. You are strongly encouraged to read the following tutorials to help you answer the problems.

<ol>

 <li><a href="https://github.com/ILXL-guides/function-file-organization">Organizing C++ files: function prototypes, implementations, and drivers</a>.</li>

 <li><a href="https://github.com/ILXL-guides/object-parameters-and-return-values">Using objects as parameters and return values in functions</a></li>

 <li><a href="https://github.com/ILXL-guides/arrays-as-parameters">Passing arrays as parameters to functions</a></li>

 <li><a href="https://github.com/ILXL-guides/cpp-file-io">File reading and writing (also includes dealing with arrays)</a></li>

</ol>

<h1><a id="user-content-instructions" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_11#instructions" aria-hidden="true"></a>Instructions</h1>

Answer the programming problems sequentially (i.e., answer prob01 before prob02). If you have questions let your instructor or the lab assistant know. You can also consult your classmates.

When you answer two programming problems correctly, let your instructor know and wait for further instruction.

<h1><a id="user-content-lab-exercise-guide" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_11#lab-exercise-guide" aria-hidden="true"></a>Lab exercise guide</h1>

Here’s a link to the <a href="https://docs.google.com/document/d/1EX01EtrO-pkHNLVPxiq7HNh1f5KnJZnr_dlJcO4T7t0/edit?usp=sharing" rel="nofollow">Lab exercise guide</a> in case you need to review the lab exercise objectives, grading scheme, or evaluation process.

PetsBreed ClassCreate a Breed class with the following:

Data membersCreate the following data members: std::string species_, name_, and color_.

Default ConstructorCreate a default constructor for Breed that sets its species_ to “Dog”, name_ to “Pug”, and color_ to “Fawn”.

Non-Default ConstructorCreate a non-default constructor that receives an std::string for species_, name_, and color_; in that order. The values from the constructor should appropriately assign the data members.

Accessors and MutatorsCreate accessors and mutators for all data members.

Pet ClassCreate a Pet class with the following:

Data membersCreate private member variables std::string name_, Breed breed_ , and double weight_.

Default ConstructorCreate a default constructor for Pet that sets its name to “Doug” and weight to 15.6. The Breed object will automatically be created using its default constructor.

Non-Default ConstructorsCreate a non-default constructor that receives an std::string for name_, Breed for breed_, and a double for weight_ in that order. The values from the constructor should appropriately assign the data members.

Create another non-defaault constructor that receives an std::string for name_, std::string species_, name_, and color_ for the Breed constructor, and double for weight_. The values from the constructor should appropriately assign the data members.

Accessors and MutatorsCreate accessors and mutators for name_, breed_, and weight_.

set_breed overloadCreate a method overload for set_breed that accepts an std::string species_, name_, and color_ that will internally create a Breed object using the values provided and then assign it to the breed_ data member.

printCreate a member function called print that returns void and does not take in any parameters. Using the data members, this function should print out the name and weight of the Pet. It should also utilize accessors of the Breed class to get the species, breed name, and color.

Other instructionsComplete the main function as described. Place your classes in pet.hpp. Member functions that take more than five lines or use complex constructs should have their function prototype in pet.hpp and implementation in pet.cpp.

Sample Output:Please enter the pet’s name (q to quit): AirBudPlease enter the pet’s type: DogPlease enter the pet’s breed: Golden RetrieverPlease enter the pet’s color: BlondePlease enter the pet’s weight (lbs): 44.5Please enter the pet’s name (q to quit): CookiePlease enter the pet’s type: DogPlease enter the pet’s breed: English BulldogPlease enter the pet’s color: Brown &amp; WhitePlease enter the pet’s weight (lbs): 31.2Please enter the pet’s name (q to quit): qPrinting Pets:Pet 1Name: AirBudSpecies: DogBreed: Golden RetrieverColor: BlondeWeight: 44.5 lbsPet 2Name: CookieSpecies: DogBreed: English BulldogColor: Brown &amp; WhiteWeight: 31.2 lbsSubmission checklistCreated function prototype and stored in .hpp file.Created function implementation and stored in .cpp file (see reference).Call function in the driverCompiled and ran the driver (main).Manually checked for compilation and logical errors.Ensured no errors on the unit test (make test).Followed advice from the stylechecker (make stylecheck).Followed advice from the formatchecker to improve code readbility (make formatcheck).Code evaluationOpen the terminal and navigate to the folder that contains this exercise. Assuming you have pulled the code inside of /home/student/labex02-tuffy and you are currently in /home/student you can issue the following commands

cd labex02-tuffyYou also need to navigate into the problem you want to answer. To access the files needed to answer problem 1, for example, you need to issue the following command.

cd prob01When you want to answer another problem, you need to go back up to the parent folder and navigate into the next problem. Assuming you are currently in prob01, you can issue the following commands to go to the parent folder then go into another problem you want to answer; prob02 for example.

cd ..cd prob02Use the clang++ command to compile your code and the ./ command to run it. The sample code below shows how you would compile code saved in pet.cpp and main.cpp, and into the executable file main. Make sure you use the correct filenames required in this problem. Take note that if you make any changes to your code, you will need to compile it first before you see changes when running it.

clang++ -std=c++17 main.cpp pet.cpp -o main./mainYou can run one, two, or all the commands below to test your code, stylecheck your code’s design, or formatcheck your work. Kindly make sure that you have compiled and executed your code before issuing any of the commands below to avoid errors.

make testmake stylecheckmake formatcheckA faster way of running all these tests uses the all parameter.

make all




<h1>Candy Shop</h1>

Create a class called <code>CandyShop</code> that will have the following:

<h3><a id="user-content-data-members" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_11/prob02#data-members" aria-hidden="true"></a>Data members</h3>

<code>CandyShop</code> should have two private data members, a <code>Candy</code> array of size <code>10</code> and an <code>int</code> to keep count of the number of elements in the array, called <code>size_</code>.

<em>NOTE</em>: The code for the object <code>Candy</code> will be provided to you.

<h3><a id="user-content-default-constructor" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_11/prob02#default-constructor" aria-hidden="true"></a>Default Constructor</h3>

Create a default constructor that sets <code>size_</code> to <code>0</code>.

<h3><a id="user-content-accessor" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_11/prob02#accessor" aria-hidden="true"></a>Accessor</h3>

Create an accessor for <code>size_</code>.

<h3><a id="user-content-add" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_11/prob02#add" aria-hidden="true"></a>add</h3>

Create a member function called <code>add</code> that passes in a <code>Candy</code> object. This member function should add the <code>Candy</code> object into the array as long as the size is less than <code>10</code>. Otherwise, it should print this error message: <code>Error, bag is full!</code>.

<h3><a id="user-content-print" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_11/prob02#print" aria-hidden="true"></a>print</h3>

Create a member function called <code>print</code> that displays the contents of the bag. Specifically, it shows the brand, flavor, and cost of every <code>Candy</code> object. Look at the output below for reference.

<h3><a id="user-content-total_price" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_11/prob02#total_price" aria-hidden="true"></a>total_price</h3>

Create a member function called <code>total_price</code> that will return a <code>double</code> for the total cost of all the candy in the bag. Take note that the member function does not display anything on screen. The value is printed in the <code>main</code> function.

<h3><a id="user-content-main" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_11/prob02#main" aria-hidden="true"></a>main</h3>

Complete the main function that should ask the user to enter in the brand, flavor, and cost of the candy, then use <code>Candy</code> and <code>CandyShop</code> objects to store and display the data as shown in the sample output below.

<h2><a id="user-content-other-instructions" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_11/prob02#other-instructions" aria-hidden="true"></a>Other instructions</h2>

Complete the <code>main</code> function as described. Place your classes in <code>candy_shop.hpp</code>. Member functions that take more than five lines or use complex constructs should have their function prototype in <code>candy_shop.hpp</code> and implementation in <code>candy_shop.cpp</code>.

<h2><a id="user-content-sample-output" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_11/prob02#sample-output" aria-hidden="true"></a>Sample output</h2>

<pre>Welcome to the Candy Shop!Enter the brand of candy (q to quit): <b>Skittles</b>Enter the flavor of candy: <b>Fruity</b>Enter the cost of candy: <b>4.25</b>Enter the brand of candy (q to quit): <b>Snickers</b>Enter the flavor of candy: <b>Chocolate</b>Enter the cost of candy: <b>5.13</b>Enter the brand of candy (q to quit): <b>Sour Patch Kids</b>Enter the flavor of candy: <b>Sour-Fruity</b>Enter the cost of candy: <b>10.12</b>Enter the brand of candy (q to quit): <b>q</b>Contents of bag:Candy 1  Brand: Skittles  Flavor: Fruity  Cost: $4.25Candy 2  Brand: Snickers  Flavor: Chocolate  Cost: $5.13Candy 3  Brand: Sour Patch Kids  Flavor: Sour-Fruity  Cost: $10.12The total cost of all the candy in the bag is: $19.50</pre>

<h1><a id="user-content-submission-checklist" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_11/prob02#submission-checklist" aria-hidden="true"></a>Submission checklist</h1>

<ol>

 <li>Created function prototype and stored in <code>.hpp</code> file.</li>

 <li>Created function implementation and stored in <code>.cpp</code> file (see <a href="https://github.com/ILXL-guides/function-file-organization">reference</a>).</li>

 <li>Call function in the driver</li>

 <li>Compiled and ran the driver (<code>main</code>).</li>

 <li>Manually checked for compilation and logical errors.</li>

 <li>Ensured no errors on the unit test (<code>make test</code>).</li>

 <li>Followed advice from the stylechecker (<code>make stylecheck</code>).</li>

 <li>Followed advice from the formatchecker to improve code readbility (<code>make formatcheck</code>).</li>

</ol>

<h1><a id="user-content-code-evaluation" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_11/prob02#code-evaluation" aria-hidden="true"></a>Code evaluation</h1>

Open the terminal and navigate to the folder that contains this exercise. Assuming you have pulled the code inside of <code>/home/student/labex02-tuffy</code> and you are currently in <code>/home/student</code> you can issue the following commands

<pre><code>cd labex02-tuffy</code></pre>

You also need to navigate into the problem you want to answer. To access the files needed to answer problem 1, for example, you need to issue the following command.

<pre><code>cd prob01</code></pre>

When you want to answer another problem, you need to go back up to the parent folder and navigate into the next problem. Assuming you are currently in <code>prob01</code>, you can issue the following commands to go to the parent folder then go into another problem you want to answer; <code>prob02</code> for example.

<pre><code>cd ..cd prob02</code></pre>

Use the <code>clang++</code> command to compile your code and the <code>./</code> command to run it. The sample code below shows how you would compile code saved in <code>candy_shop.cpp</code> and <code>main.cpp</code>, and into the executable file <code>main</code>. Make sure you use the correct filenames required in this problem. Take note that if you make any changes to your code, you will need to compile it first before you see changes when running it.

<pre><code>clang++ -std=c++17 main.cpp candy_shop.cpp -o main./main</code></pre>

You can run one, two, or all the commands below to <code>test</code> your code, <code>stylecheck</code> your code’s design, or <code>formatcheck</code> your work. Kindly make sure that you have compiled and executed your code before issuing any of the commands below to avoid errors.

<pre><code>make testmake stylecheckmake formatcheck</code></pre>

A faster way of running all these tests uses the <code>all</code> parameter.

<h6><code>make all</code></h6>

<h1>Car Class Composition</h1>

Create a class called <code>Car</code> that will utilize other objects.

<h2><a id="user-content-car" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_11/prob03#car" aria-hidden="true"></a>Car</h2>

<h3><a id="user-content-car-data-members" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_11/prob03#car-data-members" aria-hidden="true"></a>Car data members</h3>

Create two data members that are: (1) an instance of the <code>Identifier</code> class called <code>identity_</code> and (2) an instance of the <code>Date</code> class called <code>release_date_</code>.

<em>NOTE</em>: <code>Identifier</code> and <code>Date</code> are classes that will be provided to you. You <strong>DO NOT</strong> need to create them.

<h3><a id="user-content-default-constructor" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_11/prob03#default-constructor" aria-hidden="true"></a>Default Constructor</h3>

The default constructor will be <strong>EMPTY</strong>, so you do not have to initialize anything. <code>Identifier</code> and <code>Date</code>‘s respective constructors will initialize their default values.

<h3><a id="user-content-non-default-constructors" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_11/prob03#non-default-constructors" aria-hidden="true"></a>Non-Default Constructors</h3>

<ol>

 <li>Create a non-default constructor that takes in an <code>Identifier</code> object. This will assign the parameter to the <code>identity_</code> data member.</li>

 <li>Create a non-default constructor that takes in a <code>Date</code> object. This will assign the parameter to the <code>release_date_</code> data member.</li>

 <li>Create a non-default constructor that takes in an <code>Identifier</code> and a <code>Date</code> object (in this order). This will assign the parameters to the <code>identity_</code> and <code>release_date_</code> parameters correspondingly.</li>

</ol>

<h3><a id="user-content-accessors-and-mutators" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_11/prob03#accessors-and-mutators" aria-hidden="true"></a>Accessors and Mutators</h3>

Create accessors and mutators for <code>identity_</code> and <code>release_date_</code>.

<h3><a id="user-content-other-member-functions" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_11/prob03#other-member-functions" aria-hidden="true"></a>Other Member Functions</h3>

Create a <code>void</code> member function called <code>print</code> that takes in no parameters. <code>print</code> should print the name, id, license plate, and release date of the car. The release data should follow the format <strong>Month/Day/Year</strong>. See the output below for your reference.

<h2><a id="user-content-other-instructions" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_11/prob03#other-instructions" aria-hidden="true"></a>Other instructions</h2>

Complete the <code>main</code> function as described. Place your classes in <code>car_comp.hpp</code>. Member functions that take more than five lines or use complex constructs should have their function prototype in <code>car_comp.hpp</code> and implementation in <code>car_comp.cpp</code>.

Your program does not need to account for the correct dates or license plates. For example: 13/41/1 will be acceptable for your program, even though it is not an acceptable date. “1111111111111111” will be acceptable in your program, even though it is not a valid license plate number.

<h2><a id="user-content-sample-output" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_11/prob03#sample-output" aria-hidden="true"></a>Sample output</h2>

<pre><code>The name of the car is: FordThe id of the car is: 1The license plate of the car is: 123456The release date of the car is: 1/1/1885The name of the car is: HondaThe id of the car is: 3The license plate of the car is: 7B319X4The release date of the car is: 1/1/1885The name of the car is: FordThe id of the car is: 1The license plate of the car is: 123456The release date of the car is: 11/4/2018The name of the car is: HondaThe id of the car is: 3The license plate of the car is: 7B319X4The release date of the car is: 11/4/2018The name of the car is: FordThe id of the car is: 1The license plate of the car is: 123456The release date of the car is: 1/1/1885</code></pre>

<h1><a id="user-content-submission-checklist" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_11/prob03#submission-checklist" aria-hidden="true"></a>Submission checklist</h1>

<ol>

 <li>Created function prototype and stored in <code>.hpp</code> file.</li>

 <li>Created function implementation and stored in <code>.cpp</code> file (see <a href="https://github.com/ILXL-guides/function-file-organization">reference</a>).</li>

 <li>Call function in the driver</li>

 <li>Compiled and ran the driver (<code>main</code>).</li>

 <li>Manually checked for compilation and logical errors.</li>

 <li>Ensured no errors on the unit test (<code>make test</code>).</li>

 <li>Followed advice from the stylechecker (<code>make stylecheck</code>).</li>

 <li>Followed advice from the formatchecker to improve code readbility (<code>make formatcheck</code>).</li>

</ol>

<h1><a id="user-content-code-evaluation" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_11/prob03#code-evaluation" aria-hidden="true"></a>Code evaluation</h1>

Open the terminal and navigate to the folder that contains this exercise. Assuming you have pulled the code inside of <code>/home/student/labex02-tuffy</code> and you are currently in <code>/home/student</code> you can issue the following commands

<pre><code>cd labex02-tuffy</code></pre>

You also need to navigate into the problem you want to answer. To access the files needed to answer problem 1, for example, you need to issue the following command.

<pre><code>cd prob01</code></pre>

When you want to answer another problem, you need to go back up to the parent folder and navigate into the next problem. Assuming you are currently in <code>prob01</code>, you can issue the following commands to go to the parent folder then go into another problem you want to answer; <code>prob02</code> for example.

<pre><code>cd ..cd prob02</code></pre>

Use the <code>clang++</code> command to compile your code and the <code>./</code> command to run it. The sample code below shows how you would compile code saved in <code>car_comp.cpp</code> and <code>main.cpp</code>, and into the executable file <code>main</code>. Make sure you use the correct filenames required in this problem. Take note that if you make any changes to your code, you will need to compile it first before you see changes when running it.

<pre><code>clang++ -std=c++17 main.cpp car_comp.cpp -o main./main</code></pre>

You can run one, two, or all the commands below to <code>test</code> your code, <code>stylecheck</code> your code’s design, or <code>formatcheck</code> your work. Kindly make sure that you have compiled and executed your code before issuing any of the commands below to avoid errors.

<pre><code>make testmake stylecheckmake formatcheck</code></pre>

A faster way of running all these tests uses the <code>all</code> parameter.

<pre><code>make all</code></pre>