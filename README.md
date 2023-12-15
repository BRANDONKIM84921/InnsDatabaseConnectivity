# InnsDatabaseConnectivity

This project was done individually by me, Brandon Kim. I'm assuming I don't need to submit my github log as everything was done by me without the need of a collaborative environment like github.

This project functions via a notebook interface, with each functional requirement implemented in a single code chunk. Each requirement can be ran by running the labeled code chunk. The user interface is self explanatory, with each user input coming along sequentially. Aside from FR2, every FR that outputs a data set will be in the form of a pandas dataframe. 

Notes on specifities of functional requirements:

1. FR1:
  - With the test data, the output will have NA values in the "Most Recent Stay" columns. This is because the test data does not include any prior reservations before the current date (as of the submission). If prior reservations were added, these values will be reflected accordingly.

2. FR2:
  - Newly inserted reservations will have the reservation code of 1 + the highest reservation code in our data.
  - Similarity is determined by other rooms that are available in the same date range and have the same maximum occupancy. Will only return first 5 rooms ordered alphabetically by room code.

3. FR3:
  - Built in a check option to see if the cancelled reservation code even exists in the dataset to begin with. If it doesn't, a message will appear indicating that no reservations were actually deleted.

4. FR5:
  - Similar to FR1, the amount of 0's is due to the small test data. If more data was added, these values will be reflected accordingly.
