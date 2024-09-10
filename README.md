# Django testimonials app with APIs

Building a sample testimonials app with flask in the backend and react in the frontend.

## Features

- Flask backend
- Uses [venv](https://docs.python.org/3/library/venv.html) - the officially recommended Python packaging tool from Python.org.
- Development, Staging and Production settings with [django-configurations](https://django-configurations.readthedocs.org).
- Get value insight and debug information while on Development with [django-debug-toolbar](https://django-debug-toolbar.readthedocs.org).
- Collection of custom extensions with [django-extensions](http://django-extensions.readthedocs.org).
- HTTPS and other security related settings on Staging and Production.
- Procfile for running gunicorn with New Relic's Python agent.
- PostgreSQL database support with psycopg2.
- Using Neon Tech PostgreSQL managed DB [neon.tech](https://neon.tech/docs/introduction).

## How to install

```bash
# Clone the repository
git clone https://github.com/Dhruv97Sharma/testimonials_app.git
cd testimonials_app

# Create a virtual environment
# inside the container or outside the container in a localhost environment
python3 -m venv ./env
source ./venv/bin/activate
pip install -r requirements.txt
python app.py
```

## Deployment

It is possible to deploy to render.com, railway.app or to your own server.

## License

The MIT License (MIT)