Cheesy-Eagle-Vision
===================

This is a modified version of CheesyVision that will run under LabView. The original version crashes the cRio when a TCP reciever is set up under LabView to run on the cRio.
This version has the cRio ask the DS for the latest status only when needed as apposed to a continuous stream of data being sent from the DS to the cRio as implemented in the original version.

To use this, you will need to follow the installation instructions for CheesyVision found here: https://github.com/Team254/CheesyVision

Once installed and running on your DS, you can use this modified version to under LabView without crashing the cRio.

There are two files needed:

1) "CheesyEagleVision.py" runs on the DS to read driver "Hand" commands.

2) "CheesyEagle Receiver.vi" runs on the cRio and requests the most recent status from the DS when needed. REMEMBER to set the IP address in this vi to the IP of your DS, this will allow it to make a request to the DS for the current "Hand" position value.
