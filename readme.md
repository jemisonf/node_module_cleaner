# Node Module Cleaner

This is a simple Python script you can use to clean out `node_modules` folders, which can grow to take up quite a large amount of space over time. As a case study, I used this script to save myself 5 GB of space on my 100 GB /home partition.

Use is pretty simple:
```bash
./clean_node_modules.py $PATH
```

Will recursively remove all `node_modules` directories in subdirectories of `$PATH`. You can use the `-h` flag to get help.

## Other info

**Is this safe?** Not 100%, but you're probably not in danger unless you have stuff in your `node_modules` folders that you can't replace. This shouldn't break any application code for your projects, but you will have to re-install dependencies for any projects affected.

**Is this fast?** Not especially. Don't be surprised if it takes >30s-1m for larger file trees.
