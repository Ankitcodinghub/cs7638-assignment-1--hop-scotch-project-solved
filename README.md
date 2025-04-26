# cs7638-assignment-1--hop-scotch-project-solved
**TO GET THIS SOLUTION VISIT:** [CS7638 Assignment 1- Hop Scotch Project Solved](https://www.ankitcodinghub.com/product/cs7638-robotics-ai-techniques-hop-scotch-project-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;123237&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS7638 Assignment 1- Hop Scotch Project Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
<h1>Table of Contents</h1>
<ul>
<li>Introduction</li>
</ul>
<strong>– </strong>Submitting Your Assignment

<ul>
<li>Project Description <strong>– </strong>World</li>
<li>Estimation Part A</li>
<li>Jumps Part B</li>
<li>Running Tests</li>
<li>Generating New Test Cases</li>
<li>Grades</li>
<li>Academic Integrity</li>
<li>Questions</li>
</ul>
<h1>Introduction</h1>
While travelling through the milky way galaxy searching for earth, your spaceship has an engine malfunction rendering the spaceship engine mostly inoperable, only able to navigate via jumps. Luckily, a shower of asteroids dot the vast cosmic landscape, and can serve as galactic ferries for our spaceship. It is your task to receive sensor readings of the locations of these asteroids, predict where each of the asteroids will be one timestep later, and finally, jump/“hop scotch” from asteroid to asteroid to reach homebase, earth.

This project consists of two parts:

<ol>
<li>Estimation: Estimate where asteroids will be one timestep into the future 2. Jumps: Select asteroids to ‘ride’ on with the ultimate goal of reaching homebase.</li>
</ol>
<strong>Submitting Your Assignment</strong>

Your submission will consist of ONLY the spaceship.py file, which you will upload to Gradescope.

<h1>Project Description</h1>
The motion model of the asteroids takes the form

<em>x</em>(<em>t</em>) = <em>c</em><em>pos</em><em>x </em>+ <em>c</em><em>vel</em><em>xt </em>+ <em>c</em><em>acct</em>2

for the asteroid’s x-position, and

<em>y</em>(<em>t</em>) = <em>c</em><em>pos</em><em>y </em>+ <em>c</em><em>vel</em><em>yt </em>+ <em>c</em><em>acct</em>2

for its y-position.

Each timestep is <em>dt </em>= 1 seconds in duration. Each asteroid’s motion can be modeled using x, y, dx, dy, ax, ay. where ‘a’ is acceleration. C_pos, C_vel, and C_acc are respectively, the position, velocity and the acceleration term for the asteroid.

<strong>World:</strong>

In this project, your world is a rectangle of variable width x height dimension (e.g. 2×2, 4×2 etc.). (0,0) is the lower left corner. This coordinate system is used throughout this project to define all entity locations. Homebase/“Earth” is considered the upper value of the y coordinate (i.e. upper field boundary). It has been colored green. You will want to guide your spaceship here.

<h1>Part A: Estimation</h1>
<strong>Goal:</strong>

To provide “estimates” of an asteroid’s coordinates (x &amp; y) which fall within an expected margin of the asteroids true position.

In this part of the project, you are predicting the location of asteroids one timestep into the future given the asteroids’ current true positions. The (x,y) position measurements provided in test cases 1 and 2 and 16 will have no noise (i.e. the measurement information (asteroid_observations) provided to the predict_from_observations function is NOT noisy.), the remaining test cases will be noisy measurement positions. Once an asteroid leaves the field, it is removed from the tracked asteroids and is no longer passed in as input.

<strong>Scoring:&nbsp; </strong>Your estimates will be considered a ‘match’ if they fall within an expected margin of the asteroids true position. Those matches are used in calculating 3 scoring criteria. Each asteroid ID estimate returned from predict_from_observations function is scored on 3 primary criteria:

<ul>
<li>– The number of timesteps it took for an asteroid’s estimate to 1st match (i.e. How quickly were you able to get a match).</li>
<li>– The Max number of consecutive matches of an asteroid over its time within the field boundary (i.e. How consistently were you able to match).</li>
<li>– The percentage of matches over the asteroid’s time within the field boundary (i.e. How accurately were you able to match) Scores for a test case are the summed total of all scoring criteria from all asteroids.</li>
</ul>
<strong>Visualization:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </strong>When you run a case with the turtle visualization option, you should see something like what is shown in the image above. The gray circles represent the actual locations of asteroids. A red dot indicates a prediction that is too far from the asteroid’s actual location to count as correct, and a green dot indicates an estimate close enough to be counted as correct.

Figure 1: Estimation visualization

<strong>Notes on testing your Estimation Code </strong>Test cases 1 and 2 are meant to help you verify that your implementation works correctly in simple scenarios before applying it to more complex scenarios. Passing this part of the project does not guarantee that your implementation is correct, but cases 1 and 2 are small enough test cases that you can work through a timestep or two for one or more asteroids by hand while stepping through your code with a debugger to verify that your implementation is consistent with your hand calculations.

<h1>Part B: Jumps</h1>
<strong>Goal:</strong>

The True location of the spaceship/agent is currently represented as the blue Rocket, and the blue dot at its center represents the asteroid it is currently riding. The large blue circle surrounding the spaceship represents the jump range/distance the agent can hop. Locations outside this range (i.e. &gt;) are too far to jump and will result in invalid jumps! Get the spaceship blue dot to homebase. For part B of the project, you will be devising a simple algorithm to select which asteroid to navigate to. Part B of the project makes use of the predictions of the asteroid locations computed by predict_from_observations in the Estimation Part A portion of the project. When part B code is run you will see an image similar to this.

Figure 2: Estimation visualization

Once the spaceship jumps on an asteroid, its state parameters (position etc.) are updated to the true state parameters of the ridden asteroid (Note:True NOT noisy values). Note that while the agent is located at an asteroid’s true location, you do NOT have access to “TRUE” values of that location and only have noisy measurements to rely on. You are thus advised to work on part A before moving on to part B.

<h2>Causes for failing test case</h2>
<ul>
<li>Attempting to jump ‘onto’ an asteroid that is outside the spaceship’s jump radius is considered invalid.</li>
<li>Attempting to jump ‘onto’ an asteroid that is outside the field boundaries is considered invalid.</li>
<li>Attempting to jump ‘from’ the spaceship which is outside the field boundaries is considered invalid.</li>
</ul>
Once an asteroid moves outside the field boundary, the id number is removed from the provided argument ids. Note: To successfully complete Part B of this project, you will likely need to employ creative solutions as you select how best to traverse through the cosmic field.

<h2>Visual progression for a single case</h2>
Visual progression Images Read from Left to Right, Top to bottom.

<ol>
<li>The spaceship is initialized at the bottom of the field randomly between the black field markers.</li>
<li>The spaceship hops onto asteroid 28.</li>
<li>The spaceship rides along with asteroid 28.</li>
<li>The spaceship hops onto the asteroid 21.</li>
<li>The spaceship rides along with asteroid 21.</li>
<li>The spaceship hops onto the asteroid 80..</li>
<li>The spaceship reaches homebase. Success!</li>
</ol>
<strong>Visual Debugging:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </strong>A “DEBUG_DISPLAY” variable/flag has been provided in settings.py. Set it to True to show the asteroid IDs and the (x, y) coordinates of the corners of the world in the GUI.

A “DISPLAY_MATCH_RANGE” variable/flag is also provided in settings.py. Set it to True to visualize the range within/outside of which an estimate will not be considered a match. These are shown in the images above as small circles surrounding each asteroid.

A “DISPLAY_ESTIMATED_SPACESHIP_MATCH_RANGE” variable/flag is also provided in settings.py. Set it to True to visualize the range within/outside of the estimated position of the agent (your estimate of where you believe the agent to be). If this flag is activated, The estimated range of the agent is shown as a large green circle (see image below).

A “DARK_MODE” toggle button is available to view the visualization in dark mode. Default mode is currently set to Dark.

<h2>Spaceship True position vs Spaceship Estimated position</h2>
As previously noted the “TRUE” position of the spaceship is visualized as the <strong>blue </strong>dot with the blue circle range. However the spaceship’s “ESTIMATED” position is represented by red dot surrounded by the large <strong>red circle </strong>(Estimates are values you return in part A). To visualize the estimated positions, you will need to return appropriate values from the function (this is optional. See the function docstring for details). When the spaceship’s true location matches its estimated location, the estimated range is colored green.

Figure 3: Hopping visualization

<h2>Running Tests</h2>
To test your code on an estimation case and see a visualization of the simulation, run the following with the necessary case. Cases arguments may be 1 – 15. python test.py –case 1 –display turtle

To test your code on an estimation case with no visualization, run the following.

python test.py –case 16 –display text

To test your code on a part B case and see a visualization of the simulation, run the following with the necessary case. Case argument may be 16-30):

python test.py –case 16 –display turtle –method jump To run your code on a part B case no visualization, run the following. python test.py –case 16 –display turtle –method jump

To test all local estimate and jump cases with no visualization run python test.py

This is the testing mode used by Gradescope.

<h1>Generating New Test Cases</h1>
The cases used for grading on Gradescope are similar to those provided to you, but not the same. You can use generate_test_case.py to generate additional test cases to more rigorously test your code, To see all of the command line arguments for the generate_test_case.py script, run the following in your Python environment:

python generate_test_case.py –help To create a new case, run as follows:

python generate_test_case.py –case my_case# [additional arguments here] e.g.

python generate_test_case.py –case 36 –asteroid_match_range 0.09 –num_asteroids_per_time 10

To use this new test case, pass the filename to test.py using the –case argument:

python test.py –case 36 –display turtle estimate

<em>Note</em>: The new case files are not included in the cases executed by test.py.

<h1>Scoring</h1>
Grades are assigned as follows:

Part A: 70%

Part B: 30% Part A comprises 15 test cases, equally weighted. Part B comprises 20 test cases also equally weighted. For part B only your highest 15 scoring test cases count towards your grade (Note: NO Extra credit!).

<h1>Academic Integrity</h1>
You must write the code for this project alone. While you may make limited usage of outside resources, keep in mind that you must cite any such resources you use in your work (for example, you should use comments to denote a snippet of code obtained from StackOverflow, lecture videos, etc). Attempts to import or reference methods/variables in the grading suite or otherwise attempt to circumvent the grading suite in your submission will be considered an academic integrity violation. For an example of this, note how the author of this project’s code cited the source for the clamp function in utilities.py. You must not use anybody else’s code for this project in your work. We will use code-similarity detection software to identify suspicious code, and we will refer any potential incidents to the Office of Student Integrity for investigation. Moreover, you must not post your work on a publicly accessible repository; this could also result in an Honor Code violation [if another student turns in your code]. (Consider using the GT-provided Github server for your repository, or a git server such as Bitbucket that does not default to public sharing.)

<h1>Questions</h1>
Leverage the class forums to compare strategies with your colleagues as you guide your spaceship home! Good Luck!!
