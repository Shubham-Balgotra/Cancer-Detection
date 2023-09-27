# <h1 align= center>Cancer-Diagnosis</h1>
![cover image](cancer_cover.jpg)
## * Description:
<p> Source: https://www.kaggle.com/c/msk-redefining-cancer-treatment/ </p>
<p> Data: Memorial Sloan Kettering Cancer Center (MSKCC)</p>
<p> Download training_variants.zip and training_text.zip from Kaggle.</p> 

<h6> Context:</h6>
<p> Source: https://www.kaggle.com/c/msk-redefining-cancer-treatment/discussion/35336#198462</p>

<h6> Problem statement : </h6>
<p> Classify the given genetic variations/mutations based on evidence from text-based clinical literature. </p>

## * Real-world/Business objectives and constraints:
* No low-latency requirement.
* Interpretability is important.
* Errors can be very costly.
* Probability of a data-point belonging to each class is needed.

## * Data Overview:
- Source: https://www.kaggle.com/c/msk-redefining-cancer-treatment/data
- We have two data files: one conatins the information about the genetic mutations and the other contains the clinical evidence (text) that  human experts/pathologists use to classify the genetic mutations. 
- Both these data files are have a common column called ID
- <p> 
    Data file's information:
    <ul> 
        <li>
        training_variants (ID , Gene, Variations, Class)
        </li>
        <li>
        training_text (ID, Text)
        </li>
    </ul>
</p>

## * Example data:
<h6>training_variants</h6>
<hr>
ID,Gene,Variation,Class<br>
0,FAM58A,Truncating Mutations,1 <br>
1,CBL,W802*,2 <br>
2,CBL,Q249E,2 <br>
...

<h6> training_text</h6>
<hr>
ID,Text <br>
0||Cyclin-dependent kinases (CDKs) regulate a variety of fundamental cellular processes. CDK10 stands out as one of the last orphan CDKs for which no activating cyclin has been identified and no kinase activity revealed. Previous work has shown that CDK10 silencing increases ETS2 (v-ets erythroblastosis virus E26 oncogene homolog 2)-driven activation of the MAPK pathway, which confers tamoxifen resistance to breast cancer cells. The precise mechanisms by which CDK10 modulates ETS2 activity, and more generally the functions of CDK10, remain elusive. Here we demonstrate that CDK10 is a cyclin-dependent kinase by identifying cyclin M as an activating cyclin. Cyclin M, an orphan cyclin, is the product of FAM58A, whose mutations cause STAR syndrome, a human developmental anomaly whose features include toe syndactyly, telecanthus, and anogenital and renal malformations. We show that STAR syndrome-associated cyclin M mutants are unable to interact with CDK10. Cyclin M silencing phenocopies CDK10 silencing in increasing c-Raf and in conferring tamoxifen resistance to breast cancer cells. CDK10/cyclin M phosphorylates ETS2 in vitro, and in cells it positively controls ETS2 degradation by the proteasome. ETS2 protein levels are increased in cells derived from a STAR patient, and this increase is attributable to decreased cyclin M levels. Altogether, our results reveal an additional regulatory mechanism for ETS2, which plays key roles in cancer and development. They also shed light on the molecular mechanisms underlying STAR syndrome.Cyclin-dependent kinases (CDKs) play a pivotal role in the control of a number of fundamental cellular processes (1). The human genome contains 21 genes encoding proteins that can be considered as members of the CDK family owing to their sequence similarity with bona fide CDKs, those known to be activated by cyclins (2). Although discovered almost 20 y ago (3, 4), CDK10 remains one of the two CDKs without an identified cyclin partner. This knowledge gap has largely impeded the exploration of its biological functions. CDK10 can act as a positive cell cycle regulator in some cells (5, 6) or as a tumor suppressor in others (7, 8). CDK10 interacts with the ETS2 (v-ets erythroblastosis virus E26 oncogene homolog 2) transcription factor and inhibits its transcriptional activity through an unknown mechanism (9). CDK10 knockdown derepresses ETS2, which increases the expression of the c-Raf protein kinase, activates the MAPK pathway, and induces resistance of MCF7 cells to tamoxifen (6). ... 

## * Mapping the real world problem to ML problem:
<p>
    
            There are nine different classes a genetic mutation can be classified into => Multi class classification problem
   
      
    
</p>

## * Performance Metric:
Source: https://www.kaggle.com/c/msk-redefining-cancer-treatment#evaluation

Metric(s): 
* Multi class log-loss 
* Confusion matrix 

## * Result/Outcome:
### Predicted Class
Predicted Class: 4
69.27% sure that the

### Predicted Class Probabilities
Predicted Class Probabilities: [[0.06, 0.0778, 0.0207, 0.6927, 0.0457, 0.0384, 0.0549, 0.0055, 0.0043]]

### Actual Class
Actual Class: 4

---

### Text Features Present in Test Data Point
- Text feature [identified] present in test data point [True]
- Text feature [well] present in test data point [True]
- Text feature [observed] present in test data point [True]
- Text feature [additional] present in test data point [True]
- Text feature [recently] present in test data point [True]
- Text feature [previously] present in test data point [True]
- Text feature [using] present in test data point [True]
- Text feature [mutation] present in test data point [True]
- Text feature [found] present in test data point [True]
- Text feature [one] present in test data point [True]
- Text feature [studies] present in test data point [True]
- Text feature [also] present in test data point [True]
- Text feature [however] present in test data point [True]
- Text feature [10] present in test data point [True]
- Text feature [compared] present in test data point [True]
- Text feature [table] present in test data point [True]
- Text feature [showed] present in test data point [True]
- Text feature [three] present in test data point [True]
- Text feature [may] present in test data point [True]
- Text feature [used] present in test data point [True]
- Text feature [respectively] present in test data point [True]
- Text feature [presence] present in test data point [True]
- Text feature [data] present in test data point [True]
- Text feature [addition] present in test data point [True]
- Text feature [analysis] present in test data point [True]
- Text feature [expected] present in test data point [True]
- Text feature [independent] present in test data point [True]
- Text feature [12] present in test data point [True]
- Text feature [mutations] present in test data point [True]
- Text feature [different] present in test data point [True]
- Text feature [higher] present in test data point [True]
- Text feature [present] present in test data point [True]
- Text feature [two] present in test data point [True]
- Text feature [identify] present in test data point [True]
- Text feature [including] present in test data point [True]
- Text feature [known] present in test data point [True]
- Text feature [15] present in test data point [True]
- Text feature [confirmed] present in test data point [True]
- Text feature [identification] present in test data point [True]
- Text feature [reported] present in test data point [True]
- Text feature [highly] present in test data point [True]
- Text feature [cancer] present in test data point [True]
- Text feature [similar] present in test data point [True]
- Text feature [clinical] present in test data point [True]
- Text feature [25] present in test data point [True]
- Text feature [selected] present in test data point [True]
- Text feature [small] present in test data point [True]
- Text feature [obtained] present in test data point [True]
- Text feature [cell] present in test data point [True]
- Text feature [confirm] present in test data point [True]
- Text feature [significant] present in test data point [True]
- Text feature [discussion] present in test data point [True]
- Text feature [total] present in test data point [True]
- Text feature [increased] present in test data point [True]
- Text feature [16] present in test data point [True]
- Text feature [1b] present in test data point [True]
- Text feature [shown] present in test data point [True]
- Text feature [single] present in test data point [True]

Out of the top 100 features, 58 are present in the query point.

