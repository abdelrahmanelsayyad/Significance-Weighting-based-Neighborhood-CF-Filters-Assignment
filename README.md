# AIE425 Intelligent Recommender Systems  
### Assignment 2: Significance Weighting-Based Neighborhood CF Filters  

**Student Name:** Abdelrahman El-Sayyad  
**Student ID:** A20001136  

---

## Table of Contents  
1. [Outcomes of Section 3.1](#outcomes-of-section-31)  
2. [Summary of Part 1 and Part 2 Comparison](#summary-of-part-1-and-part-2-comparison)  
3. [Conclusion](#conclusion)  

---

## Outcomes of Section 3.1  

1. **Use of Dataset and Rating Scale**  
   - Used the dataset created in Assignment 1.  
   - Scaled ratings to a **1-to-5** scale.  

2. **Counting Total Users and Items**  
   - Total Users (tnu): **50**  
   - Total Items (tni): **138**  

3. **Counting Ratings per Product**  
   - Calculated the number of ratings for each product to confirm completeness before introducing missing values.  

4. **Selecting Active Users and Introducing Missing Ratings**  
   - Selected active users: **U1, U2, U3**  
   - Missing ratings: **2, 3, and 5** for each user respectively.  

5. **Target Items with Missing Percentages**  
   - Selected target items: **I1 (4% missing)** and **I2 (10% missing)**  

6. **Co-Rating Analysis and 2D Array**  
   - Performed co-rating analysis.  
   - Created a **2D array**:  
     - **Column 1:** Number of common users (descending)  
     - **Column 2:** Corresponding co-rated items.  

7. **Plotting Ratings Count Curve**  
   - Plotted a **bar chart** showing the distribution of ratings per item.  

8. **Determining Threshold β**  
   - Calculated threshold **β** for each active user where users co-rated at least **30%** of items.  

9. **Saving and Displaying Values**  
   - Saved all intermediate values including **tnu**, **tni**, co-rating arrays, and β thresholds.  

---

## Summary of Part 1 and Part 2 Comparison  

### Part 1: User-Based Collaborative Filtering  
- **Case Study 1.1:** Cosine Similarity (No Mean-Centering)  
- **Case Study 1.2:** Cosine Similarity (With Mean-Centering)  
- **Case Study 1.3:** Pearson Correlation Coefficient (PCC) with Mean-Centering  

**Key Insights:**  
- Mean-centering improved similarity accuracy by accounting for user bias.  
- **PCC** provided more meaningful correlations than cosine similarity, especially with mean-centering.  
- Applying the **Discount Factor (DF)** refined top neighbors, improving the accuracy of rating predictions.  

### Part 2: Item-Based Collaborative Filtering  
- **Case Study 2.1:** Cosine Similarity (No Mean-Centering)  
- **Case Study 2.2:** Cosine Similarity (With Mean-Centering)  
- **Case Study 2.3:** Pearson Correlation Coefficient (PCC) with Mean-Centering  

**Key Insights:**  
- Item-based CF followed similar trends to user-based CF.  
- Mean-centering and **DF** significantly improved the identification of top-N similar items and rating predictions.  

### Overall Comparison  
- Both **user-based** and **item-based** CF benefited from:  
  - **Mean-Centering:** To adjust for rating biases.  
  - **Discount Factor (DF):** To emphasize significant neighbors/items.  
- PCC outperformed cosine similarity in most cases due to its sensitivity to rating correlations.  

---

## Conclusion  

Through this assignment, we explored the following:  
- Adjusting ratings to a **1-to-5 scale**.  
- Introducing missing values to represent real-world data sparsity.  
- Comparing similarity measures (**Cosine** and **PCC**) with and without mean-centering.  
- Applying a **Discount Factor (DF)** to refine top-N neighbors and items.  

**Key Takeaways:**  
- Mean-centering and PCC improved the robustness of similarity measures.  
- DF ensured that only significant neighbors/items influenced the predictions.  
- These adjustments enhanced the overall accuracy and reliability of both user-based and item-based recommendations.  

---

## Files in This Repository  

- **Dataset:** Pre-processed dataset used for this assignment.  
- **Code:** Python implementation for user-based and item-based collaborative filtering.  
- **Report:** Detailed analysis and findings of the assignment.  
- **Plagiarism Report:** Ensures academic integrity.  

---

## Instructions for Use  

1. Clone this repository:  
   ```bash
   git clone https://github.com/<YourGitHubUsername>/<RepoName>.git
