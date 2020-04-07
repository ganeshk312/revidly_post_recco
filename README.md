# revidly_post_recco
The dataset contains 301 users having id 0 to 300 and 1001 posts with id 0 to 1000. 12000 rows of random data generated using minitab software. 	
The features used here with weightage are as follows.	
	
vote	1 for upvote, -1 for downvote, 0 for no vote, weightage is 0.5, which is maximum of all features

time spent	for the dataset I have used randomly from 0 to 300 sec. Weightage for time is 0.3 because it will depend on the length of post. Some good post may be small, so less weightage

number of times shared	post with better revies will be shared more. So have  a weightage of 0.1 because many persons don't prefer sharing.

number of views	most viewed post will be prefered more . But still have a less weightage of 0.1 because it will depend on how well the new person will like it.
	
so the final__score for each post is calculate as 
(items['vote'] * 0.5 ) + (items['time_scaled'] *0.3) +(items['share']*0.1/50)+(items['n_views']*0.1/500)	
	
the sheet 'train' have all the data	

the sheet 'pred_output' contains the post_id to be suggetsted to the user . 	

the number of post to be suggested can be varied by the variable 'n_post'  in cell 19 in the jupyter notebook. As of now n_post=20	

eg, user 0 has the post 552 as top ranked and 62 next	
