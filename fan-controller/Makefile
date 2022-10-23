all: fan.c
	gcc -o fan-controller -lwiringPi fan.c

install:
	mkdir -p /opt/Fan-Controller
	cp fan-controller /opt/Fan-Controller/
	chmod +x /opt/Fan-Controller/fan-controller
	cp fan-controller.service /lib/systemd/system/
	systemctl daemon-reload
	systemctl enable fan-controller
	systemctl start fan-controller
