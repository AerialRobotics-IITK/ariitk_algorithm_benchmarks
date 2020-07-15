# Documenting results

This is a very important part of your benchmarking process. Proper documentation allows you to easily decide between algorithms that are best fit for your use case, in the future. 

Please use Markdown files to write the benchmark document.   

You can use this template to give all the relevant results.

### <center>Algorithm Name</center>

#### Introduction
Contains a short description about your algorithm, and what the algorithm is trying to achieve. Should also contain pseudo-code if possible (especially if the algorithm is not a well known algorithm).

#### Parameters
This section should contain the list of all parameters (and a short description for non trivial parameters), constant or otherwise. The values of constant parameters should be provided. Also, the range of other parameters that are going to vary in your test bench should also be provided.

#### Test Cases
You should provide the complete list of test cases, providing links to databases/video files/ROS bag files that have been used in your test bench.

#### Results
This section details your result. It should preferably be presented in tabulated form, for easy understanding. Your table should include the test case name, values of each variable used, and the values of the benchmarking variables obtained in the test. Quick graphs can also be given.

#### Footer
This section will contain other assorted details, like the assumptions used, and your conclusions. This can also contain other relevant links, like links to research papers on the particular algorithm, github repositories, etc. 

## Example Report
For a good example you can see the benchmarking report of ORB_feature_detector algorithm, in this repository. Some general comments regarding the example report given :-

1) If you can easily find the pseudo-code for your algorithm or are well-versed in LaTeX and able to write one easily and quickly, you must provide the pseudo-code. This is so that their is less downtime in trying to understand the actual code, should someone want to implement this algorithm in a different language/package. In the example, it hasn't been provided as the pseudo-code isn't available easily and this function is already implemented in the well-known OpenCV library (so anyone who wants to implement it elsewhere can directly use the OpenCV functions).

2) This document is an example and hasn't been documented extensively, hence many of the variables in the _Parameters_ section have been set to their default values. In reality, you might want to vary every parameter to see what effect it has on the result. For deciding the range, you are the better judge. The key is striking a balance; you don't want to be wasting too much time on conducting tests and recording results by having a large range (especially of those that have a negligible effect on your result) and at the same time you shouldn't conduct very few tests, which might be insufficient to get a clear picture and also optimise performance. Also, in any case, every relevant parameter value(s) (even if kept constant) must be given so that the tests can be recreated or more extensive tests can be done, if the need arises.

3) In the benchmark result graph, you can see spikes in the time taken for the function to complete. This is caused due to processes running in the background that sometimes hog-up the CPU power. If all the programs weren't closed before running the tests, there would have been even more lag spikes. However closing all background processes is often not possible (unless you want to go so far as to open Linux in a terminal only mode with only bare minimum processes running :P. Even then you couldn't fully eliminate those spikes). Nevertheless to make your tests as accurate as possible, close as many applications as possible. Also take time based averages as done here(or if you are a little more free, implement a low-pass filter in your test bench :) ).

4) Your results can contain tables, bar graphs, line graphs, etc. However including too many images in the markdown file is not a good idea. Only keep the relevant images in this repository and reference them in the markdown file. Rest of the graphs or data generated should be transferred to a separate folder in the Benchmarks/(Algorithm sub-class) directory on the team's google drive, and proper viewing links (not with editing rights) can be provided in the results for these.

5) The footer is the most valuable place for the person who wishes to pursue this algorithm further. This should have all relevant links or information that you think might help anyone looking to go deeper into this algorithm. Any papers, repositories, documentation, articles, anything really that you found useful during your initial research should be mentioned here. This will drastically cut down the research time of anybody (or even you, if you come back after a long time to use this algorithm) trying to understand the algorithm. You can also include your own conclusions that you derived from the tests.