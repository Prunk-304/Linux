#!/bin/sh

menu_choice=""
current_cd=""
title_file="title.cdb"
tracks_file="tracks.cdb"
temp_file=/tmp/cdb.$$
trap 'rm -f $temp_file' EXIT

get_return() {
echo -e "Press return \c"
read x
return 0
}

get_confirm() {
echo -e "Are you sure? \c"
while true
do
read x
case "$x" in
	[Yy][Ee][Ss] )
	return 0;;
	[Nn][Oo] )
	echo
	echo "Cancelled"
	return 1;;
	* ) 
	echo "Invalid response";;
esac
done
}

set_menu_choice() {
clear
echo "Options:-"
echo
echo " a) Add new CD"
echo " f) Find CD"
echo " c) Count the CDs and tracks in the catalog"
if [ "cdcatnum" != "" ]; then
echo " l) List tracks on $cdtitle"
echo " r) Remove $cdtotle"
echo " u)Update track information for $cdtittle"
fi
echo " q) Quit"
echo
echo -e "Please enter choice then press return \c"
return
}

insert_title() {
echo $* >> $title_file
return
}

insert_track() {
echo $* >> $tracks_file
}

add_record_tracks() {
echo "Enter track information for this CD"
echo "When no more tracks enter q"
cdtrack=1
cdtitle=""
while [ "$cdtitle" != "q" ]
do
 echo -e "Track $cdtrack, track title? \c"
 read tmp
 cdtitle=${tmp%%, *}
 if [ "$tmp" != "$cdtitle" ] then
  echo "Sorry, no comas allowed"
  continue
 fi

 if [ -n "$cdtittle" ]; then
  if [ "$cdtittle" != "q" ]; then
   insert_track $cdcatnum, $cdtrack, $cdtitle
  fi
 else
  cdtrack=$((cdtrack-1))
 fi
 cdtrack=$((cdtrack+1))
done
}

