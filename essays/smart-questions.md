---
layout: essay
type: essay
title: "You are bad at asking questions"
# All dates must be YYYY-MM-DD format!
date: 2025-01-30
published: true
labels:
  - Questions
  - Answers
  - StackOverflow
---

<img width="300px" class="rounded float-start pe-4" src="../img/istockphoto-1386740242-612x612.jpg">

# Questioning is good... right?
Questioning is a natural thing for human beings. It allows us to learn more about the world and gives us the oppurtunity to share experiences and knowledge between other people who may not have as much experience. With the advent of technology, communication and information has been mainstreamed, and questions are being asked millions of times per second. With so many questions, technology is able to give us the information without the need of another human being. That being said, there are still a lot of questions that have yet to be answered or docummented onto the internet, partially because it needs to be formally written by a human, or partially becuase the question talks about obscure topics that have not been thought about in that particular context. It is at this point that we can rely on others to try and problemsolve and create answers to these solutions, or to find out that there is no definitive answer to the question.

## How do I ask questions to people?
In the professional setting, StackOverflow is one of many forums that are used to ask and answer questions. As a forum, anyone can post and ask for questions. StackOverflow does a great job at filtering these questions so that it answers unique quesitons, including questions that are very specific, as well as questions of programs that are not well docummented. Here we will see an example of a well written question to a forum. 

```
Q: Overlay sf object on ggmap - not aligned, specific to region

I would like to overlay an sf object (mapping geometry with organization's data) over the google map showing terrain features. This was successful when using other US states, but not Alaska. What do I need to do/change in order to overlay the map more precisely? map overlay i achieved

ak1<-ggmap(AK.base)+
  geom_sf(data=ak_region_download,mapping=aes(geometry=geometry,fill=n,color=''),inherit.aes = F,alpha=.5)+
  scale_fill_continuous(na.value=NA,low = "darkblue", high = "orange", 
                        name = 'number',
                        breaks=c(1,5,10,20,30,40))+
  scale_color_discrete('')+
  theme_bw()
ak1
For reference I achieved AK.base with a google API

AK.base <- get_map(location = c(lon=-152,lat=63.5), zoom = 4, scale = "auto", 
                   maptype = c("terrain"), 
                   messaging = FALSE, urlonly = FALSE, filename = "ggmapTemp", 
                   crop = FALSE, color = c("color"), source = c("google"))
And the dataframe looks something like this, using the geojson file from the website referenced below.

# https://gis.data.alaska.gov/datasets/DCCED::alaska-borough-and-census-area-boundaries/about
#
# Download shapefile from above link, place ZIP in folder called DataRaw within 
# project directory, unzip
ak_region_download <-
  here("DataRaw/Alaska_Borough_and_Census_Area_Boundaries.shp") |> 
  sf::st_read()
ak_region_download$n <- 1:30

I have solved this trouble in bash with:

echo $(date -d"3 month ago" "+%G%m%d")

I think that if bash has a built-in way for this purpose, then python, much more equipped, should provide something 
better than forcing writing one's own script to achieve this goal. Of course i could do something like:

if int(time.strftime('%m')) == 1:
    return '12'
else:
    if int(time.strftime('%m')) < 10:
        return '0'+str(time.strftime('%m')-1)
    else:
        return str(time.strftime('%m') -1)
        
I have not tested this code and i don't want to use it anyway (unless I can't find any other way:/)

Thanks for your help!
```
Link to [question](https://stackoverflow.com/questions/79398303/overlay-sf-object-on-ggmap-not-aligned-specific-to-region)

The heading is done pretty efficiently. It cuts straight to the point, mentioning the program that they are working with and the specific issue they are having with the program. When you click into the question, there is a short but very intricate description of the goal. They also mention that they have tried this with other states, but it is this specific state that is not working with the program. Finally, they gave the code along with the references used alongside the code. This makes it very easy for other professionals to look at and analyze any errors in the code. 

The answer that this got was just as descripitive and to the point as the question. The answer had two main points of error and attempted to list out some fixes, as well as mentioning that these fixes do not fully reach the goal set by the question. The creator of the question followed up stating that the fix did work for the purposes that they were intending for. This shows that specific and targeted questions that get straight to the point are effective in getting equally targeted answers.

## How do I NOT ask a question to people

While it may seem very simple and easy to make a good, directed, question, there is often many questions that are put onto forums that are, so to say, pointless. Here is an example of one on StackExcange:

```
Q: Should I use Ternary relationship or complex attribute [closed]

help me create the ERD of my Job recruitment system and explain succinctly how each entity can be represented, and mapped. I specifically want to ask about the Apply relationship, and weather the applicationStages is drawn and mapped correctly to reflect that the applicationStages should only be visible once an applicant has applied to a job and was shortlisted by a recruiter to start the interviewing process. Should the ApplicationStages be represented as a weak entity on this relationship, or a complex attribute?
```
Link to [question](https://stackoverflow.com/questions/79401235/should-i-use-ternary-relationship-or-complex-attribute)

This question seems like much less a question and seems more like a "can you please do this for me?" The biggest problems with this question is that there is no previous structure to work on nor is there a specific goal that should be reached. On some forums, this may be okay to post, although professionals probably won't respond, and it is a quesiton to be left as a discussion for people who are bored rather than a question for professionals to answer. This is exactly the reason why StackOverflow decided to close this question.  

## Conclusion
Questions are a very useful method of obtaining information and utilizing other peoples' expertice as knowledge for getting a task done. With the advent of computers, there is a lot of questions that have answers already on Google or other simple forums. If you want real questions answered or you can't find the same question asked anywhere else, then it is best to post to a professional forum or reach out to a professional of that subject. Be warned though, as to get an answer you must due your proper dilligence in making sure that your question is specific and targeted, and it should show that you at least tried to make it work using outside resources. This is not only corteous but it ensures that you are not wasting time for an answer, something that many professionals do not have. 
