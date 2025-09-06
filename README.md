# calculator.py

def calculator():
    print("🧮 ماشین حساب ساده")
    print("عملیات‌های موجود: + , - , * , /")
    while True:
        try:
            num1 = float(input("عدد اول: "))
            op = input("عملیات (+ - * /): ")
            num2 = float(input("عدد دوم: "))

            if op == "+":
                result = num1 + num2
            elif op == "-":
                result = num1 - num2
            elif op == "*":
                result = num1 * num2
            elif op == "/":
                if num2 == 0:
                    print("❌ تقسیم بر صفر مجاز نیست!")
                    continue
                result = num1 / num2
            else:
                print("❌ عملیات نامعتبر!")
                continue

            print(f"✅ نتیجه: {result}\n")

        except ValueError:
            print("❌ لطفا عدد معتبر وارد کنید.\n")

        again = input("می‌خوای ادامه بدی؟ (y/n): ")
        if again.lower() != "y":
            print("👋 خداحافظ!")
            break


if __name__ == "__main__":
    calculator()
