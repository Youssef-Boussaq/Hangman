# valid the word 
def  motvalid(x):
    r = True
    if len(x)<3 or len(x)>25 :
        r=False
    return r
trying=6
#input the word gusse
tcar=str(input(" guess wod : ")).lower()
if motvalid(tcar)==False:
    print("yhe word not valid try agin")
else:
 tr=[]
for i in range(len(tcar)):
    tr.append("")
while trying>0 :
    k=str(input("input lettre")).lower()
    if k in tcar :
        for index ,h in enumerate(tcar):
           if k==h:
               tr[index]=(k)
               print(tr)
        if  ""not in tr:
            print(" you win")
            break
    else:
        trying-=1
    if trying==0 :
        print("sorry")
#print the result 
print(tr)
        
