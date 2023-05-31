## About Me

I am a first year PhD student at Polytechnique in Montreal where I am in Biomedical Engineering.
My area of research revolves around improving the homogeneity of the main magnetic field (B0 shimming) in Magnetic Resonance Imaging (MRI).
To do so, I have written an open-source toolbox that allows to perform shimming calculations.

## Developing a Continuous Integration Pipeline for the Graphical User Interface of Shimming Toolbox

### Background

The open-source toolbox I have written is called [Shimming Toolbox](https://shimming-toolbox.org/en/latest/) and is version controlled in this [GitHub repository](https://github.com/shimming-toolbox/shimming-toolbox). It allows to easily compute shimming coefficients for different MRI acquisitions.
The main toolbox can be run from the command line and includes many continuous integration (CI) features such as tests and automation with GitHub Actions. A separate repository adds a graphical user interface (GUI) as a plugin to the popular NIfTI viewer [FSLeyes](https://fsl.fmrib.ox.ac.uk/fsl/fslwiki/FSLeyes). This [repository](https://github.com/shimming-toolbox/fsleyes-plugin-shimming-toolbox) does not contain many CI features and will be the one I will be improving in the BrainHack project. A challenge of this repository is that most of the code is for the GUI which makes it a lot more difficult to test, especially on platforms that do not have displays.

### Tools

This project relied on the following tools:
 * [Pytest](https://docs.pytest.org/en/7.3.x/contents.html) to write and setup unit and integration tests
 * [Github Actions](https://docs.github.com/en/actions) to automatically:
  * Launch the tests
  * Launch [pre-commit](https://pre-commit.com) to verify that commits meet certain standards
 * [Docker](https://www.docker.com) to locally launch the tests for linux

### Data

This project is unusual in the sense that the Shimming Toolbox's GUI code is the main part of the data used for this project. The different tests, CI pipelines and Docker containers will have as data the GUI code itself. For some more involved tests where shimming data is required, Shimming Toolbox already has a [testing data repository](https://github.com/shimming-toolbox/data-testing) where lightweight "somewhat" BIDS compliant data will be used.

### Deliverables

At the end of this project, we will have:
 - A directory containing unit and integration tests
 - GitHub Actions that can run these tests and prevent unwanted commits (e.g., large files, merge conflicts, etc)
 - A Dockerfile to set up images with Shimming Toolbox installed able to run the tests

## Results

### Progress overview

### Tools I learned during this project

 * **GitHub Actions**
 * **Pytest**
 * **Docker**

### Results

#### Deliverable 1: Tests

##### GUI tests

##### Unit tests

#### Deliverable 3: Continuous Integration Pipeline

##### GitHub Actions for launching Tests

##### Github Actions for launching pre-commit checks

## Conclusion and acknowledgement

## References

D'Astous A, Cereza G, Papp D, Gilbert KM, Stockmann JP, Alonso-Ortiz E, Cohen-Adad J. Shimming toolbox: An open-source software toolbox for B0 and B1 shimming in MRI. Magn Reson Med. 2022; 1-17. doi:10.1002/mrm.29528

McCarthy P. FSLeyes. 2019.
