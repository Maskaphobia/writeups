<div style="display:flex; flex-direction: column; align-items: center;">
<h1> Haunted Pumpkin CTF '25 🎃</h1>
<h3> Organized by OSINT Switzerland </h3>

</div>


## Dark Archives

<img width="651" height="409" alt="image" src="https://github.com/user-attachments/assets/00803386-6de6-4b33-9d2f-c9b5c78ba9f7" />

> We found this online. <br>
> We figured out that he is as well involved in the summoning of the haunted pumpkin. <br>
> Somewhere on the way he dropped a flag. <br>
> Can you find it ? <br>
> The flag reveals itself once you found the solution <br>

<details> 
  <summary>Solution</summary>
  
  For a CTF question that requires Github:
  1. <b>Find the project/user mentioned.</b> The question already mentioned it, which saves us alot of time.
  2. <b>Check the Github commit.</b> A Github commit is a saved set of changes to a repository, representing a snapshot of the project's state at a specific point of time. This means that there might be a possibility the author had once published the flag but deleted it. <br>
<img width="1338" height="581" alt="image" src="https://github.com/user-attachments/assets/c67015a7-1fc8-4fc6-9d4c-1be4bb9a1af3" /> <br>
However, in the picture, we found that theres nothing really interesting. 

  3. <b>Appending .patch to the pull request url.</b> You can generate a patch file from a Github pull request, which can contain changes, including email metadata. <br>
<img width="673" height="342" alt="image" src="https://github.com/user-attachments/assets/9d650ce8-3921-436c-a0a2-2aa21ba92fef" /> <br>
This leads us to find `<jackolantern.hpc7f@gmail.com>`

  4. <b>Finding it on Google Calendar.</b> Since you have their email, you can see their calendar (If it's shared publicly). <br>
<img width="1290" height="573" alt="image" src="https://github.com/user-attachments/assets/6c43ea76-6203-43c4-aba2-da1412261afd" /> <br>
This leads us to find `NHhtMmRsbzZrd2o1eTZjMnlqN21vcnd4Z2JmcXprM2M1djZrdHRobmJndnA3M3ZkM3lqZnEzcWQub25pb24=`

  5. <b>Decode the message.</b> It's an obvious base64 encoding, so decode in CyberChef and we will have `4xm2dlo6kwj5y6c2yj7morwxgbfqzk3c5v6ktthnbgvp73vd3yjfq3qd.onion`
  6. <b>Onion? Tor? What even is that?</b> Searching it up on google, we realise that .onion is a special type of website accessed only through the Tor network, which provides anonymity for both user and site operators. <br>
Tor browser is designed to enable anonymouse browsing through a process called onion routing, encypting data in multiple layers, sends it through servers, each peeling away one layer of encyption at a time. <br>
This method obscures the user's IP address and location, making it extremely difficult for anyone to trace online activity back to the user. (Dark web) <br>
That's it right? We just have to access it through Tor and we will get the fla... <br>
<img width="934" height="122" alt="image" src="https://github.com/user-attachments/assets/eff264ca-d372-4b6b-975c-839db2e86615" /> <br>
<b>NOOOOOOOOOOOOOOOOOOOOOOOOOOOOOO</b>
  7. <b>Final step.</b> The question title "Dark Archives" hints us. We have already found the "Dark" part, but what about the "Archives" part? <br>
  I would have assumed it was `internet archive (wayback machine)` instead of `archive.today` but what's the difference? <br>
* `Internet Archive` is a digital library that automatically and manually saves snapshots of webpages, books, etc. (Through crawlers)
* `archive.today` is a private snapshot tool that saves a single version of a webpage instantly and permanently <br>
Just enter the .onion url and you got it!
<img width="1347" height="193" alt="image" src="https://github.com/user-attachments/assets/e2ab130f-e55d-4331-a845-6fcc03800a93" />
</details>
<details>
<summary>Flag</summary>
  hpCTF{N1C3_Y0U_G0T_4N07H3R_0N3_4724}
</details>
