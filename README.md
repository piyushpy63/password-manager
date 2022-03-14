# password-manager
storage for passwords
#code starts here

pwd = input("what is the master password:")

def view():
    with open('passwords.txt', 'r') as f:
        for line in f.readline():
            print(line.rstrip())
def add():
    name = input("account Username:")
    password=input("password of the account :")
    with open('passwords.txt','a') as f:
        f.write(name + '|' +  password + "\n")


while True:
    mode = input("would you like to view or add the passwords or press Q for quit").lower()
    if mode == "q":
        break
    if mode=="view":
        view()
    elif mode=="add":
        add()
    else:
        print("invalid Mode:")
        continue
