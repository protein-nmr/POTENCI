# POTENCI (python3 version available from Feb 2026)
Random Coil Chemical Shift predictor from sequence

If you use POTENCI, please cite JT Nielsen &amp; FAA Mulder, J Biomol NMR 70(3):141-165 (2018)
reference to our work is kind and fair, and will help sustain funding to our lab

requires: python2.x with numpy and scipy

usage: python2.x potenci1_2.py seqstring pH temperature ionicstrength [pkacsvfile] > logfile

arguments: seqstring is single-letter code amino acid sequence. Supply pH, temperature (K), and ion (M)
optional filename in csv format contains predicted pKa values and Hill parameters,
the format of the pkacsvfile must be the same as the output for pepKalc,
only lines after "Site" is read. If this is not found no pH corrections are applied.

output:
  Table textfile in SHIFTY format (space separated)
  average of methylene protons are provided for Gly HA2/HA3 and HB2/HB3.
  
    #NOTE:pH corrections is applied if pH is not 7.0
    #NOTE:pKa predictions are stored locally and reloaded if the seq, temp and ion is the same.
    #NOTE:at least 5 residues are required. Chemical shift predictions are not given for terminal residues.
    #NOTE:change the value of VERB in the top of this script to have verbose logfile
