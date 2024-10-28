Data privacy management: how should we handle it?
=================
From the DATA3406 class, we have mentioned that data privacy needs to be considered at the start when we design the raw data - only take the sensitive information we need to avoid people’s negative perceptions such as suspicion and discomfort arising and therefore leads to the accuracy issue caused by human error. But when we collect the data, how should we handle it concerning privacy? This chapter will introduce the two basic ideas about data privacy management, from data anonymization to informed consent. \

.. raw:: html

   <p style="font-size: 24px;font-weight: bold;">Data Anonymization</p>

Anonymization is a word that means covering the identity so other people won’t be able to recognize it. From a data privacy perspective, data anonymization refers to *the process of removing personal identifiers, both direct and indirect, that may lead to an individual being identified*, which is an essential part when you are collecting your raw data; otherwise, it will bring the consequences of not only introducing the biases within the data but also not follow the relevant laws mentioned previously and generated the ethic concern as well. \

From the slides, we have seen the tools to deal with anonymization: Bin size and K-anonymity. Let's explore those tools to understand how they work.\

.. raw:: html

   <p style="font-size: 16px;font-weight: bold;">Bin Size</p>

When we anonymize the data, we can imagine that we are dividing the sensitive data into different groups. The number of the groups we divide is called bin size, and the bin size can be scaled with the data needed. In our daily lives, the most common cases we can see are the scores that are assigned A, B, C, and D levels instead of marks, or you group people by their ages, like 0 - 8, 9 - 17, etc. By utilizing the bin size, we can vague the sensitive information to make individuals harder to identify, and it is also helpful for our data analysis process to define the significant features within certain groups. 

.. raw:: html

   <p style="font-size: 16px;font-weight: bold;">K-anonymity</p>

As the lecture says, the K-anonymity normally applies under the situation that the current individual data cannot be distinguished from at least k-1 others. Be more general, think about the case that when you are dealing with patients' health data, you want the symptoms to be recorded for medical uses but hide their personal data. Between the ambiguous relationship of people knowing and people not knowing, that's how k-anonymity works.\ 

To achieve this relationship, we need to use **Quasi-identifiers** to distinguish them: *quasi-identifiers are the attributes that allow individuals to be re-identified*. Here is a table of medical records that are being divided into key attribute, queso-identifiers and sensitive attributes:\


In this scenario, the patient's name has been defined as a key attribute, the disease as a sensitive attribute, and the rest of the attributes as Quasi-Identifiers, which can be used *to identify individuals when linking anonymized datasets with other datasets*.\ 

There are two ways to handle the K-anonymity:\
 
1. Generalization: Replace quasi-identifiers with less specific but semantically consistent values until you get k identical values and partition ordered-value domains into intervals.

2. Suppression: When generalization causes too much information loss, the quasi-identifier is omitted or not released at all. This is common with outliers.

With the powerful technique of K-anonymity, we can effectively prevent an individual's identity from being distinguished, ensuring the security in dataset management.\ 

.. raw:: html

   <p style="font-size: 24px;font-weight: bold;">Informed Consent</p>

Informed consent is a really common scenario that exists in our daily lives. For example, when you try to play a game, the first loading page is to agree with the privacy of the player in collecting your relevant information; otherwise, you would not be able to access the game. But what exactly is informed consent?\ 

According to the definition, informed consent refers to *a person giving permission for use of their data, with full knowledge of the possible consequences*.\ 

During the informing process, we should *clearly explain how we want to handle individuals' personal information and communicate their requests in plain English, without legal or industry jargon*. Except that, we still have a few more "soft-laws" we need to take while we collect data based on informed consent:\

* The informed consent has to be **volunteering**. You cannot force or pressure your interviewers, and provide them sufficient time to give your proper answers.\

* People who are taking interviews need to be **capable** enough to take your questions with solid responses; people who are considered minors (children and teenagers) and have physical/mental/language limitations may not be able to take the interview properly.\ 

* The consent form has to be **clear and specific** to allow people to fully comprehend the question.\ 

* Individuals have the right to refuse to answer sensitive questions, and they are able to withdraw the informed consent at any time.\ 

.. raw:: html

   <p style="font-size: 24px;font-weight: bold;">MCQ Practice</p>
.. raw:: html

    <iframe src="https://app.cogniti.ai/agents/66b8aa3f5b856c163e9bae97/chat?k=jbiNfEtoTWvTvC2aXy3MkzT4yzzUoo_1r-zfKSEFSbU" width="1100" height="500" style="border:none;"></iframe>


.. raw:: html

   <p style="font-size: 24px;font-weight: bold;">Current Chapter Performance</p>

.. raw:: html

    <style>
         .upload-section {
            background-color: #f9f9f9;  
            padding: 20px; 
            border: 2px solid #ccc; 
            border-radius: 10px; 
            width: 1050px;  
            margin: 20px auto;  /* Center the container on the page */
            text-align: center; 
        }

        .upload-section h2 {
            margin-bottom: 20px; 
        }

        .upload-section input[type="file"] {
            margin-bottom: 10px; 
            padding: 10px;
            border-radius: 5px;
            cursor: pointer;
            background-color: #ffffff; 
        }

        .upload-section button {
            padding: 10px 20px;
            border-radius: 5px;
            background-color: #4CAF50;  
            color: white;
            border: none;
            cursor: pointer;
            margin-top: 10px;
        }

        /* hover animation?*/
        .upload-section button:hover {
            background-color: #45a049;  
        }

        .upload-section #feedback {
            margin-top: 20px;  
            color: #333;  
        }
    </style>

.. raw:: html

   <div class="upload-section"> 
        <!-- create the window to examine the keyword and grant performance level -->
        <h2>Please Upload Your Conversation File </h2>
        <input type="file" id="fileInput" />
        <button onclick="processFile()">Check File</button>
        <div id="feedback"></div>
   </div>

  

   <script>
        /* Initialise the current chapter performance */
       var chapter3_performance = "not passed";
       /* read the file */
       function processFile() {
           const fileInput = document.getElementById('fileInput');
           const file = fileInput.files[0];

            /* check file submission - if not exist giving the warning to select file again*/
           if (!file) {
               alert('Please select a file first.');
               return;
           }

           const reader = new FileReader();

            /* read the current file content, according to the key words to assign different levels of performance results */
           reader.onload = function(e) {
               const content = e.target.result;
               const feedbackDiv = document.getElementById('feedback');

                /* examine the study performance - all the current data will be temperoly kept in localStorage*/
               if (content.includes("you passed")) {
                   localStorage.setItem('chapter3_performance', 'Just Qualified');
                   feedbackDiv.innerHTML = "Good Job! You've passed this chapter's study. Please continue to next chapter.";
               } else if (content.includes("fully comprehended")) {
                   localStorage.setItem('chapter3_performance', 'Fully Comprehend');
                   feedbackDiv.innerHTML = "Congraulations! You have fully comprehend the knowledge in the current chapter. Please continue to next chapter.";
               } else {
                   localStorage.setItem('chapter3_performance', 'Not passed yet');
                   feedbackDiv.innerHTML = "Unfortunately you haven't pass this chapter's study yet. Please keep practice on the MCQs above.";
               }
           };

           reader.readAsText(file);
       }

   </script>


.. note:: 
   **Reference**\

   1. https://www.ucl.ac.uk/data-protection/guidance-staff-students-and-researchers/practical-data-protection-guidance-notices/anonymisation-and\

   2. https://elf11.github.io/2017/04/22/kanonymity.html \

   3. https://www.oaic.gov.au/privacy/your-privacy-rights/your-personal-information/consent-to-the-handling-of-personal-information 