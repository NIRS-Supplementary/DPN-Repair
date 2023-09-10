# DPN-Repair
A toolkit that allows verify and repair data-aware process models

Conditions may be either atomic or composite. Each atomic condition is a condition of variable-operator-constant and variable-operator-variable forms.

Model is imported in the extended PNML format, input examples are presented in DataPetriNetOnSmt.Visualization\Samples_For_Import.
For the input model, a transition system highlighting sources of unsoundness can be constructed during the verification.

## Requirements

- Windows 10/11
- .NET SDK 6 x64

## Run

To run the app, download the files from the repository, extract the files to an arbitrary directory and run 'DataPetriNetOnSmt.Visualization.exe'.

## Usage

1. Import a DPN choosing File -> Open DPN...
2. Choose Model -> Check Soundness. Here two algorithms for soundness verification are proposed: direct and improved. The direct approach reveals all the sources of unsoundness and highlights them on the LTS but may take more time than the improved approach. The improved approach checks whether or not the DPN is sound and present the least detailed LTS that can justify it, which generally allows to verify soundness quicker although not all the sources of unsoundness may be highlighted on the LTS. Select the approach which better corresponds to your task.
3. When the verification is done, the corresponding LTS is constructed. Green nodes represent final states. Red nodes represent deadlocks. White nodes with red border represent states from which no final state is reachable. Blue nodes represent states with markings strictly greater than the final marking.
4. To repair process model soundness, choose Model -> Transform model -> Transform model to repaired.
