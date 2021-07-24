# PenniesAndPounds_repo
 
 This repository is for data, codes and example output of models described in "Focussing on resistance to front-line drugs is the most effective way to combat the antimicrobial resistance crisis" (Meghan R. Perry, Deirdre McClean, Camille Simonet, Mark Woolhouse & Luke McNally)

 
# supplementary_material
 
 
- **TableS1.1_casecadeOfResistance_summaries**: model summaries for the mixed models of ECDC data on frequency of resistance. Excel file.

- **supplementary_dataset_research_interest**: supplementary dataset for analysis of research of interest/attention/funding on front-line and last-line antibiotics (csv file)


# simulations_output_samples
 
bla bla bla

# scripts
 
 # 1_analytical_models

 - **Analytical_results_mathematica.nb**: Mathematica notebooks analysing simple version of model. For each intervention, deriving analytical expression for equilibria and R0. Then evaluate R0 for the different possible epidemiological scenario. Basis of the "supplementary equation" section of paper's supplementary material. A pdf version is also provided.

 -**R0_manipulate_figures.nb**: mathematica code for interactive figures of R0


 # 2_simulation_models

 - **models.R**: models functions used in deSolve in the simulations script
 - **job_submission.sh**: SGE job submission script to launche simulation script in batches
 - **simulations.R**: Script for conducting simulations. Each simulation runs the three interventions types (adjuvant, diagnostic, new drug), with both front-line and last-line implementation for each. Uses options externally defined from SGE script launched (output directory, see, number of simulations to run). Alternatively, manually define it at begining of R script. Sources 'models.R'.
 	Output:
 		- sims_nb_x_seed_x.RData : R session containing all deSolve output 
 		- out_data_x_seed_x.txt: table with all public health measures from each simulation + records of parameters used, initial states (i.e. end of burn-in phase), and indication if numerical issues were detected during the run (simulation discard if that was the case)

 -**do_dynamic_plots.R**: R script to produce plot showing the dynamic of all strains in each compartment and intervention type.


# simulations_output_samples

Set of examples simulations output (RData files). Those are the ones used to produce example dynamics in figure 2c of the main text. Can be used to run do_dynamic_plots.R to visualise more examples of dynamics.


# Dynamic_plots.pdf

Output of do_dynamic_plots.R script. For this run we selected a set of simulations output that produced various dynamics in order to illustrate the variety of possible dynamics. 

