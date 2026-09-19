🏷️ **Cancer Through Time**

**Introduction**
This project traces how cancer has been talked about, funded, and survived in the US from the 1970s to today. It was built for my Machine Learning course, taught by Dr. Sarwath Unnisa, whose patience while walking us through concepts I was picking up from scratch made a genuinely difficult subject feel approachable — I'm grateful for that.

**Why This Project**
I've been listening to The Rest Is Science (sponsored by Cancer Research UK), and it got me thinking about cancer in a way I hadn't before — how differently people spoke about it in the 1970s compared to now, how survival rates have actually moved over fifty years, and how research funding ties into both. That's exactly what this project sets out to depict: the language, the survivorship, and the funding, side by side, across eras.

**What This Project Aims For**
Past the technical side, this project is also about perspective. Looking at the language shift across eras — from phrases people could barely say out loud in the 1970s, to the matter-of-fact, even hopeful language around treatment and survivorship today — is a small way of tracking how much has changed. Cancer used to be spoken about only in dread; now it's spoken about in terms of moonshots, personalized treatment, and survivors telling their own stories. I'd like this project to leave a bit of that with anyone who goes through it: a reminder that a disease once treated as almost unspeakable is one we've learned, gradually and with real progress behind it, to face and fight bravely.

**Bringing In Economics and Statistics**
I'm majoring in Economics, Mathematics, and Statistics, and this project let me put both to direct use rather than treating them as background. The funding-and-survival half of the project (Part B) is essentially applied economics — real NCI funding figures and SEER survival data, modeled with regression to see how one moves with the other over time. Statistics runs through both halves of the project: stratified train/test splits, 5-fold cross-validation to check that model rankings aren't just an artifact of one lucky split, RMSE for the regression side, and confidence thresholds on the classifier so it can honestly say "I'm not sure" instead of guessing.

**What the Notebook Does**
Part A — Language across eras: cleans a hand-built dataset of era-representative cancer-related phrases (1970s to 2020s) labeled by tone, vectorizes them with TF-IDF, and trains/compares four classifiers (Decision Tree, KNN, Random Forest, SVM) to predict tone from phrasing, validated with cross-validation for a steadier estimate.
Part B — Funding and survival: uses real and interpolated NCI funding + 5-year survival rate figures from 1976–2025 to train and compare four regressors (Decision Tree, KNN, Random Forest, Linear Regression) predicting survival rate from year and funding.
Interactive Year Explorer: a slider from 1976–2025 showing that year's era, a representative phrase and its predicted tone, that year's funding, and a predicted survival rate — tagged as actual SEER data, interpolated, extrapolated, or a model prediction, so it's always clear which numbers are real and which are estimated.
Guess the Era: type any sentence about cancer and the trained model guesses which decade it sounds like it's from, with guardrails for unrelated or low-confidence input.

**How to Run It**
Open in Google Colab, run all cells top to bottom, and upload cancer_through_time.csv when prompted — the funding/survival table is already built into the notebook.

**Looking Ahead**
This project made me want to keep working with machine learning well beyond this course — there's a lot more I want to learn and build.
