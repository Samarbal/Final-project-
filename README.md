# Final-project-
print("..................BUS BOOKING APPLICATION...............................")

class Passengers():
    Name = " "
    idnumOfpass =" "
    trip = ' '
    seatnumber = ' '
    date = " "


    def __init__(self, Name ,idnumOfpass, trip,seatnumber , date ):
        self.Name = Name
        self.idnumOfpass = idnumOfpass
        self.trip = trip
        self.seatnumber = seatnumber
        self.date = date

    def getPassengerInfo(self):
        self.pName =  input(" Enter Passenger Name: ")
        self.idnumOfpass = int(input(" Enter Your ID Number :"))
        self.date = input(" Enter the Date of the journey ")


        #self.journey = int (input("Enter Your Distenation "))

    def menu (self):
        print(""" The buses and directions
                    The station is in Gaza
                    1- Bus 1 from the station to Haifa
                    2- Bus 2 from the station to Jerusalem
                    3- Bus 3 from the station to Negev Desert
                    4- Bus 4 from the station to Hebron 
                    5- Exit """)
        choice = int(input(" Enter the number of the trip you want to take :"))
        while True :
           if  choice ==1 :
                #self.trip = " Haifa "
                print (" You have just booked a ticket to Haifa ")
           elif  choice ==2:
                #self.trip = " Jerusalem "
                print (" You have just booked a ticket to Jerusalem ")
           elif choice ==3:
                 #self.trip = " Negev Desert"
                 print (" You have just booked a ticket to Negev Desert ")
           elif  choice ==4:
                 #self.trip =  " Hebron "
                 print(" You have just booked a ticket to Hebron")
           elif choice == 5 :
                 break
           else :
                print(" Please Enter a correct Number ")

            # you need to finf a solution to repeat the procces



        #Booking a seat. these are the number of the seats
        print (" [1]_[2]_[3]_[4]_[5]_[6]_[7]_[8]_[9]_[10]_[11]_[12]_[13]_[14]_[15]")
        seatNumlist = [1,2,3,4,5,6,7,8,9,10,11,12,13,14,15]
        self.bookinglist =[]
        while True:

            self.seatnumber= int(input(" Choose a seat number & you cannot book than two seats"))
            if self.seatnumber <= 15:
                for x in seatNumlist:
                    self.bookinglist.append(self.seatnumber)
                    del seatNumlist[self.seatnumber+1]
                    count = len(seatNumlist)

                else :
                    print("The Ticket Already Booked")
                print(" Do you want to book another seat? Enter (Yes / No)")
                y = input( " ")
                if y =="Yes":
                    pass
                else :
                    break

            else :
                print("Don't choose a seat number which is not available ")

passenger =Passengers(Name= ' ',idnumOfpass= " ",trip= " ", seatnumber=" ", date=" ")


passenger.__init__(Name= ' ',idnumOfpass= " ",trip= " ", seatnumber=" ", date=" ")
passenger.getPassengerInfo()
passenger.menu()
print(" Thank you for your effort ")
