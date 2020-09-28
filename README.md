# Tensorflow

Built from latest Tensorflow image, then has object detection, opencv, Flask, PahoMQtt and basically anything else I needed to detect people on an IP camera stream and push a notification into an MQTT channel.

image expects a bash script to run, so something like:

docker run -v $(pwd):/dat deicist/object_detection /dat/runme.sh

where 'runme.sh' in the current directory is something like:

#!/bin/bash
/usr/bin/python3 /dat/detection.py
