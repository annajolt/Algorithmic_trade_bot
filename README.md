# **Algorithmic Trading Bot - Report**
----
## *Comparing Trading Models and the Results*

Mutliple algorithmic trading models were used to build a trading bot that would predict actual returns using trade signals. The SVC Classifier, ADA Booster Classifier, and Decision Tree Classifier models were used on datasets with variations in short/long day trading signals and number of month offsets.

The 3 month offset with a 4-day short and 100-day long window model presented the following results:

<img src="Resources/svc_3mo.png" alt="svc_3mo" width="400"/>
<img src="Resources/decision_tree_3mo.png" alt="decision_tree_3mo" width="400"/>
<img src="Resources/ada_3mo.png" alt="ada_boost_3mo" width="400"/>

The tuned 4 months offset with a 7-day short and 180 day long model presented the following results:
<img src="Resources/svc_6mo.png" alt="svc_6mo" width="400"/>
<img src="Resources/decision_tree_6mo.png" alt="decision_tree_6mo" width="400"/>
<img src="Resources/ada_6mo.png" alt="ada_boost_6mo" width='400'/>


Based on these results, the ADA Booster Classifier model proved to be a much better algorithmic trading model. Especially so, with the short and long term signals at 7-day and 180-day intervals and a 4 month offset. This is not only shown in the graph, but also in the classification report --- where the count balance for buy/sell trades was the most balanced.

<img src='Resources/class_report_ada_6mo.png' alt='ADA Booster Classification Report - 4month offset' width='400'/>


*Did this new model perform better or worse than the provided baseline model? Did this new model perform better or worse than your tuned trading algorithm?*

The new and tuned trading algorithm models worked better than the one baseline model that used the SVC Classifier. ADA Booster and Decision Tree models even performed better with the 4-day short, 100-day long and 3 months offset parameters. One concern that could be raised, is the number of support values for buy/sell trades that were shown on the classification report for ADA Booster and Decision Tree. The numbers were very imbalanced. 

The imbalance was fixed, once the parameters were changed.

