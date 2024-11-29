x<-c(141,134,178,156,108,116,119,143,162,130)
y<-c(62,85,56,21,47,17,76,92,62,58)
#Applying  the LM() function
relationship_model<-lm(y~x)
#printing the coefficient
print(relationship_model)
#getting summary of Relationship Model
print(summary(relationship_model))
#giving a name to chart file
png(file="sanjay.png")
#plotting the chart 
plot(y,x,col="blue",
     main="Height and weight regression",
     abline(lm(x~y)),cex=1.3,pch=16,
     xlab="weight in kg",ylab="Height in cm")
#saving file
dev.off()

