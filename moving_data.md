# General Tips
 - Compression only helps if the network link is quite slow or transferring is otherwise expensive
   - EG: LTE connection/tether

# rsync

## Examples
```bash
rsync -avW -e ssh /path/to/dir/ remote_server:/path/to/remotedir
```
https://serverfault.com/a/18142

TODO: When is this faster?


# tar

## Examples
```bash
tar -c /path/to/dir | ssh remote_server 'tar -xvf - -C /absolute/path/to/remotedir'
```
https://serverfault.com/a/18142

TODO: When is this faster?
