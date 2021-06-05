'''
gpacalculator
A simple gpa calculator for Unilag students
'''
import os
import time
import sys
print('GPA Calculator')
def g():
	animation = ['Loading |','Loading /','Loading —','Loading \\','Loading |','Loading /', "Loading —", "Loading \\"]*3
	for i in range(len(animation)):
	   	time.sleep(0.075)   
	   	sys.stdout.write('\r'+ animation[i % len(animation)])
g()
os.system('clear')
b = int(input('Number of Courses: '))
Y=[]
print('\nList of Courses in "Order":')
for n in range(b):	
	Course = input('')
	Y.append(Course)
	[]
H=[]
print('\nUnit of Courses in "Order":')
for n in range(b):
	Unit = int(input(''))
	H.append(Unit)
S=[]
G=[]
print('\nTotal Assessment Obtained in "Order":')
for n in range(b):
	a = int(input(''))
	if a >= 70:
		grade = 5
	elif (a >= 60) and (a <= 69):
		grade = 4
	elif (a >= 50) and (a <= 59):
		grade = 3
	elif (a >= 45) and (a <= 49):
		grade = 2
	elif (a >= 40) and (a <= 44):
		grade = 1
	elif (a >= 0) and (a <= 39):
		grade = 0
	ele = grade
	S.append(a)
	G.append(ele)
print('\nGrades Obtained:', G)
GradeUnit = [a*b for a, b in zip(G,H)]
gpa = sum(GradeUnit)/sum(H)
print('\n','-'*40,'\n','| Course Offered |', Y,'|\n','-'*40,'\n','| Scores\t|  ',S,'|\n','-'*40,'\n','| GPA Obtained |', gpa,'|\n','-'*40)
