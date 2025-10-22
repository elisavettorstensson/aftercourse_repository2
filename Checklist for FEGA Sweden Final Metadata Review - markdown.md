## Checklist for FEGA Sweden Final Metadata Review

This checklist serves as a comprehensive guide for reviewing the metadata associated with FEGA Sweden submissions. It is designed to ensure consistency, accuracy, and compliance with the standards established by the central EGA for submission validation. By following this checklist, reviewers, data stewards responsible for reviewing the metadata before submission finalization in the submitter portal can collaboratively maintain the integrity of metadata records, streamline the submission process, and support the seamless integration of data within the European Genome-Phenome Archive (EGA).

1. **Studies**.   
* Study title should be a 3-20 word introduction of the project.   
* Study description should be a 3-5 sentence definition of the project with some background, goals, and details.  
  * IF the title and description align with these criteria, **move on to the next object.**  
  * IF the title or/and description does not align with these criteria (e.g. it is a copy of the title, it doesn’t describe the “why” of the study), **reject the submission** and ask the submitter to update/change the title or/and description and re-finalise the submission.  

* **Rare cases**    
  * IF the submission reuses an existing study, which will be referenced in the “experiment” object, you can move on to the next object.  
2. **Samples**.   
* Samples MUST NOT contain personal data (e.g., names, national ID numbers, addresses).  
  * IF the samples do not contain personal data, **move on to the next object.**  
  * IF the samples contain personal data, **reject the submission** and ask the submitter to remove all personal data and re-finalise the submission.

* **Rare cases**    
  * If there are no samples, this means that this submission is reusing existing samples and will be referenced in the “runs” object. Move on to the next object.  
3. **Experiments**.   
   * The study ID could be a new one (no EGAD) or an existing study (EGAD5XXX or EGAD000100XXX). All options are fine  
   * **Design name:** Check if the following have been completed:A brief summary of the purpose, setup, and methodology of the library preparation. This should include the scientific goal, experimental conditions, and key steps in the library construction protocol.   

  * If everything looks fine, then **move on to the next object.**

4. **Runs and associated files** (if any runs are registered in the submission).  
   * Check the run type and files: File extensions must be correct for a Run object (*fastq, bam, cram*…).   
     * IF the name of the file extensions corresponds to the selected run type. For example, if the run type is BAM, the file extensions should be *.bam*. **Move to the next object**  
     * IF the name of the file extensions does not correspond to the selected run type. For example, if the run type is FASTQ, but the file extension is *.text*, THEN reject the submission and ask the submitter to upload the correct files.  
     * IF the file extension does not correspond to the selected run type and is unknown (srf, rds, h5, h5Seurat), [check for the accepted file extensions](https://docs.google.com/document/d/1xXJGkQ36XRmR5qAI0hzljx4tS1PKri-FwRF7ufF46Mg/edit?tab=t.0#heading=h.g4sjsh593uea)

       * IF it is an accepted file extension, THEN move on to the next object  
       * IF the file extensions are not listed, THEN reject the submission and check with the submitter whether there is an error in the name of the file extension or if there is no category for their runs/files.

   **Files (Ingested files)** 

   * Check the file size.  
     * IF the file size is o bytes, THEN reject the submission and ask the submitter to reupload the file.  
     * Otherwise, move to the next field  
   * Check the file extension.  
     * IF the extension is .c4gh only, THEN reject the submission and ask the submitter to rename their file from the INBOX.
     * IF the file extension is not listed in the [accepted file](https://docs.google.com/document/d/1xXJGkQ36XRmR5qAI0hzljx4tS1PKri-FwRF7ufF46Mg/edit?tab=t.0#heading=h.g4sjsh593uea) list, THEN reject the submission and check with the submitter whether there is an error in the name of the file extension or if there is no category for their runs/files.

* **CEGA specific cases**   
  *  Check the run ID: IF the run ID is an EBI object (EGAX000), **THEN reject the submission**. Ask the submitter not to reuse existing runs and contact the HD.

  * The sample can be a new one (no EGA ID) or an existing one (EGAN000, EGAN5). Move on to the next field.  
  * Check the experiment:  
    * IF the experiment ID is an EBI object (EGAX5), **THEN reject the submission**. Ask the submitter to not reuse existing experiments and create a new one.  
    * Otherwise, if it is a new object or a CRG object (EGAX5), **move to the next object** in the submission.  
5. **Analyses and associated files** (if any analysis is registered in the submission).   
   * Check the analysis type and files: File extensions must be correct for an analysis object (*vcf, phenotype file*…), and they must be encrypted having the extension .c4gh  
     * IF the name of the file extensions corresponds to the selected run type. For example, if the analysis type is sequence variation, the file extension should be *.vcf*. **Move to the next object**  
     * IF the name of the file extensions does not correspond to the selected run type or/ and the file extension is unknown, [check for the accepted file extensions](https://docs.google.com/document/d/1xXJGkQ36XRmR5qAI0hzljx4tS1PKri-FwRF7ufF46Mg/edit?tab=t.0#heading=h.g4sjsh593uea)  
       * IF it is an accepted file extension, THEN move on to the next object  
       * IF the file extensions are not listed, THEN reject the submission and check with the submitter whether there is an error in the name of the file extension or if there is no category for their runs/files.

   * **Rare cases**    
     * The study ID could be a new one (no EGAD) or an existing study (EGAD5XXX or EGAD000100XXX). All options are fine; move on to the next field.  
     * The sample can be a new one (no EGA ID) or an existing one (EGAN000, EGAN5). Move on to the next object of the submission.  
         
   * **CEGA specific cases**   
     * Check the analysis ID: IF the analysis ID is an EBI object (EGAX000), THEN reject the submission. Ask the submitter not to reuse existing analysis and contact the HD.

6. **Dataset.**  

   * Dataset title should be a 3-20 word description of the dataset content.  
   * Dataset description should be a 3-4 sentence definition of the dataset content, including sample number and details, file type, and technology/experimentation used.  
     * IF the title and description align with these criteria, **move on to the next object.**  
     * IF the title or/and description does not align with these criteria (e.g. it is a copy of the title, it doesn’t describe the number of samples or technology used), **reject the submission** and ask the submitter to update/change the title or/and description and re-finalise the submission.  
   * Check that the Policy is correct and belongs to the data controller.  
     * UU  **Policy**: EGAP50000000398  **DAC**: EGAC50000000433  
     * LU   **Policy:** EGAP50000000565 **DAC:** EGAC50000000619


