# Microsoft Visual Studios App for Data Collection
A MS Visual Studios project written in C#. The program is run on a PC and is able to connect to an external device through a serial port. The purpose of this project is to capture incoming EMG data being sent by a microcontroller and then save that data for later analysis in MATLAB. This project is related to the "MyoWare" project.

- Windows app that allows you to capture data that's being sent from the Tiva Launchpad
- Records all incoming data into an Excel file for later analysis
- Make sure the Tiva is connected and powered before you start the app
- Make sure there is a folder named "DataSync_JP" on your Desktop, otherwise it crashes the app. You can change the required folder name by modifying the code.

Instructions:
1) Select an available COM port
2) Set the baud rate to 115200
3) Pick a name for the Excel file that contains all of the saved data. A default name is generated if no name is entered.
4) Press the "Connect" button
5) Press the "Start Logging" button to start recording data
6) Press the "Stop Logging" button to stop recording data
7) Press the "Disconnect" button to disconnect from the serial port

Currently defined recording routine:
1) Setup serial port connection and then start recording (Press "Start Logging" button)
2) Wait 10s
3) Hold a hand gesture for 25s
4) Repeat step 3 for every gesture in your gesture list, with no breaks in between
5) Stop recording (Press "Stop Logging" button)
6) Check your Excel file and fill-in any gaps in the first row of data with random numbers  
   If you are performing 5 gestures, the recording session should last 00:02:15