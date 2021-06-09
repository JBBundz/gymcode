## create a database that should create a gym routine for each
## be able to put in what previously done and give routine
## be able to output to a file to be able to store the data of the bests and average, also your last 7 days
## manage a way to be able to create progess in the weights
import random
days = ["Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday", "Sunday"]
day=0
time=0
MuscleGroups = [["Chest","Bench Press", "Inclined Bench Press", "Cable Pulls"],
                ["Back", "Deadlifts", "Pull Backs", "Bent Pull Back", "Pull Downs", "Back Bender"],
                ["Bicep", "Bicep Curls", "Hammer Curls", "21s", "Inner Outers", "Isolated Curls"],
                ["Legs","Squats","Bulgarian Split Squats","Calf Raises","Step Up split squats","Leg Press","Quad Press","Hamstring Press"],
                ["Shoulders","Outer Wings","Inclined Swings","Tight Pulls","Shoulder Press"],
                ["Triceps","Skull Crushers","Back Extensions","Triceps Push","Triceps Pulls", "Overhead Pulls"]]
defaultweights=[[0,80, 20, 20],
                [0, 100, 40, 45, 43, 60],
                [0, 25, 25, 20, 20, 12],
                [0,60,30,24,35,60,45,24],
                [0,5,15,25,40],
                [0,15,60,65,70,40]]
durations =[[0,1, 0.75, 0.5],
                [0, 1.2, 0.75, 1, 0.75, 0.5],
                [0, 1, 0.75, 1.5, 1, 1],
                [0,1,1,0.75,1,0.75,0.5,0.5],
                [0,0.5,1.5,0.5,1],
                [0,1,0.5,0.5,1,1.5]]

muscle =int(input("Which Muscle Group? (1-5) "))
time= int(input("How long do you want to workout for? "))
repamount = [6,8,10,12]
print("Exercise, weight, rep, sets")
for y in range(0,100): 
    if time >0:
        for x in range(0,1):
            setsamount = [3,5]
            sets = setsamount[random.randint(0,1)]
            reps= random.randint(0,3)
            rep=repamount[reps]
            length = len(MuscleGroups[muscle])-1
            exercise = random.randint(1,length)
            if rep == 6:
                weight=defaultweights[muscle][exercise]+5
                duration=((durations[muscle][exercise])*0.75*sets)+2.5
                print(" Exercise: %s \t @ %d kg\t %d reps\t  %d sets" %(MuscleGroups[muscle][exercise], weight, rep, sets))
                time = time-duration
            if rep == 8:
                weight=defaultweights[muscle][exercise]
                duration=((durations[muscle][exercise])*sets)+2.5
                time = time-duration
                print(" Exercise: %s \t @ %d kg\t %d reps\t  %d sets" %(MuscleGroups[muscle][exercise], weight, rep, sets))
            if rep == 10:
                weight=defaultweights[muscle][exercise]-2.5
                duration=((durations[muscle][exercise])*1.25*sets)+2.5
                time = time-duration
                print(" Exercise: %s \t @ %d kg\t %d reps\t  %d sets" %(MuscleGroups[muscle][exercise], weight, rep, sets))
            if rep == 12:
                weight=defaultweights[muscle][exercise]-5
                duration=((durations[muscle][exercise])*1.5*sets)+2.5
                time = time-duration
                print(" Exercise: %s \t @ %d kg\t %d reps\t  %d sets" %(MuscleGroups[muscle][exercise], weight, rep, sets))
    else:
        break
#duration and weights are set to 8 reps
#decrease, decrease duration by x0.75, increase weight by +5kg
#increase, increase duration by x1.25 (10), x1.5 (12), decrease weight by -2.5kg
