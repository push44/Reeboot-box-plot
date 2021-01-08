# Educational Resource Strategies: Multi label multi class prediction
![alt_text](https://www.erstrategies.org/assets/og_images/ers-logo-254d7736762585f10156e3b3aa37aa0cf560ffa1708f64ae6ea6fffad239d7ad.png)

# Problem description:

According to Driven Data, budgets for schools and school districts are huge, complex, and unwieldy. It's no easy task to digest where and how schools are using their resources. Education Resource Strategies is a non-profit that tackles just this task with the goal of letting districts be smarter, more strategic, and more effective in their spending. Our task is a multi-class-multi-label classification problem with the goal of attaching canonical labels to the freeform text in budget line items. These labels let ERS understand how schools are spending money and tailor their strategy recommendations to improve outcomes for students, teachers, and administrators.<br><br>

In order to compare budget or expenditure data across districts, ERS assigns every line item to certain categories in a comprehensive financial spending framework. For instance, Object_Type describes what the spending "is"—Base Salary/Compensation, Benefits, Stipends & Other Compensation, Equipment & Equipment Lease, Property Rental, and so on. Other categories describe what the spending "does," which groups of students benefit, and where the funds come from.
Once this process is complete, we can finally offer cross-district insight into a partner's finances. We might observe that a particular partner spends more on facilities and maintenance than peer districts, or staffs teaching assistants more richly. These findings are not in themselves good or bad—they depend on the context, goals, and strategy of the partner district.
<br><br>
This task (which we call financial coding) is very time and labor-intensive.

## Data description:

Data source: ![Driven Data](https://www.drivendata.org/competitions/46/box-plots-for-education-reboot/)

Feature list:
<ul>
  <li>FTE (float) - If an employee, the percentage of full-time that the employee works.</li>
  <li>Facility_or_Department - If expenditure is tied to a department/facility, that department/facility.</li>
  <li>Function_Description - A description of the function the expenditure was serving.</li>
  <li>Fund_Description - A description of the source of the funds.</li>
  <li>Job_Title_Description - If this is an employee, a description of that employee's job title.</li>
  <li>Location_Description - A description of where the funds were spent.</li>
  <li>Object_Description - A description of what the funds were used for.</li>
  <li>Position_Extra - Any extra information about the position that we have.</li>
  <li>Program_Description - A description of the program that the funds were used for.</li>
  <li>SubFund_Description - More detail on Fund_Description</li>
  <li>Sub_Object_Description - More detail on Object_Description</li>
  <li>Text_1 - Any additional text supplied by the district.</li>
  <li>Text_2 - Any additional text supplied by the district.</li>
  <li>Text_3 - Any additional text supplied by the district.</li>
  <li>Text_4 - Any additional text supplied by the district.</li>
  <li>Total (float) - The total cost of the expenditure.</li>
</ul>

Label list:
<ul>
  <li>Function:
    <ul>
      <li>Aides Compensation</li>
      <li>Career & Academic Counseling</li>
      <li>Communications</li>
      <li>Curriculum Development</li>
      <li>Data Processing & Information Services</li>
      <li>Development & Fundraising</li>
      <li>Enrichment</li>
      <li>Extended Time & Tutoring</li>
      <li>Facilities & Maintenance</li>
      <li>Facilities Planning</li>
      <li>Finance, Budget, Purchasing & Distribution</li>
      <li>Food Services</li>
      <li>Governance</li>
      <li>Human Resources</li>
      <li>Instructional Materials & Supplies</li>
      <li>Insurance</li>
      <li>Legal</li>
      <li>Library & Media</li>
      <li>NO_LABEL</li>
      <li>Other Compensation</li>
      <li>Other Non-Compensation</li>
      <li>Parent & Community Relations</li>
      <li>Physical Health & Services</li>
      <li>Professional Development</li>
      <li>Recruitment</li>
      <li>Research & Accountability</li>
      <li>School Administration</li>
      <li>School Supervision</li>
      <li>Security & Safety</li>
      <li>Social & Emotional</li>
      <li>Special Population Program Management & Support</li>
      <li>Student Assignment</li>
      <li>Student Transportation</li>
      <li>Substitute Compensation</li>
      <li>Teacher Compensation</li>
      <li>Untracked Budget Set-Aside</li>
      <li>Utilities</li>
    </ul>
  </li>
  <li>Object_Type:
    <ul>
      <li>Base Salary/Compensation</li>
      <li>Benefits</li>
      <li>Contracted Services</li>
      <li>Equipment & Equipment Lease</li>
      <li>NO_LABEL</li>
      <li>Other Compensation/Stipend</li>
      <li>Other Non-Compensation</li>
      <li>Rent/Utilities</li>
      <li>Substitute Compensation</li>
      <li>Supplies/Materials</li>
      <li>Travel & Conferences</li>
    </ul>
  </li>
  <li>Operating_Status:
    <ul>
      <li>Non-Operating</li>
      <li>Operating, Not PreK-12</li>
      <li>PreK-12 Operating</li>
    </ul>
  </li>
  <li>Position_Type:
    <ul>
      <li>(Exec) Director</li>
      <li>Area Officers</li>
      <li>Club Advisor/Coach</li>
      <li>Coordinator/Manager</li>
      <li>Custodian</li>
      <li>Guidance Counselor</li>
      <li>Instructional Coach</li>
      <li>Librarian</li>
      <li>NO_LABEL</li>
      <li>Non-Position</li>
      <li>Nurse</li>
      <li>Nurse Aide</li>
      <li>Occupational Therapist</li>
      <li>Other</li>
      <li>Physical Therapist</li>
      <li>Principal</li>
      <li>Psychologist</li>
      <li>School Monitor/Security</li>
      <li>Sec/Clerk/Other Admin</li>
      <li>Social Worker</li>
      <li>Speech Therapist</li>
      <li>Substitute</li>
      <li>TA</li>
      <li>Teacher</li>
      <li>Vice Principal</li>
    </ul>
  </li>
  <li>Pre_K:
    <ul>
      <li>NO_LABEL</li>
      <li>Non PreK</li>
      <li>PreK</li>
    </ul>
  </li>
  <li>Reporting:
    <ul>
      <li>NO_LABEL</li>
      <li>Non-School</li>
      <li>School</li>
    </ul>
  </li>
  <li>Sharing:
    <ul>
      <li>Leadership & Management</li>
      <li>NO_LABEL</li>
      <li>School Reported</li>
      <li>School on Central Budgets</li>
      <li>Shared Services</li>
    </ul>
  </li>
  <li>Student_Type:
    <ul>
      <li>Alternative</li>
      <li>At Risk</li>
      <li>ELL</li>
      <li>Gifted</li>
      <li>NO_LABEL</li>
      <li>Poverty</li>
      <li>PreK</li>
      <li>Special Education</li>
      <li>Unspecified</li>
    </ul>
  </li>
  <li>Use:
    <ul>
      <li>Business Services</li>
      <li>ISPD</li>
      <li>Instruction</li>
      <li>Leadership</li>
      <li>NO_LABEL</li>
      <li>O&M</li>
      <li>Pupil Services & Enrichment</li>
      <li>Untracked Budget Set-Aside</li>
    </ul>
  </li>
</ul>

## Files:
<ol>
  <li>Initial data preparation.ipynb: Create files train.csv, test.csv, labels.csv</li>
  <li>Create multi column text data set.ipynb: Preprocess text features to save train_multi_column_text.csv and test_multi_column_text.csv</li>
  <li>logistic base model.ipynb: Create online logistic one vs rest models for each category of labels</li>
</ol>

## Evaluation metric:

Multi-multiclass log loss = <img src="https://render.githubusercontent.com/render/math?math=\frac{1}{K} \sum^N_{n=0} \sum^C_{c=1} y_{k,c,n} log(\hat{y}_{k,c,n})">

In this calculation, K is the number of dependent variables, N is the number of rows being evaluated, and C is the number of class values k can take on. As a note, if your probabilities don't sum to 1 for each class, we will normalize them for you. The goal is to minimize multi-multiclass log loss.

## Final Model Description:

After tring many different feature engineering such as entropy features, numeric feature binning, single text vectorization, etc. finally tfidf vectorization of multiple text feature columns as given in the original data set is used. Along with these text features normalized and standardized numeric features are also used.<br>

Aftering trying for many different modeling improches simple Online Logistic Regression Classifier using sklearn's SGDClassifier which uses Stochastic Gradient Descent is used for final model approach. The reason of custom building online classifier is that Sklearn's Logistic Regression Classifier fits the model on the entire data set which makes is slower and harder to run on the large data set. Where as Stochastic Gradient Descent is easy to fit and faster on a large data sets.<br>

Early stopping is an important feature while building classifier to avoid overfitting. Using some tolerance level for iterative improvement (here 0.001) we can early model iteration.<br>

Similar to sklearn's logistic classifier parameter max_iter, max_epoch is also set to 1000 epoch iteration.<br>

Finally, before providing data to the model, all features in the entire data is stacked together using scipy sparse hstack module which makes data stacked dataframe as sparse scipy matrix. This is done because online classifier makes faster passes on the scipy sparse matrix which makes the model even faster.<br>

Instead of using pure Stochastic Gradient Descent, we use mini-batch gradient descent. On this ![link](ttps://www.kaggle.com/c/instacart-market-basket-analysis/discussion/37753) author has provided iter_minibatches function that takes in chunksize, X, y as function parameters to yield randomly selected x_chunk, y_chunk with the size of provided chunksize.<br>

Last but not the least, we run such mini-batch-logistic-regression model as one-verse-rest on every class of every label. Hence, we run such model 104 times.

## Models:

|Model description|Score|
|-----------------|-----|
|Logistic hasing vectorizer without numeric features|0.8965|
|Numeric features fill na with mean|0.8201|
|Logistic hashing vectorizer + numeric features + entropy features for each labels separate|0.7934|
|Logistic tfidf vectorizer + numeric features + entropy features|0.5952|
|Same as above with multi-text-columns|0.5582|
|Logistic multi-text tfidf + original numeric features with scaling + feature drop|0.5381|
|Same as previous model but 3 more feature drop|0.5314|

## Things that did not worked out:
<ul>
  <li>We used condesed features, meaning all the text features are collapsed into a single feature</li>
  <li>Used numeric feature binning</li>
  <li>Used target encoded features</li>
  <li>Used entropy based features</li>
  <li>Fit mini-batch model on labels instead of classes of labels.</li>
  
</ul>
