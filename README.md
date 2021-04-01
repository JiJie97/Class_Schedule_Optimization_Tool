# Class_Schedule_Optimization_Tool
 
The USC Marshall School of Business has 7 departments, 22 academic programs, and enrollment of around 5000 undergraduate students and 1000 graduate students. With multiple programs, priorities, and preferences, it is difficult for Institutional Research and Academic Administration to create a classroom schedule without scrambling and headaches. Hence, the team was hired by Marshall to investigate the possibility of applying optimization to improve the efficiency and transparency of the current system and to rigorously quantify the potential gains.

In the process of data exploration based on the historical schedule, the team identified three major pain points:
 ● Time-consuming scheduling methodology
 ● Inappropriate utilization of classroom space
 ● Professors’ preferences not satisfied. 
Specifically, the team investigated two general trends regardingprofessors’ preference: 1) Avoid working more than two days a week 2) Desire back-to-back classes

To address the opportunities for improvement, the team proposed an optimization tool prototype that intakes the readily available time slots, classroom and class information, and outputs the schedule for all classes and a summary of the schedule performance. To estimate the potential gain from the optimization, the team applied the tool using sample data based on classes in the 2019 Spring term, with 533 classes, 38 classrooms, and 241 timeslots. As a result, the prototype generated a new free-from-conflict schedule within 40 minutes, which pushes the number of professors who have to work more than two days a week to 0, increases the average utilization rate to 89.58%, and increases the proportion of professors who are allocated at least one back-to-back class by 17.5%.
Based on the results, the team offered Shannon and her team with a series of final recommendations:
● Pilot the optimization tool with a small section of classes to gain confidence. For example, utilize the
model to schedule only graduate classes or MBA classes.
● Select the weight of scheduling features by sensitive analysis. Scheduling features include average
classroom utilization rate, number of professors who are allocated at least one back-to-back class, and the number of professors who have to work more than two days a week. By default, the weights for the features above are 1, 1, and 0.2.
● Adopt the output of the optimization tool as a scheduling start point, then address special cases manually. For example, very few graduate classes with a length of more than 3 hours are not considered by the model and need adjustment by hand.
● Partition the classes and run parallelly to save runtime. Currently, allocating regular spring term classes takes the model 25 - 40 minutes. To save the runtime, it is suggested to split the input courses, classrooms and time slots into 2 - 4 non-overlapping parts, run each part parallelly, and finally concatenate the outputs to create the full schedule.
