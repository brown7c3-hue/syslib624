# Module 3: CLI Work

## Searching with grep (15 Feb 2026)

[Textbook 3.1](https://cseanburns.github.io/systems-librarianship/3a-searching-with-grep.html)

### Overview

### Steps

### Discussion Post

The first grep command I ran was grep -Ei "(title|abstract)" A15 savedrecs.bib. This command helped me view information from the title to the first 15 lines of the abstract (if there were less than this number, then it showed the next lines after the abstract). The next command I ran was grep -Ei "(title|abstract)" A15 savedrecs.bib | cut -d"=" -f2 |\    sed 's/ {//' | sed 's/},//'. This helped remove the first column as well as extra characters. 

I was surprised at how specific the commands needed to be, which is something that also confused me. For example, I tried typing out the cut and sed commands when I was practicing, but I couldn't get them to work. I ended up copying and pasting the command. I'm wondering if I simply missed a space somewhere that caused it to not work because I compared what I typed to the example in the lecture, and that looked correct (I forgot to take a screenshot of this). Aside from this error on my part, it wasn't too hard to practice with. I just need to practice more with the grep command. 

I'm curious about whether or not there is a way to remove the information between the title and the abstract so that I only see those two pieces of information? Also, is there a way to view the full abstract alone? 

## Managing Software & Library Search (22 Feb 2026)

[Textbook 3.2](https://cseanburns.github.io/systems-librarianship/3b-managing-software.html)

[Textbook 3.3](https://cseanburns.github.io/systems-librarianship/3c-library-search.html)

### Overview

### Steps

### Discussion Post

The first search I performed in infocat was find @and @attr 1=4 "comics" @attr 1=21 "library science". This only returned 1 result titled “Comics and critical librarianship: reframing the narrative in academic libraries” edited by Olivia Piepmeier and Stephenie Grimm. Next, I tried to use a different attribute by entering the following command: find @and @attr 1=21 "education" @attr 1=27 "comic books". This, however, produced no results. Because this search did not produce any results, I went back to the first example and entered education in place of comics and comic books in place of library science, which resulted in 10 entries. The last search I performed produced interesting results. I searched find @and @attr 1=4 "comic books" @attr 1=30 "2025" and received 2 results. The interesting part is that neither results contained “comic books” in the title despite me using the title attribute. The two titles that did appear were “Social Psychology and the Ancient World : $b Methods and Applications” and “Visual culture of post-industrial Europe.” Overall, the installation went pretty smoothly, and I followed along with the lecture well enough. 

The last search I performed produced both interesting and confusing results. I’m curious why I received the two titles when neither contained the title I searched for. I was also surprised at the number of results I received in each search I performed. I wasn’t expecting a large number of titles, but I am still surprised at how low the numbers were. Compared to searching a library website, the experience was quite different. The search results seemed to be much more narrowed (with the exception of that last search), and I received all of the basic information I would need for each title. To compare this experience to a library website, I searched UK Libraries as well as my local public library system. I used the first search with the terms comics and library science. UK Libraries produced 4 results, and although this was more than what I originally had, only one of the results was relevant (which was actually the result I received above). My local library, on the other hand, produced no results for the same search. 

I liked this experience and seeing how different it was than performing a search directly on a library website. On a website, there are many different options you can click, yet the yaz-client was pretty direct and to the point. 
