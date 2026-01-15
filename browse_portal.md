# The VMRC Portal

## Overview

The VMRC Data Portal (https://portal.vmrc4health.org/) provides faceted search and advanced query tools that enable users to explore data in a more flexible and customized way. The VMRC data portal currently hosts raw and processed data from 6 studies, which includes sequencing files, PacBio and Illumina assembly files, annotation files and analysis/processed files from 16Samplicon/ITSamplicon processing, metagenome, metatranscriptome, metabolome, immunology and metaproteome analyses.

The portal landing page is broken up into 3 sections:

*	The **Welcome box** provides your entry to querying data, described in more detail below.
*	A **Bar graph** breaks down number of samples per modality per study. 
*	The **Data Portal Summary bar** at the bottom provides a high level summary of all data currently available through the VMRC portal.


![VMRC Homepage](images/portal/1.VMRC_portal_homepage.png)

*<p align="center">Fig. 1 : The VMRC portal landing page showing the Welcome box (left) , Bar graph breakdown of samples per modality and study (right) and the Data Portal Summary bar (bottom)</p>*

## Welcome Box

Users can begin exploring data by study or through the faceted or advanced search options. The **Studies** button takes users to a summary page listing available studies, with links to all samples or all files associated with each study. The **Data** button takes users to the faceted data search page, the heart of the portal's functionality. 
Below these buttons is a set of pre-defined queries. For example, the second query can be used to easily retrieve all isolate genome data files associated with VMRC_HMP_UMD study.

## Studies Page

The **Studies** page lists all available studies along with counts of associated samples and files, including both raw and processed files (Fig. 2). Clicking on the files or samples associated with a particular study allows users to work with that subset of data. Links to abundance matrix files are also available for each study, enabling direct access. 

Files in the portal belong to two data categories:

* **Primary** : Raw sequencing files, assembly files, annotation files 
* **Summary** : Analysis files such as Abundance matrices, KEGG Taxonomy, Report files etc. 

The contact Principal Investigator (PI) for each study is also displayed on this page. Users can customize the displayed columns using the hamburger   icon in the upper right corner.

![VMRC Studies](images/portal/2.Studies_summary_page.png)

*<p align="center">Fig. 2 : Summary page of available studies with links to associated samples and files</p>*


## Faceted Data Search Page

The VMRC Data Portal provides a simple faceted search query interface to help identify the data of interest. The faceted search page (Fig. 3), accessible through the **Data** button of the landing page welcome box, is divided into 3 sections: **Faceted search box**, the **Advanced Search box** and the **Summary results panel**.

![VMRC Faceted Data Search](images/portal/3.Faceted_data_search_page.png)

*<p align="center">Fig. 3: Faceted Search page accessible through the Data button of the landing page</p>*

The faceted search box on the left is a filter panel that allows users to select one or more of the available facets to narrow down the samples of interest (*See #1 in Fig. 4*). Selecting any facet automatically populates the advanced search box with the current query (*See #2 in Fig. 4*). The summary results panel provides dynamic pie charts summarizing data corresponding to the currently selected filters (*See #3 in Fig. 4*).

![VMRC Faceted search page 2](images/portal/4.Faceted_search_page_grouped.png)

*<p align="center">Fig. 4 : Screenshot of the Faceted Data Search page showing the 1) Faceted search box, 2) Advanced search box and 3) Summary results panel</p>*


### Faceted Search Box

The faceted search box contains two tabs of pre-configured facets associated with
* **Samples** (study, modality, stability category, geographic location, host age group, pregnancy status and entity type), or
* **Files** (data category, data type, file format, data access)
Adding Filters to the Faceted Search box:

Additional facets are available by **Add a Filter** in the upper right of the faceted search panel. The resulting pop-up lists all additional searchable facets available, which can be browsed or searched for using the search bar at the top. Clicking on any facet will add it to the top of the filter panel for incorporation into the current filter. 


![VMRC Add a filter](images/portal/5.Add_a_filter.png)

*<p align="center">Fig. 5: Adding filters to the Faceted search box. A pop up appears where you can search for available file, sample, subject and study-specific facets</p>*


Figure 5 illustrates how to add a filter and search for available facets using the search bar that pops up.  Note that **HIV Status** is not listed as a default facet under **Samples** tab in the faceted search panel. However, when you add **HIV Status** as a filter, it appears under **Samples** in the faceted search panel, as you can see in the figure below (*Fig. 6*). 

Users can also search for and add additional filters that are file-, sample-, subject- or study-specific. All study-, sample- and subject-level facets that are added will appear under the **Samples** tab in the faceted search panel, while file-specific facets will appear under the **Files** tab. A complete list of all available facets in the portal, along with their descriptions, is provided in a spreadsheet accessible via the **Documentation** option under the **Apps** button in the upper-right corner (*Fig. 17*).

To remove filters, you can either click **Remove Added Filters** to clear all added filters or remove individual filters by clicking the red **X** next to the corresponding filter.

Next to each filter, the alphabet (**AZ**) icon allows you to sort the filter terms in ascending or descending order. This is especially helpful when working with long lists of search terms, such as sample taxonomy for isolate genomes.

![VMRC Add a filter 2](images/portal/6.Remove_filter.png)

*<p align="center">Fig. 6: Screenshot illustrating how an added filter (HIV Status) appears in the Faceted search box,how to remove added filters and how to search for available search facets</p>*


### Summary Results Panel

The results from the faceted search box and additional filters are organized into three views - **Summary**, **Samples** and **Files**. 

Under the **Summary** tab, results are displayed as pie charts showing file counts by modality, community state type, taxonomy, geographic location, data type and file format. 

The number displayed next to each facet in the faceted search panel corresponds to the total number of samples associated with this attribute across all projects in the portal. This number does not change dynamically as facets are selected or deselected. What does change is the summary results panel. As facets are selected, the file count, sample count and total file volume will update to reflect the current filter(s). The pie charts also update accordingly. 

Hovering over a pie chart displays count information for each component. Each summary pie chart also includes a table icon in the upper right corner. Selecting this icon switches the view to a table showing counts of files and total file size for each component, allowing users to toggle between chart and table views.


<p float="left">
  <img src="images/portal/7a.pie_view.png" width="45%" />
  <img src="images/portal/7b.table_view.png" width="44%" />
</p>

*<p align="center">Fig.7: Screenshot of the Pie chart (left) representing File Counts by Modality, with the 16Samplicon component selected. The table view (right) lists file counts and total file volume, by modality</p>*

The **Samples** tab in the Summary results panel lists all the samples associated with the query. By default, the displayed columns include study, subject, entity type, taxonomy and community state type.  Users can customize the displayed columns using the hamburger icon in the upper right corner. 

Similarly, the **Files** tab lists files that match the search query, along with details such as file format, data type, file size, data access status (open or restricted), and the contact PI’s name, for obtaining additional information, especially regarding restricted data. 


#### Example Queries:

**A.	Retrieve all abundance matrix files from 16samplicon processing of VMRC_PreSSMat samples**

1.	Click the **Data** button in the welcome box to access the faceted search page
2.	In the **Samples** tab of the faceted search box, select:
    * ‘VMRC_PreSSMat’ under **Study** and 
    * ‘16Samplicon’ under **Modality**
3.	Switch to the Files tab of the faceted search box and select:
    * ‘summary’ as **Data category** and 
    * ‘Abundance matrix’ as **Data type**


The **Summary** tab of the Summary  Results panel will update the pie charts according to the search results. The **Files** tab in the Summary results panel will list all the 16Samplicon abundance matrix files as shown in the Fig. 8. The corresponding Advanced search query is automatically populated in the Advanced search box, as you make selections (also illustrated in Fig. 8).


![VMRC Example 1](images/portal/8.example1.png)

*<p align="center">Fig. 8 : Screenshot of the files tab of the Summary results panel listing the 16Samplicon Abundance matrix files from VMRC_PreSSMat study samples</p>*
















