# Flaskerino Fun App 🚀

A tiny Flask server that demonstrates how environment variables can tweak runtime behaviour.

## Environment Variables

| Variable       | Purpose                                         | Default |
| -------------- | ----------------------------------------------- | ------- |
| `DESIRED_PATH` | Path the server listens on (e.g. `/hello`)      | `/`     |
| `PORT`         | Port Flask binds to inside the container         | `80`    |
| `NUMBER`       | Arbitrary number displayed in the greeting       | `0`     |

## Local run (Debian/Ubuntu)

```bash
# 1. Install Python & pip (if needed)
sudo apt update && sudo apt install python3 python3-pip -y

# 2. Install dependencies
pip install -r requirements.txt

# 3. Run the server (override env vars as you like)
DESIRED_PATH="/hello" PORT=8080 NUMBER=1 python app.py
