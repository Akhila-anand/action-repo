# action-repo
Dummy repository to trigger GitHub webhook events

Hii I am Akhila
This project is a simple GitHub webhook listener.
I created this with MongoDB and flask. The main purpose of this project is to watch a GitHub repository for events like push, pull or merge and show them on webpage in real time and python is used as backend and MongoDB atlas to store data in cloud and in order to access my local server, I used ngrok.

**Prerequisites**
Python
MongoDB
GitHub account with admin access
ngrok (for local testing)

**Quick Setup**
**1. Clone & Configure**
git clone https://github.com/yourusername/github-webhook-demo.git
cd github-webhook-demo/webhook-receiver
echo "MONGO_URI=mongodb://localhost:27017/" > .env

**2. Install & Run**
# Setup virtual environment (optional)
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate

# Install & run
pip install -r requirements.txt
python app.py

**3. Make Webhook Accessible Using ngrok:**
**Install ngrok, then:**
ngrok config add-authtoken YOUR_TOKEN
ngrok http 5000
Copy the forwarding URL (e.g., https://d6d42e04b4e6.ngrok-free.app)

**4. Configure GitHub Webhook**
Repository → Settings → Webhooks → Add webhook
Set:
Payload URL: Your ngrok URL + /webhook
Content type: application/json
Events: Select "Let me select individual events"
Pushes
Pull requests
Pull request reviews
Active: ✓
**5. Access Dashboard**
Open http://localhost:5000 in your browser
Testing
Push Events

 
