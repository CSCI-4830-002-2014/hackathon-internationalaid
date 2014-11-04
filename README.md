# Team Members

* [Alexia Newgord](https://github.com/alne4294)
* [Austin Wood](https://github.com/indiesquidge)
* [Sam Korn](https://github.com/sako0938)
* [Peyman Mo](https://github.com/peymanmortazavi)
* [Ryan Roden](https://github.com/rodenr)

# Connect to MongoLab:
mongo ds051170.mongolab.com:51170/aiddata-hack -u datauser -p datapass
database: aiddata-hack
collection: hack_aid

# Mongo Query's:
var r = db.hack_aid.aggregate([{ $match:{"recipient": "Sudan" } },{$group:{"_id":"$year",total:{$sum:"$disbursement_amount"} } }]);
var sum = 0;
r.forEach(function(d) { sum = sum + d.total; } )

# Objective 1. Identify a two countries to compare.

| "High Aid" Country | Sudan | ~9 billion |
| "Low Aid" Country  | Libya | ~150 million |

# Objective 2. Analyze events occurring within each country to develop a hypothesis on the effect of aid.

## Aid Timeline

![screenshot of the timeline analysis](img/aid_timeline.png?raw=true) 

## Chosen Timeframe did you analyze and how did you pick that?

| Sudan | 2003 | 2005 |
| Libya | 2003 | 2005 |

By looking at the graph above, you can see over a 10 fold increase in Sudan's disbursement
(from ~100 million to ~1 billion in less than 2 years) while Libya stayed virtually the same.


## "High Aid" Country

##### Real GDP Growth of Sudan
|2003  | 2004 | 2005  |
|------|------|-------|
| 7.1% | 5.1% | 0.4%  |

### Before Trends

![supporting screenshots](img/sudan_data.png?raw=true) 
![supporting screenshots](img/sudan_data2.png?raw=true) 

### Differences

Sudan definitely had more commitments over time, not only reflecting on it's own
growth, but also when compared to Libya.

## "Low Aid" Country

##### Real GDP Growth of Libya
|2003 | 2004 |	2005 |
|-----|------|-------|
|13%  |	4.4% | 11.9% |

### Before Trends

![supporting screenshots](img/libya_data.png?raw=true) 
![supporting screenshots](img/libya_data2.png?raw=true) 

### Differences

As you can see, Libya has made very few commitments (only one really). Their GDP
seemed to also correlate with this as well.

# Objective 3. Bring in other data sets to help you with your hypothesis.

[Sudan research](http://data.worldbank.org/country/sudan)
[Libya research](http://data.worldbank.org/country/libya)

