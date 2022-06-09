# School District Analysis 
## Overview 

For this project, the goal was to gather, clean, and display data for a School District based on scores per  grade, per school, and much more. Furthermore, another goal of this project was to take the data that had been analyzed and remove and replace scores for a certain grade and school due to the possibility of academic dishonesty which could influence the data. 

There will be examples of the data both before and after the replacement of math and reading grades for 9th graders at Thomas High School. It is crucial that data, in any project, be as accurate and truthful as possible, no matter if the changes in the end are miniscule. 

## Replacing grades with NaN

The first step was to take the grades that need to be replaced (9th Graders from Thomas High School) and replacing the, with NaN, or No applicable number. This is going to let us do calculations later on in the analysis without the corrupted numbers affecting our outcomes. 

To do this, I used the .loc method to find and replace those grades with NaN, as shown below. When we run the code, we can see the replacement happen. 

```
student_data_df.loc[(student_data_df["school_name"] == "Thomas High School") & (student_data_df["grade"] == "9th"), ["reading_score"]] = np.nan 

student_data_df.loc[(student_data_df["school_name"] == "Thomas High School") & (student_data_df["grade"] == "9th"), ["math_score"]] = np.nan 

```
![Nan Replacement](https://user-images.githubusercontent.com/60283799/172723830-ed1d7e29-7e7f-4b7f-9280-ef7a1a7fd1d2.PNG)

## Results

- ### How was the district summary affected?

When we look at the district summary, it's evident that these numbers did not change the end number by much, only by .1 in the "Average Math Score" category. 

Before cleaning the data 
  
![District Summary before cleanup](https://user-images.githubusercontent.com/60283799/172727634-7d6186f1-910b-4eeb-aef1-392838011779.PNG)

After cleaning the data 

![District summary after cleanuo](https://user-images.githubusercontent.com/60283799/172727133-b63cf5b7-ef95-46c0-9ccf-76ef303c60a9.PNG)

- ### How was the school summary affected?

For the school summary, it was a similar result as the district summary. Since the amount of grades changed only made up a small percentage, the change was not significant in the end result. The biggest difference was the </br>
"% Passing Reading" dropping by .3

</br>

Before cleaning the data

![Titles](https://user-images.githubusercontent.com/60283799/172728834-8cacae0e-dcf4-4514-8f83-adcdc956945d.PNG)
![Per School summary beforecleanup](https://user-images.githubusercontent.com/60283799/172728100-bd4625d4-abf0-4b34-b635-5c52db6c2475.PNG)

After cleaning the data

![Titles](https://user-images.githubusercontent.com/60283799/172728853-58bc6e81-e13c-406e-b23e-fe1547a9017b.PNG)
![Per School summary after cleanup](https://user-images.githubusercontent.com/60283799/172728395-8eff1da9-875a-4d2a-94ff-a1549a1a32f6.PNG)

- ### How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?

When it comes to Thomas High Schools' ranking among the top schools, cleaning the data did not move them up or down the list, leaving them in the second spot of the "Top 5 Schools" list. 

![Top 5 school after cleanup](https://user-images.githubusercontent.com/60283799/172729471-35d151fd-7f89-47ca-b462-6d7b4ada3c2f.PNG)

- ### How does replacing the ninth-grade scores affect the following?
     - Math and Reading scores by grade
       
       For math and reading scores by grade, we can see that since we replaced the 9th Grade scores for math and reading        with "NaN", they no longer show up in the table. This is one of the major changes with the chart. Below is a photo        showing only the Math grades, however the reading looks the same it is just not shown. 
       
       Before cleaning the data:
       
       ![Math scores by grade](https://user-images.githubusercontent.com/60283799/172740072-b38fb6b4-f76a-4fd5-954e-a96703d082af.PNG)

       After cleaning the data:
       
       ![Math scores by grade](https://user-images.githubusercontent.com/60283799/172740116-d5f0ca49-1464-4369-b8ca-928f64377782.PNG)

     - Scores by School Spending
       
       When looking at scores by school spending, Thomas High School falls under the "$631-645" category and we can see that there is no change after cleaning the data. 
       
       Before cleaning the data:
       
       ![spending summary before cleanup](https://user-images.githubusercontent.com/60283799/172750492-955d0cf8-20ed-4eb2-ba16-7e379a34ff4d.PNG)

       After cleaning the data: 
       
       ![spending summaries after cleanup](https://user-images.githubusercontent.com/60283799/172750534-1e078f3c-1b9f-48bf-a639-1aad05f02ce9.PNG)

     - Scores by School Size
       
       Thomas High School is considered a "Medium" sized school, and when looking at the outcome it's evident that cleaning the data made no difference in this category. 
       
       Before cleaning the data: 
       
       ![scores by school size before cleanup](https://user-images.githubusercontent.com/60283799/172750747-d3130f10-bd15-4dcd-b466-f936fde17225.PNG)
       
       After cleaning the data:
       
       ![scores by school size after cleanup](https://user-images.githubusercontent.com/60283799/172750778-a43cab78-8149-44c9-be7e-29943ff181a1.PNG)

     - Scores by School Type 
       
       Finally we come to scores by school type. Thomas High School is a Charter school, and we notice that the cleaning the data had no impact on this category. 
       
       Before cleaning the data:
       
       ![scores by school type before cleanup](https://user-images.githubusercontent.com/60283799/172751066-7ae943d8-9ea9-42c7-bffc-3cb23cd28e89.PNG)

       After cleaning the data:
       
       ![scores by school type after cleanup](https://user-images.githubusercontent.com/60283799/172751051-b3b6bf38-eed5-4a16-84f5-510332936508.PNG)



## Summary 

Cleaning, verifying and formatting data are very important when doing any sort of analysis. This specific dataset wasn't affected much by the dishonest scores, however a different type or bigger dataset might be. As mentioned, the changes in this set were miniscule, however there were still at least 4 measurable changes. 

1. For "Average Math Score" in the District Summary, the score dropped by .1%
2. For the "% Passing Reading" in the School Summary, the score dropped by .3%
3. The 9th Grade scores for "Math scores by grade" are now "NaN" or No Applicable Number. 
4. The 9th Grade scores for "Reading scores by grade" are now "NaN" or No Applicable Number.






