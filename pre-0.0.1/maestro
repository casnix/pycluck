#!/usr/bin/python
from subprocess import call

import sys


def xprintnl(msg):
	sys.stdout.write("pyMaestro["+msg+"]\n")
	sys.stdout.flush()
	return;

def xprint(msg):
	sys.stdout.write("pyMaestro :--: "+msg)
	sys.stdout.flush()
	return;

if len(sys.argv) ==1:
	print("usage: "+sys.argv[0]+" [build | clean | install]")
elif len(sys.argv) >1:
	if sys.argv[1] =="build":
		xprintnl("Sanitizing ./base.bmp...")
		call(["./sanitize.py"])
		xprintnl("done")
		xprintnl("Automagically generating color variations...")
		call(["./autoimages.py"])
		xprintnl("done")
	elif sys.argv[1] =="clean":
		xprintnl("Cleaning up litter and useless PNG...")
		call(["rm", "./*.png"])
		xprintnl("done")
	elif sys.argv[1] =="install":
		xprintnl("Moving images to ./deploy/ ...")
		call(["cd", "./*.png", "./deploy/"])
		
