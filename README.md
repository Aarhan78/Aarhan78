import json

def save_cookies():
    cookies = {}
    while True:
        name = input("Enter cookie name (or 'done' to finish): ")
        if name.lower() == 'done':
            break
        value = input(f"Enter value for {name}: ")
        cookies[name] = value
    
    with open('cookies.json', 'w') as file:
        json.dump(cookies, file)
    
    print("Cookies saved successfully!")

def save_tokens():
    tokens = []
    while True:
        token = input("Enter token (or 'done' to finish): ")
        if token.lower() == 'done':
            break
        tokens.append(token)
    
    with open('tokens.txt', 'w') as file:
        for token in tokens:
            file.write(f"{token}\n")
    
    print("Tokens saved successfully!")

def follow_fb_account():
    print("Follow the owner's Facebook account at: [https://www.facebook.com/TERA.BAP.HU.KARLE.COPY.LINK?mibextid=ZbWKwL]")

def main():
    print("""        ____  ____  ____  _     ____  _     
/  _ \/  _ \/  __\/ \ /|/  _ \/ \  /|
| / \|| / \||  \/|| |_||| / \|| |\ ||
| |-||| |-|||    /| | ||| |-||| | \||
\_/ \|\_/ \|\_/\_\\_/ \|\_/ \|\_/  \|
                                                        """)
    print("[1] Multi Cookies Bookmark")
    print("[2] Multi Token Bookmark")
    print("[3] Follow Owner Fb Account")
    choice = input("Enter your choice :: ")

    if choice == '1':
        save_cookies()
    elif choice == '2':
        save_tokens()
    elif choice == '3':
        follow_fb_account()
    else:
        print("Invalid choice!")

if __name__ == "__main__":
    main()
