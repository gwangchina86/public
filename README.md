# Appeal for Usenix Security 2017

Dear PC Chairs,

Paper information: Paper #235 "A Novel Secure Fault-Tolerant Sensor Fusion using Interval Intersection"

We first would like to give many thinks for the reviewers’ efforts and commends.  However, we still want to provide an appeal to the PC Chairs and provide the disagreement. 

1.	The reviewers did not catch the main contribution of our paper. Also, the reviewers were not familiar with our topic, since both reviewers had only ‘some familiarity’.
2.	The main contribution of our paper is that it provides a method for security in a Fault-Tolerant Sensor fusion system. This is the first work to combine security and the Fault-Tolerant Sensor Fusion System. The first thing we should know, Security is very different from Reliability and Trustworthiness, etc.  Another major contribution is that our method uses a secure machine learning-based (linear-regression model) method to evaluate the evaluation processes which can yield a more accurate result, also keeping all the information secure. 
3.	We will provide the detailed disagreements about the reviewer 1 and reviewer 2 in the following. The reviewers may have misunderstood the main contribution and focused more on less important issues, such as related work, etc.

Review 1:

===Paper Summary ===

Mazullo’s algorithm is indeed a mature method from 1984 (that is true), however, we cannot judge the usefulness just according to the year it was invented. For example, Newton found the gravitational constant more than 200 years ago, but we could not deny its usefulness even now.

===Comments for author ===

We don’t agree the statement that “the paper does not fit a security conference due to…”. As we all know, security has at least two research directions, one is theoretical research, such as cryptographic, and the other is security for technologies. Our paper is more focusing on the second one, which combines the security issues into the fault-tolerant sensor fusion systems.  Maybe we did not submit the right tracks of USENIX Security. But our paper is indeed focusing on security and privacy, which is one of the main goals of our paper.

Methodology:

-	“observation noises of each sensor are independent”. This idea is introduced in the first part of the paper (Introduction). It is obviously true.  For the sensor fusion process, we usually deploy the sensors in different places, each pace having a different environment. We consider the data collected under these different environments as independent. For example, if we want to measure temperature in different location, the different location will have different environments, such as sun light, humidity, or wind. That is why they will have different noises and we consider these noises are independent. If all the environments are the same, we will not need the fusion system, using only one sensor reading as the system input.
-	“The introduced “secure computation protocol” is basically an already existing solution”. Yes, I agree with this point. However, to the reviewer the most important part is to use a secure computation protocol with the fault-tolerant sensor fusion system. As we knowledge, this paper is the first one to consider both parts (security and sensor fusion) together.
-	About the Trustworthiness, yes, the trustworthiness is indeed an interesting topic for a security paper. However, it is not the main point of our paper, and is out of scope of this paper, considering the page limitation and importance of our main method.
-	About the definition of faulty sensor reads, maybe the reviewer did not get the main point of sensor fusion methods. In our case, if a sensor reading is in the valid range, we consider it as a valid reading; otherwise, we consider it a fault/wrong reading. Also, maybe the reviewer misunderstood what the sample process means. We are according to one distribution to sample, and the trends of the samples should follow that distribution.

Presentation:

-	Related work is moved to the Appendix. This is only to meet the 13-page requirement. Before we submitted this paper, I email to sec17chairs@usenix.org. It said the reviewers only could see the first 13 pages.  Email replied: “As mentioned in the CFP, the paper’s contributions should be understandable within the 13 page limit. If you have content that is included on page 14, but before the bibliography, you risk having your paper rejected without review. I’d suggest moving something to an appendix to fit back in the page limit.” So we decided to move the related work in the Appendix A. 
-	Appendix B: Yes, there is no proof presented currently.  However, if the reviewer thinks some parts need proof, we will put the necessary proof at the Appendix B. Since the paper is pretty clear, we did not put any proof here currently.
-	About the strange/vague sentences, still the main problem is that the reviewer is not familiar with our research and topic. And also, this issue is much easier in the final version. 
-	About Redundancy/repetition, no, we do not think there is redundancy or repetition, we want to provide more information for readers, so that they can have the basic main idea and understand this paper very well.
-	About the definition “a new metric”, here we should know, for different applications, we can have different metrics to evaluate efficiency and accuracy.  This new matric is for our simulation.
-	Language: Yes, there exists two mistyping once. Once accepted, we will polish more the language. 

Reviewer 2:

===Comments for author===

Yes, combining sensor fusion with secure commutation is an indeed attractive idea. About the threat model, the threat model here we defined is a little bit different from the usual threat models we used. In the threat model part of our paper, we mainly focus on the potential vulnerability, with which the secure fault-tolerant sensor fusion system may be faced. Maybe we should change the name of this subsection to avoid the potential misunderstanding for the reviewers /readers if this paper is accepted. Again, these are not usual threat models, we mainly focus on the vulnerability that sensor reading systems face. Thanks to the reviewer for correction. The threat model we will provide should be based on the secure computation, not the fusion system. In the part of 2.1 secure computation protocols, we already mentioned the thread model for SC. That is why we want to emphasize the importance of the vulnerability of the sensor fusion system, so that we can give the reviewers/readers more information about sensors’ vulnerabilities. 

Other minor comments:

-	About the claim, first, we should admit the existence of noise and unperfectness of sensors. Yes, it indeed exists. I guess the reviewer may want to say the overstatement of “prevent…on a large scale”. If each sensor was accurate, we would not need to have the sensor fusion system.  Also, the inaccurate sensor readings indeed prevent the implementation.
-	About the threat model, I partially agree with the reviewer.  As stated above, it is not the general threat model used in the security area. 
-	About the initial encryption step, as I said to the reviewer 1, this paper does not focus on the encryption parts, it mainly focuses on the implementation which means combining the secure computation into the fault-tolerant sensor fusion systems. As long as we use the secure computation protocol, the security is guaranteed in semi-honest adversary models. 
-	About the usage of the sensor’s output, the accuracy can be guaranteed by the improved Marzullo’s algorithm. How to interact with the stateful history  FSM, we use the two parameters to indicate them, one is current_state and the other is next_state, also the state is updated for each following sensor readings.
-	About Pignistic probability, yes, we should provide more details about the pignistic probability.
-	About Appendixes, please refer the appeal for reviewer 1.

------------------------------------------------------------
In summary:

First, we would like to thank the reviewers for their efforts and contributions.  However, we do not think the reviewers understood the main ideas of our paper very well, as they had only ‘some familiarity’. The main contribution is that our paper combines secure computation into a fault-tolerant sensor fusion system, and it is the first paper so far to do this kind of work. For the sensor fusion part, we use an improved fusion algorithm based on machine learning method combined with our special evaluation processes to get more accurate results. For the security part, we use secure computation based on oblivious transfer processes to keep all computation of improved fusion algorithms secure. Also, the simulation provides a clear improvement with little overhead of garbled circuits. Also, according to the reviewers, the rejection is not because of the technique methods, it is about the structure and a misunderstanding the main contribution.  For the structure, it can be improved in the final version, and for the misunderstanding, it would be better to get some reviewers with more familiarity with both secure computation and sensor fusion.
