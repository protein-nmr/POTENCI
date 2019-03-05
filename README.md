# POTENCI
random coil chemical shift predictor (JT Nielsen &amp; FAA Mulder, 2018)

#########POTENCI###########
    #requires: python2.x with numpy and scipy
    #usage: potenci1_2.py seqstring pH temperature ionicstrength [pkacsvfile] > logfile
    #optional filename in csv format contained predicted pKa values and Hill parameters,
    #the format of the pkacsvfile must be the same as the output for pepKalc,
    #only lines after "Site" is read. If this is not found no pH corrections are applied.
    #Output: Table textfile in SHIFTY format (space separated)
    #average of methylene protons are provided for Gly HA2/HA3 and HB2/HB3.
    #NOTE:pH corrections is applied if pH is not 7.0
    #NOTE:pKa predictions are stored locally and reloaded if the seq, temp and ion is the same.
    #NOTE:at least 5 residues are required. Chemical shift predictions are not given for terminal residues.
    #NOTE:change the value of VERB in the top of this script to have verbose logfile
