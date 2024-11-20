Project: NaturalNumber on String
Objectives
Familiarity with writing a kernel class for a new type and its kernel operations (NaturalNumber layered on String).
Familiarity with developing and using specification-based test plans.
The Problem
The problem is to complete and carefully test implementations of all the constructors and kernel methods defined in interface NaturalNumberKernel, building the data structure representing a NaturalNumber object by layering it on top of java.lang.String.

Note that implementing and testing a kernel component is significantly different and more challenging than implementing and testing layered implementations (as you have been doing up to this point in this course sequence). For kernel implementations, if just one of the methods in the kernel is wrong then other methods might appear not to work correctly during testing. This makes debugging a challenge. One possible reason is that if your test cases use either equals or toString to check the results, these methods can essentially call any of your kernel methods. Another reason is that if your code for any method fails to make the representation invariant true at the time it returns, then the next method called in the test case might break; but the problem is actually with the previous method. Make sure you understand these difficulties so you can deal with them.

Another danger is that you might unconsciously (or even consciously) choose to use a different representation invariant and/or abstraction function than already stated in the Java class. In this case, you may achieve a result for which no test case can reveal a defect. However, if you don't follow the representation invariant and/or the abstraction function provided, you are liable to a significant deduction of points from your project. This warning applies to this project and all subsequent projects in this course. Recommendation: make sure that each public method makes whatever good use it can of assuming that the representation invariant is true when the method begins. Make sure that each public method and each constructor always makes the representation invariant true. Make sure that each public method meets its contract according to the abstraction function.

Setup
Only one member of the team should follow these steps to set up an Eclipse project for this assignment. The project should then be shared with the rest of the team by using the Subversion version control system as learned in the Version Control With Subversion lab.

For this assignment, instead of creating a new project, you will import a project already set-up for you. First you need to download the project, NaturalNumberOnString.zip, to your computer. Click on this download link and save the file somewhere on your hard drive where you can easily find it. Make sure that you do not expand this archive. If your browser automatically expands downloaded zip archives, that's OK too. Just pay attention to the special instructions in the following few steps. You may want to make a note of where you saved it.

Import your new project by following these steps:

From the File menu select Import....
In the new window, expand General and select Existing Projects into Workspace. Click Next.
Click on the radio button next to Select archive file and then click the Browse... button. (If the archive was expanded when you downloaded the file to your own computer, click on Select root directory... instead.)
In the file selection window, find the NaturalNumberOnString.zip file and select it. (If your browser expanded the archive, find the NaturalNumberOnString directory instead.) Click OK.
Click Finish.
Method
Complete the body of the private method createNewRep, of the four constructors, and of the kernel methods (multiplyBy10, divideBy10, and isZero) in NaturalNumber3 in the src folder.
Complete the body of the four constructorTest methods and of the four constructorRef methods in NaturalNumber3Test in the test folder. You can choose any of the available implementations of NaturalNumber as the reference implementation.
Develop a complete and systematic test plan for the NaturalNumberKernel constructors and kernel methods and add your test cases at the end of NaturalNumberTest in the test folder. See the lab where you implemented Queue on Sequence for an example of such a test plan, how it is designed, and how each test case is named and structured. A significant portion of your grade for this project will depend on the quality of your test plan.
When you and your teammate are done with the project, decide who is going to submit your solution. That team member should select the Eclipse project NaturalNumberOnString (not just some of the files, but the whole project) containing the complete group submission, create a zip archive of it, and submit the zip archive to the Carmen dropbox for this project, as described in Submitting a Project. Note that you will only be allowed one submission per group, that is, your group can submit as many times as you want, but only the last submission will be on Carmen and will be graded. Under no circumstance will teammates be allowed to submit separate solutions. Make sure that you and your partner agree on what should be submitted.
Additional Activities
Here are some possible additional activities related to this project. Any extra work is strictly optional, for your own benefit, and will not directly affect your grade.

Consider which of your implementations of the kernel methods (multiplyBy10, divideBy10, and isZero) would have to change if the phrase "with no leading '0'" were removed from the convention. Explain why your implementation is correct when the "with no leading '0'" phrase is present in the convention.
Take a look at the Standard methods (newInstance, clear, and transferFrom) in NaturalNumber3. We will discuss the details of these implementations later in the semester, but for now, design test cases to test these methods and add the test cases to your test fixture, NaturalNumberTest.
