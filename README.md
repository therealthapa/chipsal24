# Shared task on Devanagari Language Understanding at  [CHIPSAL@COLING 2025](https://sites.google.com/view/chipsal/home) #

The "Shared Task on Devanagari Language Understanding" at CHIPSAL@COLING 2025 focuses on addressing key challenges in processing Devanagari-scripted languages. In multilingual contexts, accurate language identification is critical, making the first subtask, Devanagari Language Identification, essential for identifying whether a given text is in Devanagari script. Hate speech detection is another significant aspect of understanding social dynamics, especially within online spaces. Subtask B, Hate Speech Detection, aims to determine whether a given text contains hate speech, with annotated datasets marking the presence or absence of such content. Building on this, Subtask C, Targets of Hate Speech Identification, focuses on identifying specific targets of hate speech, such as individuals, organizations, or communities. This shared task facilitates comprehensive Devanagari language understanding, targeting key challenges in script identification, hate speech detection, and the identification of hate speech targets. 

## Sub-task A ##
<b> Devanagari Language Identification:</b> Participants are required to identify whether a given sentence contains hate speech. The dataset consists of monolingual sentences in Nepali and Hindi, emphasizing the need for effective detection across languages within the Devanagari script.

## Sub-task B ##
<b> Hate Speech Detection in Devanagari Language:</b> The goal of this subtask is to identify the targets of hate speech in a given hateful text. The text is annotated for "individual", "organization", and "community" targets.

## Sub-task C ##
<b> Target Identification for Hate Speech in Devanagari Language:</b> For this subtask, given a hateful sentence in Devanagari script, the objective is to identify the target of the hate speech, categorized as either "individual," "organization," or "community." This task is essential for understanding the specific nature and direction of hate speech.

## Participation ##

In order to participate in the competition, please Join our codalab competition [here](https://codalab.lisn.upsaclay.fr/competitions/20000)

**Training Data:**

| SubTask | Link |
|----------|----------|
| SubTask-A | [here](https://drive.google.com/file/d/1YAo40VKJlF2dD1xlPsWDZ4uqANSh1lrx/view?usp=drive_link) |
| SubTask-B | [here](https://drive.google.com/file/d/1stCXIF8yJkywi0VDV9iBMwLPVuG5MQy2/view?usp=drive_link) |
| SubTask-C | [here](https://drive.google.com/file/d/166k7N9KV6jEDvvAr9iLTwrWyfdEcAs5p/view?usp=sharing) |

**Eval Data:**


| SubTask | Link (index-tweet)| Link (index-label)|
|----------|----------|----------|
| SubTask-A | [here](https://drive.google.com/file/d/18SQ7JXd9tJQByUeQRYJz5CdUIJWqDoCk/view?usp=sharing) | [here](https://drive.google.com/file/d/1EaYACFTY9-LL0rux8Pl0ZxnErybpdRsC/view?usp=sharing) | 
| SubTask-B | [here](https://drive.google.com/file/d/1Scwkb6kI3CG-zzHbkWri1lcypUc68Zcz/view?usp=sharing) |[here](https://drive.google.com/file/d/15hdfMZshigvS1IpyA1bEVN6B65bZdw1g/view?usp=sharing) |
| SubTask-C | [here](https://drive.google.com/file/d/1s-iV5Qpp9--eoxqrjYhoi2LPL47W1MNw/view?usp=sharing) | [here](https://drive.google.com/file/d/1m_FXICq6PmPzO3SjTHqWuV8s-XMiRlYk/view?usp=sharing) |


**Test Data:**

Will be provided after testing phase starts.

## Dataset ## 
All the text has a unique identifier called "index". The labels for training data are given along with the dataset. For evaluation and testing, the submission format is mentioned below.

## Evaluation ## 

The results are only accepted in codalab. The submission will be evaluated with a f1-score.

The script takes one prediction file as the input. Your submission file must be a JSON file which is then zipped. We will only take the first file in the zip folder, so do not zip multiple files together. 


For subtask A, the final prediction submissions should be like the following. Make sure that your hate label is given as "1" and the non-hate label is given as "0".

<b>IMPORTANT:</b> The index in JSON should be in ascending order.
```python
{"index": 15636, "prediction": 0}
{"index": 16006, "prediction": 1}
{"index": 19818, "prediction": 0}
```

Similarly, for subtask B, the final prediction submissions should be like the following. Make sure that your individual, organization, and community labels are given as "1", "2", and "3" respectively.

<b>IMPORTANT:</b> The index in JSON should be in ascending order.
```python
{"index": 13943, "prediction": 1}
{"index": 15708, "prediction": 3}
{"index": 16692, "prediction": 2}
```


Similarly, for the subtask C, the final prediction submissions should be like the following. Make sure that your support, oppose, and neutral labels are given as "1", "2", and "3" respectively.

<b>IMPORTANT:</b> The index in JSON should be in ascending order.
```python
{"index": 10433, "prediction": 1}
{"index": 18276, "prediction": 3}
{"index": 20346, "prediction": 2}
```

## Publication ##
Participants in the Shared Task are expected to submit a paper to the workshop. Submitting a paper is not mandatory for participating in the Shared Task. Papers must follow the COLING 2024 workshop submission instructions for short papers and will undergo regular peer review. Their acceptance will not depend on the results obtained in the shared task but on the quality of the paper. Authors of accepted papers will be informed about the evaluation results of their systems prior to the paper submission deadline (see the important dates). All the accepted papers will be published in ACL Anthology.

## Invitation for Special Issue ##
Top-performing teams and best models will be invited for a special issue in journals (T.B.D.).

## Timeline of the Events ##
<ul>

<li>Training & Evaluation data available: August 19, 2024 </li>

<li>Test data available: September 27, 2024 </li>

<li>Testing Phase start: September 27, 2024 </li>

<li>Test end: October 17, 2024 </li>

<li>System Description Paper submissions due: November 3, 2024 </li>

<li>Notification to authors after review: November 29, 2024 </li>

<li>Camera ready: December 13, 2024 </li>

<li>CHIPSAL Workshop: January 19, 2024 </li>
</ul>

## Organizers ##
<ul>
<li> Surendrabikram Thapa (Virginia Tech, USA) </li>
<li> Kritesh Rauniyar (Delhi Technological University, India) </li>
<li> Farhan Ahmad Jafri (Jamia Millia Islamia, India) </li>
<li> Surabhi Adhikari (Columbia University, USA) </li>
<li> Bal Krishna Bal (Kathmandu University, Nepal) </li>
<li> Usman Naseem (James Cook University, Australia) </li>
</ul>

## Contact ##
If there are any questions related to the competition, please contact rauniyark11@gmail.com

## References ##
Will be provided later.
