# systemd Unit Templates (lite)

Free subset. An oneshot, a long-running simple service, and a timer pair. The full pack adds forking, notify, a path unit, a socket stub, a drop-in, and the generator.

## English

### Deliverables

- `deliverables/backup-oneshot.service` — Type=oneshot
- `deliverables/worker-simple.service` — Type=simple
- `deliverables/report-daily.service` and `deliverables/report-daily.timer` — 06:15 calendar pair
- `deliverables/INSTALL.md` — copy path and which unit to enable

```bash
sudo cp deliverables/worker-simple.service /etc/systemd/system/
sudo systemctl daemon-reload
```

Each service sets User, ProtectSystem=strict, and NoNewPrivileges. Enable `report-daily.timer`, not `report-daily.service`.

Full version: GUMROAD_URL

## 中文

免费子集：oneshot、长期运行的 simple，以及一对 timer。完整版另有 forking、notify、path、socket、drop-in 和生成器。

### 交付物

- `deliverables/backup-oneshot.service` — Type=oneshot
- `deliverables/worker-simple.service` — Type=simple
- `deliverables/report-daily.service` 和 `deliverables/report-daily.timer` — 每天 06:15
- `deliverables/INSTALL.md` — 拷贝路径，以及应该 enable 哪一个单元

每个 service 都设置了 User、ProtectSystem=strict 和 NoNewPrivileges。要 enable 的是 `report-daily.timer`，不是 `report-daily.service`。

Full version: GUMROAD_URL

## Delivery time / 交付时间

Delivery time: instant download after purchase
