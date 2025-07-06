# Billing-System
size=int(input("Enter Product List Size :"))
Product_list=[]
price=[]


for i in range(size):
    i=input(f"Enter product {i+1}")
    Product_list.append(i)

for i in range(size):
    i=int(input(f"Enter {Product_list[i]} price"))
    price.append(i)


for i in range(size):
    print(f"{Product_list[i]}={price[i]}")

gst=input("Do You Want to add GST [Y/N]:")

total=sum(price)

if gst=="y" or gst=="Y":
    per_gst=float(input("Enter GST % :"))
    with_gst=total*(per_gst/100)
    print("**************************")
    print(f"Total :",total)
    print(f"GST :{per_gst}%")
    final_amount=total+with_gst
    print("**************************")

    print("Final Total :",final_amount)
    print("**************************")


        
elif gst=="n"or gst=="N":
    print("**************************")
    print(f"Total :",total)

else:
    print("Invalid input")



