def gen(x, mod, zahlen, ordnung, pListe):
	zahl = x
	zahlen.append(x)
	for i in range(mod-1):
		zahl = (zahl*x)%mod
		zahlen.append(zahl)
		if(zahl == 1):
			if (len(zahlen) == ordnung):
				if pListe == "w":
					print(zahlen)
				else:
					print(x)
			break

def bestimmeUntergruppe():
	mod = int(input("Welche Gruppe?: "))
	ordnungWahl = mod-1
	ordnung = int(input("Welche Ordnung? Waehle zwischen 2 und %s: " %ordnungWahl))
	pListe = input("Liste(w) oder Rang(f): ")
	for i in range(mod):
		zahlen = []
		gen(i, mod, zahlen, ordnung, pListe)

bestimmeUntergruppe()

