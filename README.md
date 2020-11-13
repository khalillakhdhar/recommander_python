
For Windows use:

    http://www.lfd.uci.edu/~gohlke/pythonlibs/

# Installation

Case Recommender can be installed using pip:

    $ pip install caserecommender

If you want to run the latest version of the code, you can install from git:

    $ pip install -U git+git://github.com/caserec/CaseRecommender.git

# Quick Start and Guide

For more information about RiVal and the documentation, visit the Case Recommender [Wiki](https://github.com/caserec/CaseRecommender/wiki). If you have not used Case Recommender before, do check out the Getting Started guide.

# Usage

Divide Database (Fold Cross Validation)

    >> from caserec.utils.split_database import SplitDatabase
    >> SplitDatabase(input_file=dataset, dir_folds=dir_path, n_splits=10).k_fold_cross_validation()

Run Item Recommendation Algorithm (E.g: ItemKNN)

    >> from caserec.recommenders.item_recommendation.itemknn import ItemKNN
    >> ItemKNN(train_file, test_file).compute()

Run Rating Prediction Algorithm (E.g: ItemKNN)

    >> from caserec.recommenders.rating_prediction.itemknn import ItemKNN
    >> ItemKNN(train_file, test_file).compute()

Evaluate Ranking (Prec@N, Recall@N, NDCG@, Map@N and Map Total)

    >> from caserec.evaluation.item_recommendation import ItemRecommendationEvaluation
    >> ItemRecommendationEvaluation().evaluate_with_files(predictions_file, test_file)

Evaluate Ranking (MAE and RMSE)

    >> from caserec.evaluation.rating_prediction import RatingPredictionEvaluation
    >> RatingPredictionEvaluation().evaluate_with_files(predictions_file, test_file)
