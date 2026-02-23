# syslib624

## Module 3 Discussions 

**(15 Feb) Searching with grep**

The first grep command I ran was grep -Ei "(title|abstract)" A15 savedrecs.bib. This command helped me view information from the title to the first 15 lines of the abstract (if there were less than this number, then it showed the next lines after the abstract). The next command I ran was grep -Ei "(title|abstract)" A15 savedrecs.bib | cut -d"=" -f2 |\    sed 's/ {//' | sed 's/},//'. This helped remove the first column as well as extra characters. 

I was surprised at how specific the commands needed to be, which is something that also confused me. For example, I tried typing out the cut and sed commands when I was practicing, but I couldn't get them to work. I ended up copying and pasting the command. I'm wondering if I simply missed a space somewhere that caused it to not work because I compared what I typed to the example in the lecture, and that looked correct (I forgot to take a screenshot of this). Aside from this error on my part, it wasn't too hard to practice with. I just need to practice more with the grep command. 

I'm curious about whether or not there is a way to remove the information between the title and the abstract so that I only see those two pieces of information? Also, is there a way to view the full abstract alone? 

**(22 Feb) Managing Software; Library Search**

The first search I performed in infocat was find @and @attr 1=4 "comics" @attr 1=21 "library science". This only returned 1 result titled “Comics and critical librarianship: reframing the narrative in academic libraries” edited by Olivia Piepmeier and Stephenie Grimm. Next, I tried to use a different attribute by entering the following command: find @and @attr 1=21 "education" @attr 1=27 "comic books". This, however, produced no results. Because this search did not produce any results, I went back to the first example and entered education in place of comics and comic books in place of library science, which resulted in 10 entries. The last search I performed produced interesting results. I searched find @and @attr 1=4 "comic books" @attr 1=30 "2025" and received 2 results. The interesting part is that neither results contained “comic books” in the title despite me using the title attribute. The two titles that did appear were “Social Psychology and the Ancient World : $b Methods and Applications” and “Visual culture of post-industrial Europe.” Overall, the installation went pretty smoothly, and I followed along with the lecture well enough. 

The last search I performed produced both interesting and confusing results. I’m curious why I received the two titles when neither contained the title I searched for. I was also surprised at the number of results I received in each search I performed. I wasn’t expecting a large number of titles, but I am still surprised at how low the numbers were. Compared to searching a library website, the experience was quite different. The search results seemed to be much more narrowed (with the exception of that last search), and I received all of the basic information I would need for each title. To compare this experience to a library website, I searched UK Libraries as well as my local public library system. I used the first search with the terms comics and library science. UK Libraries produced 4 results, and although this was more than what I originally had, only one of the results was relevant (which was actually the result I received above). My local library, on the other hand, produced no results for the same search. 

I liked this experience and seeing how different it was than performing a search directly on a library website. On a website, there are many different options you can click, yet the yaz-client was pretty direct and to the point.

## Module 2 Discussions

**(25 Jan) Using Gcloud for Virtual Machines**

This process was a bit intimidating in the beginning. My screen looked a little bit different as this was my first time logging into google cloud. It prompted me to enable billing from the start before I created a new project, which threw me off a bit as it was a little different from the lecture. I’ve taken a couple of tech-related courses previously in this program, including one where I had to install R-studio, so I’m familiar with following the steps to get something set up. I think once I got past the beginning stage of this exercise, it became a lot more manageable. I found it exciting to be working from a command line as it’s easier for me to learn something when I’m performing exercises rather than reading about it. I was quite confused on all of the terminology like ubuntu, vm instances, etc. I know we’re still in the beginning stage of this course, but I’m curious about what the difference is between typing in commands in R-studio versus something like google cloud or how R-studio differs from google cloud? Also, I was wondering if it’s normal/okay for me to have a different number of updates from the 18 that were in the lecture (I only had 4 updates)? 

**(01 Feb) Learn the CLI**

Overall, I had a good experience using the command line for the first time despite being quite intimidated at first, especially when I was listening to the lecture and hearing so many new terms and not knowing what anything meant. I started feeling a lot more comfortable with this lesson the more I practiced, especially with the flashcards, which I had to fail a lot before it started making more sense. There were straightforward commands like “help,” “cp,” “ls,” and so on, but I struggled a bit with other commands like “grep,” “df,” and “du.” I was struggling a bit with the “systemctl” command as I misread it as “systemct1” (with the number one). It surprised me that I was able to slowly catch on to what I was learning, which I think was possible through actually practicing with the commands and the programs. I don’t think I would have had the same experience if I were simply reading about it. The biggest challenge for me might simply be getting over the initial intimidation of doing something completely new, but I’m sure this will get easier with more practice. There is also a lot of terminology that is completely new to me, so it may be a challenge for me to remember everything. 

**(08 Feb) Using nano, Git, GitHub, and Markdown for Docs**

I decided to use nano as my text editor as it seems to be a simpler option and because it is the most common text editor on Linux systems. I had an easy time setting up Git/GitHub, and I thought it was cool to see how sections are made and how to bold and italicize words. I struggled a little bit this week getting used to working with the text editor (learning how to copy and paste, for example, was different than what I’m used to doing), but it became easier with practice. It also took me many tries to commit my repository. I ended up going back and re-configuring some things, which ended up working in the end. I think I was frustrating myself by not getting things right immediately. Overall, though, I thought it was really interesting seeing how my edits in google cloud appeared in github after being connected. 


## 09 Feb 2026

**My Work So Far**

So far, I have connected Github with my virtual machine (VM), and I have
learned of different text editors. I decided to work with nano for this 
class as it is the most commone text editor. I have learned how to 
start working in my repository after signing back in to my VM by changing
my directory and performing the cat README.md command. 

**About This Repo**

This repository will primarily contain my notes for this course (LIS 624), including 
reminders of specific commands and general reflection on course material. 




