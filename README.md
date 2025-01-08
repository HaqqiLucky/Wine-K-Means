Explanation

first of all i wanna know all the data types, in order there are object type, because the data is completely number. i used df.info and there is no broken data

after that i normalize the data first, this is for make the data become same in scale. k-means are sensitive, if one dimension has big value but others arent it will make k-means arent correct... idk how to explain it but we have to make all data into one scale.. in this jupyter i used Min-Max Scaling so i turn all the data into 1 or 0, the module is StandardScaler

after all the data has been scaleable now i need to find how much group/cluster that can be grouped, i use Elbox Method to check one by one start from cluster 0 to 10, we gonna watch the wcss (the circle go down), and as you can see the wcss just jump down sharply until cluster number 3 from cluster number 1, after that the wcss go down slowly.. why go down slowly? it because the changes give less separation data/ different data. so i can conclude that i got 3 cluster here because it go down sharply which means the differents bettween wcss are big

after got the cluster now start to clustering them with kmeans, in kmeans parameters you will see n_clusters = 3 which means the cluster are 3, then init='k-means++' means firsr posisiton/ centroid, max iter means interation so how many iteration the algorithm is. after that show the visualization using pca and scatter

that all after that we move into evaluate, different with supervised because it hasnt have variabel target, so we gonna evaluate the compactness, the seperation, and interprebality, the compactness method is siloutte score, then about the separation we can use Davies Boulden Index and Calinski, if you want to see the data of clustering with table then use groupby and use mean/median to show it

And after that we move to analysis, here i use  histplot to see how many data are inside the cluster / frequency, we can see cluster 1 have the biggest frequency of alchohol, then cluster 2 and 1. after that i use boxplot to see the alchocol content and if we see tha graph we gonna see cluster num 2 has the biggest value of alcohol, and then continue with number 1 and 0

conclusion:
if you seeking low alchocol you can choose the cluster 0, its also have many stock
if you seek the highest content of alchohol then cluster 2 gonna suitable, but the stock are lower than cluster 0 but higher than cluster 1
but if you want to keep your body health just dont drink wine

thats all :D