✈️TravelGo 

A full-stack travel booking web application built with Flask and AWS that allows users to book buses, trains, flights, and hotels — with real-time booking confirmation via AWS SNS.



🚀 Features

- 🔐 User Registration & Login with session management
- 🚌 Bus, 🚆 Train, ✈️ Flight & 🏨 Hotel booking
- 💺 Seat selection interface
- 💳 Payment processing with method & reference tracking
- 🎫 Ticket generation after successful booking
- 📧 Real-time booking confirmation via AWS SNS (email/SMS)
- 📊 User dashboard to view all past bookings



🛠️ Tech Stack

| Layer     | Technology |

| Backend       | Python, Flask |

| Frontend      | HTML, CSS (Jinja2 Templates) |

| Database      | AWS DynamoDB |

| Notifications | AWS SNS |

| Cloud         | AWS (EC2, DynamoDB, SNS) |



📁 Project Structure

TravelGo-main/

└── zoroo/

    ├── app.py                  # Main Flask application
    
    └── templates/
    
        ├── index.html          # Home page
        
        ├── login.html          # Login page
        
        ├── register.html       # Registration page
        
        ├── dashboard.html      # User booking dashboard
        
        ├── bus.html            # Bus listings
        
        ├── train.html          # Train listings
        
        ├── flight.html         # Flight listings
        
        ├── hotels.html         # Hotel listings
        
        ├── seat.html           # Seat selection
        
        ├── payment.html        # Payment page
        
        └── ticket.html         # Booking confirmation ticket



⚙️ Setup & Installation

Prerequisites
- Python 3.8+
- AWS Account with DynamoDB and SNS configured
- AWS CLI configured with credentials

1. Clone the repository
```bash
git clone https://github.com/your-username/TravelGo.git
cd TravelGo/zoroo
```

2. Install dependencies
```bash
pip install flask boto3
```

3. Set environment variables
```bash
export FLASK_SECRET_KEY="your-secret-key-here"
export AWS_REGION="ap-south-1"
```

4. AWS Setup
- Create a DynamoDB table named **`Travel_user`** with `email` as the partition key
- Create a DynamoDB table named **`bookings`** with a GSI named `email-index`
- Create an SNS topic and update the `SNS_TOPIC_ARN` in `app.py`

5. Run the application
```bash
python app.py
```
Visit `http://localhost:5000` in your browser.


🙋‍♀️ Author

Afrah R 
(B.Tech Computer Science and Business Systems)
