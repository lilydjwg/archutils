My personal scripts for Arch Linux
====

Find orphan files
----

To find orphan files in `/usr` (files that are not owned by any packages), run

```sh
./findorphanfiles
```

But it will output many generated files that are expected to be orphans. So
a filter can be used to filter out common known orphan files:

```sh
./findorphanfiles | ./filter_noextract orphanfiles.filter
```
