#!/bin/bash
# Program_Name: weather.sh
# Copyright Updated by Copilot. All rights reserved.
# Syntax to run it ./weather.sh -l location
# Date: 4/2/25

program="Weather"
version="1.0"
year="2025"
developer="Microsoft Copilot"

case $1 in
  -h | --help)
    echo "$program $version"
    echo "Copyright $year $developer. All rights reserved."
    echo
    echo "Usage: weather [options]"
    echo "Option        Long Option       Description"
    echo "-h            --help            Show the help screen"
    echo "-l [location] --location        Specifies the location"
    ;;
  -l | --location)
    curl https://wttr.in/$2
    ;;
  *)
    curl https://wttr.in
    ;;
esac
