# Python-Challenge
PyBank Challenge: 

To begin with I inputed the csv file that went along with the challenge. Then the line below I set up the output file as the text file that I exported to the analysis folder when I was done with the code. 
I then listed out all my variables: 
  
    total_months = 0
    month_of_change = []
    net_change_list = []
    greatest_increase = ["",0]
    greatest_decrease = ["", 99999999999]
    total_net = 0
  
Then I opened the file with a with statement and skipped the first row because that is the header row. 
Then within that with statement I started my for statement, where I calculated the total months and the total net amount. Then I went and put in my equations for the net change and I appended the net change and the changing months. The equations are below: 

    net_change = int(row[1]) - previous_net
    net_change_list.append(net_change)
    month_of_change.append(row[0])

I then did two if statements within the for statement and each if statement is to calculate the greatest increase in profits and the greatest decrease in profits. The equations are below: 

     if (net_change > greatest_increase[1]):
     greatest_increase[0] = row[0]
     greatest_increase[1] = net_change
     
     if (net_change < greatest_decrease[1]):
     greatest_decrease[0] = row[0]
     greatest_decrease[1] = net_change
     
The last equation I had to do was to calculate the net average, round it to two decimals and the equation is below: 

     net_average = round(int(net_change) / len(net_change_list), 2)
     
Then I had to create the output summary that summarized all the different variables I needed for the challenge. This included the total months, the total, the average change, the greatest increase in profits, and the greatest decrease in profits. The last thing I had to do was export the table below as a text file using a with statement. 
A table summarizing the variables is below: 

    Total Months= 86
    Total= $22564198
    Average Change= $-8311.11
    Greatest Increase in Profits: 13-Mar $52857
    Greatest Decrease in Profits: 10-Dec $-2283116     

PyPoll Challenge: 

To begin with I imported the csv file that went along with the challenge. Then in the line below I set up the output file as a text file that I exported to the analysis folder when I was done with the code. 
For my variables, I set total votes= 0, I created a list for candidate options, I created a dictionary for candidate votes, I kept winning candidate open and set winning count= 0. 

Then I started with a with statement to open the data file and I skipped the first row because that was the header row. Then I delt with the total vote count where I used the equation: 

    total_votes = total_votes + 1
    
The candidate name is in the third row of the csv file so I extracted that row and named it the candidate name. Then within the for statement I created an if statement for if the candidate's name is not in candidate options. I used the following equations within the if statement: 

    candidate_options.append(candidate_name)
    candidate_votes[candidate_name] = 0   
    candidate_votes[candidate_name] = candidate_votes[candidate_name] +1    
    
Then with a with statement I wrote it as a text file and exported the text file. 

After that I created another for statement for candidate in candidate votes. The following equations are the ones I used within the for statement: 

      votes = candidate_votes.get(candidate)
      vote_percentage = round(int(votes) / int(total_votes) *100, 3)  
      
For the vote percentage I used the round function and then rounded it to three decimals places. 

Then I created an if statement within that for statement: 

        if (votes > winning_count):
            winning_count = votes
            winning_candidate = candidate      
      
I then created voter_info which prints the candidate, then the percentage of votes the candidate got, and then the total votes the candidate got. Then I saved that as a text file. Lastly I printed the winning candidate and saved that as a text file as well. The table summarizing the results is below: 

       Total Votes= 369711
       Charles Casper Stockham: 23.049% (85213)
       Diana DeGette: 73.812% (272892)
       Raymon Anthony Doane: 3.139% (11606)
       Winner: Diana DeGette
