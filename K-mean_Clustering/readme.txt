# Apply K-mean
newiris <- iris
newiris$Species <- NULL
(KC <- kmeans (newiris, 3) )

# compare species lable with clustering results
table (iris$Species, kc$cluster)

# Plot the clusters and centers
plot(newiris[c("Sepal.Length","Sepal.Width")],col=KC$cluster)
plot(KC$centers[c("Sepal.Length","Sepal.Width")], col=1:3,pch=8,cex=2)