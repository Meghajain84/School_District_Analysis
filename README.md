# School_District_Analysis

## Overview of the school district analysis:
Maria, the chief data anlyst for city school district was given student standardized test(math and reading) scores, and school funding data. The task was to aggregate data, clean it and showcase the trend in school performances based on various factors. This analysis would help the board and supridentant to priortize school budget and priorties. As part of annalysis, the following was done:

* A high-level snapshot of the district's key metrics, presented in a table format
* An overview of the key metrics for each school, presented in a table format
* Tables presenting each of the following metrics:
    *   Top 5 and bottom 5 performing schools, based on the overall passing rate
    *   The average math score received by students in each grade level at each school
    *   The average reading score received by students in each grade level at each school
    *   School performance based on the budget per student
    *   School performance based on the school size 
    *   School performance based on the type of school

In addition, the school board had notified Maria and her supervisor that the data showed evidence of academic dishonesty; specifically, reading and math grades for Thomas High School ninth graders appeared to have been altered. Although the school board did not know the full extent of the academic dishonesty, they wanted to uphold state-testing standards and had turned to Maria for help. So, the task was to replace the math and reading scores for Thomas High School with NaNs while keeping the rest of the data intact. 

After that the school district analysis was repeated with modified data and this report describes how these changes affected the overall analysis.


## Results: Using bulleted lists and images of DataFrames as support, address the following questions.

### How is the district summary affected?

![dist_summary_before_after](https://github.com/Meghajain84/School_District_Analysis/blob/main/Resources/dist_summary_before_after.PNG)
    
* There is no impact on total schools count, students count and budget
        
* The PERCENTAGE math, reading and combined were calculated using the count after subtracting Thomas high school ninth graders count from total student count. The impact is that all these three new percentages got slightly pulled down as seen in the comparison images above.

* The AVERAGE math and reading scores were calculated using all students, including the ninth graders of Thomas high school. Since ninth graders math and reading scores were modified to NaNs, the new percenatges got pulled down(can be seen in previos image). For reading average, unformatted averages(shown in below image) have been compared as they round to same number: 

![dist_summary_unformat](https://github.com/Meghajain84/School_District_Analysis/blob/main/Resources/dist_summary_unformat.PNG)

* Overall the district summary shows slighly less performace in scores and percentages after the NaNs modifictaion.

    
### How is the school summary affected?

![school_summary_inc_ninth](https://github.com/Meghajain84/School_District_Analysis/blob/main/Resources/school_summary_inc_ninth.PNG)
    
* The average math score very slightly dropped

* The average reading score very slightly improved

* The passing percentage for math, reading and overall significantly dropped for Thomas High school as the percentage accounted for all Thomas High school's students including 9th graders whose scores were modified to NaNs(equal to 0) 

* When we considered only Thomas high school's 10th to 12th graders in total school count for the same school, we saw the passing percentages for math, reading and overall improved (as seen in image below)

![ninth_graders_in_not_school_sum](https://github.com/Meghajain84/School_District_Analysis/blob/main/Resources/ninth_graders_in_not_school_sum.PNG)
    
        
### How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?

![school_sum_inc_ninth](https://github.com/Meghajain84/School_District_Analysis/blob/main/Resources/school_sum_inc_ninth.PNG)

* When considered their 9th graders in the total student count for Thomas High school, their performance dropped to level of few other low performing schools

![school_sum_NOT_inc_ninth](https://github.com/Meghajain84/School_District_Analysis/blob/main/Resources/school_sum_NOT_inc_ninth.PNG)

* When only their 10th - 12th graders were considered in the total student count for Thomas High school, their performance was comparable to other high performing schools

* Average reading and math scores were not changed much 

### How does replacing the ninth-grade scores affect the following:
    * Math and reading scores by grade
    * Scores by school spending
    * Scores by school size
    * Scores by school type


## Summary: Summarize four changes in the updated school district analysis after reading and math scores for the ninth grade at Thomas High School have been replaced with NaNs.

(1) 