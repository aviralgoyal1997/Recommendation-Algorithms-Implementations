# Recommendation-Algorithms-Implementations
<h3>Code Implentation of various approaches for making recommendation engine</h3><br>
<b>References</b> : <br>
 <href>https://datasciencebasicsblog.wordpress.com/2018/04/27/recommendation-system/</href><br>
 <href>https://drive.google.com/open?id=1KHmtJuL-357Ff7svozg_EC7mLj67-1rr</href><br>
 <href>https://drive.google.com/open?id=1F1zMHVjjKqDRSmfoOiUapkVKViDfM6Kr</href><br>
 
Because of size issues could not upload code with outputs run so you can see outputs in code here : <br>
<href>https://drive.google.com/open?id=1ycG_NYX3NtALW7cI6NQ7MyBHz64c6izp</href>

<h3>Making hybrid content based recommendation system</h3>
While making content based recommender approach will be mostly same but now similarity for users and items will not be calculated using their rating but using their own featurs like genres for items and gender or other for users.After this when we have similarity matrix for both users and items we gonna use same approach as before to calculate rating but little changes as now there will be two ratings one from item similarity matrics and one from user similarity matric so we need touse both of them to get one final rating for an item.<br>
<b>Combining user based and item based ratings to get one rating</b><br>


if (user_pred_cosine != 0 and user_pred_cosine != 5) and (item_pred_cosine != 0 and item_pred_cosine != 5):
				   pred_cosine = (user_pred_cosine + item_pred_cosine)/2
else:
				   if (user_pred_cosine == 0 or user_pred_cosine == 5):
					       if (item_pred_cosine != 0 and item_pred_cosine != 5):
						          pred_cosine = item_pred_cosine
					       else:
						          pred_cosine = 3.0
			   	   else:
					       if (user_pred_cosine != 0 and user_pred_cosine != 5):
						         pred_cosine = user_pred_cosine
					       else:
                                                   pred_cosine = 3.0
