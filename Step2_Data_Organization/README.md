# Analysis of Input and Output Data

## Data and Description

1. The automated pet feeder system requires an input of scheduled feeding time which will be used to make the decision for feeding period (IS_FEEDING_TIME) and will be considered as a boolean value. Let us consider it to be boolean values i.e. value 1 for True condition(Feeding time as per the schedule) and 0 for False condition(not the feeding time as per the schedule).

2. The weight of the feeding bowl is taken as an input where the weight of the feeding bowl is checked to ensure that the weight lies within the assumed threshold. For example: weight of feeding bowl is between 20 grams and 300 grams. The value would be 1 for True condition (the weight lies within the defined limits) and 0 for False condition (the weight is not within the defined limits).

3. The system after processing would provide an output signal to the motor that would open or close the feeding channel. A signal 1 would rotate the motor and open the food channel and a signal 0 would close the channel.

4. The system would also output signals to the red LED in the case of an error message. Signal 1 would switch on the Red LED while signal 0 would switch off the LED.

5. The system would require the time for feeding to be set beyond which if the food is not consumed, and alert would be given.

The table below represents the data, their types and some example values

| Parameter                   | Type              | Example values                         |
| --------------------------- | ----------------- | -------------------------------------- |
| Scheduled feeding time      | Constant          | 8:00, 12:00, 18:00                     |
| Weight of the bowl          | Variable          | 100 grams, 200 grams                   |
| Max consumption time        | Constant          | 5hours, 3 hours                        |
| IS_FEEDING_TIME             | Decision          | Yes/ No                                |
| IS_WEIGHT_CHANGED           | Decision          | Yes/ No                                |
| IS_WEIGHT_BETWEEN_THRESHOLD | Decision          | Yes/ No                                |
| Feeder channel control      | Output (Decision) | Open/ Close                            |
| Red LED                     | Output            | On/ off                                |
| Alert trigger               | Output            | On/ off                                |
| Alert Message               | Output            | "Feeding Bowl Overflow" , "Bowl Empty" |
