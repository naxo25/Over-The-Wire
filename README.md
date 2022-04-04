# OverTheWire

https://overthewire.org/wargames/bandit/

## Conexión ssh
	ssh banditX@bandit.labs.overthewire.org -p 2220 

## Ej
	ssh bandit0@bandit.labs.overthewire.org -p 2220 
	pw: bandit0
	cat readme

## 5
Buscar archivo con permisos de lectura y escritura

	find inhere -type f -readable ! -executable -size 1033c

## 6
Buscar a nivel global un archivo correspondiente a usuario bandit7 con grupo bandit6 y el peso del archivo de 33 bits

	find / -user bandit7 -group bandit6 size 33c

## 7
Buscar una linea con una palabra

	grep 'palabra' data.txt

## 8
Buscar lúnea única

	cat data.txt | sort | uniq -u

## 9
Separar las lineas cuando terminan los carácteres y contengan varios '='

	cont=1; strings data.txt | grep '===' | while read line; do echo "Línea $cont"; let cont+= 1; done

## 10
Decodificar

	cat data.txt | base64 -d

## 11
Rotar 13 posiciones

	cat data.txt | tr '[G-ZA-Fg-za-f]' '[T-ZA-St-za-s]'
