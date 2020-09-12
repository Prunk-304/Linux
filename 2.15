#!/bin/sh

trap 'rm -f /tmp/tmp_file_$$' INT
echo Crearing file: /tmp/tmp_file_$$
date > /tmp/tmp_file_$$

echo "Press CTRL+C to interrupt..."
while [ -f /tmp/tmp_file_$$ ]; do
	echo File still exist
	sleep 1
done
echo The file no longer exists

trap INT
echo Creating file: /tmp/tmp_file_$$
date > /tmp/tmp_file_$$

echo "Press CTRL+C to interrupt..."
while [ -f /tmp/tmp_file_$$ ]; do
        echo File still exist
        sleep 1
done

echo We never get here
exit 0
