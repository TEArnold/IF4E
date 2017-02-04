# IF4E
Python - Eukaryotic translation initiation factor 4E


RNA_codon_table = {
# 			Second Base
#    U 	         C             A             G
# U
'UUU': 'Phe', 'UCU': 'Ser', 'UAU': 'Tyr', 'UGU': 'Cys', # UxU
'UUC': 'Phe', 'UCC': 'Ser', 'UAC': 'Tyr', 'UGC': 'Cys', # UxC
'UUA': 'Leu', 'UCA': 'Ser', 'UAA': '---', 'UGA': '---', # UxA
'UUG': 'Leu', 'UCG': 'Ser', 'UAG': '---', 'UGG': 'Trp', # UxG
# C
'CUU': 'Leu', 'CCU': 'Pro', 'CAU': 'His', 'CGU': 'Arg', # CxU
'CUC': 'Leu', 'CCC': 'Pro', 'CAC': 'His', 'CGC': 'Arg', # CxC
'CUA': 'Leu', 'CCA': 'Pro', 'CAA': 'Gln', 'CGA': 'Arg', # CxA
'CUG': 'Leu', 'CCG': 'Pro', 'CAG': 'Gln', 'CGG': 'Arg', # CxG
# A
'AUU': 'Ile', 'ACU': 'Thr', 'AAU': 'Asn', 'AGU': 'Ser', # AxU
'AUC': 'Ile', 'ACC': 'Thr', 'AAC': 'Asn', 'AGC': 'Ser', # AxC
'AUA': 'Ile', 'ACA': 'Thr', 'AAA': 'Lys', 'AGA': 'Arg', # AxA
'AUG': 'Met', 'ACG': 'Thr', 'AAG': 'Lys', 'AGG': 'Arg', # AxG
# G
'GUU': 'Val', 'GCU': 'Ala', 'GAU': 'Asp', 'GGU': 'Gly', # GxU
'GUC': 'Val', 'GCC': 'Ala', 'GAC': 'Asp', 'GGC': 'Gly', # GxC
'GUA': 'Val', 'GCA': 'Ala', 'GAA': 'Glu', 'GGA': 'Gly', # GxA
'GUG': 'Val', 'GCG': 'Ala', 'GAG': 'Glu', 'GGG': 'Gly'  # GxG
}

AAsingles = {'Cys': 'C', 'Asp': 'D', 'Ser': 'S', 'Gln': 'Q', 'Lys': 'K', 'Trp': 'W', 'Asn': 'N', 'Pro': 'P', 'Thr': 'T', 'Phe': 'F', 'Ala': 'A', 'Gly': 'G', 'Ile': 'I', 'Leu': 'L', 'His': 'H', 'Arg': 'R', 'Met': 'M', 'Val': 'V', 'Glu': 'E', 'Tyr': 'Y', '---': '*'}



DNA = 'ATGGCGACTGTCGAACCGGAAACCACCCCTACTCCTAATCCCCCGACTACAGAAGAGGAGAAAACGGAATCTAATCAGGAGGTTGCTAACCCAGAACACTATATTAAACATCCCCTACAGAACAGATGGGCACTCTGGTTTTTTAAAAATGATAAAAGCAAAACTTGGCAAGCAAACCTGCGGCTGATCTCCAAGTTTGATACTGTTGAAGACTTTTGGGCTCTGTACAACCATATCCAGTTGTCTAGTAATTTAATGCCTGGCTGTGACTACTCACTTTTTAAGGATGGTATTGAGCCTATGTGGGAAGATGAGAAAAACAAACGGGGAGGACGATGGCTAATTACATTGAACAAACAGCAGAGACGAAGTGACCTCGATCGCTTTTGGCTAGAGACACTTCTGTGCCTTATTGGAGAATCTTTTGATGACTACAGTGATGATGTATGTGGCGCTGTTGTTAATGTTAGAGCTAAAGGTGATAAGATAGCAATATGGACTACTGAATGTGAAAACAGAGAAGCTGTTACACATATAGGGAGGGTATACAAGGAAAGGTTAGGACTTCCTCCAAAGATAGTGATTGGTTATCAGTCCCACGCAGACACAGCTACTAAGAGCGGCTCCACCACTAAAAATAGGTTTGTTGTTTAA'


DNA0 = DNA.replace('T', 'U')



answer = []
for i in range (0, len(DNA0)/3):
        Triplet_DNA0 = DNA0[i*3:i*3+3]
        list1 = AAsingles[RNA_codon_table[Triplet_DNA0]]
        answer.append(list1)
print "".join(answer)
