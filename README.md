# volunteer-tracker
sends email updates to volunteers to notify them of their upcoming responsibilities using google sheets and notion

## google sheets
The google sheet has tabs for volunteers and each year (ex. 2025, 2026, 2027, ...) 

### volunteer tab
Required Headers: 
ID: unique volunteer ID (ex. JohnD) 
FirstName: John
LastName: Doe
Email: johndoe@email.com
* I have extra headers for each volunteering capacity and total service count, but these features are not implemented properly yet.

### year tab
Required Headers:
Sunday: MM/DD/YYYY 
Week: Week # out of 52 (this was primarily for debugging purposes)
Counting 1, 2, 3: for each volunteer who counts (1, 2 are primary, and 3 is backup) 
Music 1, 2, 3, 4, 5: for each team member of the music team 
AV 1, 2, 3: for running audio/visual (1, 2 are primary, and 3 is backup)
MorningLead: for the volunteer who leads the morning service
EveningLead: for the volunteer who leads the evening service
EveningMusic: for the music leader who leads the evening music
EveningPreach: for the evening preacher

* More features coming for children's ministry including the standard email reminders + attached curriculum for the week + standard operating procedures (SOP)

## app script
sends out weekly emails to the corresponding row in the year tab and uses the unique volunteer IDs to determine their email, full name, and phone number. This email contains a full-sized bulletin for the week for the morning/evening service and instructions for each volunteering capacity. 

sends out monthly emails to remind volunteers of the weeks they are scheduled for the upcoming two months. volunteers can then ask to be rescheduled for any blackout dates they may be signed up for. 

uses notion page owned by pastor to pull extra information such as any guest speakers scheduled for a particular week. 

