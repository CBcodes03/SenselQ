## Manual Deployment

```bash
cd folder  # The folder you want to clone project into
```

```bash
git clone https://github.com/CBcodes03/combined.git .
```

```bash
pip install -r requirements.txt
```

```bash
gunicorn -w 4 -b 0.0.0.0:8000 app:app
```
