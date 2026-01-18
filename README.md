import requests

def test_site(url):
    try:
        response = requests.get(url)
        print(f"Status Code: {response.status_code}")
    except Exception as e:
        print(f"Error: {e}")

url = input(" URL  ")
test_site(ur
import requests
import time

def test_site(url, requests_count, delay):
    print(f"جارٍ اختبار {url}...")
    for i in range(requests_count):
        try:
            response = requests.get(url)
            print(f"طلب {i+1}: {response.status_code}")
        except Exception as e:
            print(f"Error: {e}")
        time.sleep(delay)

url = input("ادخل URL الموقع: ")
count = int(input("عدد الطلبات: "))
delay = float(input("الفاصل بين الطلبات (ثواني): "))

test_site(url, count, delay)
