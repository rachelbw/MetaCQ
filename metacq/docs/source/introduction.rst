Introduction to data privacy: what is it?
=====

.. raw:: html

   <p style="font-size: 24px;font-weight: bold;">Definition</p>

**Data privacy** generally refers to the *access and control of how personal information is collected and used*, especially including sensitive information with limited access, such as your date of birth, IP address, bank statements, etc. The organization that collected the data should follow the relevant laws to keep the data secure and safe; they are only allowed to use and publish the data that is relevant to the topic under the consent, and the person who got data collected has the right to control over their data, including the ability to decide how organizations collect, store and use their data.\

Without data privacy, our world will be such a mess - your personal information may leak out and cause identity theft, your email address will receive spam emails all the time, your data may get over-abused, and all the content generated on your page will follow exactly what you just recently viewed, isn't that scary? That’s why data privacy exists, constraint organizations to manage the data and assist people in keeping their data rights with corresponding laws such as GDPR and PPIP Act (which will be introduced in the next chapter) and let data scientists be aware of how to properly collect and deal with the data (which will be introduced in the 3rd chapter). \

.. raw:: html

   <p style="font-size: 24px;font-weight: bold;">7 Key Terms</p>
To comprehend what is about data privacy, here are 7 key terms we need to know about data privacy: \

- **Data breach**: data breach has been defined as “any security incident in which unauthorized parties access sensitive or confidential information, including personal data (Social Security numbers, bank account numbers, healthcare data) and corporate data (customer records, intellectual property, financial information)”, normally caused due to accident, malicious insiders who abusing the data to gain themselves benefits or hackers.

- **Data minimization**: a principle that allows the organisation to only collect, process and store the necessary amount of personal information required for a specific purpose.

- **Access control**: access control regulates who or what can view or use resources in a computing environment, which has two types: physical and logical. Physical access control refers to the physical access to the buildings, rooms etc., in our scenario we refer to the logical access control which limits the accessibility to data, networks and so on.

- **Accountability**: A principle requires you to take responsibility for what you do with personal data and how you comply with the other principles. You must have appropriate measures and records in place.

- **Transparency**: transparency in data privacy can be explained as people have the right to know what their personal information has been collected, used and processed.

- **Consent**: consent includes two-ways communication. Organisations need to ask people’s permission to disclose/collect/process their data, and people can respond yes or no to the request. This will be further explained in Chapter 3.

- **Confidentiality**: Confidentiality refers to the obligation of organisations that collect information to ensure that no person or organisation is likely to be identified from any data released.

.. raw:: html

   <p style="font-size: 24px;font-weight: bold;">MCQ Practice</p>
   
.. raw:: html

    <iframe src="https://app.cogniti.ai/agents/668b0324381ece828e5fb325/chat?k=tjcjOpRuUW07ybd57Ruc3PKBjECfJKtNoAOoXYTL5bQ" width="1100" height="500" style="border:none;"></iframe>

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
       var chapter1_performance = "not passed";
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
                   localStorage.setItem('chapter1_performance', 'Just Qualified');
                   feedbackDiv.innerHTML = "Good Job! You've passed this chapter's study. Please continue to the next chapter.";
               } else if (content.includes("fully comprehended")) {
                   localStorage.setItem('chapter1_performance', 'Fully Comprehend');
                   feedbackDiv.innerHTML = "Congraulations! You have fully comprehended the knowledge in the current chapter. Please continue to the next chapter.";
               } else {
                   localStorage.setItem('chapter1_performance', 'Not passed yet');
                   feedbackDiv.innerHTML = "Unfortunately you haven't pass this chapter's study yet. Please keep practice on the MCQs above.";
               }
           };

           reader.readAsText(file);
       }

   </script>

.. note:: 
   **Reference**

   1. https://www.ibm.com/topics/data-privacy \

   2. https://www.ibm.com/topics/data-breach \

   3. https://en.wikipedia.org/wiki/Data_minimization \

   4. https://www.techtarget.com/searchsecurity/definition/access-control \

   5. https://ico.org.uk/for-organisations/uk-gdpr-guidance-and-resources/data-protection-principles/a-guide-to-the-data-protection-principles/the-principles/accountability-principle/ \

   6. https://www.edps.europa.eu/data-protection/our-work/subjects/transparency_en \

   7. https://www.ipc.nsw.gov.au/fact-sheet-consent \

   8. https://www.abs.gov.au/statistics/understanding-statistics/statistical-terms-and-concepts/confidentiality \
