from tkinter import *
from chatterbot import ChatBot
from chatterbot.trainers import ListTrainer
import pyttsx3
import speech_recognition
import threading

bot=ChatBot('JAI')
trainer=ListTrainer(bot)
data=open('greetings.yml','r',encoding='utf-8').readlines()
trainer.train(data)

def botreply():
    ques=Qfield.get()
    ques=ques.capitalize()
    ans=bot.get_response(ques)
    textarea.insert(END,'YOU:'+ques+'\n')
    textarea.insert(END,'BOT:'+str(ans)+'\n\n')
    pyttsx3.speak(ans)
    Qfield.delete(0,END)

def audiototext():
    while True:
        sr=speech_recognition.Recognizer()
        try:
            with speech_recognition.Microphone()as m:
                sr.adjust_for_ambient_noise(m,duration=0.3)
                audio=sr.listen(m)
                #convert recognized voice into text
                query=sr.recognize_google(audio)

                Qfield.delete(0,END)
                Qfield.insert(0,query)
                botreply()
        except Exception as e:
            print('e')

#GUI PART

root=Tk()
root.geometry('700x750+50+5')
root.title('SHIVANI_S CHATBOT')
root.config(bg='red')

chatbotpic = PhotoImage(file='img_1.png')
chatbotpiclabel=Label(root,image=chatbotpic,bg='red',height=200,width=300)
chatbotpiclabel.pack(pady=5)

frame=Frame(root)
frame.pack()

scrollbar=Scrollbar(frame)
scrollbar.pack(side=RIGHT)

textarea=Text(frame,font=('georgia',15,'bold'),bg='white',height=15,yscrollcommand=scrollbar.set,wrap='word')
textarea.pack(side=LEFT)
scrollbar.config(command=textarea.yview)

Qfield=Entry(root,font=('times new roman',15,'bold'))
Qfield.pack(pady=15,fill=X)

askpic=PhotoImage(file='button1.png')

ask=Button(root,image=askpic,command=botreply,bg='black',height=100,width=100)
ask.pack(pady=2)

def click(event):
    ask.invoke()
root.bind('<Return>',click)

thread=threading.Thread(target=audiototext)
thread.setDaemon(True)
thread.start()

root.mainloop() #with the help of this we will be able see the gui continuosly
