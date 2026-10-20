# Install (lite)

```bash
sudo cp worker-simple.service /etc/systemd/system/
sudo systemctl daemon-reload
sudo systemctl enable --now worker-simple.service
```

For the daily report, copy both `report-daily.service` and `report-daily.timer`, then enable the timer only:

```bash
sudo cp report-daily.service report-daily.timer /etc/systemd/system/
sudo systemctl daemon-reload
sudo systemctl enable --now report-daily.timer
```

`backup-oneshot.service` is a one-shot you start with `systemctl start`.

Each service sets `User=root` until you replace it with a dedicated account, `NoNewPrivileges=yes`, and `ProtectSystem=strict`. `systemd-analyze verify` reports "not executable" when the ExecStart path is not installed yet. That is not a syntax error.

The full pack adds forking, notify, a path unit, a socket stub, a drop-in override, and `gen_unit.py`.
