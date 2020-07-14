## Introduction
Depression is a common mental health disorder affecting more than 300 million people worldwide.[1] It is
one of the leading causes of disability and premature mortality preventing people from reaching their full
potential.[1,2] One in every twelve American adults aged 20 and above had depression in a given two-week
period during 2013-2016.[3] In 2017, more than 17 million adults in the United States were estimated to have
at least one major depressive episode.[4]
Depression disproportionately affects vulnerable subgroups of the population. For example, women are twice
as likely as men to have depression.[3] Lower socioeconomic status was also found to be associated with higher
rate of depression.[5] Despite the availability of successful psychological and pharmacological treatments for
moderate and severe depression,[6] an estimated 56.3% of people with depression left untreated.[7]
With a view to promoting remission, preventing relapse, and reducing emotional and financial burden of
mental health diseases, it is imperative to emphasize on early detection, intervention, and appropriate
treatment of depression.[8] An increasingly available large electronic medical records made it possible to
apply advanced analytic approach to predict a range of health conditions.[9] In some cases, machine learning
techniques may be able to outperform conventional discourse of clinical diagnosis and prognosis.[10,11] The
1
aim of this study was to predict depression with the available data in the US ambulatory healthcare setting
with the application of a range of machine learning techniques.
3 Data Exploration
Data Source: The data for this study was taken from the US National Ambulatory Medical Care Survey
(NAMCS). The survey collects data on a national sample of ambulatory care services in the emergency and
outpatient departments, and ambulatory surgery locations of noninstitutional general and short-stay hospitals.
The details of the survey have been documented elsewhere.[12]
For the purpose of this study, the 2014 cycle of the survey was used because this was the first (and the
largest) NAMCS survey with all the required variables, especially the comorbidities and risk behaviours
postulated to be associated with depression.
Outcome variable: The outcome variable, depression, was based on the survey question whether, regardless
of other diagnoses elsewhere recorded, the participants currently had depression at that time. In this survey,
depression “includes affective disorders and major depressive disorders, such as episodes of depressive reaction,
psychogenic depression, and reactive depression.”[12]
Predictors (features): To make the prediction models clinically relevant, the predictors were selected on
previous literature.[1-8] The predictors considered in the models include:
• Demographic variables:
– Patient’s age: Since age was available as both numeric and categorical, an exploratory logistic
regression analysis was conducted with depression as the outcome variable. The model with age as
a categorical variable had lower AIC (Akaike Information Criteria), and so it was later used in all
the analysis.
* Sex: Male and female.
* Race: White, Black, and Other.
* Body-mass index (BMI): Classified as Underweight (BMI <18.5), normal weight (BMI: 18.5-
24.9), overweight and obesity (BMI: 25 and above), and missing or unknown. Insurance type:
Private insurance, Medicare, Medicaid, Other, and Unknown or missing Geographic region in USA:
Northeast, Midwest, South, and West
• Risk behaviours
– Tobacco use: Never, Former, Current, Unknown or missing.
– Substance abuse: Yes/no.
– Alcohol misuse, abuse or dependence: Yes/no.
– History of medication use: Number of medications used.
• Comorbidities (whether the patient currently had):
– Alzheimer’s disease
– Arthritis
– Asthma
– Depression
– Cancer
– Cerebrovascular disease
– Chronic kidney disease
– Chronic obstructive pulmonary disease
– Congestive heart failure
– Coronary artery disease
– Diabetes mellitus Type 1
– Diabetes mellitus Type 2
2
– End-stage renal disease
– Pulmonary embolism or deep vein thrombosis
– HIV infection
– Hyperlipidemia
– Hypertension
– Obstructive sleep apnea
– Osteoporosis

## References
[1] Patel V, Chisholm D, Parikh R, et al. Addressing the burden of mental, neurological, and substance use
disorders: key messages from Disease Control Priorities. The Lancet. 2016;387(10028):1672-85.
[2] Herrman H, Kieling C, McGorry P, et al. Reducing the global burden of depression: a Lancet–World
Psychiatric Association Commission. The Lancet. 2019;393(10189):e42-3.
[3] Brody DJ, Pratt LA, Hughes JP. Prevalence of Depression Among Adults Aged 20 and Over: United
States, 2013-2016. NCHS Data Brief. 2018;(303):1-8.
15
[4] National Institute of Mental Health. Major depression. February 2019. URL: https://www.nimh.nih.gov
/health/statistics/major-depression.shtml
[5] Freeman A, Tyrovolas S, Koyanagi A, et al. The role of socio-economic status in depression: results from
the COURAGE (aging survey in Europe). BMC Public Health. 2016;16(1):1098.
[6] World Health Organization. Depression: Key Facts. December 4, 2019. URL: https://www.who.int/newsroom/
fact-sheets/detail/depression
[7] Kohn R, Saxena S, Levav I, Saraceno B. The treatment gap in mental health care. Bulletin of the World
Health Organization. 2004;82(11):858–66.
[8] Halfin A. Depression: the benefits of early and appropriate treatment. American Journal of Managed
Care. 2007;13(4 Suppl):S92-7.
[9] Chen JH, Asch SM. Machine learning and prediction in medicine—beyond the peak of inflated expectations.
New England Journal of Medicine. 2017;376(26):2507.
[10] Obermeyer Z, Emanuel EJ. Predicting the future—big data, machine learning, and clinical medicine.
New England Journal of Medicine. 2016;375(13):1216.
[11] McKinney, S.M., Sieniek, M., Godbole, V. et al. International evaluation of an AI system for breast
cancer screening. Nature. 2020;577:89–94.
[12] National Health Care Surveys Registry. 2014 NAMCS MICRO-DATA FILE DOCUMENTATION. URL:
ftp://ftp.cdc.gov/pub/Health_Statistics/NCHS/Dataset_Documentation/NAMCS/doc2014.pdf.
[13] Ladapo JA, Larochelle MR, Chen A, et al. Physician prescribing of opioids to patients at increased risk
of overdose from benzodiazepine use in the United States. JAMA psychiatry. 2018;75(6):623-30.
[14] Fluss R, Faraggi D, Reiser B. Estimation of the Youden Index and its associated cutoff point. Biometrical
Journal: Journal of Mathematical Methods in Biosciences. 2005;47(4):458-72.
