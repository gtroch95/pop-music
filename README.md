# Physical Pop Music Releases in the Streaming Age

## Project Description:

This project examines the past 10 years of pop music physical releases on vinyl, CD, and cassette using the Discogs API. The project visualizes changes over the past decade across major labels, independent labels, and self-released artists, and uncovers current collector interest in an era dominated by streaming services.

## Rationale Statement: 

Streaming services are the main method by which people currently listen to music; nevertheless, there has remained a strong community of collectors of physical albums. This community has the potential to grow due to streaming and subscription fatigue, the desire for personal ownership, and nostalgia. Additionally, public awareness has developed around the dire compensation of artists by streaming services, which affects artists on independent labels and especially those who are not signed at all; an increased interest in purchasing physical albums would tangibly affect these artists’ ability to make music. 
  
With these factors in mind, this project was undertaken to understand how physical pop record releases have developed over the past decade and where pop record collecting actually stands in 2025. Pop music in particular was chosen for this project because it moves with the trends and encompasses a wide diversity of artists, from the most commercially successful to the truly bedroom-produced.  

## Workflow:

I fetched data from the Discogs API using Discogs’ proprietary client, **discogs_client**. Because the API’s request limits and automatic pagination made it difficult to gather the necessary data for the project, I opted to create a workflow to reuse for each year that would separate requests into manageable chunks, those being the four sub-genres encompassing most pop music on Discogs: alt-pop, indie pop, synth-pop, and dance-pop. **Pandas** was utilized to create data frames for each sub-genre, as well as to merge these data frames into one. I used this workflow for each year, exporting the merged data frames as separate CSVs. **OpenRefine** was used to combine the CSVs into one that encompassed 2015 - 2025, as well as to clean the data. From the main CSV, I again used **Pandas** to create separate data frames for use with **Seaborn** for visualization.  

## Further Uses:

In the future, this project could be built upon to examine further developments in record collecting and physical music releases in pop. Currently, it could be used to examine other genres. The workflow I used for separating requests into manageable chunks might be particularly useful for those that are having trouble with Discogs’ limitations on bulk data gathering.

## Files:

- Discogs_pop.ipynb contains the initial code used to fetch data from Discogs, create and merge the separate subgenre data frames, and save the resulting dataframe to CSV

- Pop_2015.csv, Pop_2016.csv, Pop_2017.csv, etc… are the 11 CSVs that were created from Discogs_pop.ipynb

- Pop_cleaned.csv is the merged CSV of all 10 years that was created using OpenRefine, with formatting cleaned

- Discogs_pop_visualization.ipynb contains the code used to create smaller dataframes from the CSV for visualization
