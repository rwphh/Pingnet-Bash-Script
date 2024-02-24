# Pingnet-Bash-Script
#!/bin/bash  if [ "$1" == "" ]  then         echo "Modo de uso: $0 + rede" else for ip in {1..254}; do ping -c 1 $1.$ip | grep "64 bytes" | cut -d " " -f 4 | sed 's/.$//'  done fi
