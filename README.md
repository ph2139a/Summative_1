# **Software Engineering - Summative 1** 
## **December 2023**

This repo has been created for [Software Engineering Summative 1](https://nchlondon.instructure.com/courses/3329/assignments/35561). The project was managed via the linked GitHub project. Status and label functionality within GitHub projects was used to keep track of relevant work.

![NCH London Image](images/nch-at-northeastern-st-katharine-docks-1536x922.jpg)

&nbsp;

## 1.  **Propose a new product for your employer or a small-scale side project for your organisation**

**Project Charter**

-   **Overview** - This information technology project will focus on development of an adversarial patching application that can fool an object detection model. At upload of an image the application will generate and apply an adversarial patch that will force a misclassification of objects that appear within the patched image when it is passed to a deep learning-based convolutional neural network. 

-   **Scope** - A web application will be developed that permits image upload, adversarial patch generation, patch application and image presentation. This application will output the classification results for the unpatched and patched image. The minimum viable product is a system that demonstrably completes these goals with a small set of test images. Ensuring that this system is robust enough to handle a wide variety of image inputs is out of scope for this project. 

-   **Schedule** - This project will be completed by 19th January 2024. A hybrid project management approach will be utilised as only one person will work on the project, the outcome is to some degree predictable and work will be completed in a series of tightly time-bound sprints. In practice these sprints are the days on which I am free to work on my apprenticeship assignments during the working week.  

-   **Risks** - The principal risk stems from the inherent complexity of the task that the web app seeks to complete. The most straightforward approach will be taken, focussing on test driven development to ensure succinct and robust implementation.

-   **Stakeholders** - I am a key stakeholder as I am completing the project as part of a data science university course. The other key stakeholder is the university faculty that will review the assignment. 

**Deliverable List**

-   A GitHub repository containing a web application that permits image upload, adversarial patch generation, patch application and image presentation.

-   A zip file from which the application can be run

-   A PDF copy of this README file

**Task List & Schedule**

-   This project's tasks and schedule are managed via GitHub projects. 

**Risk Register**

-   At project outset the principal risk is that the application is more complex than appears to be required by the assessment brief and as a result will take longer to complete than expected. Despite this risk a minimum viable product will be developed and submitted as the product is of significant value to the organisation.

&nbsp;

## 2.  **Design your product using Figma or an alternative**

![Prototype](images/prototype.png)

&nbsp;

## 3.  **Outline how you planned your project using modern planning techniques. Reflect on your planning using a project Project Management Tool** 

A hybrid methodology was selected for management of the project as it is an assignment that will be worked on over six specific working days as part of my usual working pattern. The methodology is linear in that it has a series of sequential steps, essentially those that are listed as items 1-10 on the Assessment Brief for this piece of work. On the other hand the development will be somewhat iterative; an MVP will be developed and iterated upon as far as time permits, hopefully resulting in a product that is operationally valuable within my workplace. 

The schedule and cost for this project are fixed as the schedule is determined by the university and the cost must be 0. I have selected a somewhat open scope for the project to leave open the possibility of iterative improvements. A stretch goal is to request feedback from those that might actually use an adversarial patching tool within my workplace; though the management must be linear in that a hard deadline must be met, this visibility would result in development that is more aligned with agile methodologies.

GitHub Projects has been a very effective tool for managing the tasks that need to be completed for this assignment. In addition to the 10 tasks that are detailed on the Assessment Brief, issues were created and labelled for tasks that needed to be completed once coding was underway. The ability to reorder and label these was valuable, as was the ability to add comments containing detail and the options to filter out tasks that had been completed. The titles of issues that did not represent a task that appears on the Assessment Brief were prefixed with “---” to ensure that they stood out visually. 

&nbsp;

## 4. **Capture the requirements for your project as issues or tickets shown via your chosen Project Management Tool**

![Project Management Tool](images/project_management_tool.png)

&nbsp;

## 5. **Summarise how you built the minimal viable product or a prototype step by step in a written report** 

The first step towards development of a minimum viable product (MVP) for this project was to identify an adversarial patching implementation that could serve as a starting point for my work. I researched the topic and focussed on the identification of attacks on the specific architecture that is relevant to my workplace. This research led me to the Github page for Adversarial Robustness Toolbox (ART) (Trusted-AI, 2023a) and a series of example notebooks. 

I selected the notebook that best fit my requirements and imported it into Google Colab (Trusted-AI, 2023b). At runtime the notebook caused a series of errors. I edited the code to resolve these, refactored to reduce complexity and added comments and markdown that make the more complex processes easier to understand. As one of my goals is to facilitate user selection of a target class I researched and implemented fiftyone (voxel51, 2023) to facilitate the retrieval of a subset of images that appear in the dataset that was used to train the model that is "attacked" by the patching. The pre-trained model, You Only Look Once (YOLO) (Redmon et al, 2016), was trained on data from COCO (Lin et al, 2014).

My next step was to develop a test of my implementation. I identified a suitable image on the internet and wrote code to display the object detection output before and after the application of the adversarial patch. At MVP the patching represented an effective attack on the object detection model in that it caused the model to behave erratically and introduced unexpected results in the model's output. The next steps for development will focus on improving the patching so that the patch itself is classified as expected by YOLO.

&nbsp;

**References**

Redmon, J., Divvala, S., Girshick, R. and Farhadi, A. (2016). You only look once: Unified, real-time object detection. In Proceedings of the IEEE conference on computer vision and pattern recognition (pp. 779-788).

Trusted-AI (2023). Adversarial Robustness Toolbox. Available at: <https://github.com/Trusted-AI/adversarial-robustness-toolbox/tree/main> (Accessed: 21/12/2023)

Trusted-AI (2023). ART - Adversarial Patch - PyTorch - YOLO. Available at (<https://github.com/Trusted-AI/adversarial-robustness-toolbox/blob/main/notebooks/adversarial_patch/attack_adversarial_patch_pytorch_yolo.ipynb> (Accessed: 21/12/2023)

Lin, T.Y., Maire, M., Belongie, S., Hays, J., Perona, P., Ramanan, D., Dollár, P. and Zitnick, C.L. (2014). Microsoft coco: Common objects in context. In Computer Vision--ECCV 2014: 13th European Conference, Zurich, Switzerland, September 6-12, 2014, Proceedings, Part V 13 (pp. 740-755). Springer International Publishing.

voxel51 (2023). fiftyone. Available at: <https://github.com/voxel51/fiftyone>



```
# This is a sample comment
this_is = sample_code
```

   

