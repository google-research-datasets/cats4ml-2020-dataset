# cats4ml-dataset
This dataset is a result of the CATS4ML (Crowdsourcing Adverse Test Sets for Machine Learning) <a href="https://cats4ml.humancomputation.com/">Data Challenge</a> - an adversarial test-set sampling images and labels from the <a href="https://opensource.google/projects/open-images-dataset">Open Images Dataset</a> for state-of-the-art image classification models. The challenge invited participants to sample this publicly available dataset for images that are incorrectly classified by image classification models. In this github repository we currently publish a random sample of 60% (n=7500) of the data (stratified by labels). This will allow us to use the held out 40% data as the test to ensure overfitting for the subsequent challenge. After the next data challenge is completed, we will release the held out data to the same github repository.

We are releasing the dataset under Creative Commons Attribution 4.0 International License. Users will be allowed to modify and repost it, and we encourage them to analyze and publish research based on the data.

# cats4ml challenge
CATS4ML challenge implemented a human-in-the-loop submission-verification-scoring workflow similar to the Find-Fix-Verify approach to Crowdsourcing introduced in 
<a href="https://dl.acm.org/doi/10.1145/1866029.1866078">Soylent: a word processor with a crowd inside</a> (Bernstein et al, 2010). It was announced at the AAAI HCOMP2020 conference and was intended as a proof-of-concept of the adversarial sampling approach of existing benchmark datasets. The challenge ran for three months (Jan-April 2021). It attracted 2,000 unique website visitors, 70 registered users and 10 active participants from both industry (n=2) and academia (n=8) from around the world, e.g. Japan (n=1), Australia (n=2), US (n=4), India (n=2), The Netherlands (n=1). This resulted in more than 14000 submissions, where more than half of the participants each submitted about 2000 image-label pairs. Less than 500 image-label pairs were erroneous (e.g. image IDs and label IDs submitted were not from the target sources) and almost all of them were submitted by just one participant. About 1800 submissions were duplicates - submitted either by more than one participant, or submitted more than once by the same participant. However, this relatively high overall number of duplicates was contributed by just one participant. All this points to the efficacy of challenge rules to stimulate unique submissions. Half of the valid submissions were deemed to be adverse, i.e. scored, and more than 80% of them are false negative (i.e. the participants discovered images which were missed by the classifiers). False negatives have higher value, in general, as they are quite difficult to acquire through automatic methods.

The main components of the challenge workflow engage three groups of actors Finders, Verifiers and Machines, who all work with a target dataset (<a href="https://opensource.google/projects/open-images-dataset">Open Images Dataset</a>) and a set of target labels (a subset of 23 label classes sampled from the all 30K classes in the Open Images Dataset). The target labels were selected to scope the challenge and in the following five sections we provide details on the data, actors, verification and scoring components of the challenge. These labels represent a set of object classes (n=7), event classes (n=3), professions and roles classes (n=9), abstract concept classes (n=3) and sports (n=1). 
 
The paper accompaning this dataset reports on the results of the entire set of 14000 submissions to the challenge. 

blog post:<a href="https://ai.googleblog.com/2021/02/uncovering-unknown-unknowns-in-machine.html">Uncovering Unknown Unknowns in Machine Learning (2021). Lora Aroyo and Praveen Paritosh, Research Scientists, Google Research</a>
paper: <a href="https://arxiv.org/abs/2306.15777">"Is a picture of a bird a bird": Policy recommendations for dealing with ambiguity in machine vision models (2023). Alicia Parrish, Sarah Laszlo, Lora Aroyo, Google Research </a>
challenge website: <a href="https://cats4ml.humancomputation.com/">https://cats4ml.humancomputation.com/</a>
