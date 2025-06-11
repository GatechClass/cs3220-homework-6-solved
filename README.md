# cs3220-homework-6-solved
**TO GET THIS SOLUTION VISIT:** [CS3220 Homework 6 Solved](https://mantutor.com/product/cs3220-hw6-solved/)


---

**For Custom/Order Solutions:** **Email:** mantutorcodes@gmail.com  

*We deliver quick, professional, and affordable assignment help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;112365&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;3&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (3 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS3220 Homework 6 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

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
            5/5 - (3 votes)    </div>
    </div>
Part 0 : Open jupyter notebook on pynq board cluster

Please use synestia cluster access to know how to access pynq board. We are encourage to use ODD

Part 1 : Follow the overlay tutorial with providied bistream

In this part you’ll run a tutorial program on jupyter notebook with tutorial bistream.

This instruction is based on this tutorial. The tutorial file is copied from this repo: https://github.com/PeterOgden/overlay_tutorial.git [step 1] Check out hw6_files from the class git

[step 2] Go to the directory with your GT account ID and upload files to pynq board’s ARM processor (scalaradd.ipynb, tutorial_1.bit, tutorial_1.hwh)

If you are using onDemand GUI, you can skip this step since the ARM processor on Pynq board already has an access to your home.

[step 3] Open scalaradd.ipynb in jupyternotebook and edit the file location to your directory (/nethome/[GT account ID]) in cell 1 and 7

Press the run button for each cell and see whether it works or not.

Part 2 : Generate and run your own bistream

In this part, you will create a bitstream from Vivado and extend the tutorial to load your own bitstream design.

Step-Vitis: Open Vitis HLS and generate ip

Start Vitis HLS program (similar to HW#5) Note that the following figures are using a different version of HLS, pls follow the texts if the figure looks different from the Vitis HLS/Vivado in synestia cluster.

[1] Click on â€œCreate New Projectâ€ in the very first page.

[2] Specify the â€œProject nameâ€ and â€œlocationâ€ of the project

[3] Click on â€œAdd Filesâ€¦â€ to add â€œadd.cppâ€ and â€œadder.hâ€. Put “add” as the top function. Do not add the test file yet.

[4] In the same window, click on Browse, to choose the top function (you can add it later).

[5] In the next window, click on â€œAdd Filesâ€¦â€ to add â€œadd_test.cppâ€, which is our testbench.

[6] In the next window, you can leave Solution Name and Period as it is, and just click on â€œâ€¦â€ to choose pynq-z2 boards. Then click â€œFinishâ€.

[7] Then, your project is opened. You can see the files in the left.

[8] If you haven’t added top module, open “project settings” -&gt; “Synthesis” and add top module “add” in this example as top function.

[10] “Solution”-&gt;”Run C Synthesis” -&gt;”All Solutions”

[12] “solution”-&gt;”Export RTL”

[13] Copy AXI data register ids for inteface on the later step. The location for these IDs is in /solution1/impl/ip/drivers//src/_hw.h

[14] Copy the data range somewhere to match with pynq boards. Please see below image as example of what data range we are talking abouthere.

define ADDR*_DATA addresses

Step-Vivado:Open Vivado and import IP and generate Bitstream

Start Vivado application

[1] Create new project, select RTL project and then select pynq-z2 for your board. (you don’t need to add any new files and just select defaultoptions)

[2] Click on the “IP Integrator/Create Block design,” use default name “design_1”, do “OK”

[3] Project Manager -&gt; IP -&gt; IP Repository -&gt; click the “+” icon to add the directory &lt;project_name&gt;/solution1/impl/ip from the Vitis HLS step.

[4] Create Block Design (using default name design_1) -&gt; In the Diagram Window, right click -&gt; add ip -&gt; search Zynq Processing system and add our HLS IP module Add.

[5] Click on the “Run block automation” and “Run connection automation” -&gt; Click “Validate Design”

[6] Go to “sources” and right click on your block design name, click on “Create HDL wrapper”. Click on “Let Vivado do …” option and press”OK”.

[7] Click on Project -&gt; Generate Bitstream (it will ask to synthesize etc. and click yes)

[8] Click on File-&gt;Export-&gt; Export block design, select the option of including bitstream

[8.a] Copy bit stream file *.bit, for example .runs/impl_1/design_1_wrapper.bit

[8.b] Copy tcl script file *.tcl, for example .runs/impl_1/design_1_wrapper.tcl

[9] Copy hwh file from .gen/sources_1/bd/design_1/hw_handoff you can find hwh file.

[10] Make all files in the same names (e.g. add.bit, add.tcl, add.hwh) and place where they are easy to find

[11] Upload the three files (add.hwh, add.tcl, add.bit) into pynq boards (as you did in Part 1)

[12] Repeat part-1 using jupyter-notebook with myadd.ipynb file

Part 3: Convert the add example to take 3 inputs and change the name of module to add3

IMP Note: Please create new Vitis HLS project and new Vivado project for part 3

In Part 2 you created an addition IP that used 2 ports (a &amp; b). For Part 3, you need to modify add.cpp and adder.h to make it into 3 port IP. So inputs will be a,b,c and output will be d.

d = a + b + c

Name of module is add3. (create add3.cpp add3.h myadd3.ipynb for 3 incput cases)

Overview of general steps we follow:

Step [1] Open Vitis HLS and generate ip : please pay attention to create HLS interface for d.

Step [2] Open Vivado: Add ip and PS and generate bitstream, metafiles

Step [3] Copy the bitstream of add3 into jupyter (pynq boards)

Step [4] Update myadd.ipynb to work with new module add3 and change the new file as myadd3.ipynb

Useful github links:

PYNQ repo : https://github.com/Xilinx/PYNQ

Overlay tutorial code: [https://github.com/PeterOgden/overlay_tutorial]

What to submit: add3.cpp add3.h a myadd3.ipynb, a screenshot of working proof from the jupyter notebook

Example screenshot ** Grading poicy ** (1 pt) If you cannot complete part-3, submit a screenshot of part-2. If you complete part-3, you will get a full 3-point credit.

In order to do project #4, hw#6 needs to be completed first. Please finish it ASAP.
