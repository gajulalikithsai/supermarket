# supermarket
from datetime import datetime
print("WELCOME TO -MIDDLE CLASS HYPERMART-")
name=input("ENTER YOUR NAME: ")
items_list='''
==========GROCERY LIST==========
**RICE VARIETIES**
1.Basmathi rice              - RS 30/KG
2.Brown rice                 - RS 20/KG
3.Idli rice                  - RS 18/KG
**BEVERAGES(paniyalu)**      
4.Tea powder                 - RS 15/250grm
5.Coffee powder              - RS 13/250grm
6.Suger                      - RS 19/KG
7.Helth Drik                 - RS 19/250grm
8.Green tea                   - RS 35/250grm
**BREAK FAST**
9.Atukulu                    - RS 15/KG                 
10.Wheat Rava                - RS 09/KG
11.Ground nuts               - RS 55/KG
12.Idli rava                 - RS 33/KG
13.Moong dal                 - RS 19/KG
14.pesulu                    - RS 19/KG
15.Wheat flour               - RS 09/KG
15.Rice flour                - RS 13/KG
16.Senaga flour              - RS 14/KG
17.Corn flour                - RS 33/KG
18.Maida                     - RS 14/KG
**Oil varieties**
19.Sunflower oil                 - RS 56/KG
20.Groundnut oil             - RS 54/KG
21.Coconut oil               - RS 50/KG
22.Ghee                      - RS 88/KG
**pooja items**
23.pasupu                    - RS 19/250grm
24.kumkuma                   - RS 17/250grm
25.sandal                    - RS 15/250grm
26.Match box                 - RS 1(LARGEBOX)/8
**DRY FRUITS**
27.Cashew(kajuu)            - RS 69/250grm
28.Almond(bhadam)           - RS 68/250grm
29.Raisins(endu dhraksha)   - RS 84/250grm
**CLEANING ITEMS**
30.Bathroom cleaner         - RS 48/1 LITTER
31.Dish wash cleaner        - RS 56/1 LITTER
32.Tooth paste              - RS 33/1 
33.Shampoo                  - RS 40/20
34.soaps(for cloths)        - RS 56/1 LITTER'''
s_items=[]
price=0
totalprice=0
finalprice=0
ilist=[]
pricelist=[]
qlist=[]

items={"basmathi rice":30,"brown rice":20
    ,"idli rice":18,"tea powder":15,"coffee powder":13
    ,"suger":1,"helth drik":19,"green tea":35,"atukulu":15,
    "wheat rava":9,"ground nuts":55,"idli rava":33,
    "moong dal":19,"pesulu":19,"wheat flour":9,
    "rice flour":13,"senaga flour":14,"corn flour":33,
    "maida":14,"sunflower oil":56,"groundnut oil":54,
    "coconut oil":50,"ghee":88,"pasupu":19,"kumkuma":17,
    "sandal":15,"match box":1,"cashew":69,
    "almond":68,"raisins":84,"bathroom cleaner":48,
    "dish wash cleaner":56,"tooth paste":33,"shampoo":40,
    "soaps":56}
option=int(input("FOR LIST OF ITEMS PRESS 1:: "))
if option==1:
    print(items_list)
for i in range(len(items)):
    option1=int(input(("**IF YOU WANT BUY PRESS 1 (OR) EXIT FOR 2**: ")))
    if option1==2:
        break
    if option1==1:
        item=input("ENTER ITEM: ")
        quntiy=int(input("ENTER QUNTIY: "))
        if item in items.keys():      
            price=quntiy*(items[item])
            s_items.append((item,quntiy,price))
            totalprice+=price
            ilist.append(item)
            qlist.append(quntiy)
            pricelist.append(price)
            gst=(totalprice*5)/100
            finalprice=gst+totalprice
        else:
            print("sorry you enterd item is not avalabule")
    else:
        print("you enterd wrong number")
# print(s_items)
inp=input("CAN I BILL THE ITEMS YES (OR) NO: ") 
if inp=="yes":
    print(50*" ","-MIDDLE CLASS HYPERMART-")
    print(50*" ","SBI COLONY,JNTU MAIN ROAD")
    print(50*" ","ANANTAPUR,AP,PIN CODE-515001")
    print(80*"-")
    print('DATE:',datetime.now(),10*" ","TIME:",datetime.now().time())
    print(80*"-")
    print("Sno",10*" ","Description",10*" ","MRP",10*" ","QTY",10*" ","AMOUNT")
    for i in range(len(s_items)):
        print(i,12*" ",ilist[i],13*" ",items[ilist[i]],18*" ",qlist[i],20*" ",pricelist[i])
    print(80*"-") 
    print("AMOUNT",25*' ',totalprice )
    print("GST AMOUNT",20*" ","RS",gst)
    print("TOTAL",25*" ",'RS',finalprice)
    print(80*"-")
    print(30*" ","!!THANKING YOU VISITAGAIN!!")
    print(80*"-")
    print("!!THANK YOU !!")
    print("VISIT AGAIN !!")
      
                                
