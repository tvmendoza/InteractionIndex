# InteractionIndex

Interaction Index calculator is a file that reads a json file with different criteria and calculates the shappley values.  


## Usage Instructions

Just run the script with the input file you want to run the script against:

$ python interactionIndex.py test.json

## Input data

Sample input data should be a json file with two or more labeled alternatives, one or more labeled criteria, and the numeric responses to each criteria for each alternative.  This example input file shows response data for 4 criteria for two different patients. 

     {
    "participants": [{
        "Cost": {
            "FIT:": 1.0,
            "Colonoscopy:": 0.1,
            "Flexible Sigmoidoscopy:": 0.6
        },
        "Further Testing": {
            "FIT:": 1.0,
            "Colonoscopy:": 1.0,
            "Flexible Sigmoidoscopy:": 1.0
        },
        
        "Test Preparation": {
            "FIT:": 1.0,
            "Colonoscopy:": 1.0,
            "Flexible Sigmoidoscopy:": 1.0
        },
        
        "Time": {
            "FIT:": 1.0,
            "Colonoscopy:": 1.0,
            "Flexible Sigmoidoscopy:": 1.0
        }
    },
    {
        "Cost": {
            "FIT:": 0.1,
            "Colonoscopy:": 1.0,
            "Flexible Sigmoidoscopy:": 1.0
        },
        
        "Further Testing": {
            "FIT:": 1.0,
            "Colonoscopy:": 1.0,
            "Flexible Sigmoidoscopy:": 1.0
        },
        
        "Test Preparation": {
            "FIT:": 1.0,
            "Colonoscopy:": 1.0,
            "Flexible Sigmoidoscopy:": 1.0
        },
        
        "Time": {
            "FIT:": 1.0,
            "Colonoscopy:": 1.0,
            "Flexible Sigmoidoscopy:": 1.0
         }
    }]
    }

## Output data

The script will have two outputs: 
1)The shell will print each of the shappley values
2)A results.txt file will be created with the shappley values of each participant plus the average of each criteria. 


    Process started.
    *************
    The pair [Further Testing , Test Preparation] has an interaction index of: 0.0972302584584
    The pair [Time , Test Preparation] has an interaction index of: 0.294529614547
    The pair [Cost , Time] has an interaction index of: 0.982478423989
    The pair [Further Testing , Cost] has an interaction index of: 0.28635119713
    The pair [Cost , Test Preparation] has an interaction index of: -0.00372101684786
    The pair [Further Testing , Time] has an interaction index of: 0.0265879745834
    *************
    The pair [Further Testing , Test Preparation] has an interaction index of: -0.118894721951
    The pair [Time , Test Preparation] has an interaction index of: 0.226931709109
    The pair [Cost , Time] has an interaction index of: 0.984777423227
    The pair [Further Testing , Cost] has an interaction index of: 0.396755551096
    The pair [Cost , Test Preparation] has an interaction index of: 0.171091457811
    The pair [Further Testing , Time] has an interaction index of: -0.207988480552
    *****************
    **** Average ****
    The pair [Further Testing , Test Preparation] has an average of:  -0.0594473609756
    The pair [Time , Test Preparation] has an average of:  0.113465854554
    The pair [Cost , Time] has an average of:  0.492388711614
    The pair [Further Testing , Cost] has an average of:  0.198377775548
    The pair [Cost , Test Preparation] has an average of:  0.0855457289053
    The pair [Further Testing , Time] has an average of:  -0.103994240276
    Process completed.

## Requirements

This project requires Python 2.7 or greater.


## Contributions

The Biomedical Informatics mHealth lab welcomes contributions to this project. Please fork and send pull requests with your revisions.
