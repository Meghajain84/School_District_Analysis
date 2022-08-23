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


## Results: Addressing the following questions using bulleted lists and images of DataFrames as support

### How is the district summary affected?

![dist_summary_before_after](https://github.com/Meghajain84/School_District_Analysis/blob/main/Resources/dist_summary_before_after.PNG)
    
* There is no impact on total schools count, students count and budget
        
* The PERCENTAGE math, reading and combined were calculated using the count after subtracting Thomas high school ninth graders count from total student count. The impact is that all these three new percentages got slightly pulled down as seen in the comparison images above.

* The AVERAGE math and reading scores were calculated using all students, including the ninth graders of Thomas high school. Since ninth graders math and reading scores were modified to NaNs, the new percenatges got pulled down(can be seen in previous comparison image). For reading average, unformatted averages(shown in below image) have been compared as they round to same number: 

![dist_summary_unformat](https://github.com/Meghajain84/School_District_Analysis/blob/main/Resources/dist_summary_unformat.PNG)

* Overall the district summary shows slighly less performace in scores and percentages after the NaNs modifictaion.

    
### How is the school summary affected?

![school_summary_inc_ninth](https://github.com/Meghajain84/School_District_Analysis/blob/main/Resources/school_summary_inc_ninth.PNG)
    
* The average math score very slightly dropped

* The average reading score very slightly improved

* The passing percentage for math, reading and overall (math and reading combined) significantly dropped for Thomas High school as the percentage was calculated using all Thomas High school's students' count including 9th graders whose scores were modified to NaNs. 

* When we considered only Thomas high school's 10th to 12th graders in total school count for the same school, we saw the passing percentages for math, reading and overall improved (as seen in image below)

![ninth_graders_in_not_school_sum](https://github.com/Meghajain84/School_District_Analysis/blob/main/Resources/ninth_graders_in_not_school_sum.PNG)
    
        
### How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?

* When considered their 9th graders in the total student count for Thomas High school, their performance dropped to lower performing schools' level (see in image below)

![school_sum_inc_ninth](https://github.com/Meghajain84/School_District_Analysis/blob/main/Resources/school_sum_inc_ninth.PNG)

* When only their 10th - 12th graders were considered in the total student count for Thomas High school, their performance was comparable to other high performing schools. (see in image below)

![school_sum_NOT_inc_ninth](https://github.com/Meghajain84/School_District_Analysis/blob/main/Resources/school_sum_NOT_inc_ninth.PNG) 

* Average reading and math scores of Thomas High school were not impacted much with NaNs modification (as discussed in the school summary section above); therefore, these don't play role in this section.

### How does replacing the ninth-grade scores affect the following:

#### Math and reading scores by grade

![math_read_score_by_grade_old](https://github.com/Meghajain84/School_District_Analysis/blob/main/Resources/math_read_score_by_grade_old.PNG)

![math_read_score_by_grade](https://github.com/Meghajain84/School_District_Analysis/blob/main/Resources/math_read_score_by_grade.PNG)

* By replacing NaNs for 9th graders, the mean is showing as NaN only for 9th graders for Thomas High Schools

#### Scores by school spending

![school_spending_score_before_After](https://github.com/Meghajain84/School_District_Analysis/blob/main/Resources/school_spending_score_before_After.PNG)

* For the same buckets of ($586-$630) and ($631-$645), the average math and reading score, and the math,reading and combined passing percentage numbers increased. That means schools would require students to have better score to be in same budget category of state.

#### Scores by school size

![size_score_before_After](https://github.com/Meghajain84/School_District_Analysis/blob/main/Resources/size_score_before_After.PNG)

* We don't see any impact here when rounded off to whole number.

#### Scores by school type

![type_score_before_After](https://github.com/Meghajain84/School_District_Analysis/blob/main/Resources/type_score_before_After.PNG)

* We don't see any impact here when rounded off to whole number.

## Summary: Summarize changes in the updated school district analysis after reading and math scores for the ninth grade at Thomas High School have been replaced with NaNs.

(1) District performance slighltly dipped.

(2) Thomas High School's performance slightly dipped when only 10-12th standards were considered.

(3) Thomas High school's 9th graders couldn't be compared to their fellow 9th graders from other schools. Their performance wasn't compared to their peers.

(4) For the same buckets of ($586-$630) and ($631-$645), the average math and reading score, and the math,reading and combined passing percentage numbers increased. That means schools would require students to have better score to be in same budget category of state.