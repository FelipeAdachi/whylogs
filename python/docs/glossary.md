# Glossary

The following is a glossary of terms commonly used throughout the WhyLabs Documentation. Note that some of these terms
have a special meaning in the context of whylogs/WhyLabs.

##### whylogs
whylogs is a data logging library that captures statistical properties of data and ML models.

##### Batch
A batch is a collection of datapoints, often grouped by time.

###### Batch Mode
In batch mode, whylogs processes a dataset in batches.

###### Streaming Mode
In streaming mode, whylogs processes individual data points. However, the underlying algorith groups these
data points together into micro batches.

#### Dataset
**Dataset** is a collection of related data that will be analyzed together. In case of tabular data: each column of
the table represents a particular variable, and each row represents a record of the dataset. When used alongside a
statistical model, the dataset often represents features as columns, with additional columns for the output. For
non-structured/complex data, the representation depends on the datatype, explore other data
types [here](https://docs.whylabs.ai/docs/whylabs-monitoring/#discrete-vs-continuous-columns).

#### DatasetProfile
A **DatasetProfile** is a collection of summary statistics and related metadata for a dataset that whylogs has
processed.

#### Data Sketching
**Data sketching** is a class of algorithms that efficiently extract information from large or streaming datasets in a
single pass. This term is sometimes used to refer specifically to the Apache DataSketches project.

#### Logger
A **logger** represents the whylogs tracking object for a given dataset (in batch mode) or a collection of data points (
in streaming mode). A logger is always associated with a timestamp for its creation and a timestamp for the dataset.
Different loggers may write to different storage systems using different output formats.

#### Metadata
**Metadata** is data that describes either a dataset or information from whylogs’ processing of the dataset.

#### whylogs file

A whylogs-generated profile can be stored as a protobuf binary file. Protobuf is a lightweight binary
format that maps one-to-one with the memory representation of a whylogs object.

#### Metric
The summary statistics of a dataset is composed by a collection of metrics. Metrics are defined according to its namespaces. Some of the whylogs' default namespaces are: `counts`, `types`, `distribution`, `cardinality`, `frequent items/frequent strings`. By default, a column of a given data type will have a defined set of metrics assigned to it. The metrics to be tracked are customizable according to data type or column name (see [Schema Configuration](examples/basic/Schema_Configuration.ipynb)) . New metrics can also be created in a custom fashion, according to the need of the user (see TBD).


##### Metric component
NEED TO DEFINE HERE
