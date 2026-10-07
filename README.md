# Docker Assignment 1 - Part 2
## Step 2: Run the Docker Container:
docker run -d --name webapp -p 5002:5000 syedshah3994/hello-flask:1.0
6994005580c4d7f44124f951223a1647a4366cf7b9e114f39002add495dc5751
PS C:\Users\syedshah\Documents\GitHub\assignment1-part2> docker ps
CONTAINER ID   IMAGE                          COMMAND           CREATED          STATUS          PORTS                                         NAMES
6994005580c4   syedshah3994/hello-flask:1.0   "python app.py"   14 seconds ago   Up 13 seconds   0.0.0.0:5002->5000/tcp, [::]:5002->5000/tcp   webapp
094a00193310   syedshah3994/hello-flask:1.0   "python app.py"   22 minutes ago   Up 22 minutes   0.0.0.0:5001->5000/tcp, [::]:5001->5000/tcp   test-app
PS C:\Users\syedshah\Documents\GitHub\assignment1-part2> curl.exe http://localhost:5002
Hello from Docker! Assignment 1 - Syed Muhamamad Moin Ali Shah

## Step 3: Use Different Docker Container Commands"
### docker ps:
PS C:\Users\syedshah\Documents\GitHub\assignment1-part2> docker ps
CONTAINER ID   IMAGE                          COMMAND           CREATED          STATUS          PORTS                                         NAMES
6994005580c4   syedshah3994/hello-flask:1.0   "python app.py"   6 minutes ago    Up 6 minutes    0.0.0.0:5002->5000/tcp, [::]:5002->5000/tcp   webapp
094a00193310   syedshah3994/hello-flask:1.0   "python app.py"   28 minutes ago   Up 28 minutes   0.0.0.0:5001->5000/tcp, [::]:5001->5000/tcp   test-app

### docker logs webapp:
docker logs webapp
 * Serving Flask app 'app'
 * Debug mode: off
WARNING: This is a development server. Do not use it in a production deployment. Use a production WSGI server instead.
 * Running on all addresses (0.0.0.0)
 * Running on http://127.0.0.1:5000
 * Running on http://172.17.0.3:5000
Press CTRL+C to quit
Home page requested
172.17.0.1 - - [07/Oct/2026 09:57:12] "GET / HTTP/1.1" 200 -

### docker inspect webapp:
[
    {
        "Id": "6994005580c4d7f44124f951223a1647a4366cf7b9e114f39002add495dc5751",
        "Created": "2026-10-07T09:56:31.897402172Z",
        "Path": "python",
        "Args": [
            "app.py"
        ],
        "State": {
            "Status": "running",
            "Running": true,
            "Paused": false,
            "Restarting": false,
            "OOMKilled": false,
            "Dead": false,
            "Pid": 881,
            "ExitCode": 0,
            "Error": "",
            "StartedAt": "2026-10-07T09:56:31.946568435Z",
            "FinishedAt": "0001-01-01T00:00:00Z"
        },
        "Image": "sha256:58dba124f2934766b34abbb24a251f4ac20cf2459fdc8728c34419d8d8959558",
        "ResolvConfPath": "/var/lib/docker/containers/6994005580c4d7f44124f951223a1647a4366cf7b9e114f39002add495dc5751/resolv.conf",
        "HostnamePath": "/var/lib/docker/containers/6994005580c4d7f44124f951223a1647a4366cf7b9e114f39002add495dc5751/hostname",
        "HostsPath": "/var/lib/docker/containers/6994005580c4d7f44124f951223a1647a4366cf7b9e114f39002add495dc5751/hosts",
        "LogPath": "",
        "Name": "/webapp",
        "RestartCount": 0,
        "Driver": "overlayfs",
        "Platform": "linux",
        "MountLabel": "",
        "ProcessLabel": "",
        "AppArmorProfile": "",
        "ExecIDs": null,
        "HostConfig": {
            "Binds": null,
            "ContainerIDFile": "",
            "LogConfig": {
                "Type": "local",
                "Config": {}
            },
            "NetworkMode": "bridge",
            "PortBindings": {
                "5000/tcp": [
                    {
                        "HostIp": "",
                        "HostPort": "5002"
                    }
                ]
            },
            "RestartPolicy": {
                "Name": "no",
                "MaximumRetryCount": 0
            },
            "AutoRemove": false,
            "VolumeDriver": "",
            "VolumesFrom": null,
            "ConsoleSize": [
                21,
                196
            ],
            "CapAdd": null,
            "CapDrop": null,
            "CgroupnsMode": "private",
            "Dns": null,
            "DnsOptions": [],
            "DnsSearch": [],
            "ExtraHosts": null,
            "GroupAdd": null,
            "IpcMode": "private",
            "Cgroup": "",
            "Links": null,
            "OomScoreAdj": 0,
            "PidMode": "",
            "Privileged": false,
            "PublishAllPorts": false,
            "ReadonlyRootfs": false,
            "SecurityOpt": null,
            "UTSMode": "",
            "UsernsMode": "",
            "ShmSize": 67108864,
            "Runtime": "runc",
            "Isolation": "",
            "CpuShares": 0,
            "Memory": 0,
            "NanoCpus": 0,
            "CgroupParent": "",
            "BlkioWeight": 0,
            "BlkioWeightDevice": [],
            "BlkioDeviceReadBps": [],
            "BlkioDeviceWriteBps": [],
            "BlkioDeviceReadIOps": [],
            "BlkioDeviceWriteIOps": [],
            "CpuPeriod": 0,
            "CpuQuota": 0,
            "CpuRealtimePeriod": 0,
            "CpuRealtimeRuntime": 0,
            "CpusetCpus": "",
            "CpusetMems": "",
            "Devices": [],
            "DeviceCgroupRules": null,
            "DeviceRequests": null,
            "MemoryReservation": 0,
            "MemorySwap": 0,
            "MemorySwappiness": null,
            "OomKillDisable": null,
            "PidsLimit": null,
            "Ulimits": null,
            "CpuCount": 0,
            "CpuPercent": 0,
            "IOMaximumIOps": 0,
            "IOMaximumBandwidth": 0,
            "MaskedPaths": [
                "/proc/acpi",
                "/proc/asound",
                "/proc/interrupts",
                "/proc/kcore",
                "/proc/keys",
                "/proc/latency_stats",
                "/proc/sched_debug",
                "/proc/scsi",
                "/proc/timer_list",
                "/proc/timer_stats",
                "/sys/devices/virtual/powercap",
                "/sys/firmware"
            ],
            "ReadonlyPaths": [
                "/proc/bus",
                "/proc/fs",
                "/proc/irq",
                "/proc/sys",
                "/proc/sysrq-trigger"
            ]
        },
        "Storage": {
            "RootFS": {
                "Snapshot": {
                    "Name": "overlayfs"
                }
            }
        },
        "Mounts": [],
        "Config": {
            "Hostname": "6994005580c4",
            "Domainname": "",
            "User": "",
            "AttachStdin": false,
            "AttachStdout": false,
            "AttachStderr": false,
            "ExposedPorts": {
                "5000/tcp": {}
            },
            "Tty": false,
            "OpenStdin": false,
            "StdinOnce": false,
            "Env": [
                "PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin",
                "LANG=C.UTF-8",
                "GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305",
                "PYTHON_VERSION=3.12.15",
                "PYTHON_SHA256=c2c4321961fab0fb999d66e0cecf521c2ab3994c7992873ea99e306c1094fd5a",
                "PYTHONUNBUFFERED=1"
            ],
            "Cmd": [
                "python",
                "app.py"
            ],
            "Image": "syedshah3994/hello-flask:1.0",
            "Volumes": null,
            "WorkingDir": "/app",
            "Entrypoint": null,
            "Labels": {}
        },
        "NetworkSettings": {
            "SandboxID": "2e6fe07287e9513fd18fc64b4081ea6a7a9e22e09cac56f3092e271c0b6eb532",
            "SandboxKey": "/var/run/docker/netns/2e6fe07287e9",
            "Ports": {
                "5000/tcp": [
                    {
                        "HostIp": "0.0.0.0",
                        "HostPort": "5002"
                    },
                    {
                        "HostIp": "::",
                        "HostPort": "5002"
                    }
                ]
            },
            "Networks": {
                "bridge": {
                    "IPAMConfig": null,
                    "Links": null,
                    "Aliases": null,
                    "DriverOpts": null,
                    "GwPriority": 0,
                    "NetworkID": "be6ceb46ab9ad051cd05c642bda585154a306dc33996934c0764496e12eeccde",
                    "EndpointID": "bd92aa4ea6fa19f17cf073e7dff4723e3ac803eaf99e9d6e165615326f370a47",
                    "Gateway": "172.17.0.1",
                    "IPAddress": "172.17.0.3",
                    "MacAddress": "be:75:d6:4b:33:13",
                    "IPPrefixLen": 16,
                    "IPv6Gateway": "",
                    "GlobalIPv6Address": "",
                    "GlobalIPv6PrefixLen": 0,
                    "DNSNames": null
                }
            }
        },
        "ImageManifestDescriptor": {
            "mediaType": "application/vnd.oci.image.manifest.v1+json",
            "digest": "sha256:e5965c43e35ec60e35185bffb99de0ce07452c139a37ddbedf58146e7a8fa9c9",
            "size": 1810,
            "platform": {
                "architecture": "amd64",
                "os": "linux"
            }
        }
    }
]

### docker exec webapp ls /app:
docker exec webapp ls /app
app.py
requirements.txt

### docker top webapp:
UID                 PID                 PPID                C                   STIME               TTY                 TIME                CMD
root                881                 857                 0                   09:56               ?                   00:00:00            python app.py

### docker stats --no-stream:
CONTAINER ID   NAME       CPU %     MEM USAGE / LIMIT    MEM %     NET I/O         BLOCK I/O        PIDS
6994005580c4   webapp     0.02%     21.89MiB / 15.5GiB   0.14%     1.5kB / 784B    10.2MB / 176kB   1
094a00193310   test-app   0.01%     21.34MiB / 15.5GiB   0.13%     1.38kB / 126B   0B / 176kB       1

### docker port webapp:
5000/tcp -> 0.0.0.0:5002
5000/tcp -> [::]:5002

### docker cp webapp:/app/app.py ./app_copy.py:
Successfully copied 273B (transferred 2.05kB) to C:\Users\hamza\Documents\GitHub\assignment1-part2\app_copy.py

### docker commit webapp syedshah3994/hello-flask:committed:
sha256:dbddb9bdfcc6eafec44b68538211527967a054575ae9db57036dc6424ed1475d

### docker pause webapp:
webapp

### docker unpause webapp:
webapp

### docker rename webapp webapp-renamed:
### docker update --memory 256m --memory-swap 512m webapp-renamed
webapp-renamed

### docker restart webapp-renamed:
webapp-renamed

### docker attach:
docker: 'docker attach' requires 1 argument

Usage:  docker attach [OPTIONS] CONTAINER

### docker stop webapp-renamed:
webapp-renamed

### docker start webapp-renamed:
webapp-renamed

### docker wait:
docker: 'docker wait' requires at least 1 argument

Usage:  docker wait CONTAINER [CONTAINER...]

### docker rm:
docker: 'docker rm' requires at least 1 argument

Usage:  docker rm [OPTIONS] CONTAINER [CONTAINER...]