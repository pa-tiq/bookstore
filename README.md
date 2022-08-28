```bash
git clone https://github.com/pa-tiq/bookstore.git
cd bookstore
python -m venv .venv
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
pip install -r requirements.txt
docker-compose up -d --build
docker-compose exec web python manage.py migrate
```
http://127.0.0.1:8000/