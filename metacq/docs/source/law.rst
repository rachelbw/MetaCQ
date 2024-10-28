Laws about data privacy you need to know
=====


In the previous Chapter, we understood data privacy, especially since organizations need to follow the laws to protect individuals' data privacy rights. **GDPR**, or General Data Protection Regulation, is a famous law about human rights and data privacy in the EU. At the same time, the **PPIP Act 1998** focuses on New South Wales, Australia, to protect individual data on how it is processed, collected, and stored. One of those two laws has been applied in many countries, and the other is closely related to us. In this Chapter, let's look at them in detail with relevant principles to enhance the legal knowledge about data privacy and be aware of those rules when we collect data.\

.. raw:: html

   <p style="font-size: 24px;font-weight: bold;">GDPR</p>

The completed GDPR has 11 chapters, mentioning key issues of consent, personal data, privacy by design, processing activities, right of access and so on about data privacy. \

Dr. Giovanni Butera has summarised the GDPR in the following lists: \

* **Be informed and give consent**: you need to be able to demonstrate that data subjects have been informed about their right to consent, and that consent was freely given, specific and unambiguous.\

* **Access their information**: whenever requested you need to be able to provide a copy of the data collected, explain how it is used, list any third-party access, and indicate for how long it will be stored within a month from when the request was made.\

* **Anonymity**, or pseudonymisation: where necessary, you must be able to transform identifying data into a manner that prevents any person with unauthorized access to trace it back to an individual.\

* **Rectification**: you must comply with any request to have inaccurate data corrected.\

* **Object to or restrict data processing**: if an individual objects to the processing of their data, or requests it be restricted, you will be required to provide a legal and compelling reason for continuing to do so, or demonstrate that data is processed in limited circumstances and only with the data subject’s consent.\

* **Data portability**: you must comply with any request by a data subject to have their personal data transferred to another organisation (e.g., a competitor).\

* **Erasure, or the “right” to be forgotten**: data subjects have the right to withdraw consent that was previously given, which means that if requested you must permanently remove their personal data from wherever it is held in your organisation.\

* **Notification of breach**: if a data breach is highly likely to compromise the rights of an individual you must notify the individual immediately, and inform the relevant supervisory authority within 72 hours of becoming aware of the breach.\


.. raw:: html

   <p style="font-size: 24px;font-weight: bold;">PPIP Act 1998</p>

Privacy and Personal Information Protection Act 1998, abbreviated as PPIP Act, which is a well-known policy that outlines how New South Wales (NSW) public sector agencies manage personal information and the functions of the NSW Privacy Commissioner.\
To allow agencies to properly manage the data, the PPIP ACT has announced 12 Information Protection Principles (IPPs) as the guidance in 5 parts, summarised as:\

* **Collection**: During the data collection process, the collection needs to keep people informed, **open** and **directly** taken from individuals. Only collect **relevant** information for a **lawful** purpose.\

* **Secure**: Storing collected information **securely** and preventing unauthorized access, use, modification, or disclosure.\

* **Access and Transparency**: The collected data has to be kept **transparent** by explaining an individual's data functions, and individuals have the right to update, **correct** or amend their personal information with no excessive delay or expense to **access** it.\

* **Use**: The information is **limited** on use that has to be under the consent or the purpose of use is directly related to the purpose for which it was collected, and make sure that the personal information is relevant, **accurate**, up to date and complete before using it.\

* **Disclosure**: Disclosure of the information **restricts** on an agreement of an individual's consent or being noticed when the information gets disclosed, and the information will be **safeguarded** so that no sensitive information will be disclosed.\

.. raw:: html

   <p style="font-size: 24px;font-weight: bold;">MCQ Practice</p>

.. raw:: html

    <iframe src="https://app.cogniti.ai/agents/66b8a9307eaee19a46ae8b25/chat?k=VPUBLGWG6JBYH7qy0p2HRrIOSEkvYE5C9_qeg8M4JoY" width="1100" height="500" style="border:none;"></iframe>


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
        <!-- This is a single-line comment -->
        <h2>Please Upload Your Conversation File </h2>
        <input type="file" id="fileInput" />
        <button onclick="processFile()">Check File</button>
        <div id="feedback"></div>
   </div>

  

   <script>
        /* Initialise the current chapter performance */
       var chapter2_performance = "not passed";
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
                   localStorage.setItem('chapter2_performance', 'Just Qualified');
                   feedbackDiv.innerHTML = "Good Job! You've passed this chapter's study. Please continue to the next chapter.";
               } else if (content.includes("fully comprehended")) {
                   localStorage.setItem('chapter2_performance', 'Fully Comprehend');
                   feedbackDiv.innerHTML = "Congraulations! You have fully comprehended the knowledge in the current chapter. Please continue to the next chapter.";
               } else {
                   localStorage.setItem('chapter2_performance', 'Not passed yet');
                   feedbackDiv.innerHTML = "Unfortunately you haven't pass this chapter's study yet. Please keep practice on the MCQs above.";
               }
           };

           reader.readAsText(file);
       }

   </script>

.. note:: 
   **Reference**\

   1. https://www.dfat.gov.au/sites/default/files/nixora-group-eufta-submission.pdf\

   2. https://www.ipc.nsw.gov.au/privacy/nsw-privacy-laws/ppip \

   3. https://www.ipc.nsw.gov.au/information-protection-principles-ipps-agencies 