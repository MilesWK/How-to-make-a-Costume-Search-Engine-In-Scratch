# How to create a costume search engine in Scratch

Hello! This little document is going to teach you how to make a Costume Search Engine in Scratch! There is a pre-made .sb3 file in this project so you can see what you are making. Also, check out the more advanced version of this at https://scratch.mit.edu/projects/723200352/. Let's get started!

What you need:  
  - A Scratch account
  - A knowlage of Scratch.

If you have all that... You are ready to go!!! 

**Step 1**: Make a new sprite:

You need to create a new sprite with a variety of random costumes. I would recomennd using the "surprise" button to do this. Do it about 10 times. 

![image](https://user-images.githubusercontent.com/121042782/208458270-4e967888-c69b-4a55-b15e-7800a5a40117.png)

Once you have a fairly long list of totally random costumes, you are ready to move on to the next step.

**Step 2**: Getting all the random costumes into a list:

There are a couple of ways to do this:

One way is to make a new list, and just put a bunch of ![image](https://user-images.githubusercontent.com/121042782/208459108-478739da-7c8b-439d-bd7d-650826cc9b2a.png) to the program.

The other way (the one we are going to use) is to make a program that finds all the costumes and adds them to the list. This allows us to add costumes to the sprite and still have the new costumes in the list... without changing the program.

To start, we are going to make a new My-Block called "Get Costumes" and a list called "Costumes." For the first line in the definition of the My-Block, we are going to delete all the items in the "Costumes" list:

![image](https://user-images.githubusercontent.com/121042782/208460289-e0de1adf-6538-4aca-a7bf-07fe9e2c684c.png).

Next in the definition, add a Forever loop with a "Next costume" block inside:

After the "Next costume" block, we need to create a "if else" statement. This is where it gets tricky. In the condition of the "if" statement, add a ![image](https://user-images.githubusercontent.com/121042782/208530906-0429d088-1b1f-4dfb-945c-f259cacf20c8.png) block. In the "thing" option, add the "Costume[name]" variable. 

Inside the "if" statment, add the "Stop [this script]" block.

Inside the "else" section of the "if" statement, add a "Add "thing" to [list]" boolean. In that block, replace the "thing" with the "Costume[name]" variable. Make sure you set the list you are adding the item to to our "Costumes" list. 

After we finish that, we are done with getting the costumes. 

Here is how our completed My-Block should look: 

![image](https://user-images.githubusercontent.com/121042782/208534522-c586228d-1b6b-4f14-91d3-df16af48d322.png)

To test the My-Block, get a "When flag clicked" block and put our My-Block underneath. 
When we run our program, we should get this output in our list:

![image](https://user-images.githubusercontent.com/121042782/208532697-d77abc26-a287-48ee-8102-eed08cae5861.png)

Your list might have a diferant output due to what costumes you added to your sprite. If you think something is incorrect, you can look at the costumes you added to your sprite and compare them to the output recieved by the list. 

**Step 3:** Making it search:

We need to make a program that recieves input, finds all the information in our "Costumes" list that matches the input, and outputs the information it got. This may sound very hard, but it is acctually fairly easy. 

To start out, we need to create a new variable called "Item number in Costumes." Next, we need to create a list called "Search Results." And finally, we need to create a My-Block called "Run search" with a Text/Number input called "Search."

In the beginning of the definition of our new My-block, we need to delete all of the items in the "Search Results" list with the "Delete all of [Search Results]."

Next, we need to set the "Item number in Costumes" variable to 0 with the "Set [Item number in Costumes] to [1]" block. Now we need to get a "Repeat" loop and set the times the program inside of the "Repeat" loop to the "Length of [Costumes]" variable **FROM THE LIST SECTION.** 

Inside the "Repeat" loop, add a "if else" statement. In the boolean input of the "if else" statement, add a "contains" boolean. In the first text input of the "contains" block, add the "item [] in [costumes]" variable. in the Text input of the "item [] in []" variable, add the "Item number in Costumes" variable we made. In the final input for the "contains" block, add the "Search" variable inside the "Run Search" My-Block. Now our "contains" boolean is complete! Here is how it should look: 

![image](https://user-images.githubusercontent.com/121042782/208540697-74c322c6-a187-474f-972a-ac6fe3eaa7ed.png)

Make sure you put that in the "if else" statement. In the "if" section, add a "Change [Item number in Costumes] by [1]" block, Next we need to add a "Add [string] to [Search results]" Block. In the text input of that block, we need to add a "Item [number] in [Costumes]" input. In the number input, Get a "minus" operator. In the first input, we need to enter our "Item number in Costumes" variable, and in the other input, enter "1." So our "minus" operator says "[Item number in Costumes] - [1]." So our "add [] to [Costumes]" block should look like this:

![image](https://user-images.githubusercontent.com/121042782/208695494-7cea4f4f-901f-4cb0-b0f5-e7cd7daf6bfb.png)

We have finished our "if" part of our "if else" statement! Now we need to get our "else" statement up and running. This part is easy. All we need to do is place a "Change [Item number in Costumes] by [1]" block. And now we have finished our "if else" statement. Here is how the completed statement should look:

![image](https://user-images.githubusercontent.com/121042782/208697089-80f82f3c-e6e0-4fcd-82f4-25176b7e8b4d.png)

Now we need to make the output. Underneath the "Repeat" loop we need another "if else" statement. In the boolean input, we need an "equals" operator. we need it to say "[Length of [Search Results]] = [0]" Again, make sure you get the "Length of [list]" block comes from the "List" section and not the "operators" section. Inside the "if" section, add a "Insert [We couldn't find any results for the search.] at [1] of [Search Results]." Underneath _that_ block, add another "Insert [Press enter to search again.] at [2] of [Search Results]."

In the "else" statement, add a "Insert [We found some results!] at [1] of [Search Results]." Next, add a "Insert [Here they are:] at [2] of [Search Results]." Finally, add a "add [Press enter to search again.] to [Search Results]."

We have finished our search! Here is how the "Run Search" My-Block should look:

![image](https://user-images.githubusercontent.com/121042782/208703214-d85b540b-fe34-43ad-b461-d91b098de8b7.png)

**Step 4: Adding a setup:**

We need to make a brodcast block called "Setup." place a "When I recieve [Setup]" block. Underneath that add a "Show list [Search Results]" block, then under _that_, add a "hide" block, and finally, add a "Hide list [costumes]."

Here is how our brodcast block should look:

![image](https://user-images.githubusercontent.com/121042782/208705399-a59a9a88-86f6-49d8-b274-b699b9bad852.png)

**Step 5: Creating a start:**

We need to create another Brodcast called "Start." Get a "When I recive [Start]" block, and underneath, add a "Delete all of [Search Results]" block. Next, add a "add [Search something with the prompt below!!!] to [Search Results]" block. After that, add our My-Block called "Get Costumes." Next, get a "Forever" loop. Inside the forever loop, add a "Ask [Type here to search!!!] and wait" block. Underneath _that_, add our other My-Block called "Run Search." In the input of the My-Block, add the "Answer" variable from the "Sensing" section. 

Finally, get a "When flag clicked" block. Underneath add a "Brodcast [setup] and wait" block. and finally, add a "brodcast [start]" block!

Here is how all the programs should look:

**The "When Flag Clicked" script:**

![image](https://user-images.githubusercontent.com/121042782/208709321-2bb9cb28-f80a-4d58-8ff0-81a460b00355.png)

**The "Setup" Brodcast:**

![image](https://user-images.githubusercontent.com/121042782/208709437-66e2ac5e-67fd-4145-83d1-ed6ce660d8bf.png)

**The "Start" Brodcast:**

![image](https://user-images.githubusercontent.com/121042782/208731351-18307563-1c3e-4112-9e69-616d93219ad3.png)

**The "Get Costumes" My-Block:**

![image](https://user-images.githubusercontent.com/121042782/208731486-05ed9812-fdd1-49d6-a2d6-a883d670494f.png)

**The "Run Search" My-Block:**

![image](https://user-images.githubusercontent.com/121042782/208731653-c40ea51a-2a33-4e15-a31f-ce0910f9de59.png)

##Notes:

There is a .sb3 file attchched to this repos. It is the program that you make in this repos. 

There are two "Length of []" blocks. One, the one from the "operators" section shows how many LETTERS there are in a list, and the other one is from the "list" section which shows how many items are in a list. Make sure not to confuse these two!

The operator "Length of []:"

![image](https://user-images.githubusercontent.com/121042782/208732271-b48cf56f-0c43-44d1-b57c-fd500d60dd55.png)

The list "Length of []:"

![image](https://user-images.githubusercontent.com/121042782/208732360-d47b41bb-5bf2-4e85-b447-c05a50352156.png)

Thank you for reading this repository! If you use this code in a Scratch project, please give credit to me! Thank you!!!







