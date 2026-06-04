# Overview
This is an example project used as a demonstration of IQ Features.

The drug used for this project is a fictional monospecific mAb. The purpose of this example is to demonstrate the main features of Certara IQ as well as provide a starting point for building
models and code. This example project can act as a place to explore the software with a very basic example model.

All of the files in this example project are introduced in one demo or walk through videos. You can follow along with one of the videos using this example project, or on your own.

# Files

## Models

1. Models/1compartment_PKRO_finished.iqd
    * A 1 compartment model to demonstrate the process of building a graphical model
    * This model is built in the "01 - IQ Design - Introduction to Model Building (Full Walkthrough)" video
2. Models/2compartment_Ab
    * A 2 compartment PK RO model for a fictional antibody
    * This model is reviewed in the "02 - Demo Intro to IQ Design" video
    * This model is used (though not reviewed) in all other Demo videos
    * This model is called in all Analyze Notebooks to demonstrate IQ Analyze features
    * This model has metadata formatted to be able to open within IQ Explore
3. Models/ModelFile_TextBased.model
    * An example model using the text based ReactionModel syntax
    * This model format can encode the same exact reaction types as the GUI models above
    * This example is for those users that are more comfortable coding in a text based environment
    * There is no video training for this example
    * See Models/TextModel_complete.ipynb for a notebook based walk through of how to build this type of model

## Data Files

1. Data/ Data_example_subset.csv
   * Example data file in the format accepted by IQ Analyze for optimization purposes
   * Used in the Analyze_Optimization_completed.ipynb Notebook and associated training video

## Parameter Files

1. Parameters/Parameter.csv
   * IQ Analyze Parameter file for a nominal parameter set
   * This parameter file is first used in the "03 - Demo - IQ Analyze" video
   * This parameter file is called in the following IQ Analyze notebooks:
     * Analyze_Simulate_completed.ipynb
     * Analyze_Scan_completed.ipynb
     * Analyze_Optimization_completed.ipynb
2. Parameters/Vpop.csv
   * IQ Design Vpop parameter file for a nominal parameter set and several dosing schedules
   * This Vpop file is first used in "02 - Demo Intro to IQ Design"
   * This Vpop file is loaded into the 2compartment_Ab model file during simulation
3. Parameters/Parameter_labels.csv
   * IQ Analyze Parameter file to demonstrate labeling of separate individuals or populations
   * This parameter file is called in the Analyze_Labels_completed.ipynb Notebook and associated video
   * This parameter file contains the same information as the Vpop_labels.csv file
4. Parameters/Vpop_labels.csv
   * IQ Design Vpop file to demonstrate labeling of separate individuals or populations
   * This Vpop file is called in the Analyze_Labels_completed.ipynb Notebook to demonstrate its equivalence to the Parameter_labels.csv file
   * This Vpop file is used with the 2compartment_Ab model within Design to simulate three separate populations
5. Parameters/TextBased_Tables
   * This is a folder containing the tables necessary to run the text based model example
   * This folder contains three csv tables
     1. DoseTable_filled.csv:
        * A completed dose table to define and set up simulations for the example text based reaction model
        * This table is used in Models/TextModel_complete.ipynb
     2. ParameterTable.csv:
        * A completed parameter table to define the parameterization for the example text based reaction model
        * This table is used in Models/TextModel_complete.ipynb
     3. SimulationTable_filled.csv:
        * A completed simulation table to select which of the defined simulations are run for the example text based reaction model
        * This table is used in Models/TextModel_complete.ipynb

## IQ Analyze Notebooks

1. Analyze_Simulate_completed.ipynb
   * This notebook demonstrates an example of simulating a model in IQ Analyze
   * This notebook is introduced in the "03 - Demo - IQ Analyze" video
2. Analyze_Scan_completed.ipynb
   * This notebook demonstrates an example of scanning over parameters in IQ Analyze
   * This notebook is introduced in the "04 - Demo - IQ Parameter Scans" video
3. Analyze_Labels_completed.ipynb
   * This notebook demonstrates an example of simulating multiple populations in IQ Analyze with one model and in a single function call through the use of parameter labeling
4. Analyze_Optimization_completed.ipynb
   * This notebook demonstrates an example of fitting parameters to a set of data in IQ Analyze
5. Dependency_completed.ipynb
   * This notebook demonstates the use of notebook dependencies in IQ Analyze
   * This notebook reads the "Analyze_Optimization_completed.ipynb" notebook as a dependency and imports the results of that notebook
6. Analyze_Workflow_Demo.ipynb
   * This notebook is a combined demo of several features within Analyze
   * This notebook contains an example of:
       * Simulation
       * Parameter scan
       * One at a time sensitivity (including tornado plot generation)
       * Optimization
7. Plotting_1_Basics.ipynb
   * This notebook demonstrates basic plotting using `plotnine`, a plotting package similar to R's `ggplot`
   * It covers line and point graphs, customizing axes and labels, faceting (subplots), visual customization, and saving figures
8. Plotting_2_Examples.ipynb
   * This notebook provides examples of plots built using `plotnine`
   * It includes a tornado plot, an observed versus predicted plot, a heat map, and text labels
9. Models/TextModel_complete.ipynb
   * This notebook walks through the building and running of a text based reaction model
   * The simulation portion of this notebook is identical to the options covered in the previous Analyze notebooks
   * The new material convered in this notebook is related to desinging and coding a text based reaction model
     