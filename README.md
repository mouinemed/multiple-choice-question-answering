## License

This project is licensed under the [Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International License](LICENSE.txt).
# multiple-choice-question-answering
NLP challenge with Coveo
# Exploratory Data Analysis and Fine-Tuning BERT Model for Multiple-Choice Question-Answering

## Introduction

In this report, we present our exploration of a multiple-choice question-answering task using the Coveo dataset and our approach to fine-tuning a BERT-based model for improved performance. We will cover the process of Exploratory Data Analysis (EDA), our modeling approach, the evaluation of the model's performance, explanations of key design choices, and a discussion of potential future work. It is essential to note that due to time constraints, we were limited to a maximum of 10 hours for this task.

## Exploratory Data Analysis

During the Exploratory Data Analysis phase, we began by loading the Coveo dataset, which contains a variety of passages with [BLANK] placeholders and candidate word choices. We identified the distribution of different word choices and their frequencies, which informed us about potential class imbalances. The dataset was preprocessed to handle missing values, and we observed that approximately 15% of the dataset's samples were missing candidate word choices. For the majority of the questions, only 4 candidate choices were available, making it a challenging multiple-choice task.

## Modeling Approach

For the multiple-choice question-answering task, we chose a BERT-based model due to its strong performance on natural language processing tasks. The model was pre-trained on a large corpus of text data and then fine-tuned using the Coveo dataset to make it more task-specific.

Due to the time constraint, we limited our fine-tuning process to 10 hours. We split the dataset into train, validation, and test sets and fine-tuned the BERT model using the Coveo dataset during this time frame. The use of early stopping during training ensured that the model was saved at the point of the highest validation accuracy, preventing overfitting.

## Performance Evaluation of the Model

We evaluated the initial performance of the pre-trained BERT model on the Coveo dataset to establish a baseline. The initial accuracy was approximately 14.60% to 24.10%, indicating that the out-of-the-box model was not suitable for the specific task.

Next, we embarked on the fine-tuning process, and within the limited 10-hour window, we observed substantial improvements in the model's performance. After two epochs of training, the accuracy reached 88.38% on the validation set, showcasing the potential of the BERT model for this task.

## Explanation of Design Choices

Given the time constraint, we had to make informed design choices to maximize the effectiveness of the fine-tuning process. We handled missing values in the dataset by considering only the first four candidate word choices, as they contained no NaN values. This ensured that the model was trained on meaningful data and improved convergence during training.

Additionally, we used a dynamic data collator to handle multiple-choice inputs during training. The data collator allowed us to efficiently pad the input data for the model, making it more memory-efficient and speeding up the training process.

## Discussion of Future Work

While achieving an accuracy of 88.38% is promising, it is essential to acknowledge that more time could be devoted to enhancing the model further. Given the time limitation of 10 hours, the size of the dataset used for training was restricted. Therefore, one avenue for future work is to explore larger datasets, which may enable the model to capture more diverse patterns and improve generalization.

Moreover, conducting a deeper analysis of class imbalances and evaluating the impact of different evaluation metrics could lead to insights into model performance and potential areas of bias.



## Conclusion

In this report, we explored the Coveo dataset through EDA and fine-tuned a BERT-based model for the multiple-choice question-answering task. Despite being constrained by a maximum of 10 hours for this task, the fine-tuned model achieved significant improvements in accuracy, reaching 88.38% on the validation set. Key design choices, such as handling missing values and using a dynamic data collator, contributed to the model's performance.

Future work involves exploring larger datasets, conducting a more comprehensive analysis of model biases, and dedicating more time to fine-tuning and evaluating the model. By iteratively refining the model, we aim to develop a robust and accurate solution for the multiple-choice question-answering task in Coveo's domain.

In summary, the combination of exploratory data analysis, fine-tuning a BERT-based model, and potential future enhancements pave the way for creating a more powerful and task-specific natural language processing solution, despite the time constraints imposed on this task.

*Note: Due to the time constraints of 10 hours for this task, our approach and results may be further optimized and improved with additional time and resources.*
