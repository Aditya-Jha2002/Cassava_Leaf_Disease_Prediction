# Cassava Leaf Disease Prediction

As the second-largest provider of carbohydrates in Africa, cassava is a key food security crop grown by smallholder farmers because it can withstand harsh conditions. At least 80% of household farms in Sub-Saharan Africa grow this starchy root, but viral diseases are major sources of poor yields. With the help of data science, it may be possible to identify common diseases so they can be treated.

Existing methods of disease detection require farmers to solicit the help of government-funded agricultural experts to visually inspect and diagnose the plants. This suffers from being labor-intensive, low-supply and costly. As an added challenge, effective solutions for farmers must perform well under significant constraints, since African farmers may only have access to mobile-quality cameras with low-bandwidth.

## Data

The dataset consists of 21,367 labeled images collected during a regular survey in Uganda. Most images were crowdsourced from farmers taking photos of their gardens, and annotated by experts at the National Crops Resources Research Institute (NaCRRI) in collaboration with the AI lab at Makerere University, Kampala. This is in a format that most realistically represents what farmers would need to diagnose in real life.

The data can be found in the folder 'input/train_images/train_images.csv"

## Labels

{0: 'Cassava Bacterial Blight (CBB)',
 1: 'Cassava Brown Streak Disease (CBSD)',
 2: 'Cassava Green Mottle (CGM)',
 3: 'Cassava Mosaic Disease (CMD)',
 4: 'Healthy'}

## Evaluation Metric

The Data distribution is very skewed:
label 0: 1087
label 1: 2189
label 2: 2386
label 3: 13158
label 4: 2577

As you can see that the label 3 has almost 13 times more samples than label 0.

Thus Accuracy is not a good metric here, We are going to Validate our model using "AUC ROC"

## Cross-Validation

We are going to use Stratified K Fold cross-validation method, because there is high class imbalance in the dataset. We are using 5 folds.

## Model

We are using CNN based model with the efficien-net-b4 architecture for the classification of the leafs.

