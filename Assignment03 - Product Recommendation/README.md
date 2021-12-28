# Product Recomment

## Dataset
A survey asking whether or not the user (students from the class) has ever purchased/used an item. We received 29 responses, and each respondent rated each item from 26 items as Yes or No.

## Top Least common items
To see how common (ever purchased by users) each item is

![image](https://user-images.githubusercontent.com/95351692/147573440-b056fa65-1dea-4ba9-88dd-59323281c2f3.png)

## Association Rules
the visualization of 1-itemset association rules (filtered by Support > 0.4 and Lift > 1)
Nodes represent items and directed edges represent rules (antecedents ➞ consequents). Edge labels annotates Lift values. Note that for 1-to-1-itemset, both directions of rules (A➞B, B➞A) have the same lift values.

![image](https://user-images.githubusercontent.com/95351692/147573620-be2482d8-38c4-47a8-85fb-d834588c254f.png)

## Collaborative Filtering - Item Similarity
By using users' ratings for each item as its feature vector, calculates cosine similarity values for each pair of items. We could recommend items based on item similarity.
Filtering the similarity using 0.65 threshold, and visualize them in graph. A node represents an item. Edge thickness and color represent cosine similarity between 2 items.

![image](https://user-images.githubusercontent.com/95351692/147573708-9846ceae-7fdc-4cea-ac2a-e7a86aa8b2ed.png)
![image](https://user-images.githubusercontent.com/95351692/147574193-33467606-aa9d-4634-a908-0fd3374c21ae.png)

