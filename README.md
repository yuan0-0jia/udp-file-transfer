# UDP-File-Transfer

A UDP client-server program with data recovery.

## Usage

First run the server with the following command:

```
./myserver server_port drop_rate output_file_folder
```
Server takes in drop_rate, between 0 and 100, to drop packets, 0 means no packet will be dropped, 100 means all packets will be dropped.
It also stores the transfered file into the output_file_folder.

Then run the client to transfer file to the server with the following command:

```
./myclient server_ip server_port mtu window_size input_file output_file_name
```

Client sents out at most window_size number of packets that are yet to be acknowledged, each packet sizes upto mtu.
