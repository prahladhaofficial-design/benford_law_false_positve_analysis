# Technical Notes


Programming Project - 1
E
Instructions
1. The project version deadline on 9 February 25 is firm, i.e. no extensions will be permitted.
2. Submitting late will cost you 25% penalty per day.
3. Only Jupyter notebooks (.ipynb) should be submitted.
4. The code should be neatly documented. This includes proper variable names and functions. Comments
should be used effectively.
5. Avoid usage of external libraries apart from numpy, matplotlib, pandas. Usage of other libraries may lead
to a penalty.
Modules
1. False Positives
In a particular village, 70% of the population is vaccinated. A particular disease is on the rise. The
probability of a person being affected by the disease, if they are not vaccinated, is 0.80. If they are
vaccinated, the probability of being affected is 0.15.
The disease detection machine is not fully accurate:
 It correctly identifies an affected person with probability 80%.
 It correctly identifies an unaffected person with probability 75%.
You are required to simulate the situation as follows:
Each person is identified by a pair of boolean values. The first entry in the pair determining if the person
is vaccinated or not and the second entry being if the person has been affected or not.
Define the function
def generate_population(
population_size,
vaccination_coverage=0.70,
disease_prob_not_vaccinated=0.80,
disease_prob_vaccinated=0.15
):
The function generate_population should return a numpy array of dimension N  2, where each row
corresponds to a person. The first entry of each row indicates whether the person is vaccinated (1 if
vaccinated, 0 if not) and the second entry indicates whether the person is affected by the disease (1 if
affected, 0 if not).
Each person then has to be classified into two different arrays based on whether they were detected by the
machine as affected or not.
In order to do so, pass the population through a function called
disease_checker(
population,
prob_detect_affected = 0.8,
prob_detect_unaffected = 0.75
):
1


that returns two lists called detected_affected and detected_unaffected which contain the indices of
people who have been identified as affected or unaffected by the machine based on the probabilities.
Note: You could also modify this function according to the subpart that you are currently
working on. (For example, you could create two lists called detected_affected and
detected_unaffected which contain 1s and 0s based on whether the person has been
vaccinated or not)
After all this has been done, find out the following:
(a) Find the probability that a person who has been identified as affected is vaccinated.
(b) Find the probability that a person who has been identified as not affected is not vaccinated.
(c) Find the probability that a person who has been identified as not affected has actually been affected.
(d) Find the probability that a person who has been identified as affected has not been affected.
(e) Find the probability that a person who has been identified as affected is actually affected.
2. Benford's Law
Benford's Law is a fascinating mathematical phenomenon that reveals an unexpected pattern in numbers:
in many real-world datasets, the first digit is more likely to be 1 than 9! Instead of being evenly distributed,
smaller digits appear more frequently at the start of numbers.
Refer to the following video.
The theoretical probability of a leading digit d according to Benford's Law is:
(cid:18) (cid:19)
1
P(d) = log 1 +
10 d
Your task is to demonstrate Benford's law using the Country population dataset provided to you.
 For each population value (across all years), extract the first nonzero digit.
 Count how often each digit (1-9) appears as the first digit and calculate the relative frequencies.
 Plot them using Matplotlib for each year seperately.
 Plot the Benford's proposed PMF on the same plot comparing your observed first-digit frequencies
against the expected Benford distribution.
Dataset: world_population.csv
Figure 1: Country - Population Dataset
2
