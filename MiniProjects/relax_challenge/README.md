This dataset of 12,000 users who signed up for a product and logged in between May 31, 2012 and June 6, 2014 was evaluated to identify factors that can predict user adoption.  An adopted user was defined as "a user who has logged into the product on three separate days in at least one seven day period."

Once adopted users were identified and coded as a variable, unnecessary features (such as creation time and name) were removed. The creation source variable was hot encoded.

Logistic regression as a predictive model was tried first, but proved unsuccessful due to the imbalanced class weights in the adopted feature.  Random forest classification was used more successfully, to create an untuned model with ~80% accuracy.

The features of greatest importance in generating user adoption appear to be org_invite (invited to the organization as a full member) and invited_by_user_id (the user who invited the adopted user).  These factors appear to be the primary drivers in user adoption.
