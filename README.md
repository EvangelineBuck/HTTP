import requests

def send_http_request(url):
    try:
        response = requests.get(url)
        if response.status_code == 200:
            print("HTTP request successful")
            print("Response content:")
            print(response.text)
        else:
            print(f"HTTP request failed with status code: {response.status_code}")
    except requests.exceptions.RequestException as e:
        print(f"HTTP request failed: {e}")

# Example usage
if __name__ == "__main__":
    url = "https://www.example.com"
    send_http_request(url)
