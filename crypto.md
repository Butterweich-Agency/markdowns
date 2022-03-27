#How to mine Crypto with us

### General Info 
Many people think that mining simply kills their GPU. This is not true. Mining does not generally hurt a GPU. Mining just utilizes a GPU, which causes heat. Like gaming and video rendering. There are specifications for the electric parts on your GPU board and how long they are able to work under heat. So basically you can mine forever (what many ppl do...) as long as you stay in a safe heat-zone. There are many ways to reduce that heat. Most important is of course cooling. I recommend you to not change anything on your stock one. Just make sure your case can provide fresh cool air. You can underclock (opposite of overclocking) the GPU with if you like to (advanced but effective). You can also set limits in the mining software on how much the GPU should be utilized (only 80% instead of 100% - I do it so the fan is not loud). And to avoid what you are afraid of: You can set 2 temp limits (core and VRAM) which you feel comfortable with. As soon as you reach the limits, the miner will pause until its below the limit again. So if you run this mode, you are safe.
There are many great blogs telling you whats good and whats bad. \
I will post the blog with the by far most strict temp limits here: https://www.cputemper.com/what-is-the-safe-gpu-temperature-while-mining/ --> Keep in mind, he is talking about 24/7 mining for years. We are talking about days. Just so noone starts panicking...\
\
I will not give instructions on how to underclock your GPU. But you can google it. Keep in mind this is advanced! If you know what your doing, consider google some settings for ETH and your card. It really lowers your temps. 

### How to set it up
#### Step 0: Check if you even got the right Hardware
I do recommend to not use a Laptop (especially not stuff like a surface) for this! The components are way to close to each other. You would need to set the temp limits very low (65?). It probably doesnt make sense to do it then...\
Then, find out what GPU u got. For this open the Task-Manager, go to "Performance" and scroll down to "GPU". Click on it and it will tell you the name. Open this page following link and verify that your GPU earns more than 0.5$ "Est daily" per day:
https://minerstat.com/coin/ETC/profitability \
Just so you know: If you would mine 0.70$ for us for one day, that would keep our core fallback server (the most important one) running for 2 days! Just to put in perspective for you on how important each cent is. 

#### Step 3: Download and setup the Miner
I recommend using gminer: https://gminer.info/download/latest/ \
There are many others too, ofc you can use whatever you would like to. Keep in mind that parameters will differ. Download it and unpack the ZIP somewhere. Let me explain what you can see in the folder: The "miner.exe" is the miner-application. You cant just start it. If you just double click it, it instantly closes itself again as you didnt tell the tool what to do. To tell the tool what to do, there are other files in the folder. Like "mine_etc.bat". In this case we want to mine etc, so open and edit it to the following please:
> ./miner.exe --algo etchash --server etc.2miners.com:1010 -i 85 -t 70 --templimit_mem 90 --user 0xE5d6F4e8dC1db3a9fDd22c841C1B76495485C60e.ANONYM


Let me explain this: Every --WORD or -LETTER is a parameter. After the specification of this you can see the value that is set to it. For example we got "--algo etchash" which tells the miner.exe to use the etchash-algorithm for mining. _"--server etc.2miners.com:1010"_ specifies the server. You could mine of another one of course, but we dont recommend to. Now the important part: "-i 80" means that the GPU only should be utilized up to 80%. You can change this of course. "-t 70" is the GPU Core temperature limit. The miner will pause if the limit is reached. You can of course also change that, but please google settings before! "--templimit_mem 90" is another temperature limit, but this time for the memory of your GPU. Feel free to change to if you like to. Finally _"--user 0xE5d6F4e8dC1db3a9fDd22c841C1B76495485C60e.ANONYM"_ means that you are "working" for our wallet _"0xE5d6F4e8dC1db3a9fDd22c841C1B76495485C60e"_ and you want to name your computer(=worker) for the statistics _"ANONYM"_. Feel free to change the "ANONYM" to any name if you want to track your worker online. At the end of course safe your file. \
\
**CONGRATS U R DONE! **

#### Step 4: Start the miner
Double click the mine_etc.bat (make sure its really only mine_etc.bat - rename to "mine_for_bwa.bat" if you want to...). A window opens and starts mining. After a few minutes you can see your worker here (if you changed name from anonym to something else): https://etc.2miners.com/account/0xE5d6F4e8dC1db3a9fDd22c841C1B76495485C60e#farms
\
With above settings the miner will all the time reach the limit, then pause for some seconds to cool down again. This is normal and you dont need to worry about it. We want it to be like that. \
 \
 \
 \

#### (OPTIONAL) Step 5: Overwrite the Fan-Control
Download "MSI Afterburner" from the offical webpage https://www.msi.com/Landing/afterburner/graphics-cards
Open the Application and set the GPU Fan as high as you feel comfortable with. If its not super loud and annoying, feel free to set to 100%. This will prevent the miner from overheating so fast. 

#### (OPTIONAL ADVANCED) Step 6: Underclock your Core Speed to further reduce heat
If you know what u are doing, you can reduce the core speed of your GPU in afterburner. I recommend googling some settings for your individual GPU in combination with ETC mining. Mostly you underclock by around -200. 
