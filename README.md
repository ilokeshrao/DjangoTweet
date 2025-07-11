# DjangoTweet
# DjangoTweet 🐦

A simple Twitter-like microblogging application built using Django. Users can register, login, post tweets with optional images, and edit/delete their own tweets.

## 🚀 Features

- User Registration & Authentication
- Tweet Creation with optional image upload
- Edit/Delete your own Tweets
- Responsive UI with Bootstrap 5
- Media support (images in tweets)
- Custom templates with layout extension

## 📷 Screenshots

![Tweet Feed](screenshots/tweet_feed.png)
![Tweet Form](screenshots/tweet_form.png)

## 🛠️ Tech Stack

- **Backend:** Django (Python)
- **Frontend:** HTML, CSS (Bootstrap 5), Django Templates
- **Database:** SQLite (default with Django)

## 🧩 Project Structure

DjangoTweet/
│
├── tweet/ # Main app (tweets, views, forms, templates)
│ ├── migrations/
│ ├── templates/
│ │ └── tweet/
│ ├── static/
│ ├── models.py
│ ├── views.py
│ └── forms.py
│
├── djangopro/ # Project settings
│ └── settings.py
│
├── media/ # Uploaded images
├── db.sqlite3
├── manage.py
└── README.md

bash
Copy
Edit

## 🔧 Setup Instructions

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/ilokeshrao/DjangoTweet.git
   cd DjangoTweet
Create and Activate Virtual Environment:

bash
Copy
Edit
python3 -m venv .venv
source .venv/bin/activate  # macOS/Linux
.venv\Scripts\activate     # Windows
Install Dependencies:

bash
Copy
Edit
pip install -r requirements.txt
Apply Migrations:

bash
Copy
Edit
python manage.py migrate
Create Superuser (optional):

bash
Copy
Edit
python manage.py createsuperuser
Run the Server:

bash
Copy
Edit
python manage.py runserver
Visit:
http://127.0.0.1:8000/tweet/

📂 Media Support
Make sure your MEDIA_URL and MEDIA_ROOT are properly configured in settings.py:

python
Copy
Edit
MEDIA_URL = '/media/'
MEDIA_ROOT = BASE_DIR / 'media'
And add this to your urls.py:

python
Copy
Edit
from django.conf import settings
from django.conf.urls.static import static

urlpatterns += static(settings.MEDIA_URL, document_root=settings.MEDIA_ROOT)
