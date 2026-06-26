# Supply Chain Control Tower: Predictive Logistics (Machine Learning)
## Business Task
Shift from reactive to proactive supply chain management by building a Machine Learning model capable of predicting late delivery risks at the point of checkout, allowing warehouse managers to dynamically adjust routing and shipping modes.
## Tech Stack & Data Processing
- Python (Pandas, Scikit-Learn): Processed 180,000+ rows of global supply chain data.
- Data Engineering: Prevented data leakage by isolating checkout-phase variables. Utilized One-Hot Encoding (pd.get_dummies) to transform categorical variables (Shipping Mode, Region) into binary features.
- Machine Learning: Trained and evaluated a Random Forest Classifier using an 80/20 train-test split to predict binary outcomes (Late_delivery_risk).
## The BLUF (Key Insights from the AI)
By extracting feature_importances_ from the Random Forest model, the algorithm identified the root causes of delayed shipments:

- Order Item Total (Value): High-value orders have a distinct correlation with delivery delays, likely due to additional customs or fraud-check bottlenecks.
- Standard Class Shipping: The model heavily penalized 'Standard Class' shipping modes to specific regions, marking them as the primary operational bottleneck.
## Strategic Recommendations
- Dynamic Upgrades: Integrate this predictive model into the checkout architecture. If the algorithm flags a high-value cart with an 80%+ late probability, automatically upgrade the customer to 'First Class' shipping on the backend to protect brand loyalty.
- Regional SLA Audit: Initiate an immediate vendor audit for 'Standard Class' logistics partners operating in the highest-risk regions identified by the model.
