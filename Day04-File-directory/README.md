# Day 04 – Linux Directory Management Commands

## Objective

Learn how to create, navigate, copy, move, remove, and inspect directories in Linux. These commands are essential for Linux Administrators and Database Administrators to manage database files, backup directories, configuration folders, and log locations.

---

# Topics Covered

- Create Directory
- Nested Directory Creation
- Navigate Between Directories
- Display Current Directory
- Copy Directory
- Move Directory
- Remove Directory
- Display File & Directory Information
- View Directory Structure
- File & Directory Metadata

---

# 1. Create Directory

### Create a Single Directory

```bash
mkdir welina_db
```

### Create Nested Directories

```bash
mkdir -p /welina_db/node_1/conf
```

**Real-Time DBA Example**

Create a directory structure for PostgreSQL configuration.

```text
/welina_db
└── node_1
    └── conf
```

---

# 2. Change Directory

Move into a directory.

```bash
cd /welina_db/node_1/conf
```

Return to Home Directory.

```bash
cd
```

Move to Previous Directory.

```bash
cd -
```

Move One Level Up.

```bash
cd ..
```

Move Two Levels Up.

```bash
cd ../../
```

---

# 3. Display Current Working Directory

```bash
pwd
```

Example Output

```text
/welina_db/node_1/conf
```

---

# 4. Copy Directory

Copy an entire directory recursively.

```bash
cp -rpf /welina_db/ /tmp/
```

### Options

| Option | Description |
|---------|-------------|
| `-r` | Copy recursively |
| `-p` | Preserve permissions and timestamps |
| `-f` | Force overwrite |

Verify:

```bash
ls -ld /tmp/welina_db/
```

---

# 5. Move Directory

Move a directory to another location.

```bash
mv /welina_db/ /tmp/
```

Verify:

```bash
ls -ld /tmp/welina_db/
```

---

# 6. Remove Directory

Remove an empty directory.

```bash
rmdir /tmp/welina_db/
```

If the directory is not empty:

```text
rmdir: failed to remove '/tmp/welina_db/': Directory not empty
```

Remove a non-empty directory.

```bash
rm -rf /tmp/welina_db/
```

Verify:

```bash
ls -ld /tmp/welina_db/
```

---

# 7. View File and Directory Information

Display detailed information about a file.

```bash
stat index.html
```

Display detailed information about a directory.

```bash
stat snap/
```

Useful Information

- File Size
- Permissions
- Owner
- Group
- Last Access Time
- Last Modification Time
- Inode Number

---

# 8. Display Directory Structure

Install Tree Utility (if required)

```bash
sudo apt install tree
```

View Directory Structure

```bash
tree /tmp/welina_db/
```

Example Output

```text
welina_db/
└── node_1
    └── conf

3 directories, 0 files
```

---

# Real-Time DBA Examples

### PostgreSQL

```text
/var/lib/postgresql/

/var/lib/postgresql/data

/var/lib/postgresql/archive

/backup

/log
```

### MongoDB

```text
/data/db

/var/log/mongodb
```

### Cassandra

```text
/var/lib/cassandra

/commitlog

/data

/hints
```

---

# Interview Questions

### Q1. Which command creates a directory?

```bash
mkdir
```

---

### Q2. Which command creates nested directories?

```bash
mkdir -p
```

---

### Q3. Which command displays the current directory?

```bash
pwd
```

---

### Q4. Which command moves a directory?

```bash
mv
```

---

### Q5. Which command copies a directory recursively?

```bash
cp -r
```

---

### Q6. Difference between `rmdir` and `rm -rf`?

| Command | Description |
|----------|-------------|
| `rmdir` | Removes only empty directories |
| `rm -rf` | Removes non-empty directories recursively |

---

### Q7. Which command displays file metadata?

```bash
stat
```

---

### Q8. Which command displays the directory tree?

```bash
tree
```

---

# Student Practical

- Create a directory named `linux_lab`.
- Create nested directories using `mkdir -p`.
- Navigate using `cd`.
- Verify the current directory using `pwd`.
- Copy the directory to `/tmp`.
- Move the copied directory.
- Display the directory tree.
- View metadata using `stat`.
- Delete the directory using `rm -rf`.

---

# Commands Learned

```text
mkdir
mkdir -p
cd
cd -
cd ..
pwd
cp -rpf
mv
rmdir
rm -rf
stat
tree
ls -ld
```

---

# Real-Time DBA Use Cases

- Create database directories.
- Organize backup locations.
- Manage log directories.
- Verify filesystem structure.
- Preserve directory permissions during migration.
- Move database files between storage locations.

---

**Prepared By:** RNOS Technology  
**Course:** Linux for PostgreSQL DBA  
**Day:** 04 – Directory Management Commands