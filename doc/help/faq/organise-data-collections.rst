.. _faq-organise-data-collections:

Organize data collections
=========================

.. _faq-dac-files:

1.  **Which files should and should I not upload to a Data Acquisition Collection (DAC)?**

    A DAC must contain all raw data plus a description that would allow a colleague to make sense of the data. By raw, we mean without any manipulations that limit future analyses of these data. In other words, raw data are original data.

    Some examples for the different methods:

    **Behavioral experiments**
 
    - stimulus files
    - computer scripts for presenting the stimuli (to be run by Presentation or PsychoPy)
    - experiment log files
 
    **Anatomical MRI experiments**
 
    - DICOM files
 
    **Functional MRI experiments**
 
    - DICOM files
    - possibly eye tracker data
    - possibly video files
    - possibly ExG files
    - (if applicable) the files specified under "behavioral experiments"
 
    **EEG experiments**
 
    - EEG files (vhdr/vmrk/dat)
    - Presentation log files
    - possibly eye tracker data
    - possibly video and audio files that were recorded along with the EEG
    - (if applicable) the files specified under "behavioral experiments"
 
    **MEG experiments**
 
    - MEG datasets
    - Presentation log files
    - possibly eye tracker data that was recorded along
    - possibly video and audio files that were recorded along with the EEG
    - (if applicable) the files specified under "behavioral experiments"
 
    In general, you should also upload a copy of the Presentation code and stimulus material that you used during the experiment and of the lab notes that you took during the experiment. Also include a description of the experimental setup.
 
    You should not upload personal information to a DAC (or any other collection). Personal information are data that directly identify your subjects (e.g., their name, address, telephone number, bank account, etc.). This also means that you should not upload the informed consent form that is signed by the subject. Note that the DAC is allowed to contain indirectly identifying information, such as detailed questionnaire results (but with the personal information removed), photos, audio and video recordings or facial features in an anatomical MRI.

    You should not upload any data that can be obtained as the result of analyses that take raw data as input (processed data). Documenting the data analysis is a part of the Research Documentation Collection (RDC).

.. _faq-dac-organisation:

2.  **How should I organize the data in a Data Acquisition Collection (DAC)?**

    Organize your DAC in a standard way (such as BIDS), because will make it much easier to share the data at a later point in time. Below is one example from the BIDS website. See for more examples here.
   
    .. figure:: images/BIDS.PNG
        :scale: 50%
   
    For all types of data we recommend that you add a 'readme' document that describes the organization of the data over the files and directories.
   
    For an example of a well-organized DAC from a DCCN project see this :download:`example <documents/DAC_example.pdf>`. The first page of this document contains the content of the 'readme general' file, including the DAC abstract.

.. _faq-rdc-files:

3.  **Which files should and should I not upload to a Research Documentation Collection (RDC)?**

    An RDC has three functions: documenting the scientific process, sharing preliminary results within the project team, and documenting the editorial and peer-review process.

    In general, a RDC must contain all the information that a knowledgeable colleague needs to reproduce the results in the publication that is linked to this collection. More specifically, an RDC should contain files that document the process in which raw data are converted into results (statistical tests, summary measures, figures, tables, etc.). In a common scenario, this conversion from raw data to results is (partially or fully) specified by analysis scripts that can be executed by software packages such as MATLAB, R, Python, SPSS, Bash+FSL, etc. In this scenario, the obvious way of documenting the scientific process is by providing these analysis scripts. Also the version number of the software being use should be specified. 

    Our definition of “data” is a broad one. For instance, it also includes computer scripts, as used for analysis or modeling work. Thus, if the published results depend on computer scripts, these must be added to the RDC.

    The RDC is a platform for sharing preliminary results (figures, tables, PowerPoint presentations, etc.) with collaborators in a project team. A RDC should contain the documents of the editorial and peer-review process pertaining to the publication that is linked to this collection (uploaded manuscripts, reviews, reply to the reviewers, ...). An archived RDC must be linked to one publication. 

    Also include a description of the experimental setup.

    Before closing the RDC, the preliminary results may be removed.

.. _faq-refer-data-not-collected-by-researcher:

4.  **How to refer to the data that the researcher did not collect?**

    It is possible to publish papers without having collected data yourself. For example, modeling work or using an existing data set. There are three ways to link these types of data to the new RDC.

    If the data is already represented in the repository as one or more DAC’s, specify the DAC identification numbers in the RDC. This only works for archived DACs. A single archived DAC may be associated with multiple RDCs.

    If the data is not represented in the repository, the researchers must either add the data to the repository, or document the data by a persistent identifier (e.g. DOI or URL). This situation applies when a DAC is not yet archived or the data was collected at another institute. 

.. _faq-rdc-organisation:

5.  **How should I organize the data in a Research Documentation Collection (RDC)?**

    Data in a RDC should be organized in separate folders and sub-folders according to the type of data (e.g. raw data, scripts, peer-review process, etc.). The names of the folders should clearly indicate to the content of the folder.

    .. _faq-preferred-formats:

6.  **Which data formats should I use to ensure that my data remains usable in the future?**
    Using general and common file formats is important to ensure research data will remain usable in the future. For research data collected or processed within the Donders Institute and archived or published using the Donders Repository, it is encouraged to use the following standard, open or exchangeable file formats:


    ============================  ===================================================
    Type                          Preferred format
    ============================  ===================================================
    Free text                     ASCII text, MarkDown, .docx (MS Word), .pdf
    Structured text               .json, .xml
    Tabular data                  CSV or TSV (comma- or tab-separated values)
    Images                        .jpg, .tiff, .PNG
    Videos                        .avi or .mp4 with h264 coding
    Audio                         .wav
    Numerical data                CSV, TSV, .mat (MATLAB), .npz(NumPy)
    EEG data                      .eeg, .vhdr, .vmrk (BrainVision), EDF, BIDS
    MEG data                      .ds (CTF), BIDS
    MRI data                      .ima (DICOM), .nii(NIFTI) with header details in .json,                               BIDS
    Eye tracker data              .edf (Eyelink), .idf (SMI), ASCII text
    Articles and documentation    .docx (MS Word), .pdf
    Code and analysis scripts     Native representation, for example .m (MATLAB), .py                                   (Python), .sps (SPSS)
    README files                  Plain text (ASCII) 
    ============================  ===================================================


.. _faq-document-experimental-setup:

7.  **How should I document the experimental setup?**

    You must describe your experiment in a document (txt, csv, tsv, pdf, MS Word or MS Excel) that you upload to the collection. In this document, give a brief description of your experimental setup, which tasks you used and what they attend to manipulate and measure. In that document, you also explain how the conditions, stimuli and responses are represented in the presentation log files and the trigger channel of your data acquisition system. A PowerPoint presentation of the project proposal will contribute to the documentation of the experiment. Also the original presentation code (NBS Presentation, E-Prime, etc.) will contribute to the documentation. Add relevant part of this information to the appropriate collection (DAC, RDC and DSC).

.. _faq-where-store-personal-information:

8.  **Where should I store personal information about the participants?**

    For data acquisition you have to know who are your participants and you need to be able to contact them. This requires personal information to be stored. The mapping of the personal information on the participant number is called the "pseudonimization key". The pseudonimization key should be stored in an encrypted file that is stored separately from the experimental data. The file should be protected by a strong password according to the RU password policy. The password is only to be known to the PI and the researchers involved in data acquisition.

    The pseudonimization key must never be stored in the repository.