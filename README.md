# Puzzlesolverv1
Can evaluate scrambled 2x2 image and return a string of the correct sequence

What it does
The code takes input of a puzzle-like picture shuffled into four pieces and returns a string with the correct order, such as '2013 or 0132'.

How we built it
To input the data, we iterated through each folder, then through each image in the folder and append a label equal to the folder name, and then opened, resized and appended the image to the image list. After we transformed the lists to np arrays, and then split them into training_images, training_labels, test_images, test_labels. Following that we created a 4-layer sequential model with a softmax activation using the keras library. After that we compiled the model with the adam optimizer having an accuracy metric. Then we trained the model with or train test data using 5 epochs (Alt text). Finally we evaluated the model with our test data and recorded the accuracy and some accuracy/loss plots. Alt text Then we saved the model to an h5 file and inserted it into the submission code that was given to us.

Challenges we ran into
It took us a long time to import our dataset into a keras model. This is im sure due to our lack of experience. It took us a long time to fully understand importing a large dataset into google colab. Even with working code, with our colab subscription we could only train with ~1000 images from each folder. This was because when training on GPU we would exceed our RAM capacities and the runtime would crash. Unfortunately our workaround here was to buckle and purchase a monthly subscription. We never got to perform a data augmentation on our training set. This was the one area I feel we most failed. The way we set up our code made it hard to add in data augmentation, and we did not have the time to figure it out.

Accomplishments that we're proud of
Getting our data to run in an image classifier model was a huge win. Another big win was finally getting our accuracy score above 4.16%, it was a great feeling when our second epoch finally rose because that meant that it was better than randomly choosing. In that run, it ended around 50% accuracy after 3 epochs. After tweaking with the configuration of the model we were able to get our model to run at about ~76.55% accuracy.

Inspiration
We chose this project because we thought it was going to be the most fun and rewarding challenge for us. In all honesty, we had no idea what we were getting into. We thought we had an idea of how this was going to work, but now as I reflect, we couldn't have been more wrong. This was all of my team's first hackathon, more than anything we knew were not the most skilled group in the room. We all have a love for programming and wanted to learn more and see what a hackathon would be like. I am glad to say that this event helped us learn so much, and catch up to speed on what's possible right now!

What we learned
I learned that python has so many integrated libraries that you can pull from, you just have to know how to use them the right way. I better know what to look for when approaching a coding problem.

What's next for Puzzle Solver
First we would like to try and add data augmentation to the training set, so that we can see if it will increase the accuracy score. We are going to implement a version of puzzle solver that will be able to take the string output, and recompile the original picture into the correct order. We want to be able to truly show off what we accomplished at this hackathon to our friends and family, and I believe that this would be the best way to do so. In addition, we will continue to tweak the model of the puzzle solver, and see how high we can get the accuracy to be. This was an amazing 24 hour challenge, but the puzzle solver hit tip of the iceberg for us.

Built With:
keras
matplotlib
pandas
pillow
python
scikit-learn
