# Useful commands

% UsefulCommands

## hostDiscover - extract IPs
#plateform/linux #target/remote #port/80 #protocol/http #cat/ATTACK/
```
cat <nmap-shOut> | grep report | awk '{print $NF}'
```

## hashcat - create list using rules
#plateform/linux #target/remote #port/80 #protocol/http #cat/ATTACK/
```
hashcat --force <passwordlist> -r <customrule> --stdout | sort -u > mut_password.list
```

## Phishing - accents - acute
#plateform/linux #target/remote #port/23 #protocol/smtp #cat/ATTACK/
```
cat <mail.html> | sed 's/á/\&aacute;/g; s/é/\&eacute;/g; s/í/\&iacute;/g; s/ó/\&oacute;/g; s/ú/\&uacute;/g' > <outMail.html>
```

## Ports list
#plateform/linux #target/remote #port/80 #protocol/http #cat/ATTACK/
```
for port in {1..65535};do echo $port >> ports.txt;done
```

## URL encode with jq
#plateform/linux #target/local #port/21 #protocol/ssh #cat/ATTACK/
```
echo "<text>" | jq -sRr @uri
```

## php webserver
#plateform/linux #target/local #port/21 #protocol/ssh #cat/ATTACK/
```
sudo php -S 0.0.0.0:80
```

## rustscan
#plateform/linux #target/remote #port/ #protocol/ #cat/ATTACK/
```
rustscan -a <targetIP> --ulimit 3000 -- -sVC -Pn
```
