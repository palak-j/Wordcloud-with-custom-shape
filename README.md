# Wordcloud-with-custom-shape

Wordcloud is a powerful visual representation for text data and it is very simple to make wordcloud in different shapes using 'wordcloud' library  in python. <br> 

In this python notebook (Wordcloud-using-image.ipynb), I have demonstrated how to make wordcloud in any particular shape using an image. <br>

We can make simple wordcloud where words are usually single words, and the importance of each is shown with font size or color using code mentioned here - <br>

https://www.python-graph-gallery.com/wordcloud/ <br>

But if we want wordcloud to be in specific shape, let's say we want it to be in shape of car, then we have to use an image(.jpg, .png , .jpeg) and use that as a mask for wordcloud. <br>

For example, let's say we want our wordcloud to be in the shape of a below car-
<img width="637" alt="image" src="https://user-images.githubusercontent.com/33736823/169430681-85644529-0839-4fd5-b96e-8ac58b2e8117.png">


Here, we have to mask it and load it in the form of array. <br>

mask = np.array(Image.open('car.jpg'))

Now, keep this mask as parameter to wordcoud method.

wordcloud = WordCloud(width = 7000, height = 5000, random_state=1, prefer_horizontal=1,background_color='white', contour_color='cornflowerblue', colormap='Set2', contour_width=4, collocations=True, mask=mask).generate(text)  <br>

Now, plot it: <br>

plt.imshow(wordcloud) 
plt.tight_layout(pad=0)

Our resultant wordcloud will be: <br>
<img width="737" alt="image" src="https://user-images.githubusercontent.com/33736823/169430127-144d5033-e344-47d0-9721-6816ed5b8098.png">








