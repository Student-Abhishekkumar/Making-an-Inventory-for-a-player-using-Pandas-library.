# Making-an-Inventory-for-a-player-using-Pandas-library.
In this code i made an inventory for a player where he will store his item he buys at the shops. I used pandas library to make my code more visually appealing.

# Code:-

''' python
#game inventory

import pandas as pn

def menu():
    print("\n...........Welcome! Sir...........")
    print("Please take a look :- ")
    print("\n\t1. Weapons")
    print("\t2. Portions")

player_inventory=[]
quantity=[]
while True:
    menu()
    choice=input("\nEnter your choice : ")
    print()
    if(choice=='1'):
        Inventory=pn.DataFrame({
            "Weapons":['Katana','Shield','Bow','Knife']
        },index=[1,2,3,4])
        print(Inventory)
        print()
        choice2=int(input("Enter your choice : "))
        plyr_invent=Inventory.at[choice2, 'Weapons']
        player_inventory.append(plyr_invent)

        h_many=int(input("\nEnter how manty you want : "))
        quantity.append(h_many)
        print("\n.......Thank you! sir, come again......\n")
        ask=input("Do you want to continue or not [y/n] : ")
        if ask=='y':
            continue
        elif ask=='n':
            break
        else:
            print("Invalid code")

    elif(choice=='2'):
        Inventory=pn.DataFrame({
            "Portions":['Small Tier portion','Mid Tier portions','High Tier portions','Resurrection portion']
        },index=[1,2,3,4])
        print(Inventory)
        choice3=int(input("Enter your choice : "))
        plyr_invent=Inventory.at[choice3, 'Portions']
        player_inventory.append(plyr_invent)

        h_many=int(input("\nEnter how manty you want : "))
        quantity.append(h_many)
        print("\n.......Thank you! sir, come again......\n")
        ask=input("Do you want to continue or not [y/n] : ")
        if ask=='y':
            continue
        elif ask=='n':
            break
        else:
            print("Invalid code")

    else:
        print("Invalid Choice....")

print("\n...........Player's Iventory............")
print()
p=pn.DataFrame({
    "INVENTORY":player_inventory,
    "QUANTITY":quantity
})    
print(p)
'''
