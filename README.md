# hello_world
# 登录验证
import os
welcome = ("welcom to KMF")
i = 1

while True:
    username = input("请输入用户名:")
    password = input("请输入密码:")
    locked = ("三次登录错误,用户: %s 已锁" % username)

    if os.path.isfile('lock.log'):
        print(locked)
        break;
    # i += 1;  放在if外,无论输入是否正确,在大于第3次输错的情况下都break
    if username == 'yu' and password == '123':
        pass
    elif i < 3:
        i += 1;
        print("-----请输入正确的用户名或密码!")
    else:
        open('lock.log','w').write(username)
        print(locked)
        break;
    continue
    print(welcome)
