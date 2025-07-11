if name == "main": print("Режимы: [1] Шифровать, [2] Дешифровать") mode = input("Выбери режим (1 или 2): ").strip() 

if mode == "1": 
    message = input("Введи сообщение для шифрования: ") 
    key_text = input("Введи текст-ключ: ") 
    try: 
        result = encrypt(message, key_text) 
        print(f"\n🔐 Зашифровано: {result}") 
    except Exception as e: 
        print(f"❗ Ошибка: {e}") 
 
elif mode == "2": 
    code = input("Введи зашифрованную строку (через точки): ") 
    key_text = input("Введи текст-ключ: ") 
    try: 
        result = decrypt(code, key_text) 
        print(f"\n🔓 Расшифровано: {result}") 
    except Exception as e: 
        print(f"❗ Ошибка: {e}") 
 
else: 
    print("❗ Неверный режим. Введи 1 или 2.") 
   
