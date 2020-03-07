# General Tips
 - Compression only helps if the network link is quite slow or transferring is otherwise expensive *and* both ends have sufficient CPU power to compress/decompress.
   - EG: LTE connection/tether

# Python HTTP Server
```bash
cd /dir/containing/files
python3 -m http.server
```
Open a web browser on destination computer and navigate to `sourcecomputernameorIPaddress:8000`

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
