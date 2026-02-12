# solved-cs6035-binexp-ec-login-spring26
**TO GET THIS SOLUTION VISIT:** [[SOLVED] CS6035 binexp ec_login Spring26](https://www.ankitcodinghub.com/product/cs6035-binexp-ec_login-spring26/)


---

📩 **If you need this solution or have special requests Email:** ankitcoding@gmail.com 
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top kksr-disabled" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;145125&quot;,&quot;readonly&quot;:&quot;1&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS6035 binexp ec_login  Spring26&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

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
Resources

<ul>
<li><a href="https://hashcat.net/wiki/">https://hashcat.net/wiki/</a></li>
</ul>
Challenge Instructions

To complete this exercise, you will need to leverage GDB in order to extract information embedded within the binary and weaponize it to attain the flag. Here are some guiding comments to bear in mind:

<ul>
<li>Frustratingly, the source code (flag.c) is pretty sparse. However, we compiled the binary such that it preserved all of its symbols under-the-hood, so you should be able to glean plenty of insight about what the program is doing by (s)tepping into various functions.</li>
<li>When the flag binary is ran, it prompts you for login credentials (username and password). Figuring out what those are is the whole challenge. If the account you login with is recognized as an Administrator, you get your flag!</li>
<li>One of the first things you’re going to want to do is enumerate the struct that contains all of the users and their information. The flag.c source code hints at how this is organized, but you may want to do some research about GDB’s commands in order to scrape up everything you need.</li>
<li>Unfortunately for us, the binary doesn’t store any passwords in plaintext; instead, it only stores password hashes. Since hashing is a one-way function, there’s no way for us to “undo” the hashing: our only hope is to try to crack the password(s).</li>
<li>You are welcome to leverage password cracking software explored in any other part of the class, but we recommend using hashcat.</li>
<li>The hashcat password cracker is an incredibly powerful piece of password cracking software. To run it, you need to specify<u> the hash-mode</u> (-m) a number which specifies the type of algorithm used (e.g. MD5), the type of attack hashcat should perform (-a), the list of hashes to crack, the dictionary wordlist to reference, and any modifiers/rules to use.</li>
<li>We’ve provided a wordlist (passwords.txt) that the Administrator’s account password is derived from; the <em>exact </em>password is not within the list, however. You’ll need to leverage context clues from your analysis of the binary in order to determine what kinds of rules/mutations need to be accounted for by your password cracking attack. This list – compared to others – is <em>very </em>short, so cracking the correct password should be near instant when ran correctly.</li>
</ul>
