# TroFi Metaphor Dataset

    Begin3
    Title:          TroFi Example Base
    Version:        1.0
    Entered-date:   11 July 2005
    Description:    A database of literal/nonliteral sentence clusters for 50 words
    Keywords:       clustering nonliteral metaphor nlp
    Author:         Julia Birke <jbirke@alumni.sfu.ca>
    Maintained-by:  Anoop Sarkar <anoop@sfu.ca>
    Home-page:      http://natlang.cs.sfu.ca/
    Alternate-site:
    Primary-site:   http://natlang.cs.sfu.ca/software/trofi.html
    Platform:       
    Copying-policy: GPL
    End3           

## Data:

* [TroFi Example Base](TroFiExampleBase.txt)

If you use this data, please cite the following paper(s):

* [Clustering Approach for the Nearly Unsupervised Recognition of Nonliteral Language](http://aclweb.org/anthology/E/E06/E06-1042.pdf). Julia Birke and Anoop Sarkar. In Proceedings of the 11th Conference of the European Chapter of the Association for Computational Linguistics, EACL-2006. Trento, Italy. April 3-7, 2006.
* [Active Learning for the Identification of Nonliteral Language](http://aclweb.org/anthology/W/W07/W07-0104.pdf). Julia Birke and Anoop Sarkar. In Proceedings of the Workshop on Computational Approaches to Figurative Language, NAACL-HLT 2007 workshop. Rochester, NY. April 26, 2007.

Before installing please read the contents of the [LICENSE](LICENSE.html) file that accompanies this distribution.

## General Description:

The TroFi Example Base consists of literal and nonliteral usage clusters for 50 English verbs.  The clusters contain sentences using these words drawn from The 1987-89 Wall Street Journal (WSJ) Corpus Release 1.  The clusters were automatically generated using TroFi, a system for the unsupervised recognition of nonliteral language.  For detailed information on the TroFi Example Base and the system used to produce it, please see:

* Birke, J. 2005.  [A clustering approach for the unsupervised recognition of nonliteral language](jbirke_thesis.pdf). Masters Thesis. School of Computing Science.  Simon Fraser University.
* [EACL 2006 Presentation Slides](Presentation_EACL06.ppt)

## Contents:

The TroFi Example Base contains literal/nonliteral clusters for the following words:

|            |             |          |          |          |
|------------|-------------|----------|----------|----------|
| absorb     | drink       | flow     | pass     | sleep    |
| assault    | drown       | fly      | plant    | smooth   |
| attack     | eat         | grab     | play     | step     |
| besiege    | escape      | grasp    | plow     | stick    |
| cool       | evaporate   | kick     | pour     | strike   |
| dance      | examine     | kill     | pump     | stumble  |
| destroy    | fill        | knock    | rain     | target   |
| die        | fix         | lend     | rest     | touch    |
| dissolve   | flood       | melt     | ride     | vaporize |
| drag       | flourish    | miss     | roll     | wither   |
-------------------------------------------------------------

Average accuracy is estimated at approximately 64%.


## Structure:

The TroFi Example Base is organized by the target words listed above.  Under each target word, first the nonliteral cluster, then the literal cluster, is given.  The order of the examples is dependent on the TroFi run in which they were clustered.  The examples from the original run are given first, in numerical order; the examples from the iterative augmentation run are given next. (See [Birke, 2005](jbirke_thesis.pdf))

The examples contain three tab-delimited columns.  

The first column contains an identifier to link the sentence back to the WSJ source files used by TroFi.  For TroFi, the WSJ sentences were split into 86 files.  In an identifier, for example wsj02:2251, the first number is the file number; the second, the line within that file.  

The second column contains one of three labels for the status of human annotation: L (Literal), N (Nonliteral), or U (Unannotated).  There are two reasons a sentence may have an annotation of L or N.  For the first run, all the sentences were manually annotated for testing purposes.  For the iterative augmentation run, only those sentences that were sent to the human for active learning (Birke, 2005) will have an L or N label.  All other sentences have a U label for "Unannotated".  

The third column is the tokenized WSJ sentence.  Each sentence ends with "./."

For example:

    ***absorb***
    *nonliteral cluster*
    wsj02:2251  U   Another option will be to try to curb the growth in education and other local assistance , which absorbs 66 % of the state 's budget ./.
    wsj03:2839  N   But in the short-term it will absorb a lot of top management 's energy and attention , '' says Philippe Haspeslagh , a business professor at the European management school , Insead , in Paris ./.
    *literal cluster*
    wsj11:1363  L   An Energy Department spokesman says the sulfur dioxide might be simultaneously recoverable through the use of powdered limestone , which tends to absorb the sulfur ./.

