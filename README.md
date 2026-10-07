## Reproducing DeepRBPL Results Using Your Own Dataset

The following procedure describes how to reproduce DeepRBPL results using your own positive and negative protein sequence datasets.

### Step 1: Generate PSSM Features for the Positive Dataset

Use the R code provided in `DeepRBPL.R` to extract PSSM features from your **positive dataset containing RBP sequences**.

Save the resulting feature file as:

```text
positive_feature.txt
```

### Step 2: Generate PSSM Features for the Negative Dataset

Use the R code provided in `DeepRBPL.R` to extract PSSM features from your **negative dataset containing non-RBP sequences**.

Save the resulting feature file as:

```text
negative_feature.txt
```

### Step 3: Create the Training Directory

Create a new directory named:

```text
Training_DeepRBPL
```

Place the following three files inside this directory:

```text
Training_DeepRBPL/
├── positive_feature.txt
├── negative_feature.txt
└── Train_DeepRBPL.py
```

### Step 4: Open the Terminal

Open a terminal and navigate to the `Training_DeepRBPL` directory:

```bash
cd Training_DeepRBPL
```

### Step 5: Train the DeepRBPL Model

Run the following command:

```bash
python Train_DeepRBPL.py positive_feature.txt negative_feature.txt
```

The script will train the DeepRBPL model using the supplied positive and negative PSSM feature datasets.

### Step 6: Access the Results

After training is completed, the generated results will be stored in the following output directory:

```text
Training_DeepRBPL/
└── DeepRBPL_Training_Results/
```

The `DeepRBPL_Training_Results` folder contains the output files generated during the DeepRBPL training procedure.

---

## Developers

* **Dr. Anil Kumar**, ADG (TC), ICAR-IASRI, New Delhi, India
* **Dr. Prabina Kumar Meher**, Senior Scientist, ICAR-IASRI, New Delhi, India
* **Dr. Upendra Kumar Pradhan**, Senior Scientist, ICAR-IASRI, New Delhi, India

