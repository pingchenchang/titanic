This is a data set from kaggle - Titanic Machine Learning from Disaster.
I tried to use random forest, Support Vector Machine, K-Nearest Neighbor and CNN to predict which Model will have the highest accuracy.

1. Data Part
    - Fill up null value
        For Age,
        I use titles to calculate avarage age. Then, fill up those empty age data depends on their title.
        
        For Cabin,
        I get the first string of cabin letter and use fare to calculater each unique cabin's mean price. Then fill up those empty cabin data by compare their fare price and avarage price.

    - Optimize data
        For Age,
        I group up every 10 age a batch. it would be more easier to see the survived precent of each group of people.

        For Sex, Embarked, Cabin
        I update those string data with integer.

        Drop off PassengerId, Age, Name, Ticket
    - Proprocessing
        Normalize the data with MinMaxScaler
2. Model Part
    - Random Forest
        n_estimators=100
        Accuracy: 0.8268156424581006

    - Support Vector Machine
        probability=True, random_state=0
        Accuracy: 0.8100558659217877

    - K-Nearest Neighbor
        n_neighbors = 13 has the highest accuracy
        Accuracy: 0.8156424581005587

    - CNN
        Layers: relu -> relu -> relu -> softmax
        Accuracy: 0.8156424581005587

