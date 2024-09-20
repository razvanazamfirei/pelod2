![GitHub release (latest SemVer)](https://img.shields.io/github/v/release/razvanazamfirei/pelod2?style=flat-square)
![DOI](https://img.shields.io/badge/doi-10.2478%2Fjccm--2023--0033-blue?style=flat-square)
![GitHub](https://img.shields.io/github/license/razvanazamfirei/pelod2?style=flat-square)

# Getting Started

This is a command developed for the calculation of Pediatric Logistic Organ Dysfunction 2 (PELOD-2) scores.

Azamfirei, Razvan; Mennie, Colleen; Fackler, James; Kudchadkar, Sapna R. Pediatric Critical Care Illness Severity Toolkit: Stata Commands for Calculation of Pediatric Index of Mortality and Pediatric Logistic Organ Dysfunction Scores. The Journal of Critical Care Medicine 10(1):16-18, January 2024. | DOI: 10.2478/jccm-2023-0033

For detailed documentation, please visit the [PCCM Toolkit Command Documentation](https://azamfirei.com/pccmtoolkit/pelod2).


## Installation Instructions

### Using net

Open Stata. Run the following command:

```stata
net install pelod2, from(https://azamfirei.com/pelod2)
```

### Using ssc

Open Stata. Run the following command:

```stata
ssc install pccmtoolkit
```

### Manually

Download all files from the /src subfolder. Copy them into your adopath. If you're not sure where that is, run the following:

```stata
adopath
```

The output will look similar to this: *(your directories will differ depending on your OS)*

```stata
[1]  (BASE)      "/Applications/Stata/ado/base/"
[2]  (SITE)      "/Applications/Stata/ado/site/"
[3]              "."
[4]  (PERSONAL)  "/Users/{yourusername}/Documents/Stata/ado/personal/"
[5]  (PLUS)      "/Users/{yourusername}/Library/Application Support/Stata/ado/plus/"
[6]  (OLDPLACE)  "~/ado/"
```

Open the directory listed under (PLUS). Copy the files into the folder. For extra style-points, find the `p` subfolder, and copy the files there.

## Usage Instructions

For more information about the PELOD-2 score see the following references.[^1] There are two main ways of running this command.

[^1]: Leteurtre S, Duhamel A, Salleron J, Grandbastien B, Lacroix J, Leclerc F; Groupe Francophone de Réanimation et d’Urgences Pédiatriques (GFRUP). PELOD-2: an update of the PEdiatric logistic organ dysfunction score. Crit Care Med. 2013 Jul;41(7):1761-73.

### Stata dialog

Launch the dialog with `db pelod2`. Alternatively, add this line to your profile.do file:

```stata
window menu append item "stUserData" "PELOD Score" "db pelod2"
```

If you do not already have one, open a dofile editor, copy the line above, and save it as profile.do in your personal directory.
See [Manual Installation](#manually) instructions; your personal directory is folder (PERSONAL)

### Command-Line Interface

```stata
pelod2 [syntax]
```

See `help pelod2` for more information.

