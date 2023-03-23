# Python-Challenge
PyBank Challenge 
To begin with I inputed the csv file that went along with the challenge. Then the line below I set up the output file as the text file that I exported to the analysis folder when I was done with the code. 
I then listed out all my variables: 
  
total_months = 0
month_of_change = []
net_change_list = []
greatest_increase = ["",0]
greatest_decrease = ["", 99999999999]
total_net = 0
  
Then I opened the file with a with statement and skipped the first row because that is the header row. 
Then within that with statement I started my for statement, where I calculated the total months and the total net amount. Then I went and put in my equations for the net change and I appended the net change and the changing months.

net_change = int(row[1]) - previous_net
net_change_list.append(net_change)
month_of_change.append(row[0])
