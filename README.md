# hyperdrive-backwards
Automagically figure out which hyperdrive version to use

- If a specific drive version was specified, use that.
- If not, create a proxy object
- Initialize a hypercore for metadata feed
- Have the proxy fulfill whatever is possible using the hyprecore data
- Have all other methods wait for the hyperdrive to load and queue up commands
- Attempt to get the [hypercore header](https://github.com/datprotocol/DEPs/blob/master/proposals/0007-hypercore-header.md)
- Detect the archive type from there
- Initialize the correct type of hyperdrive
- Switch out the proxy to use the hyperdrive and execute the commands in the queue
