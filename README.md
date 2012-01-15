#ASCII, Dammit

Stupid library to turn MS chars (like smart quotes) and ISO-Latin
chars into ASCII, dammit. Will do plain text approximations, or more
accurate HTML representations. Can also be jiggered to just fix the
smart quotes and leave the rest of ISO-Latin alone.

##Usage
		french = '\x93Sacr\xe9 bleu!\x93'
		print "First we mangle some French."
		print asciiDammit(french) #"Sacre bleu!"
		print htmlDammit(french) #&ldquo;Sacr&eacute; bleu!&ldquo;

		print
		print "And now we fix the MS-quotes but leave the French alone."
		print demoronise(french) #"Sacr� bleu!"
		print htmlDammit(french, 1) #&ldquo;Sacr� bleu!&ldquo;

		print "Let's try some french in unicode"
		frenchu = u'sacré bleu'
		print asciiDammit(frenchu) #sacre bleu

		dejavu = u'Déjà Vu'
		print "It's usually a glitch in the Matrix. It happens when they change something."
		print asciiDammit(dejavu) #Deja Vu

##Sources:
 http://www.cs.tut.fi/~jkorpela/latin1/all.html
 http://www.webreference.com/html/reference/character/isolat1.html

- 1.0 Initial Release (2004-11-28)
- 1.1 Fixed handling of unicode strings (2012-01-15) - Tom Najdek

##License
The author hereby irrevocably places this work in the public domain.
To the extent that this statement does not divest the copyright,
the copyright holder hereby grants irrevocably to every recipient
all rights in this work otherwise reserved under copyright.