# prepare-exodus-params

Tekton task that prepares exodus configuration options from the data file. The task looks at the data file
in the workspace to extract the `cdn.env` key. Depending on the values, correct configuration options are returned. 

exodus-gw is a microservice dedicated to writing data onto the CDN.

## Parameters

| Name     | Description                                                                                                                 | Optional | Default value |
|----------|-----------------------------------------------------------------------------------------------------------------------------|----------|---------------|
| dataPath | Path to the merged data JSON file generated by collect-data task and containing the exodus configuration options to use     | No       | -             |

## Changes in 0.2.2
* Use `cdn.env` instead of `exodus.env` to align RPA data with other pipelines

## Changes in 0.2.1
* remove unnecessary new line before outputting the result

## Changes in 0.2.0
* Updated the base image used in this task
