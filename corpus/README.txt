-----------------------------------------------------------------------
corpus.csv - Contains all the editorials and their acquired summaries 
-----------------------------------------------------------------------
Note: (X = [1,5] for five summaries)

- article_id : Article ID in the corpus
- title : Title of the editorial
- article_text : Plain text of the editorial
- summary_{X}_text : Plain text of the corresponding summary 
- thesis_{X}_text : Plain text of the thesis from the corresponding summary
- lead : top 15% of the editorial's segments
- body : segments between lead and conclusion sections
- conclusion : bottom 15% of the editorial's segments
- article_segments: Collection of paragraphs, each further divided into collection of segments containing:
 { "number": segment order in the editorial,
   "text" : segment text,
   "label": ADU type
 }
- summary_{X}_segments: Collection of summary segments containing:
{ "number": segment order in the editorial,
  "text" : segment text,
  "adu_label": ADU type from the editorial,
  "summary_label": can be 'thesis' or 'justification'
}

------------------------------------------------------------------------------------------------------------------
quality-groups.csv - Contains the IDs for high(and low)-quality summaries for each quality dimension per editorial
------------------------------------------------------------------------------------------------------------------
For example: article_id 2 has four high_quality summaries (summary_1, summary_2, summary_3, summary_4) and one low_quality summary (summary_5) in terms of overall quality.
The summary texts can be obtained from corpus.csv respectively.
