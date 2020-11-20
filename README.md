# note:  
We have to hide the EHR data in the dataset due to the data privacy. Please contact authors if you need the dataset and codes.


# LATTE
A knowledge-based method to normalize various expressions of laboratory test results in free text of Chinese electronic health records


# introduction
Lab test results in free text of Chinese EHRs are full of variations in expression forms and terms.  

LATTE aims to integrate various expressions of lab test results, and convert them to a unified, structured form as "specimen-analyte-abnormality".  

Specimen and analyte determine a specific test and abnormality reflects whether a test is normal or abnormal (higher or lower). We argued that this information model for lab test results not only reduce data heterogeneity of EHRs, but also provide a more machine-understandable format to follow-up applications.   


# language 
Chinese EHRs  

# programming 
python

# package dependence
chardet  
interval  
pandas  

# usage 

We provided two version of LATTE.   

one (latte4batch) is for batch processing of EHRs, and the other (latte4brat) is for pre-annnotation in brat.  

(1) Usuage of latte4batch  

Step 1. Put your documents (utf-8) in "raw_texts" directory  
Step 2. Run python(3) latte4batch  
Step 3. Check results in "triplets_in_text" directory  


(2) Usuage of latte4brat  

Step 1. Prepare a document (utf-8) (e.g. demo.txt)  
Step 2. Run python(3) latte4brat demo.txt  
Step 3. Check the "demo.ann" file in the same directory with "demo.txt"  
Step 4. Put "demo.txt" and "demo.ann" into the data directroy of brat  
Step 5. Open brat in brower, and correct extractions based on pre-annotations.   
  
Attention : Since brat is run on linux, if your documents are generated on windows, please use a command "dos2unix demo.txt".  
Otherwise, you will meet position errors due to differnt line break characters on windows and linux.  
