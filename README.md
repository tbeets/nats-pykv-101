# nats-pykv-101
Basic kick the tires on NATS Key-Value API (Python)

# Pre-requisites
* Python 3.8+

# Installation

```bash
git clone https://github.com/tbeets/nats-pykv-101.git; cd nats-pykv-101
python3 -m venv ./venv; ./venv/bin/activate; python3 -m pip -r requirements.txt
```

# Execution

```bash
# mybucket
python __main__.py --servers "nats://vbox1.tinghus.net:4222" --creds "/home/todd/lab/nats-cluster1/vault/.nkeys/creds/NatsOp/AcctA/UserA1.creds" hello "world"

# mywatch
python __main__.py --servers "nats://vbox1.tinghus.net:4222" --creds "/home/todd/lab/nats-cluster1/vault/.nkeys/creds/NatsOp/AcctA/UserA1.creds" hello
```
# API Notes

```python
kv = await js.create_key_value(bucket='bucket name')
```
| Type | Methods, Attr |
| --- | --- |
| kv | put, get |
| entry | .key, .value |


