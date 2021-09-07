print("-----Welcome to BigMart-----\n")
final=[]
def shopping():
    items=["Apple","Banana","Mango","Guava"]
    price=[10,20,30,40]
    total=0
    print("Below are Available items")
    for i, j in zip(items,price):
        print(i,"\t\tPrice:",j)
    order=input("\nPlease select your order: ")
    Order=order.title()
    if  Order  in items:
        print(Order,"added to cart successfully :-)")
        pos=items.index(Order)
        final.append(pos)
        response=input("\nDo you want to add more(Y/N)? ")
        if (response.lower()=="yes" or response.lower()=="y"):
            shopping()
        elif (response.lower()=="no" or response.lower()=="n"):
            print("Below are your purchased item")
            for i in final:
                print(items[i],"\t\tPrice: ",price[i])
                total+=price[i]
            print("Total Bill: ",total)
            print("\n-----Thank You for shopping with us-----")
        else:
            print("Invalid Input")
            shopping()
    else:
        print("Item not found Or Unavailable at the moment:-(")
        shopping()

   
shopping()
