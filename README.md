print("\033[1;36mAnh La Yas x Ank La Boaz")
import os
import ssl
from http.client import HTTPSConnection
from sys import stderr
from json import dumps
from time import sleep
import requests
import re
import time
from datetime import datetime
import os
import random
from colorama import Fore, Style, init

# Khởi tạo colorama
init(autoreset=True)

def ndp_delay_tool(p):
    while p > 1:
        p -= 1
        print(f'\033[1;36m[ 👑 VUI LÒNG ĐỢI 👑 ][-][..............][{p}]', '     ', end='\r')
        sleep(1 / 6)
        print(f'\033[1;35m[ 👑 Tool Đang Được 👑 ][+][Đ.............][{p}]', '     ', end='\r')
        sleep(1 / 6)
        print(f'\033[1;34m[ 👑 Khởi Động 👑 ][|][ĐA............][{p}]', '     ', end='\r')
        sleep(1 / 6)
        print(f'\033[1;33m[ 👑 Tool Siêu Bá 👑 ][/][ĐANG..........][{p}]', '     ', end='\r')
        sleep(1 / 6)
        print(f'\033[1;32m[ 👑 By Ank La Yas 👑 ][-][ĐANG K........][{p}]', '     ', end='\r')
        sleep(1 / 6)
        print(f'\033[1;31m[ 👑 w Ank La Boaz 👑 ][+][ĐANG KẾT......][{p}]', '     ', end='\r')
        sleep(1 / 6)
        print(f'\033[1;37m[ 👑 From  👑 ][\\][ĐANG KẾT N....][{p}]', '     ', end='\r')
        sleep(1 / 6)
        print(f'\033[1;38m[ 👑 Anh Em Minh Tien 👑 ][|][ĐANG KẾT NỐI..][{p}]', '     ', end='\r')
        sleep(1 / 6)
        os.system("cls" if os.name == "nt" else "clear")  # Thay cls() bằng lệnh này

p = random.randint(3, 3)
ndp_delay_tool(p)

# Màu sắc
xnhac = "\033[1;36m"
do = "\033[1;31m"
luc = "\033[1;32m"
vang = "\033[1;33m"
xduong = "\033[1;34m"
hong = "\033[1;35m"
trang = "\033[1;37m"
whiteb = "\033[1;37m"
red = "\033[0;31m"
redb = "\033[1;31m"
end = '\033[0m'
cam='\033[38;5;208m'

password = "ALY-ALB-AEMT"

# Kiểm tra mật khẩu
for i in range(3):
    mat_khau = input(Fore.CYAN + Style.BRIGHT + "🔑 Nhập Key Để Chạy Tool:  " + Style.RESET_ALL)
    if mat_khau == password:  
        print(Fore.GREEN + Style.BRIGHT + "✔️ Bạn đã nhập đúng key!" + Style.RESET_ALL)
        break
    else:
        print(Fore.RED + f"❌ Bạn đã nhập sai key, số lần còn lại {2 - i}" + Style.RESET_ALL)
else:
    print(Fore.MAGENTA + "🔒 Bạn đã nhập sai quá 3 lần, chương trình kết thúc!" + Style.RESET_ALL)
    exit()

print("\033[1;31m──────────────────────────────────────────────────")           
print("\033[38;5;208m𝑪𝒐𝒑𝒚𝒓𝒊𝒈𝒉𝒕 : 𝑨𝒏𝒉 𝑳𝒂 𝒀𝒂𝒔 𝒙 𝑨𝒏𝒌 𝑳𝒂 𝑩𝒐𝒂𝒛") 
print("\033[1;32m──────────────────────────────────────────────────")           
print("\033[0;31m𝑪𝒐𝒅𝒆 𝑪𝒓𝒆𝒂𝒕𝒐𝒓 : 𝑨𝒏𝒉 𝑳𝒂 𝒀𝒂𝒔")
print("\033[1;33m──────────────────────────────────────────────────")      
print("\033[0;34m𝑪𝒐𝒅𝒆 𝑪𝒓𝒆𝒂𝒕𝒐𝒓 𝟐: 𝑨𝒏𝒌 𝑳𝒂 𝑩𝒐𝒂𝒛")
print("\033[1;32m──────────────────────────────────────────────────")                
print("\033[0;36m𝑻𝒐𝒐𝒍 𝑪𝒖̉𝒂 𝟐 𝑻𝒖̣𝒊 𝑨𝒏𝒉 𝑳𝒂̀𝒎 𝑪𝒉𝒊̉ 𝑪𝒐́ 𝑩𝒂́ !")
print("\033[1;35m──────────────────────────────────────────────────")     
      
tokens = []
print("\033[1;31m🪙 Nhập token acc cần treo (Nhấn Enter để dừng):\033[0m")
while True:
    token = input().strip()
    if token == '':
        if not tokens:
            print("\033[1;31m❗ Bạn cần nhập ít nhất một token.\033[0m")
            continue
        break
    tokens.append(token)

servers = input("\033[1;35m🔗 Nhập link mời server, cách nhau bằng dấu phẩy: \033[0m").strip().split(',')
channels = input("\033[1;34m🆔 Nhập id channel, cách nhau bằng dấu phẩy: \033[0m").strip().split(',')

while True:
    try:
        file_path = input("\033[1;33m📄 Nhập file .txt chứa nội dung spam: \033[0m").strip()
        with open(file_path, 'r', encoding='utf-8') as file:
            duy1 = file.read().strip()
        if not duy1:
            print("\033[1;31m⚠️ File trống, vui lòng nhập lại.\033[0m")
            continue
        break
    except FileNotFoundError:
        print("\033[1;31m❗ File không tồn tại. Vui lòng nhập lại đường dẫn chính xác.\033[0m")
    except Exception as e:
        print(f"\033[1;31m⚠️ Đã xảy ra lỗi: {e}\033[0m")
        break


cd = int(input("\033[1;32m⏲️ Nhập delay (Trên 4-8): \033[0m").strip())

os.system("cls" if os.name == "nt" else "clear")  # Thay cls() bằng lệnh này
print("\033[93m[ Ank La Yas w Ank La Boaz] Bọn Anh Quá Đẳng Cấp\033[0m")

ssl._create_default_https_context = ssl._create_unverified_context

def get_connection():
    return HTTPSConnection("discord.com", 443)

def send_message(conn, channel_id, message_data):
    try:
        conn.request("POST", f"/api/v9/channels/{channel_id}/messages", message_data, header_data)
        resp = conn.getresponse()
        data = resp.read()

        if resp.status == 401:
            print(f"\033[1;31m❗ Lỗi xác thực: Token không hợp lệ. {resp.status} - {resp.reason}\033[0m")
        elif 199 < resp.status < 300:
            print(f"\033[1;31m📤 Đã Spam Tin Nhắn Đến =>> \033[1;37m{channel_id} \033[1;31m<<= \033[1;32mThành Công \033[0m")
        else:
            print(f"\033[1;31m⚠️ Lỗi khi gửi tin nhắn: {resp.status} - {resp.reason}. Response: {data}\033[0m")
    except Exception as e:
        print(f"\033[1;31m❗ Đã xảy ra lỗi: {e}\033[0m")

def main():
    global header_data
    for token in tokens:
        header_data = {
            "Content-Type": "application/json",
            "Authorization": token,
            "User-Agent": "DiscordBot (https://discord.com, v0.1)"
        }
        for server in servers:
            for channel_id in channels:
                message_data = {
                    "content": duy1,
                    "tts": False
                }
                send_message(get_connection(), channel_id, dumps(message_data))

def countdown(time_sec):
    while time_sec:
        mins, secs = divmod(time_sec, 60)
        timeformat = '{:02d}:{:02d}'.format(mins, secs)
        print(timeformat, end='\r')
        sleep(1)
        time_sec -= 1
    print("\033[1;36m=>> ↑ Tool Discord Đang Chạy")

if __name__ == '__main__':
    while True:
        main()
        countdown(cd)
