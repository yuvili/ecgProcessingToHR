# ecgProcessingToHR.slx
## ECG data analysis from a given file
 ![image](https://user-images.githubusercontent.com/76939624/185109000-281477ef-5512-4602-b896-b1b026c43f9b.png)


- **Green block**: The resulting ECG data file after running `fix_data_mat` in MATLAB at the end of a simulation scenario. In this block, the column of `measurement time` and `ECG` is selected.
This data is received at 512hz.
- **Yellow block**: This block converts the data received from the file to 200hz in order to weight them for heart rate calculation and noise filtering.
- **Light-blue block**: Calculates the heart rate while filtering additional noises, and outputting the results to the scope.
-	Blue block: In case of abnormal heart rate (over 100 or under 60) the green light will turn red.

### Running the model
Given a file containing ECG data, click on the green block and update the data as follows:
![image](https://user-images.githubusercontent.com/76939624/185109103-33ba2fa5-7c0e-4422-903d-5c235b781c07.png)



## ECG real-time data analysis using G.tec
 ![image](https://user-images.githubusercontent.com/76939624/185109130-26c33262-7136-4fb6-85c6-00f6e0475949.png)


-	**Green block**: a g.tec connection receiving data in real time, this data is received at 512hz.
-	**Yellow block**: This block converts the data received from the file to 200hz in order to weight them for heart rate calculation and noise filtering.
-	**Light-blue block**: Calculates the heart rate while filtering additional noises and outputting the results to the scope.
-	**Blue block**: In the case of an abnormal heart rate (over 100 or under 60) the light will be red (as in the picture - the heart rate is 160).

### Running the model
We will click on the blue block and update the data as follows: 
![image](https://user-images.githubusercontent.com/76939624/185109153-87dca2fb-db19-4a03-921c-93cc7871a8e7.png)

The heart rate calculation time is 5 seconds, therefore a delay of 5 seconds is possible in receiving the heart rate.
