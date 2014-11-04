# Team Members

* [Alexia Newgord](https://github.com/alne4294)
* [Austin Wood](https://github.com/indiesquidge)
* [Sam Korn](https://github.com/sako0938)
* [Peyman Mo](https://github.com/peymanmortazavi)

# Connect to MongoLab:
mongo ds051170.mongolab.com:51170/aiddata-hack -u datauser -p datapass
database: aiddata-hack
collection: hack_aid

# Mongo Query's:
var r = db.hack_aid.aggregate([{ $match:{"recipient": "Sudan" } },{$group:{"_id":"$year",total:{$sum:"$disbursement_amount"} } }]);
var sum = 0;
r.forEach(function(d) { sum = sum + d.total; } )

# Objective 1. Identify a two countries to compare.

| "High Aid" Country | {{country name}} | {{aid total}} |
| "Low Aid" Country | {{country name}} | {{aid total}} |


# Objective 2. Analyze events occurring within each country to develop a hypothesis on the effect of aid.

## Aid Timeline

![screenshot of the timeline analysis](image.png?raw=true) 

## Chosen Timeframe did you analyze and how did you pick that?

| {{country name}} | {{start datel}} | {{end datel}} |
| {{country name}} | {{start datel}} | {{end datel}} |

{{explain why you picked these dates}}


## "High Aid" Country

### Before Trends

![supporting screenshots](image.png?raw=true) 

### After Trends

![supporting screenshots](image.png?raw=true) 

### Differences

{{explanation of your observations}}


## "Low Aid" Country

### Before Trends

![supporting screenshots](image.png?raw=true) 

### After Trends

![supporting screenshots](image.png?raw=true) 

### Differences

{{explanation of your observations}}


# Objective 3. Bring in other data sets to help you with your hypothesis.

{{link to additional data sets that helped/could help this analysis}}


## Conclusions

{{your hypothesis on the best approach for international development}}
