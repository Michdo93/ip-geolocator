# IP Geolocator

A simple and efficient Python tool to fetch geographical information (such as country, city, region, ISP, and coordinates) from any IP address using the `ipinfo` API.

---

## Features

* **Detailed Geolocation:** Retrieve City, Region, Country, Postal Code, and Coordinates (Latitude/Longitude).
* **Network Insights:** View the Internet Service Provider (ISP) and ASN details associated with the IP.
* **Timezone & Currency:** Automatically fetches the local timezone.

---

## Prerequisites: Getting an ipinfo.io Token

To use this application, you need a free API token from [ipinfo.io](https://ipinfo.io/). 

1. Go to [ipinfo.io/signup](https://ipinfo.io/signup) and create a free account.
2. Once logged in, navigate to your **Dashboard**.
3. Copy your unique **Access Token** from the dashboard.

### Adding the Token to the Code

Open your Python script and locate the token variable (or initialization). Replace the placeholder with your actual token:

```python
import ipinfo

# Replace 'YOUR_TOKEN_HERE' with your actual ipinfo.io access token
access_token = 'YOUR_TOKEN_HERE'
handler = ipinfo.getHandler(access_token)
...
```

---

## Installation

Follow these steps to set up the project locally using a virtual environment (`venv`).

### 1. Clone the Repository

```bash
git clone [https://github.com/Michdo93/ip-geolocator.git](https://github.com/Michdo93/ip-geolocator.git)
cd ip-geolocator
```

### 2. Create a Virtual Environment

It is highly recommended to use a virtual environment to avoid conflicting dependencies.

* **Windows:**
```bash
python -m venv .
.\Scripts\activate
```


* **macOS / Linux:**
```bash
python3 -m venv .
source ./bin/activate
```



### 3. Install Dependencies

Install the official `ipinfo` wrapper library via `pip`:

```bash
pip install -r requirements.txt
```

*(If you do not have a `requirements.txt` file yet, you can install it directly via `pip install ipinfo`)*

---

## Usage

Once your virtual environment is active and your token is configured in the code, run the script from your terminal:

```bash
python geolocate_ip.py
```

### Example Output

When you look up an IP address, the tool will output the details in a structured format:

```text
Details for IP: 8.8.8.8
----------------------------------------
City: Mountain View
Region: California
Country: US
Geolocation: 37.4056,-122.0775
Postal Code: 94043
Timezone: America/Los_Angeles
Organization: AS15169 Google LLC

```

---

## License

This project is open-source and available under the [MIT License](https://github.com/Michdo93/ip-geolocator/LICENSE).


---
