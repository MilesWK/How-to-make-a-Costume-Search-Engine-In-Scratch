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

Inside the "else" section of the "if" statement, add a "Add "thing" to [list]" block. In that block, replace the "thing" with the "Costume[name]" variable. Make sure you set the list you are adding the item to to our "Costumes" list. 

After we finish that, we are done with getting the costumes. 

Here is how our completed My-Block should look: 

![image](https://user-images.githubusercontent.com/121042782/208534522-c586228d-1b6b-4f14-91d3-df16af48d322.png)

To test the My-Block, get a "When flag clicked" block and put our My-Block underneath. 
When we run our program, we should get this output in our list:

![image](https://user-images.githubusercontent.com/121042782/208532697-d77abc26-a287-48ee-8102-eed08cae5861.png)

The list might look diferant due to what costumes you added to your sprite. 






       

