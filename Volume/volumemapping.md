docker run --name ubuntu2 -v hostpath:containerpath -d ubuntu /bin/sh -c "while true; do ping 8.8.8.8; done"
