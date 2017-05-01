# reposearch
A little helper shell script for searching repositories.

Yeah, Atom/whatever can do it, but this is mad fast.

## Installation

Add files to somewhere in your $PATH, perhaps `/usr/local/bin`

```
sudo cp repo* /usr/local/bin
```


## Usage

```
reposearch [terms]
reposearch [grep arguments] [terms]

# Example--to see a few lines of context,
reposearch -3 [terms]
```

If the index does not yet exist, `reposearch` will call `repoindex` automatically. 

Indexes are created a directory above the repository, as `.index.REPONAME.gz`

If the index becomes stale, use `repoindex`:

```
repoindex 
# looks for a repository in the current directory or higher

repoindex [repo base dir]
```

## Future improvements

- Automatically reindex after X days

## Caveats

- Ignores `*.min.*`, `app.*`, `.git/*`



