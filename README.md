# roster
Hi. I am trying to automate my team's roster and learn code this way. 
So, I am very new here and looking to learn Python. 
My project is this: A program that allows users to input data -- team members, their name, leaves required, which are their days off -- and get an output that has the duty chart.
I have done some partial code. But, stuck. Hit me up if you are interested in helping out.

#lists
team=[]
leaves=[]
date=[]
weekends = 8
#modules
from employee import employeedetails
import calendar


def number():
  try:
    global team_number
    team_number = int(input("Enter number of members on team: "))
  except:
    print("Sorry! Please input only numerals")
    number()

def working():
  global working_number
  working_number = int(input("How many employees do you want working on a particular day?: "))

number()
Year, month = int(input("Enter Year: ")), int(input("Enter month: "))
while team_number != 0:
  team_member = input("Enter team member " + str(team_number) + " ")
  team.append(team_member)
  team_number = team_number-1
team_number = i = len(team)
working()
while working_number > team_number:
  print("Oops, too few team members for that! Let's do that again")
  working()

for x in team:
  a = input("Does " + x + " want leaves this month? (Type Y if yes) ")
  if a == "Y":
    l = int(input("Enter number of days leave: "))
    d = int(input("Enter starting date: "))
  else:
    l = 0
    d = 0
  leaves.append(int(l))
  date.append(int(d))

i=0
employee=[]
while i != len(team):
  employee.append(employeedetails(team[i], leaves[i], date[i]))
  i += 1

