# python flow-control
 1. if..else and elif 
 2. for loop
 3. while loop
 4. break and continue
  
## if..else statement
    age=int(input("enter your age:"))
    if  age>=18:
       print("you are eligible for voting")
    else:
       print("you are not eligible for voting")

## elif statement
    number=int(input("enter your number:"))
     if  number>=1:
       print("positive number")
    elif number<=-1:
       print("negative number")
    else:
      print("the number is zero or neutral")
## for loop
    for i in range(5):
    print("class", i)
## while loop
     i = 0
    while i < 5:
    print("door no:", i)
    i += 1              
## break and continue
    i = 0
    while i < 5:
    if i == 2:
        i += 1
        continue  
    if i == 4:
        break  
    print("class", i)
    i += 1

   
 
   