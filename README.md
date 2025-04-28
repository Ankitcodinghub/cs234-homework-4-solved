# cs234-homework-4-solved
**TO GET THIS SOLUTION VISIT:** [CS234 Homework 4 Solved](https://www.ankitcodinghub.com/product/cs234-hw-4-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;118628&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;2&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (2 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS234 Homework 4 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (2 votes)    </div>
    </div>
For submission instructions please refer to website For all problems, if you use an existing result from either the literature or a textbook to solve the exercise, you need to cite the source.

1 Estimation of the Warfarin Dose [60 pts]

1.1 Introduction

Commonly used approaches to prescribe the initial warfarin dosage are the pharmacogenetic algorithm developed by the IWPC (International Warfarin Pharmacogenetics Consortium), the clinical algorithm and a fixed-dose approach.

In practice a patient is typically prescribed an initial dose, the doctor then monitors how the patient responds to the dosage, and then adjusts the patient’s dosage. This interaction can proceed for several rounds before the best dosage is identified. However, it is best if the correct dosage can be initially prescribed.

This question is motivated by the challenge of Warfarin dosing, and considers a simplification of this important problem, using real data. The goal of this question is to explore the performance of multi-armed bandit algorithms to best predict the correct dosage of Warfarin for a patient without a trial-an-error procedure as typically employed.

Problem setting Let T be the number of time steps. At each time step t, a new patient arrives and we observe its individual feature vector Xt ∈ Rd: this represents the available knowledge about the patient (e.g., gender, age, …). The decision-maker (your algorithm) has access to K arms, where the arm represents the warfarin dosage to provide to the patient. For simplicity, we discretize the actions into K = 3

• Low warfarin dose: under 21mg/week

• Medium warfarin dose: 21-49 mg/week

• High warfarin dose: above 49mg/week

If the algorithm identifies the correct dosage for the patient, the reward is 0, otherwise a reward of −1 is received.

1.2 Dataset

We use a publicly available patient dataset that was collected by staff at the Pharmacogenetics and Pharmacogenomics Knowledge Base (PharmGKB) for 5700 patients who were treated with warfarin from 21 research groups spanning 9 countries and 4 continents. You can find the data in warfarin.csv and metadata containing a description of each column in metadata.xls. Features of each patient in this dataset includes, demographics (gender, race, …), background (height, weight, medical history, …), phenotypes and genotypes.

21 mg/week, medium: 21-49 mg/week and high: more than 49 mg/week, as defined in Consortium (2009) and Introduction.

The data processing is already implemented for you

1.3 Implementing Baselines [10 pts]

Please implement the following two baselines in main.py

1. Fixed-dose: This approach will assign 35mg/week (medium) dose to all patients.

2. Warfarin Clinical Dosing Algorithm: This method is a linear model based on age, height, weight, race and medications that patient is taking. You can find the exact model is section S1f of appx.pdf.

Run the fixed dosing algorithm and clinical dosing algorithm with the following command:

python main.py –run-fixed –run-clinical

You should see the total_fraction_correct to be fixed at about 0.61 for fixed dose and 0.64 for clinical dose algorithm. You can run them individually as well. Just use one of the command line arguments instead.

1.4 Implementing a Linear Upper Confidence Bandit Algorithm [15 pts]

Please implement the Disjoint Linear Upper Confidence Bound (LinUCB) algorithm from Li et al. (2010) in main.py. See Algorithm 1 from paper. Please feel free to adjust the –alpha argument, but you don’t have to. Run the LinUCB algorithm with the following command:

python main.py –run-linucb

1.5 Implementing a Linear eGreedy Bandit Algorithm [5 pts]

Is the upper confidence bound making a difference? Please implement the e-Greedy algorithm in main.py. Please feel free to adjust the –ep argument, but you don’t have to. Does eGreedy perform better or worse than Upper Confidence bound? (You do not need to include your answers here) Run the ε-greedy LinUCB with the following command:

python main.py –run-egreedy

1.6 Implementing a Thompson Sampling Algorithm [20 pts]

python main.py –run-thompson

1.7 Results [10 pts]

At this point, you should see a plot in your results folder titled “fraction_incorrect.png”. If not, run the following command to generate the plot:

python main.py

Include this plot in for this part. Please also comment on your results in a few sentences. How would you compare the algorithms? Which algorithm “did the best” based on your metric?

2 A Bayesian regret bound for Thompson sampling [40 pts]

Consider the K-armed bandit problem: there are K “arms” (actions), and we will choose one arm at ∈ [K] to pull at each time t ∈ [T], then receive a random reward rt ∼ p(r|θ,a = at). Here θ is a random variable that parameterizes the reward distribution. Its “true” value is unknown to us, but we can make probabilistic inferences about it by combining prior belief with observed reward data. We denote the expected reward for arm a (for a fixed θ) as µθ(a) := E[r|θ,a].

A policy specifies a distribution over the next arm to pull, given the observed history of interactions

Ht = (a1,r1,…,at−1,rt−1). Formally, a policy is a collection of maps ,

where Ht is the space of all possible histories at time t and ∆(A) is the set of probability distributions over A. We denote the probability of arm a under policy π at time t as πt(a|Ht).

For a fixed value of θ, the suboptimality of a policy π can be measured by the expected regret:

where the expectation is taken with respect to the arms selected, at ∼ πt(a|Ht), and rewards subsequently observed, rt ∼ p(r|θ,a = at). We use H as a shorthand for HT+1 = (a1,r1,…,aT ,rT ). Note that a∗ is random because θ is random, but for a given θ it is fixed and can be computed by a∗ = argmaxa µθ(a). (Assume for simplicity that there is one optimal action for any given θ.)

Our goal in this problem is to prove a bound on the Bayesian regret, which is the expected regret averaged over a prior distribution on θ:

BRT (π) = Eθ[RT,θ(π)]

We will analyze the Thompson sampling (or posterior sampling) algorithm, which operates by sampling from the posterior distribution of the optimal action a∗ given Ht:

πtts(a|Ht) = p(a∗ = a|Ht)

We can sample from πtts by first sampling θt ∼ p(θ|Ht) and then computing at = argmaxa µθt(a).

(a) [7 pts] Let and be lower and upper confidence bound sequences (respectively), where each Lt and Ut depends on Ht. Show that the Bayesian regret for Thompson sampling can be decomposed as

BR

This equality does not hold in general, so its proof will require using some property of πts.

(b) [8 pts] Now assume the rewards rt are bounded in [0,1] and Lt ≤ Ut. Show that

BR

where the notation I{·} refers to an indicator random variable which equals 1 if the expression inside the brackets is true and equals 0 otherwise.

Let us now impose a specific form of confidence bounds:

where µˆt(a) is the mean of rewards received playing action a before time t, and nt(a) is the number of times action a was played before time t. (If action a has never been played at time t, Lt(a) = 0 and Ut(a) = 1.)

and thus, the bound from part (b) implies

BR

(c) [5 pts] Show that

(d) [7 pts] Show that

(Hint: Bound the sum by an integral.)

(e) [8 pts] Use the previous parts to obtain

BRT (πts) ≤ 2K + 4pKT(2 + 6logT)

(f) [5 pts] Suppose the prior over θ is wildly misspecified, such that the prior probability of the true θ is extremely small or zero. What goes wrong in the regret analysis we have done above?

References

I. W. P. Consortium. Estimation of the warfarin dose with clinical and pharmacogenetic data. New England Journal of Medicine, 360(8):753–764, 2009.

L. Li, W. Chu, J. Langford, and R. E. Schapire. A contextual-bandit approach to personalized news article recommendation. In Proceedings of the 19th international conference on World wide web, pages 661–670, 2010.
