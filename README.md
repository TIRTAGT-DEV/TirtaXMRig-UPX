# TirtaXMRig-UPX

TirtaXMRig-UPX is a unrestircted version high performance uPlexa (UPX) CPU miner, that can be used on Windows and Linux based platform. Originally based on the official XMRig-UPX by @QuantumLeaper.


![Screenshot of the TirtaXMRig-UPX screen](https://github.com/TIRTAGT-DEV/TirtaXMRig-UPX/blob/master/res/TirtaXMRig-UPX.png?raw=true "Screenshot of TirtaXMRig-UPX")

***

## Download
* Releases: https://github.com/TIRTAGT-DEV/TirtaXMRig-UPX/releases
* Git URL: https://github.com/TIRTAGT-DEV/TirtaXMRig-UPX.git
* Clone with `sudo git clone https://github.com/TIRTAGT-DEV/TirtaXMRig-UPX.git`
 
[Build instructions](https://github.com/TIRTAGT-DEV/TirtaXMRig-UPX/Guide/build/readme.md).

## How to use
Directly configure the app using the available command line options or the `Config.KenF` file on the build folde then execute the app and it should start running.

## Command Line Options
```
Short | Long Command      | Explanation
  -a  | --algo=ALGO       |  specify the algorithm to use
  -o  | --url=URL         |  URL of mining server
  -O  | --userpass=U:P    |  username:password pair for mining server
  -u  | --user=USERNAME   |  username for mining server
  -p  | --pass=PASSWORD   |  password for mining server
        --rig-id=ID       |  rig identifier for pool system
  -t  | --threads=N       |  number of miner threads
  -v  | --av=N            |  algorithm variation, 0 auto select
  -k  | --keepalive       | send keepalived packet for prevent timeout
        --nicehash        | enable nicehash.com support
        --tls             |  enable SSL/TLS support (needs pool support)
        --tls-fingerprint=F | pool TLS certificate fingerprint
  -r  | --retries=N       | number of retry before switch to backup pools
  -R  | --retry-pause=N   | time to pause between retries (seconds)
        --cpu-affinity    |  set affinity to CPU core, mask 0x3 for 0,1 core
        --cpu-priority    |  set process priority [0 idle, 2 normal, 5 highest]
        --no-huge-pages   |  disable huge pages support
        --no-color        | disable colored output
        --variant         |  algorithm PoW variant
        --donate-level=N  |  donate level, default 0%
        --user-agent      |  set custom user-agent string for pool
  -B  | --background      | run the miner in the background
  -c  | --config=FILE     |  load a JSON-format configuration file
  -l  | --log-file=FILE   |  log all output to a file
  -S  | --syslog          |  use system log for output messages
        --max-cpu-usage=N |  maximum CPU usage for automatic threads mode
        --safe            |  safe adjust threads and av settings for CPU
        --asm=ASM         |  ASM code for cn/2 [auto, none, intel, ryzen.]
        --print-time=N    |  print hashrate report every N seconds
        --api-port=N      |  port for the miner API
        --api-access-token=T | access token for API
        --api-worker-id=x | custom worker-id for API
        --api-id=ID       |  custom instance ID for API
        --api-ipv6        |  enable IPv6 support for API
        --api-no-restricted |  enable full remote access if API token set
        --dry-run         | test configuration and exit
  -h  | --help            |  display this help and exit
  -V  | --version         |  output version information and exit
```

Also you can use configuration via config file, default name **Config.KenF**.

## Algorithm variations

- `av` option used for automatic and simple threads mode (when you specify only threads count).

| av | Hashes per round | Hardware AES |
|----|------------------|--------------|
| 1  | 1 (Single)       | yes          |
| 2  | 2 (Double)       | yes          |
| 3  | 1 (Single)       | no           |
| 4  | 2 (Double)       | no           |
| 5  | 3 (Triple)       | yes          |
| 6  | 4 (Quard)        | yes          |
| 7  | 5 (Penta)        | yes          |
| 8  | 3 (Triple)       | no           |
| 9  | 4 (Quard)        | no           |
| 10 | 5 (Penta)        | no           |

## FAQ Section

-`` Huge Pages Not available ?  ``Run the miner with admin permission.
``* No HTTP support available ? `` Yes, only stratum protocol support.
``How to maximize performance ? `` These guide can help you : 
```
* Let the System mine without any interruptions 
* Do not exceed optimal thread value (Leave it auto or not configured).
* Use modern CPUs with AES instruction set.
* Enable Fast memory (Large/Huge pages).
```

## TIRTAGT Community
* [Discord Server](https://discord.gg/GJjQ3at)
