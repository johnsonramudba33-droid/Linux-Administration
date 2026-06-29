# Day 02 - Linux Basic Commands

## Objective
Learn the basic Linux commands used in a production environment.

---

## 1. Host Information

### Find Hostname

```bash
hostname
```

### Find IP Address

```bash
hostname -I
```

---

## 2. System Uptime

```bash
uptime
uptime --pretty
```

---

## 3. Hardware Resources

### Memory

```bash
free -gh
```

### CPU

```bash
lscpu
```

### Disk

```bash
lsblk
df -h
```

---

## 4. User Management

Normal User Prompt

```text
rnos@server:~$
```

Root User

```bash
sudo -i
```

```text
root@server:~#
```

---

## Practice

Run the following commands:

- hostname
- hostname -I
- uptime
- free -gh
- lscpu
- lsblk
- df -h