# Details on the method of calculs

To calculate the proportions of each wine needed to create the desired formula, we can use the input formula provided by the client (e.g., 1.2%wine1+2.7%wine2+etc.). We can parse this formula to extract the percentage of each wine and store it in a list or array.

Next, we can normalize the percentages so that they add up to 1. This step ensures that we have a valid probability distribution that can be used to create the wine blends. To normalize the percentages, we can simply divide each percentage by the sum of all percentages.

Once we have the normalized percentages, we can create a vector of wine blends in K dimensional space. Each wine can be represented as a point in K dimensional space, where K is the number of attributes or characteristics that we want to consider (e.g., aroma, flavor, color, acidity, body, etc.). The attributes can be represented as axes in the K dimensional space, and the wines can be plotted as points based on their values for each attribute.

To calculate the wine blends, we can use the normalized percentages as weights and compute the weighted average of the wine vectors. The resulting vector represents the ideal blend that satisfies the desired formula.

To ensure that the resulting blend is as close to the input formula as possible, we can use the Euclidean distance as a measure of similarity. The Euclidean distance is a mathematical concept that measures the distance between two points in K dimensional space. We can calculate the Euclidean distance between the ideal blend vector and the vector that corresponds to the input formula, and minimize this distance by adjusting the weights of the wine vectors. This optimization process can be achieved using techniques such as gradient descent or genetic algorithms.
