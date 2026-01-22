all: main.c policy.txt
	cc -g main.c -o normal -Wl,--compartment-policy=policy.txt
	cp normal compart
	elfctl -e +nocheric18n ./normal
	elfctl -e +cheric18n ./compart

clean:
	rm -f main compart main.core
