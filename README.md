# SCARFS

This is the dataset described in the paper:

> Trott, S., Bergen, B., Wittenberg, E. (Under Review) SCARFS Database: Spontaneous, Controlled Acts of Reference between Friends and Strangers. 

## Data

### Primary data files 

The key data files can be found in `data/processed`:

- `data/processed/aligned_results_public.csv`: the complete corpus of nominal referring expressions (NREs), all anonymized and time-locked to the game data.  
- `data/processed/behavioral_results_public.csv`: the original game data (i.e., without the linguistic corpus).  
- `data/processed/full_nps.csv`: a reduced dataset of the complete corpus, containing only NREs that were classified as Full NPs.  

#### Relevant features

The complete corpus file has a number of columns. We anticipate that the most relevant will be:

- `RE_type`: the form of the referring expression (e.g., full NP vs. 3rd-person pronoun).
- `RE_type_granular`: a more granular breakdown of RE form.  
- `card`: the topic being communicated.  
- `dep`: the dependency arc label for the NRE.  
- `det`: the determiner used, if relevant.  
- `final_transcription`: the complete, corrected utterance from which the NRE was extracted.  
- `head_noun`: the head noun for the NRE (primraily relevant for Full NPs).  
- `head_noun_tag`: the type of noun for the head noun (e.g., plural or singular).  
- `length`: the number of words for the NRE.
- `raw_utterance`: the original transcription for that utterance (uncorrected).  
- `round`: the round in which that utterance occurred (out of 8).  
- `session_id`: the session ID.  
- `text`: the text of the NRE itself.  
- `trial_with_partner`: an index indicating how many trials the participant has completed with their partner.  
- `trial_result`: the outcome of the trial.  
- `ppt_id`: the ID of the particiapnt.  
- `partner_id`: the ID of the partner.

Other columns include other individual level characteristics, which may or may not be of interest, such as the participant's MINT score (`MINT_Score_Uncued_Correct`).

### Lexical statistics

The analyses of the behavioral data involve a number of lexical statistics, including:  

- Age of acquisition (`AoA_ratings_Kuperman_et_al_BRM.csv`) 
- Concreteness (`brysbaert_norms.csv`)  
- Frequency (`taboo_with_distances.csv`)  
- The semantic distance between the target and Taboo words (`taboo_with_distances.csv`) 
- Lancaster Sensorimotor Norms (`lancaster_norms.csv`)   

## Analyses

Finally, the key analyses can be found in `analyses/reports`:

- `behavioral_analysis_public.Rmd`: the analysis of the game data.  
- `target_word_analysis.Rmd`: analyses about how properties of the target word correspond to trial success.  
- `linguistic_analysis_prereg.Rmd`: the pre-registered analyses of the corpus data itself.  

Additionally, the Jupyter notebook "Guessing Game" contains the code to run the guessing game described in the experiment. (Note that this depends on the [Glove dataset](https://www.kaggle.com/thanakomsn/glove6b300dtxt), which is too large to include in the GitHub directory).

