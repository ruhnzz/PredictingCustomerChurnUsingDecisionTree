# PredictingCustomerChurnUsingDecisionTree
data = {
    'CustomerID': range(1, 101),                         # 100 values
    'Age': [20, 25, 30, 35, 40, 45, 50, 55, 60, 65]*10,   # 10 values × 10 = 100
    'MonthlyCharge': [50, 60, 70, 80, 90, 100, 110, 120, 130, 140]*10,  # 100
    'CustomerServiceCalls': [1, 2, 3, 4, 0, 1, 2, 3, 4, 0]*10,          # 100
    'Churn': ['No', 'No', 'Yes', 'No', 'Yes', 'No', 'Yes', 'Yes', 'No', 'Yes']*10   # 100
}
it will 100 rows in dataset.

everything is simple go through code you will understand

tree.plot_tree(clf, filled=True, feature_names=['Age', 'MonthlyCharge', 'CustomerServiceCalls'], class_names=['No Churn', 'Churn'])

the function tree.plot_tree() comes from scikit-learn, not from matplotlib directly
clf: This is your trained decision tree classifier (usually created using DecisionTreeClassifier()).

filled=True: Fills the boxes with colors to indicate the predicted class and their purity (darker = purer nodes).

feature_names=[...]: Names of the features used for training — shown at each split in the tree.

class_names=[...]: Labels for the output classes. Without this, the tree just shows numbers like 0, 1.

diagram:
Condition: e.g., CustomerServiceCalls <= 3.5

gini: Gini impurity – a measure of node purity. Lower = better.

samples: Number of samples (rows) reaching this node.

value: [No Churn, Churn] — count of each class at that node.

class: The final predicted class at this node.


