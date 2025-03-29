# YCB-Handovers
Dataset Repository for the YCB-Handovers Dataset


A total of 6 participant pairs (12 participants involved). For each pair, they were assigned participant 1 and participant 2. The baton was transferred to and fro between them. The particpants wear motion capture suits (MoCap) and the experiment occured in a MoCap room. The upeer body movement is tracked for them.

Each pair's data is divided into four folders, corresponding to baskets having different objects, and further 4 folders: Pitcher-NC (non-careful), Pitcher-C (careful), Cup-C, Cup-NC, representing careful or non-careful handovers with a heavy weighted YCB pitcher and a small weighted cup.

Each of these folders has 2 folders: 'forward_handovers' and 'reverse_handovers'. The 'handovers' folder contains all recorded and segmented handovers as separate folders when participant 1 acts as giver and passed the objects to participant 2, who acted as taker. The 'handovers_reverse' contains all handovers when participant 2 acted as giver and participant 1 as taker. This is done for purely analytical purposes.

The labels for what a handover represents in a each 'forward_handovers' and 'reverse_handovers' is given in the label_handovers.csv file in that folder.

Here's a weight (in grams) mapping for these labels: 
label_weights = {
    "MS": 8, "M": 118, "W": 242, "MB": 600, "CB": 1131,
    "R": 40, "J": 190, "MC": 374, "HD": 874, "SB": 1020, "E": 1450,
    "LM": 55, "SC": 149, "P": 202, "SBX": 410, "H": 728, "SK": 1300,
    "pitcherC": 2060, "pitcherNC": 2060, "cupC": 8, "cupNC": 48,
    "SP": 15, "B": 95, "C": 183, "CC": 514, "WB": 608, "BW": 925}


Each handover folder has 26 .csv files, with 901 rows implying the saved duration (901 timesteps @120 Hz) of the handover representing:
Giver upper body skeletal representation- pose of 13 individual frames
Taker upper body skeletal representation- pose of 13 individual frames

Above can be seen in the handover_Sample folder provided which has data of a sample handover.
