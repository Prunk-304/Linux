#!/bin/sh

identf() {
	echo "Is your  name $*?"
	while true
	do
	echo -n "Enter yes or no: "
	read x

	case "$x" in
	[Yy][Ee][Ss] ) return 0;;
	[Nn][Oo] ) return 1;;
	* ) echo "Try again."
	esac	
	done
}

echo "Entered name is $*"
if identf "$1"
then
echo "Hi $1, nice to meet you."
else
echo "Never mind"
fi
exit 0
exit 0
