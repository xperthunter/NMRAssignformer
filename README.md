# NMRAssignformer
Code repository for NMR Assignment problem with transformers.

# Background
The NMR Spectral Assignment problem is a classification problem given a spectrum or spectra can each peak in the data be assigned to a specific atom of the analyzed molecule. NMR assigment is particularly hard for protein NMR where the spectral lines are broad and many. 

# Approach
Our approach is to use machine learning to identify the assignments of peaks in an NMR spectrum using the information about available peaks as well as information about a structure. 

# Organization

** data_collection
	-- where we place our work in collecting data
** data
	-- where training/testing data will go
	-- tinydata/
		-- small dataset
		-- 1% cs
		-- 1% peaks
** toy_models
** assignformer
	-- where architecture for assignformer will go

# AssignFormer
Transformer on peaks
Transformers on structure
Communication between the two

## Toy models
1. Encoder-Decoder to predict peak positions
	-- mask out a peak
	-- predict location of peak
	-- how to understand masking in transformers
	

## Mechanism of prediction

N peaks by L resuidues
F.softmax(x, dim=1)


# To-Do
1. mechanism to get BMRB data
	-- provide a way to rsync, but don't necessarily have to rsync/have the 					databank on repo
	-- go back to bmrb_tools and figure it out from there
	-- just a sh script to get the data
2. tinydata
	-- 1% cs
	-- 1% peaks
3. Running alphafold on those structures
4. Finding the BMRB/PDB entries
5. Make a toy model with just peaks
	-- attention tokens are the peaks (coord1, coord2, confidence/measure)
	-- attention between peaks, multihead
	-- predicting matrix at the end
	-- N peaks by L residues
	-- Need to figure out masks



	 
