# Restart a worker

### Prerequisite
Login to the machine with your ssh key under the ubuntu user.

### To stop the validator
Run
> No needed if its not already stopped / dead
```bash
sudo systemctl stop sol
```

### To restart it
Run
```bash
python3 snapshot-finder.py --snapshot_path /mnt/solana-snapshots --version 1.18 --max_latency 150 ; sudo systemctl start sol
```

### To check if everything is going well
```bash
solana-validator --ledger /mnt/solana-ledger/ monitor
```
