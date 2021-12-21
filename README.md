# Python_hemmelige_koder
# Starter code from www kidsakoder no
# krypteringsdelen:

# alphabet er navnet på teksten fra a til å
alphabet = "abcdefghijklmnopqrstuvwxyzæøå"

# Den hemmelige bokstaven (letter) og det hemmelige tallet
# (key) vi bruker for å kode det
letter = "a"
key = 3

# Finn posisjonen til bokstaven. Python vil gi oss et
# tall fra 0 til 28 (python teller fra 0)
pos = alphabet.find(letter)

# Gå like langt fremover som det hemmelige tallet sier
newpos = (pos + key)

# Hvis vi har telt for langt, må vi gå en runde tilbake
# for å få et tall mellom 0 og 28
if newpos >= 29:
    newpos = newpos - 29

# Slå opp denne posisjonen for å se hvilken bokstav
# i alfabetet som står der
secretletter = alphabet[newpos]

# Skriv denne bokstaven ut på skjermen
print(secretletter)


# dekrypteringsdelen:
alphabet = "abcdefghijklmnopqrstuvwxyzæøå"

key = 17
secretletter = "r"

pos = alphabet.find(secretletter)

newpos = pos - key

if newpos < 0:
    newpos = newpos + 29

letter = alphabet[newpos]

print(letter)
