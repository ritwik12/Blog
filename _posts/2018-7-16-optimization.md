---
layout: post
title: Look both ways before crossing a one way street!
---

<p style="text-align:justify;">
I had to develop a tool where I was supposed to extract specific data from a log file. The log file was really big. More than 
2 million lines.</p>

<h3>The log file was somewhat like this:</h3>

![_config.yml]({{ site.baseurl }}/images/log.JPG)

<p style="text-align:justify;">
Log file consists of logs with some ID and timestamp. Task was to get <b>"Time", "Totaltime", "Views" and "ActiveRecord"</b>
for each and every ID. For that first I had to find Unique IDs in the log file, then find data corresponding to that particular 
ID and print accordingly. So, I followed this approach and wrote a Python script for this and it worked. The only problem was 
that it was taking a lot of time. Since, the file was really large so it was taking more than 3 hours to complete. It was not 
feasible as there were files with more than hundreds of millions of lines too.</p>

<h3>This was the code that I first wrote:</h3>

![_config.yml]({{ site.baseurl }}/images/filter.JPG)

<p style="text-align:justify;">
I tried to optimize this code as much as I could. I thought that it's complexity is 0(n^2), So I tried to reduce that, then I 
thought it is taking time to print data. So, I tried saving it to a file. But the result was the same. Then I thought of using 
Parallel processing too. Still, no good. I was using a system with 8 core i7 processor and 16 GB ram. I thought maybe the system
is slow. So, I tried my code on one of my servers with 64 cores and 256 GB ram. But it was taking almost the same time. I got to 
know that the problem is with approach only. I wasn't able to do anything with my code with this approach. At last, I started 
debugging my code line by line to see which part is taking time, once I thought Regex is consuming time, but it wasn't. Then 
after debugging line by line, I noticed that it was the data structures which were making my code slow. <b>SET</b> and <b>LIST</b> inside loops 
were the ones creating all the problem.</p>

<p style="text-align:justify;">
I had to rewrite the code with another approach as nothing worked. So, instead of finding unique IDs and extracting data 
according to each ID, I did just the opposite.</p>

<h3>Code with new approach:</h3>
![_config.yml]({{ site.baseurl }}/images/production.JPG)

<p style="text-align:justify;">
Here, it is looking for the data first and finding ID corresponding to that data which automatically finds all the unique IDs 
with data corresponding to them.</p>

<h3>This was the output:</h3>

![_config.yml]({{ site.baseurl }}/images/prod.JPG)

At first, it was taking more than 3 hours to complete. So, now the question is: How much time it took after all this struggle? 
Just <h3>3.5</h3> <b>seconds!!</b>.
