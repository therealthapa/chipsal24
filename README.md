# Shared task on Natural Language Understanding of Devanagari Script Languages at  [CHIPSAL@COLING 2025](https://sites.google.com/view/chipsal/home) #

The "Shared task on Natural Language Understanding of Devanagari Script Languages" at CHIPSAL@COLING 2025 focuses on addressing key challenges in processing Devanagari-scripted languages. In multilingual contexts, accurate language identification is critical, making the first subtask, Devanagari Script Language Identification, essential for identifying whether a given text is in Devanagari script. Hate speech detection is another significant aspect of understanding social dynamics, especially within online spaces. Subtask B, Hate Speech Detection, aims to determine whether a given text contains hate speech, with annotated datasets marking the presence or absence of such content. Building on this, Subtask C, Targets of Hate Speech Identification, focuses on identifying specific targets of hate speech, such as individuals, organizations, or communities. This shared task facilitates comprehensive Devanagari Script Language understanding, targeting key challenges in script identification, hate speech detection, and the identification of hate speech targets. 

## Sub-task A ##
<b> Devanagari Script Language Identification:</b> Given a sentence in Devanagari script, the goal is to determine the language it belongs to among Nepali, Marathi, Sanskrit, Bhojpuri, and Hindi. This task addresses the critical need for accurate language identification in multilingual contexts.

## Sub-task B ##
<b> Hate Speech Detection in Devanagari Script Language:</b> Given a text, the goal of this task is to identify whether it contains hate speech or not. The text dataset for this subtask will have binary annotations for the prevalence of hate speech.

## Sub-task C ##
<b> Target Identification for Hate Speech in Devanagari Script Language:</b> The goal of this subtask is to identify the targets of hate speech in a given hateful text. The text is annotated for "individual", "organization", and "community" targets.


## Participation ##

In order to participate in the competition, please Join our codalab competition [here](https://codalab.lisn.upsaclay.fr/competitions/20000)

**Training Data:**

| SubTask | Link |
|----------|----------|
| SubTask-A | [here](https://drive.google.com/file/d/1YAo40VKJlF2dD1xlPsWDZ4uqANSh1lrx/view?usp=drive_link) |
| SubTask-B | [here](https://drive.google.com/file/d/1stCXIF8yJkywi0VDV9iBMwLPVuG5MQy2/view?usp=drive_link) |
| SubTask-C | [here](https://drive.google.com/file/d/166k7N9KV6jEDvvAr9iLTwrWyfdEcAs5p/view?usp=sharing) |

**Eval Data:**


| SubTask | Link (index-tweet/text)| Link (index-label)|
|----------|----------|----------|
| SubTask-A | [here](https://drive.google.com/file/d/1wmivix0utKHmq6d6ICvpRBTo1pebV3yI/view?usp=drive_link) | [here](https://drive.google.com/file/d/1IicURjnKv8IRvcB99VmSBUIO7SzDfwSu/view?usp=sharing) | 
| SubTask-B | [here](https://drive.google.com/file/d/1SD7bn-5bU0g13GQrZ-RXGDGyAFNSy6VC/view?usp=drive_link) |[here](https://drive.google.com/file/d/1apPJPZnZTke9PJi7z1NvkJKaxn70bCYT/view?usp=drive_link) |
| SubTask-C | [here](https://drive.google.com/file/d/1-2TjS6xPfjWj9YaJGSf-JXXXfNz-2pNT/view?usp=sharing) | [here](https://drive.google.com/file/d/1-1k1yHOGP7Wij1mUG2iKaSTN8i1WUgPz/view?usp=sharing) |


**Test Data:**

| SubTask | Link (index-tweet/text)|
|----------|----------|
| SubTask-A | [here](https://drive.google.com/file/d/1m9q9iC4y7kAkOHxX7QuXNwNTlcnzX77p/view?usp=sharing) |
| SubTask-B | [here](https://drive.google.com/file/d/14uwPoYxL-DXiYPumMA_Qf5GpXNU29ggg/view?usp=sharing) |
| SubTask-C | [here](https://drive.google.com/file/d/1-8s5pEl6nga3qlEIVEWCJTPGFcNz2V5m/view?usp=sharing) |


## Dataset ## 
All the text has a unique identifier called "index". The labels for training data are given along with the dataset. For evaluation and testing, the submission format is mentioned below.

## Evaluation ## 

The results are only accepted in codalab. The submission will be evaluated with a f1-score.

The script takes one prediction file as the input. Your submission file must be a JSON file which is then zipped. We will only take the first file in the zip folder, so do not zip multiple files together. 


For subtask A, make sure that your 'Nepali' label is given as '0', 'Marathi' label is given as '1', 'Sanskrit' label is given as '2', 'Bhojpuri' label is given as '3', and 'Hindi' label is given as '4'.


<b>IMPORTANT:</b> The index in JSON should be in ascending order.
```python
{"index": 10017, "prediction": 0}
{"index": 27943, "prediction": 4}
{"index": 38870, "prediction": 2}
{"index": 54601, "prediction": 3}
{"index": 69131, "prediction": 1}
```

Similarly, for subtask B, the final prediction submissions should be like the following. Make sure that your hate label is given as "1" and non-hate label is given as "0".

<b>IMPORTANT:</b> The index in JSON should be in ascending order.
```python
{"index": 10001, "prediction": 0}
{"index": 10068, "prediction": 1}
{"index": 10542, "prediction": 0}
```


Similarly, for the subtask C, the final prediction submissions should be like the following. Make sure that your individual, organization, and community labels are given as "0", "1", and "2" respectively.

<b>IMPORTANT:</b> The index in JSON should be in ascending order.
```python
{"index": 50001, "prediction": 0}
{"index": 50010, "prediction": 1}
{"index": 50074, "prediction": 2}
```

## Publication ##
Participants in the Shared Task are expected to submit a paper to the workshop. Submitting a paper is not mandatory for participating in the Shared Task. Papers must follow the COLING 2025 workshop submission instructions for short papers and will undergo regular peer review. Their acceptance will not depend on the results obtained in the shared task but on the quality of the paper. Authors of accepted papers will be informed about the evaluation results of their systems prior to the paper submission deadline (see the important dates). All the accepted papers will be published in ACL Anthology.

## Invitation for Special Issue ##
Top-performing teams and best models will be invited for a special issue in journals (T.B.D.).

## Timeline of the Events ##
<ul>

<li>Training & Evaluation data available: August 19, 2024 </li>

<li>Test data available: September 27, 2024 </li>

<li>Testing Phase start: September 27, 2024 </li>

<li>Test end: October 27, 2024 </li>

<li>System Description Paper submissions due: November 3, 2024 </li>

<li>Notification to authors after review: November 29, 2024 </li>

<li>Camera ready: December 13, 2024 </li>

<li>CHIPSAL Workshop: January 19, 2025 </li>
</ul>

## Organizers ##
<ul>
<li> Surendrabikram Thapa (Virginia Tech, USA) </li>
<li> Kritesh Rauniyar (Delhi Technological University, India) </li>
<li> Farhan Ahmad Jafri (Jamia Millia Islamia, India) </li>
<li> Surabhi Adhikari (Columbia University, USA) </li>
<li> Kengatharaiyer Sarveswaran (University of Jaffna, Sri Lanka) </li>
<li> Bal Krishna Bal (Kathmandu University, Nepal) </li>
<li> Usman Naseem (Macquarie University, Australia) </li>
</ul>

## Contact ##
If there are any questions related to the competition, please contact surenthapa5803@gmail.com

## References ##
Will be provided later.
