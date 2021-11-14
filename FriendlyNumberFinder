# This program finds friendly numbers for the number specified

import time
matchcount=0

#-----------------------------------------------------#

def main():
    abundancyIndex()

#-----------------------------------------------------#

# Function for the abundancy index of the number to be checked
# Runs through the digits of the number to be checked
# and checks to see if it is a factor
# and adds it to the sum

def abundancyIndex():
    chksum=0
    chkdigit=int(input('Number to Check: '))
    lowdigits=int(input('Low Number to Check: '))
    highdigits=int(input('High Number to Check: '))
    chkai=0 # Abundancy Index
    start_time = time.time()
    for i in range(1,chkdigit):
        if chkdigit%i==0:
            chksum+=i
    chkai=chksum/chkdigit
    print(f"Abundancy Index: {chkai}")
    for testdigit in range(lowdigits,highdigits):
        testDigits(chkai, testdigit, chkdigit)
    if matchcount==0:
        print("No Matches")
    print("--- %s seconds ---" % (time.time() - start_time))

#-----------------------------------------------------#

def testDigits(chkai, testdigit, chkdigit):
    global matchcount
    testsum=0
    testai=0
    for i in range(1,testdigit):
        if testdigit%i==0:
            testsum+=i
    testai=testsum/testdigit
    if testai==chkai and testdigit!=chkdigit:
        print(f"MATCH - {testdigit}")
        matchcount+=1
#-----------------------------------------------------#

main()
