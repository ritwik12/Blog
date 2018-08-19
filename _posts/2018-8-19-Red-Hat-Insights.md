---
layout: post
title: Red Hat Insights!
---

<p style="text-align:justify;">
Red Hat® Insights gives your business the ability to predict and prevent problems before they occur. You get real-time, in-depth 
analysis of your Red Hat infrastructure to proactively identify threats to security, performance, and stability.
</p>

<iframe width="560" height="315" src="https://www.youtube.com/embed/MfRnKe-xxLM" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

<h3>My part in this:</h3>
<p style="text-align:justify;">
I wrote Insight rules for Satellite Performance, rules are written to Tune Satellite in a way so that customers can use Insights
and will get the solution to their problem without reporting it as a bug. Most of the times customers using Satellite report bugs 
which aren't exactly bugs but just an untuned installation of Satellite. Such as using System memory far more than required or using 
it lower than needed. For such cases, a person should go through the Satellite Tuning guide which we expect he will not :P So, for 
that if a person is using Insights then we can help him to know the problem and also the solution to that problem. It works by using <a href="https://github.com/RedHatInsights/insights-core">insights-core</a> which contains the parsers and combiners which are required in writing rules so as to get the information from the <b>sos-report</b>. Every rule consists of logic through which it decides whether it needs to report or not. Things that it reports <b>- ERROR-KEY, Tuning guide link, Conflicting values such as low number of cpu-cores, low version of some software, etc. </b> To know more about Red Hat Insights visit 
 <a href="https://www.redhat.com/en/technologies/management/insights">Red Hat Insights</a>.
</p>
