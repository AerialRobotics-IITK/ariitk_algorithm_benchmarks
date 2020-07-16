# Benchmarking Documentation

This repository maintains all the benchmarking results of various algorithms. A benchmark basically consists all the statistical data that allows the reader, without much hassle, to judge the performance of a particular algorithm, and how it is affected by various parameters. It also contains other relevant information about the algorithm, in case the reader wants to analyse the algorithm in depth.

The algorithms currently docmented are:-

- [Vision](Vision)    
    - [ORB feature detector algorithm](Vision/ORB_feature_detector_algorithm)

If you are going to benchmark and document algorithms yourself, please read how to [benchmark algorithms](BENCHMARKING.md) and [document the results](RESULTS.MD) carefully.

This is directory structure to be maintained in this respository.

```
root
|   README.md (this file)
|   BENCHMARKING.md
|   RESULTS.md
|   .gitignore
|
└───Vision
│   │   
│   └───Algorithm_1
│   |       Algorithm_1.md
│   |       <any other relevant files>
│   |
│   └───Algorithm_2
│   |       Algorithm_2.md
|   |       <any other relevant files>
|   '
|   '
|   '
│   └───Algorithm_n
│           Algorithm_n.md
|           <any other relevant files>
|   
└───Localisation
│   │   
│   └───Algorithm_1
│   |       Algorithm_1.md
│   |       <any other relevant files>
│   |
│   └───Algorithm_2
│   |       Algorithm_2.md
|   |       <any other relevant files>
|   '
|   '
|   '
│   └───Algorithm_n
│           Algorithm_n.md
|           <any other relevant files>
'
'
'
└───<Any other class of algorithms>
    │   
    └───Algorithm_1
    |       Algorithm_1.md
    |       <any other relevant files>
    |
    └───Algorithm_2
    |       Algorithm_2.md
    |       <any other relevant files>
    '
    '
    '
    └───Algorithm_n
            Algorithm_n.md
            <any other relevant files>
```

When adding a benchmark, please make a new branch with the name `<algorithm_class>/<algorithm_name>`and when you are done benchmarking, open a PR to merge your branch into master.