Essentially in this code we wanted to take microarray data and be able to turn it into more 
readable and usable information that the general population could understand. 

The overall framework of this program includes:
1. Loading in the microarray data and confirting it into red, green and blue as an array. This was done
so that we have a way to distinctly quantify the expressions.

2. From there the cell size was assessed in order to determine how exactly we would partition the groupings.
  
3. We created a blank image of the cells to begin to compare how many different cells would exist. This was
particularly important because not all cells exhibit any pixels.

4. The circles are than overlaid to match the image of the microarray provided. You can
visually confirm that this is correct by showing the plot.
<img width="512" alt="Screenshot 2024-11-26 at 2 30 58 PM" src="https://github.com/user-attachments/assets/056f07fd-a01b-44d7-86e0-2dcfe4392820">

5. From there, we calculated the average color in each circle this will help us to understand
what expression rate is present.

6. For each circle created, we stored both the poition and the RBG values to create a dataframe with.

7. Then the corresponding color was added to the corresponding circle on the blank cells. This helped
to simplify the overall expression and create an image of such.

8. Then a new image was created with the averaged colors of each cell. Any cells that were black or did not
show any expression at all whatsoever were minimized to be black.

9. Then each of the colors red and green were saved as a tiff file to isolate the values. Each
of these intensities was added to a dataframe to store.
<img width="537" alt="Screenshot 2024-11-26 at 2 31 23 PM" src="https://github.com/user-attachments/assets/07dbb19b-d439-44bb-82a5-a53b97572cd2">

10. Because each cell represents a gene, we added the correlating gene to the dataframe to begin to associate
genes with expressions other than being just values.

11. From there we plotted red and green intensities to overall determine what would be an appropriate threshold
for our heat map so that we can leave out the wells with no binding.
<img width="552" alt="Screenshot 2024-11-26 at 2 30 24 PM" src="https://github.com/user-attachments/assets/386cae00-f9f5-4539-a040-6a1a5196d510">

12. Based on threshold values we created a dataframe with those thresholds that we determined in step 11.
Then, we created a heat map based on this.

This is a screenshot of overall results. 
<img width="514" alt="Screenshot 2024-11-26 at 2 29 48 PM" src="https://github.com/user-attachments/assets/46f775f6-353d-427e-8aac-556b7cab0b85">
