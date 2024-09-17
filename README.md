
# News Dataset Text Preprocessing Experiment

This project investigates the impact of different text preprocessing techniques on the fine-tuning of a RoBERTa model for a news dataset. We conduct an experiment to compare two preprocessing approaches and analyze their effectiveness.

## Experiment Setup

* **Original Dataset:** [News Category Dataset](https://www.kaggle.com/datasets/rmisra/news-category-dataset/code)
*  **Sub-dataset Creation:** 18,981 items were randomly selected from the original dataset in a stratified manner to ensure proportional representation of different news categories.
* **Preprocessing Techniques:**
	 -   **Dataset 1:** Removal of numbers, stop words, and punctuation.
	-   **Dataset 2:** Removal of numbers, stop words, and punctuation, plus stop words removing.
* **Models:**
    * Two Roberta models were fine-tuned, each on one of the preprocessed datasets.
    * A final model was trained based on results of the 2 model.

## Project Structure

* `experiments/`
    * Contains 4 Jupyter notebooks detailing the experimental process:
	    -   `data-preprocessing-nostopwords-vs-stopwords.ipynb`: Creation of the two experimental datasets, one with and one without stop words.
		-   `roberta-fine-tuning-stopwords.ipynb`: Fine-tuning of the Roberta model on the  dataset with stop words.
		-   `roberta-fine-tuning-nostopwords.ipynb`: Fine-tuning of the Roberta model on the dataset without stop words.
		- `dataset-preprocessing.ipynb`: Processes the entire dataset based on the insights gained from the fine-tuning experiments.
 * `news-classification-big-dataset.ipynb`: Trains and evaluates the final model on the full dataset using the best preprocessing technique identified in the experiments.
* `README.md`

## Experimental Results and Analysis

* Compare the performance of the two fine-tuned models.
* Discuss which preprocessing technique proved more effective.
* Explain the rationale behind the final model training.
