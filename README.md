# Automatic Drone Inspection Service (ADIS)
🤖DL Research

## Description

I am developing a high-tech automated inspection system for conveyor belts for large mining enterprises (Norilsk Nickel, Polymetal, Evraz). We remove the human factor and reduce the loss of conveyor transport and conveyor downtime. If the conveyor is damaged by a roller that is out of order, the belt breaks and it takes a day to replace it, so the conveyor does not work and its idleness costs a lot. The main idea is to use a neural network based on YOLOv5. We use high-tech equipment for capturing the conveyor: a drone with a dual camera (RGB & IR), an RTK module to track the precise positioning of the drone, complex mathematics to determine the GPS coordinates of broken rollers, and other modern technologies. Stack: Python, Yolo V5, Detectron2, OpenCV, Django \[In progress\]

![alt text](https://github.com/v-mk-s/ADIS/blob/master/ADIS-Video-test-15-sec.gif "")


# Chatty Bot

You can talk with a very chatty bot. 
You can ask a question or say something, and the bot will answer you in a talkative manner. 

There are three user ranks: admin, moderator, and user.
There is using a combination of Retrieval and Generative Q/A model.

MongoDB is used to store states in [FSM](https://en.wikipedia.org/wiki/Finite-state_machine)

## Run

0. Install [mongoDB](https://www.mongodb.com/)
1. Clone this repo
> `git clone https://github.com/v-mk-s/Chatty-Bot-DL`
2. Install dependencies
> `cd Chatty-Bot-DL/`  
> `pip3 install --no-cache-dir -r requirements.txt`
3. Set environment variables
> `set PYTHONPATH="." (on Windows)`

Let Python know that the package is here, otherwise it raise a exception «module chatty_bot not found»  
Now set up other environment variables or write them directly in config.py

```
set TOKEN="<Bot's token here>"
set OWNER_ID="<Admin id>"
set FILES_PATH="<Path to directory with questions>" # Ex: "./files"
set DB_NAME="aiogram"
set PORT ="27017"
set HOST="localhost"
set SEND_ERRORS="True" // "True" if you want that exceptions message will sent to you
```
4. Make sure Mongodb is running
5. Run  
>  `python ./chatty_bot/bot.py`
> 
> 
## TODO list
* Improve [LM](https://en.wikipedia.org/wiki/Language_model)
* New feature: users will be able to rate themselves, and the bot will collect statistics.
* Fix bugs related to [race condition](https://en.wikipedia.org/wiki/Race_condition)
* Optimize files sending by sending file_id which will be stored for each file
