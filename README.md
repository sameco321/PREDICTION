README

This document groups the four fundamental questions of the project, these are:
        
1- how did I build my model?
2- because I make the decisions I make
3- which I think the expected error was out of the sample?
4- how do I use cross validation?
        
the headings will be named so that it is known which of the subjects I am dealing with.

alternate to this document we have an HTML document "MACHINE LEARNING PRACTICE" in which are the codes of the points that we are going to talk about in this document.

POINT 1 AND 2

EXPLANATION OF HOW I BUILT MY MODEL AND WHY I MAKE THE DECISIONS I MAKE

We all know that building a model according to what we learned in this course is asking a good question and then going out to find the data that will help us answer that question, but in this case we already have the data and it will be from that data that we will build our model so, First of all I started reading the instructions given and noticed that they told us about two important things, the first was the variable that we would use and the second was the recommendation they gave us to take into account the weight lifting data, so I noticed that of the two data sets that they gave us, the one that met the requirements of the recommendations was the pml.trainin data set, which although it was not the weightlifting data set, did have an adequate structure and a size that fit to train my model.
I tried to find some codebook that came with the dataset to understand the meaning of each of the variables well but I did not find it just general information so I decided to use two variables to predict the class and these variables were belt roll and Tone belt that correspond according to my assignment to the loss of cm at the waist and the gain in muscle tone respectively according to the type of exercise performed by the participants.

perform a correlation to determine the degree of association between the variables and I obtained a correlation of -0.22 so with that information, I continued deciding which model to use if a linear model or a prediction tree and decided to use a prediction tree in general is more easy to interpret and has a better performance, when we are presented with non-linear situations, apart from that they are perfect for carrying out cross-validation since if we do not carry it out we may be falling into over-adjustments and this would make it difficult to estimate the uncertainty, added to all this It is a perfect model to show how to cross validate.

POINT THREE
WHAT DO I THINK IS THE EXPECTED ERROR OUT OF THE SAMPLE?
        
The first thing I did was build my model and in the specifications of point one are the details of how and why I did it that way, after that what I did was define the data set that I would use and although I could have used the set of Weightlifting data like these do not have the same variables, what I did was use the data set with which I trained my model, apart from this I also define the date because as the interpretation of the variables is my way, I wanted to clarify that maybe This model is not scalable, it is a shame because obviously, by being able to perform this operation with another data set, my model would be more robust.
so to define the expected error outside the sample what I did was first train an algorithm and see the error within the sample and then apply it to the entire data set to see the error outside the sample, for this I basically thought to identify the waist width use the waist width variable so if there are more lost centimeters these people correspond to group A and if they lost fewer centimeters these correspond to other classes to know this I built a predictor to identify those groups, and after building it I applied it to the entire data set, in order to determine the out-of-sample error below we can see the results and the mean for the out-of-sample error.


POINT FOUR
HOW TO USE CROSS VALIDATION

for cross validation i decided to use k-flod method and use my training data for this process so i split my dataset into equal size sets and use three fold cross validation and apply it to test data which It is the same training data divided into three groups, check the length of the folds, then check how the folds were. for this case, in cocreo, do not check the indices corresponding to the test set or do resampling, you just want to do a complete cross-validation.