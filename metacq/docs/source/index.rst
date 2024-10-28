.. MetaCQ documentation master file, created by
   sphinx-quickstart on Mon Jul 29 02:16:55 2024.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

MetaCQ: Intoduction to Data Privacy 
====================

Data exists everywhere in our daily life: when you scroll your social media, like some posts, the recommendation system will collect your likes and pop up the content you may interested in on your page; when you are shopping online but want to do in-store pick up, the website will take your location information to check your closest store and product storage; whenever you enter a game, you will always need to agree with the data policy to access the game for developers to make development etc. There are so many things around us that we need to use our data to assist us in an easier life. Still, too much data collecting will make us feel uncomfortable: what if someone has stolen my data and therefore they can fake themselves as me? What if they get access to my financial data as well? Or even feel unsafe as we are under surveillance? All my secrets might be exposed! \

Besides, as data science students, using data is a large part of our daily work. Whether we are conducting surveys to collect other people’s opinions about something or downloading existing datasets from GitHub or a website, we still need to be aware of data privacy when we apply them to our work. \

So, what exactly is data privacy? How can we effectively manage it in our work? This E-textbook platform, **MetaCQ**, integrates data privacy content from the *DATA3406: Human-in-the-Loop Data Analytics* unit and will answer these questions across three chapters. We will explore data privacy, from its basic definitions to the relevant laws and management strategies. By the end, you will have a comprehensive understanding of data privacy, which will also assist your future work in data science. \  

Contents
--------

.. toctree::
   introduction 
   law
   management


Current Study Progress
-----------------

.. raw:: html
   
   <style>
        table.progress-summary {
            /* Set up table design */
            border-collapse: separate; /* Ensures spacing between cells */
            border-spacing: 15px; /* Space between cells */
            width: 100%; /* Table width */
            text-align: center;
            border-collapse: collapse; 
        }

        table.progress-summary th {
            background-color: #53CAAE; 

         }

         table.progress-summary td {
            background-color: #ffffff; 

         }

    </style>

    <!-- Fill the table with content, while each chapter with default progress value of "Not passed yet" -->
    <table class="progress-summary" border="1" cellspacing="1"> 
        <thead>
            <tr>
                <th>Chapter</th>
                <th>Performance</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>Chapter 1 - Introduction to Data Privacy </td>
                <td id="chapter1_performance"> Not passed yet </td>
            </tr>
            <tr>
                <td>Chapter 2 - Laws about Data Privacy </td>
                <td id="chapter2_performance"> Not passed yet </td>
            </tr>
            <tr>
                <td>Chapter 3 - Data Privacy Management </td>
                <td id="chapter3_performance"> Not passed yet </td>
            </tr>
        </tbody>
    </table>

.. raw:: html
   
   <script>
    document.addEventListener("DOMContentLoaded", function() {
        // Set up the function to update each chapter's study performance after the user submitted the performance evaluation
        // Retrieve performance results from localStorage allocated in each chapter 
        var chapter1_performance = localStorage.getItem('chapter1_performance') || "not passed";
        var chapter2_performance = localStorage.getItem('chapter2_performance') || "not passed";
        var chapter3_performance = localStorage.getItem('chapter3_performance') || "not passed";

        // Update the table content
        document.getElementById("chapter1_performance").innerText = chapter1_performance;
        document.getElementById("chapter2_performance").innerText = chapter2_performance;
        document.getElementById("chapter3_performance").innerText = chapter3_performance;
    });
   </script>
