# Harvard CS109 Exploratory Analysis

1. Start with a good question
2. visualization goals
  * communicate (Explanatory)
    * Present data and ideas
    * Provide evidence and support
    * Influence and persuade
  * Analyze (Exploratory)
    * Explore the data
    * Assess a situation
    * Determine how to proceed
    * Decide what to do

# What make a visualization effective?
* To reduce the cognitive load
* Website tip: WTF visualizations
The five principles:
1. Have grahical integrity
2. Keep it simple
3. Use the right display
4. Use color strategically
5. Tell a story with data

## Graphical integrity
* Your bar chart has to start at zero!
* For minute change use something that does not use length.  Like a __dot plot__
* Scale distortions are bad
* Tell non zero based graphs clearly
* The math must be right
* Remove chartjunk (anaything that does not convey data)
* Don't use 3D
* Use the right display (google search 'chart suggestion - thought starter')

### Comparison
* Use bar char (with zero)
* Don't use lines

### Trends
* lines
* stacked area charts are zero
* bar charts

### Proportions (change)
* stacked area charts are permissible (trends with proportions)
* stacked bar charts
* pie charts (angle judgment + area judgment)
* difference bar graphs
* slope graph

### Correlations
* scatterplots
* Don't do 3D scatterplots

### Distributions
* Histograms (play with bin size)
* Density plots (= continous histogram of data)
* Heat maps (2d Density)

## visualization
Answers usually one question. To answer more than one most often use more than one visualization.
For qualitative measures colors can be used

## Don't
* Use color for quantitative encoding

## Quantitative use: (most efficient)
* position
* length
* slope

## Ordered use: (efficient)
* area (relative/qualitative judgment)
* intensity

## categories use: (least efficient)
* color
* shape

## Don't use color (only strategically)
* 5 to 7 colors max
* use luminance and saturation for ordinal data
* do not use rainbow for color map (non linearity)
* use gray scale for data
* use color brewer tool also in Seaborn

## Read
* Edward Tufte
* Stephen Few

# Databases, SQL and pandas
## Data engineering
* compute: code, python, R, julia, spark, hadoop
* storage/database: git, SQL, NoSQL, HBase, disk, memory
* devops: AWS, docker, mesos, repeatability (google)
* product: database, web, API, viz, UI, story

What kind of data storage do you need?
* memory
* disk: what if it does not fit?
* cluster: what if it still does not fit?(partition the data in a cluster)
* cluster: what if we need/can use parts?
* What if we MUST bring compute to disk? (when network is too slow to transfer; on site computing)

What kind of data access do you need?
* relational: pandas, SQL, Postgres, sqlite, Hbase (OS Google's Big Table), VoltDB
* document oriented: MongoDB, CouchDB
* key-value: Riak, Redis, Memcached (fast)
* graph oriented: Neo4j (networks)

Use database according to what kind of access do you need. If not sure chose relational. Longest in business and support.

# Relational database
Grammar of data is what a database can do for you.
* collection of tables
* rows are attributes
* column is values of one attributes
* tables connected by keys

### Scales of Measurement
* Quantitative (float, integer)
* nominative (text style)
* ordinal

### Grammar of data
* Simple verbs for simple things ie functions corresponding to common data manipulation tasks
* backend does not matter
* multiple backends implementation possibilities
  *  Impala, Pig, ibis, blaze
* http://chrisalbon.common

## PandasAndSQL.ynb
* integer is NOT NULL (nothing there)
* start with permissive datatype descriptions
* FOREIGN KEY may not be NULL (lookup)

Relational databases must be committed.


# Lab3
* Each finite length run is called a sample, which has been obtained from the generative model of our fair coin.
* Bernouille distribution talks about one coin toss
* Binomiminal distribution talks about n tosses (k heads in n, like n Bernouille tosses)

# Lab3-freq
* Samples are always drawn as Histograms
