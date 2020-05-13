# ANALYSE-AND-CLASSIFY-MUSIC-BY-LYRICS
<b>Group Members: Danlei Qian, Siqi Jiang, Xi Zhang</b><br>
Music emotion recognition and recommendation is changing the way people find and listen to music they like. And Lyrics can deliver emotions. So it provides an opportunity for NLP mode to analyze.The accurate classification of music enables the media to quickly match the audience, thus making the music market more efficient.
<img align="center" src="https://github.com/xzhangfox/ANALYSE-AND-CLASSIFY-MUSIC-BY-LYRICS/blob/master/img/767271-cool-coldplay-wallpapers-3840x2160-notebook.jpg" />
# Requirements
* Python 3
* NLTK
* pyLDAvis
* pandas
* aux_bisect
# Motivation
We wanted to use what we learned in the NLP course to make the lyric data truly marketable. To achieve this goal, we fixed the research framework on the goal of how to make the lyrics data needed by the market. You will see in our project how we preprocess the data, adjust and select the optimal model, and how the final result is applied to the actual example.
# Workflow
<img align="center" src="https://github.com/xzhangfox/ANALYSE-AND-CLASSIFY-MUSIC-BY-LYRICS/blob/master/img/Screen%20Shot%202020-05-12%20at%205.59.03%20PM.png" />

# Data
<img align="center" src="https://github.com/xzhangfox/ANALYSE-AND-CLASSIFY-MUSIC-BY-LYRICS/blob/master/img/Picture1.png" />
Our data is from the million song dataset website and we randomly select 1000 songs from it. But the dataset doesn’t include lyrics. Therefore, we wrote script by python to download lyrics from Lyric Wiki by searching artist and music titles.

# Preprocessing
<img align="center" src="https://github.com/xzhangfox/ANALYSE-AND-CLASSIFY-MUSIC-BY-LYRICS/blob/master/img/Screen%20Shot%202020-05-12%20at%208.53.41%20PM.png" />
The basic lexicon we used for filtering of lyrics is ANEW (Affective Norms for English Words) which provides a set of normative emotional ratings for 1034 unique English words. Since our dataset wasn't big enough, we incorporated another sentiment lexicon, which contained both positive and negative emotions, to filter out more words that contained emotions.

# Modeling
We decided to use the Latent Dirichlet Allocation model(LDA). LDA is a generative probabilistic model that assumes each topic is a mixture over an underlying set of words, and each document is a mixture of over a set of topic probabilities. Compared to the other topic models like Latent semantic analysis(LSA) and Hierarchical Dirichlet Process(HDP), the LDA model gives us the best Topic Coherence, which measures the degree of semantic similarity between high scoring words in the topic.
If you are interested in more details, please move to our [report](https://github.com/xzhangfox/ANALYSE-AND-CLASSIFY-MUSIC-BY-LYRICS/blob/master/Report/NLP%20Final%20Report.pdf).

# References
* Kaggle:https://www.kaggle.com/mousehead/songlyrics
* Oramas, S.(2018), Natural Language Processing for Music Knowledge Discovery,https://arxiv.org/abs/1807.02200
* Oramas, S.(2018), Natural Language Processing for Music Information Retrieval,https://www.upf.edu/web/mdm-dtic/tutorial-natural-language-processing-for-music-information-retrieval
