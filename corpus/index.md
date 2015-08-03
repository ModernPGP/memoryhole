This page contains examples of Memory Hole-compliant e-mails. You can
check your favourite mail user agent's compliance with the Memory Hole
standard by checking the screenshots associated with each e-mail.
### Contents
<ul>
  
<li>
    
  <a href="#A">A: alternative text/html message with embedded header, signed   </a>
  </li>
<li>
    
  <a href="#B">B: alternative text/html message with embedded header, unsigned   </a>
  </li>
<li>
    
  <a href="#C">C: alternative text/html message with embedded header, signed, with Subject tampered   </a>
  </li>
<li>
    
  <a href="#D">D: alternative text/html message with embedded header, encrypted+unsigned   </a>
  </li>
<li>
    
  <a href="#E">E: alternative text/html message with embedded header, encrypted+signed   </a>
  </li>
<li>
    
  <a href="#F">F: headers in top-level MIME object: plaintext email   </a>
  </li>
<li>
    
  <a href="#G">G: headers in top-level MIME object: signed multipart email   </a>
  </li>
<li>
    
  <a href="#H">H: headers in top-level MIME: tampered subject and from   </a>
  </li>

</ul>
### Examples
<h3 id="A" class="mail-example">
Email A: 
</h3>
alternative text/html message with embedded header, signed 
<pre>
└┬╴multipart/signed 1819 bytes
 ├┬╴multipart/mixed 917 bytes
 │├─╴text/rfc822-headers attachment 205 bytes
 │└┬╴multipart/alternative 504 bytes
 │ ├─╴text/plain 86 bytes
 │ └─╴text/html 202 bytes
 └─╴application/pgp-signature 455 bytes</pre>
<div class="code-block"><span style="color:#dc322f;">Subject:</span> alternative text/html message with embedded header, signed
<span style="color:#268bd2;">Message-ID:</span> A@memoryhole.example
<span style="color:#268bd2;">Date:</span> Thu, 16 Jul 2015 11:44:44 +0200
<span style="color:#859900;">To:</span> Julia <julia@example.org>
<span style="color:#cb4b16;">From:</span> Winston <winston@example.net>
<span style="color:#268bd2;">MIME-Version:</span> 1.0
<span style="color:#268bd2;">Content-Type:</span> multipart/signed; micalg="pgp-sha256";
 protocol="application/pgp-signature"; boundary="cccccccccccc"

<span style="color:#2aa198;">--cccccccccccc</span>
<span style="color:#268bd2;">MIME-Version:</span> 1.0
<span style="color:#268bd2;">Content-Type:</span> multipart/mixed; boundary="bbbbbbbbbbbb"

<span style="color:#2aa198;">--bbbbbbbbbbbb</span>
<span style="color:#268bd2;">MIME-Version:</span> 1.0
<span style="color:#268bd2;">Content-Type:</span> text/rfc822-headers
<span style="color:#268bd2;">Content-Disposition:</span> attachment

<span style="color:#268bd2;">Date:</span> Thu, 16 Jul 2015 11:44:44 +0200
<span style="color:#dc322f;">Subject:</span> alternative text/html message with embedded header, signed
<span style="color:#cb4b16;">From:</span> Winston <winston@example.net>
<span style="color:#859900;">To:</span> Julia <julia@example.org>
<span style="color:#268bd2;">Message-ID:</span> A@memoryhole.example

<span style="color:#2aa198;">--bbbbbbbbbbbb</span>
<span style="color:#268bd2;">MIME-Version:</span> 1.0
<span style="color:#268bd2;">Content-Type:</span> multipart/alternative; boundary="aaaaaaaaaaaa"

<span style="color:#2aa198;">--aaaaaaaaaaaa</span>
<span style="color:#268bd2;">MIME-Version:</span> 1.0
<span style="color:#268bd2;">Content-Type:</span> text/plain

This is a test
message on multiple lines

with a silly bit more.
-- 
and a .sig here.

<span style="color:#2aa198;">--aaaaaaaaaaaa</span>
<span style="color:#268bd2;">MIME-Version:</span> 1.0
<span style="color:#268bd2;">Content-Type:</span> text/html

<html>
<head>
<title>titles are usually unrendered</title>
</head>
<body>
<p>This is a test<br/>message on multiple lines</p>
<p>with a silly bit more.</p>
<hr/>
<p>and a .sig here.</p>
</body>
</html>

<span style="color:#2aa198;">--aaaaaaaaaaaa</span>

<span style="color:#2aa198;">--bbbbbbbbbbbb</span>

<span style="color:#2aa198;">--cccccccccccc</span>
<span style="color:#268bd2;">MIME-Version:</span> 1.0
<span style="color:#268bd2;">Content-Type:</span> application/pgp-signature

-----BEGIN PGP SIGNATURE-----

iQEcBAABCAAGBQJVt/DjAAoJEBX7TryOLWy3JkIH/iYCfu47jAxUqRDy2AgOL31n
4Sscl806URFG4940w5OTMiXHz0Ji0fCrMo8jSS+D3JCD6e2f+yC0tn4TFDkmNp8n
iuwQzJ7ytGy97MiTjom8+ThqWWaeHvxiHBLnpWIqN71+1ozBkF2MKqrPvJu/U83Z
H+hQA8qtggUXpXPSFgedYMHfTo0DpnaK3Xd+ZWgKOSEn+kPhlepjMsrgVkq2IGsn
IYyyEQYKf9mrsgs6oCq37ggnB367/kfBPq27E4TxXxK4mOjctNEM9/9aetKFXhRr
f33w+GO0+/1NeVKxul/25Q+Emt0LtZeMFS5Aj3E9JqD0TfKWo0j5k2lEjMqiFnA=
=2Vyw
-----END PGP SIGNATURE-----

<span style="color:#2aa198;">--cccccccccccc</span>
</div>
<h3 id="B" class="mail-example">
Email B: 
</h3>
alternative text/html message with embedded header, unsigned 
<pre>
└┬╴multipart/mixed 1126 bytes
 ├─╴text/rfc822-headers attachment 207 bytes
 └┬╴multipart/alternative 504 bytes
  ├─╴text/plain 86 bytes
  └─╴text/html 202 bytes</pre>
<div class="code-block"><span style="color:#dc322f;">Subject:</span> alternative text/html message with embedded header, unsigned
<span style="color:#268bd2;">Message-ID:</span> B@memoryhole.example
<span style="color:#268bd2;">Date:</span> Thu, 16 Jul 2015 11:44:44 +0200
<span style="color:#859900;">To:</span> Julia <julia@example.org>
<span style="color:#cb4b16;">From:</span> Winston <winston@example.net>
<span style="color:#268bd2;">MIME-Version:</span> 1.0
<span style="color:#268bd2;">Content-Type:</span> multipart/mixed; boundary="bbbbbbbbbbbb"

<span style="color:#2aa198;">--bbbbbbbbbbbb</span>
<span style="color:#268bd2;">MIME-Version:</span> 1.0
<span style="color:#268bd2;">Content-Type:</span> text/rfc822-headers
<span style="color:#268bd2;">Content-Disposition:</span> attachment

<span style="color:#268bd2;">Date:</span> Thu, 16 Jul 2015 11:44:44 +0200
<span style="color:#dc322f;">Subject:</span> alternative text/html message with embedded header, unsigned
<span style="color:#cb4b16;">From:</span> Winston <winston@example.net>
<span style="color:#859900;">To:</span> Julia <julia@example.org>
<span style="color:#268bd2;">Message-ID:</span> B@memoryhole.example

<span style="color:#2aa198;">--bbbbbbbbbbbb</span>
<span style="color:#268bd2;">MIME-Version:</span> 1.0
<span style="color:#268bd2;">Content-Type:</span> multipart/alternative; boundary="aaaaaaaaaaaa"

<span style="color:#2aa198;">--aaaaaaaaaaaa</span>
<span style="color:#268bd2;">MIME-Version:</span> 1.0
<span style="color:#268bd2;">Content-Type:</span> text/plain

This is a test
message on multiple lines

with a silly bit more.
-- 
and a .sig here.

<span style="color:#2aa198;">--aaaaaaaaaaaa</span>
<span style="color:#268bd2;">MIME-Version:</span> 1.0
<span style="color:#268bd2;">Content-Type:</span> text/html

<html>
<head>
<title>titles are usually unrendered</title>
</head>
<body>
<p>This is a test<br/>message on multiple lines</p>
<p>with a silly bit more.</p>
<hr/>
<p>and a .sig here.</p>
</body>
</html>

<span style="color:#2aa198;">--aaaaaaaaaaaa</span>

<span style="color:#2aa198;">--bbbbbbbbbbbb</span>
</div>
<h3 id="C" class="mail-example">
Email C: 
</h3>
alternative text/html message with embedded header, signed, with Subject tampered 
<pre>
└┬╴multipart/signed 1814 bytes
 ├┬╴multipart/mixed 940 bytes
 │├─╴text/rfc822-headers attachment 228 bytes
 │└┬╴multipart/alternative 504 bytes
 │ ├─╴text/plain 86 bytes
 │ └─╴text/html 202 bytes
 └─╴application/pgp-signature 455 bytes</pre>
<div class="code-block"><span style="color:#dc322f;">Subject:</span> the subject has been tampered!
<span style="color:#268bd2;">Message-ID:</span> C@memoryhole.example
<span style="color:#268bd2;">Date:</span> Thu, 16 Jul 2015 11:44:44 +0200
<span style="color:#859900;">To:</span> Julia <julia@example.org>
<span style="color:#cb4b16;">From:</span> Winston <winston@example.net>
<span style="color:#268bd2;">MIME-Version:</span> 1.0
<span style="color:#268bd2;">Content-Type:</span> multipart/signed; micalg="pgp-sha256";
 protocol="application/pgp-signature"; boundary="cccccccccccc"

<span style="color:#2aa198;">--cccccccccccc</span>
<span style="color:#268bd2;">MIME-Version:</span> 1.0
<span style="color:#268bd2;">Content-Type:</span> multipart/mixed; boundary="bbbbbbbbbbbb"

<span style="color:#2aa198;">--bbbbbbbbbbbb</span>
<span style="color:#268bd2;">MIME-Version:</span> 1.0
<span style="color:#268bd2;">Content-Type:</span> text/rfc822-headers
<span style="color:#268bd2;">Content-Disposition:</span> attachment

<span style="color:#268bd2;">Date:</span> Thu, 16 Jul 2015 11:44:44 +0200
<span style="color:#dc322f;">Subject:</span> alternative text/html message with embedded header, signed, with Subject tampered
<span style="color:#cb4b16;">From:</span> Winston <winston@example.net>
<span style="color:#859900;">To:</span> Julia <julia@example.org>
<span style="color:#268bd2;">Message-ID:</span> C@memoryhole.example

<span style="color:#2aa198;">--bbbbbbbbbbbb</span>
<span style="color:#268bd2;">MIME-Version:</span> 1.0
<span style="color:#268bd2;">Content-Type:</span> multipart/alternative; boundary="aaaaaaaaaaaa"

<span style="color:#2aa198;">--aaaaaaaaaaaa</span>
<span style="color:#268bd2;">MIME-Version:</span> 1.0
<span style="color:#268bd2;">Content-Type:</span> text/plain

This is a test
message on multiple lines

with a silly bit more.
-- 
and a .sig here.

<span style="color:#2aa198;">--aaaaaaaaaaaa</span>
<span style="color:#268bd2;">MIME-Version:</span> 1.0
<span style="color:#268bd2;">Content-Type:</span> text/html

<html>
<head>
<title>titles are usually unrendered</title>
</head>
<body>
<p>This is a test<br/>message on multiple lines</p>
<p>with a silly bit more.</p>
<hr/>
<p>and a .sig here.</p>
</body>
</html>

<span style="color:#2aa198;">--aaaaaaaaaaaa</span>

<span style="color:#2aa198;">--bbbbbbbbbbbb</span>

<span style="color:#2aa198;">--cccccccccccc</span>
<span style="color:#268bd2;">MIME-Version:</span> 1.0
<span style="color:#268bd2;">Content-Type:</span> application/pgp-signature

-----BEGIN PGP SIGNATURE-----

iQEcBAABCAAGBQJVt/DkAAoJEBX7TryOLWy33LEH/jPLbaxnlJhvTBt66umGjXHg
f+fi6vnG8lV4UsqJmj8RkZpNXkL3n+nCRAKAnAQwzMFep1VaFe8jLBHwQETpTHc4
L67npH3UFySpQ2IYO5K5NmHX9a9fLLiveHJTjVko/hwNm+SibW5YvBbJlk8snRjM
Isw5yWhc5bUpr7Dj/6j3xjLTKx/vaLExbHu6Q72eLqavazJG6devacRp5yurrCXB
m5mSmvSF/pIgyN/+EI2ALw4CpmTNT2vzxG9WCqPr/gLS6S8fCd+BzOULpC5lOYIN
vPqYZZbXbM2b8E1DldjOURbcDsfAImKmboz3e0ZRo1MeZNJmg1rJXsfuPM42jyo=
=mxAW
-----END PGP SIGNATURE-----

<span style="color:#2aa198;">--cccccccccccc</span>
</div>
<h3 id="D" class="mail-example">
Email D: 
</h3>
alternative text/html message with embedded header, encrypted+unsigned 
<pre>
└┬╴multipart/encrypted 1943 bytes
 ├─╴application/pgp-encrypted 10 bytes
 └─╴application/octet-stream 1475 bytes</pre>
<div class="code-block"><span style="color:#dc322f;">Subject:</span> Memory Hole Encrypted Message
<span style="color:#268bd2;">Message-ID:</span> D@memoryhole.example
<span style="color:#268bd2;">Date:</span> Thu, 16 Jul 2015 11:44:44 +0200
<span style="color:#859900;">To:</span> Julia <julia@example.org>
<span style="color:#cb4b16;">From:</span> Winston <winston@example.net>
<span style="color:#268bd2;">MIME-Version:</span> 1.0
<span style="color:#268bd2;">Content-Type:</span> multipart/encrypted; protocol="application/pgp-encrypted";
 boundary="cccccccccccc"

<span style="color:#2aa198;">--cccccccccccc</span>
<span style="color:#268bd2;">MIME-Version:</span> 1.0
<span style="color:#268bd2;">Content-Type:</span> application/pgp-encrypted

<span style="color:#268bd2;">Version:</span> 1
<span style="color:#2aa198;">--cccccccccccc</span>
<span style="color:#268bd2;">MIME-Version:</span> 1.0
<span style="color:#268bd2;">Content-Type:</span> application/octet-stream

-----BEGIN PGP MESSAGE-----

hQEMA5I+4kg3RI5lAQgApGN7idnq0tNxVeSjOVPfNF9sfW3n+brS+sHC8JWPW2x8
c7lfjkdLf4Fe4I4jff46gqgYXKxHrPn3ogyh1jAoqFfFIxm/HKoggiup3hQGsCpn
MgEsy5n6KDKeda0sCFKtdbNdqqAKHx1UDrXPRfQdNhQkQyLofPYIav1D6TxVSSkY
smCsfao7/pp2q4RkhDyjHr4WQ1mXqJezbxcgAP6bd0y/kqcPYYJl/V01AdcNLVZd
aKW2yHYGczsJvR+7LKfuQTSXigOCysHlOr3KXF/kHJBRWv/Q2IpbdTodHHOZ6awa
m9GojOqT0k1V8Wb48afvaAi/XfM8yif4DuNh0d/tS4UBDANLbJvEVDbKBwEH/jM+
QDdCagRW2skbQNMNd96nP17GoUt7niwK7Fdeljg2A0jk5VfgF5NY+1zMtUFyIg7g
tF7gg27N7zaoD64Gq7Ex5TrOq0dm1yQMEpnqw1jTbNu/EWO84uGJDz8kvmpsmlNc
lpWowHMM4BConqD0dfO8iVhyyBYuBoRjmaZirR2KR1gQJrf4h0fodtNihZ0mbQk6
FhWGjUZ3hRp+RygkVowZBkB+e1uH5mGPTa4xe1FcV3HLoFoRWWHtkYUQKHTpAR0E
Cr5H9jm7DJE5nIlqK+Qyj3woc+dw8ArFbKxHeycHmSSEC0d4s7Z18vopuNa+Yhit
58BcpNARmjrSMvDjUxXSwTIBPA8Tda9GnPn6Lzlout6IiyoCTCxE9/fV+erpA4ed
CXOeSelQqsEQq1/lAevoxgf7BDgs5XijneMeV3ND4j0Td5XVR99/gbYB2P6NB5IK
zJSVnmnlbX5qvpFn0EN2rj8AwlctQUl03OB5AKwnGZBJZ/Wdix2bSGdCAy3i1CCr
IiObBsssrvWKq0HnWYValDvW87xwYSmcLrJZLzpfyEOiOPLWHNM7MMDWeKQH25J8
91T9590zHlpVdg/MKSkKTLGiAmpbur0omYS2fTntLX13Zm8lxCRUXtkRWIClhOzZ
hECL1Jd3fPtqILK9DC3/DU8sa89EQUlBKI8kYg7/n1ZLghytWjuIizvzsbkPjSQk
EkEpovHTsOfyLITIcqhaLT8tWja7o4wi5ngsVCWSRumOi/3mthxPMVxjT1c4ronF
W6IQzlqPHFVxD6Mz/A6g5VrOXGRXvDKleXacxEXiYE0QE1C9iAH9pORKJlEOlucE
2kGA1kaNXOqz7jJ9jpHOYkgbnmnFOd/00CawTyEn8T+FyReSa3I500/kRG3k7FJA
UH71T440yWU3jTOGtH8z0SAjTdNnULTpKrsJ1KCKbX8ipnsWN5SZN90q53/tSw0i
KRO7wjc9E8HDheP20zIMo1XStDVqUfg09AK3PCO+AFWvRgE=
=1vb/
-----END PGP MESSAGE-----

<span style="color:#2aa198;">--cccccccccccc</span>
</div>
<h3 id="E" class="mail-example">
Email E: 
</h3>
alternative text/html message with embedded header, encrypted+signed 
<pre>
└┬╴multipart/encrypted 2435 bytes
 ├─╴application/pgp-encrypted 10 bytes
 └─╴application/octet-stream 1967 bytes</pre>
<div class="code-block"><span style="color:#dc322f;">Subject:</span> Memory Hole Encrypted Message
<span style="color:#268bd2;">Message-ID:</span> E@memoryhole.example
<span style="color:#268bd2;">Date:</span> Thu, 16 Jul 2015 11:44:44 +0200
<span style="color:#859900;">To:</span> Julia <julia@example.org>
<span style="color:#cb4b16;">From:</span> Winston <winston@example.net>
<span style="color:#268bd2;">MIME-Version:</span> 1.0
<span style="color:#268bd2;">Content-Type:</span> multipart/encrypted; protocol="application/pgp-encrypted";
 boundary="cccccccccccc"

<span style="color:#2aa198;">--cccccccccccc</span>
<span style="color:#268bd2;">MIME-Version:</span> 1.0
<span style="color:#268bd2;">Content-Type:</span> application/pgp-encrypted

<span style="color:#268bd2;">Version:</span> 1
<span style="color:#2aa198;">--cccccccccccc</span>
<span style="color:#268bd2;">MIME-Version:</span> 1.0
<span style="color:#268bd2;">Content-Type:</span> application/octet-stream

-----BEGIN PGP MESSAGE-----

hQEMA5I+4kg3RI5lAQf9GnSQ0RWh4GAmoKXYRKwvSU2Kg1GF8QXq/vnRaCfb1IGj
zz1vPaTy+6ti0xMvWQ0madR/NsvGdKJPxtqYWHqKm3KEWLWTP1M1lxG6YrBOLGDX
kud51MG8cToAPlhFxypbGasyyi32ZABShRZiVGAoQPAg6PpGxEmwEvMUHsoWg7wb
Z75r9BPnBfj9kCESajrvUtt/G3Y36I3wr8AtupId1cDs9OnDbu4+aevRpdMabQ0Y
61K+1OoMf/C4l5/s2zpQreCW9ZZtMnw+FBRmC5+5pY2aT4NeazOWjinPZNcEQWCi
VUy/EmEnBJGD8a44FGYJrrzVOwNLULIvrb4LnhEd3IUBDANLbJvEVDbKBwEIAIfp
0+ECchWUW69M2+8RAOoyw47tmJiBO+YXMM+Z19saTey7naGHwdQCzOOh3JL07wjd
m0dA2sMmVlGhj3Q/VoxcTlKPc2KxDEi6YEF43QM7OWjEBzhfcbomkDjbbBuezZLD
Dl7EZwWVqQLp+hK0YUqACSmVRTqPUwe+9gYvcojn6d6KFyEF6Rdm4aGzNa1M4Ga/
Uk04ohRIGxBTUkLWim8GVMB3umi0TDZ/S5aaG8BcnR0+jStPPM7yqPIDUzQDYUUz
s+LrdzSs6MT1S2E2ApKvAyz9CFdo4FF2Sz9o2jqzvxZPhuroSRb7hbftLvGV0oSS
81sGHubbiZLQojnF9cDS6QGidCDS4SFgYvO10jq120nrNAjrpfJJl2TZGJLGVpxL
lceCQs0pVUD0JGr7GQyKeUoMZZzv5ijJ0biCxbTlS71cu4PeeYCq8QfIS1aGJGdm
8IwbfMdzCZtyHhm5owUig7IR6VyXHJKhXMEYmzWZFMMsvseL9IjnWZMoyGKr3xBw
6tNXuYRhmcUZaFEb+We1LYP8k0Vrx+Yt+BFfR7zQWRolmyW6pgoUcdntgqW5wjrf
5pZNovAYGxs6PsHjC+CqDl/og1rJfD04RNUO+0vLESmkx0q7/GDcpzabE4w58yfb
Ga/9YPyaObrYQ+Al4oKTbnZhfLlu3LpECPUhxvzwStr8O3wZAT+u7FigaUZ1QyWN
2VD9ydtPhcI7sIglSI0MsHEYMJLYpMylG4uq/vpuip4S2iZaNcrEunPgdZamvvjB
/LGRv87Nv5kFM1nNeuW43M9yEuVm73TR7dPZgDydlmfK/F6YlXc51ATy3zMsECOQ
snpjFETKTE4ZJsXX2hx3D12A0QSSuiU/iBCCAdYpDXBvtvaoj8hv7h/jMguL+O/G
EG/TqBEt6J+kD4YpHl7g1TvemwRbhsa9waNE2PeDF2vRY9RScausC1EmQi6HrOm0
dBRZHblrShXm5ISoKx8qTUVr/oNdea1SSyE/43FjV7mx8q+fHIzEoKYse2NOETAi
wJsb7bcbwA3QcU9tCR71FlgPZIiiVo2tQp2qtrVCHU+eb3PPufWx33Qkt6Gmo4lR
aAV7CtTPlyVOBkaTzUH/mvvatcuoLnCS1pOMRMei8PwkTp/IJSoB09iFTrtxj8WZ
6iIs8NxSEiTgoI6QUycjz3XM4HZd3erG6YXRel3PPEDziISgsAT05XtwGD7ROk1E
6xLqD+ojeKOPUAtW5E9lxP3qbBjK1yrQ0N9fRC+6VFPIVoegVpkFCjJECPKBUkGh
TYEUFjkIiCBQ/ckJMnb7DUqNUF1BSWhfjM2cviaG2tgAePvZO8JVZzPzR8w3KZuT
sdDHAJ+4Frn5hMJ/wnWv5a7Y1+sYbiTHEdae71tj0ZFVv3vXAsyngGFodLnJfVCM
+NZQ2N+MKw7Cin57JrymlUEMT4nG4OURBFqqcHpOO6nQY3ll7JQyJLImnAai63xM
B9YJby0XSiuV8oNzAQ==
=+yhD
-----END PGP MESSAGE-----

<span style="color:#2aa198;">--cccccccccccc</span>
</div>
<h3 id="F" class="mail-example">
Email F: 
</h3>
headers in top-level MIME object: plaintext email 
<pre>
This message demonstrates including the memoryhole headers inside the
top-level MIME object. The signed Subject and From are headers of the
text/plain part, rather than having their own rfc822-headers part.

└┬╴multipart/signed 1264 bytes
 ├─╴text/plain 207 bytes
 └─╴application/pgp-signature 455 bytes</pre>
<div class="code-block"><span style="color:#dc322f;">Subject:</span> headers in top-level MIME object: plaintext email
<span style="color:#268bd2;">Message-ID:</span> F@memoryhole.example
<span style="color:#268bd2;">Date:</span> Wed, 29 Jul 2015 09:31:44 +0100
<span style="color:#859900;">To:</span> Julia <julia@example.org>
<span style="color:#cb4b16;">From:</span> Winston <winston@example.net>
<span style="color:#268bd2;">MIME-Version:</span> 1.0
<span style="color:#268bd2;">Content-Type:</span> multipart/signed; micalg="pgp-sha256";
 protocol="application/pgp-signature"; boundary="bbbbbbbbbbbb"

<span style="color:#2aa198;">--bbbbbbbbbbbb</span>
<span style="color:#268bd2;">MIME-Version:</span> 1.0
<span style="color:#268bd2;">Content-Type:</span> text/plain; boundary="aaaaaaaaaaaa"
<span style="color:#dc322f;">Subject:</span> headers in top-level MIME object: plaintext email
<span style="color:#cb4b16;">From:</span> Winston <winston@example.net>

This message demonstrates including the memoryhole headers inside the
top-level MIME object. The signed Subject and From are headers of the
text/plain part, rather than having their own rfc822-headers part.

<span style="color:#2aa198;">--bbbbbbbbbbbb</span>
<span style="color:#268bd2;">MIME-Version:</span> 1.0
<span style="color:#268bd2;">Content-Type:</span> application/pgp-signature

-----BEGIN PGP SIGNATURE-----

iQEcBAABCAAGBQJVuJwYAAoJEBX7TryOLWy3ogEH/0UVXKyW1bjRnvf7aEewl6m0
SGrJhEy9jhHlOXNZ05XFrGUgjd0vox2oOgR2Wd0cUqxFSGE9JEP9QuI+WsfzBRv0
3nY2ytQN8HbZifGlDXlzFTpnrf7ORVNytVZD7TibIrp9vUon7s9bt4iRifpUCxUD
ZYpZpPap8FvDnJ48KbiS1FTmHxm//aJIVBzi2Wh14GdeIGog6O44q3/Y2QzjIf2L
icdtwDaFA7lQtGfbnl53TNpWFFq9cwNkLIAmR3UhVhWUndcz9FZOIZzvkz7KRxL7
BJY/tcsrl9c762V6KlDVYw9PP9jS1yPxDPff8kLG+Kg8eD8lDcbWty8XizN+NYI=
=SeGc
-----END PGP SIGNATURE-----

<span style="color:#2aa198;">--bbbbbbbbbbbb</span>
</div>
<h3 id="G" class="mail-example">
Email G: 
</h3>
headers in top-level MIME object: signed multipart email 
<pre>
This message demonstrates including the memoryhole headers inside the
top-level MIME object. The signed Subject and From are headers of the
multipart/alternative part, rather than having their own
rfc822-headers part.

└┬╴multipart/signed 1638 bytes
 ├┬╴multipart/alternative 738 bytes
 │├─╴text/plain 218 bytes
 │└─╴text/html 202 bytes
 └─╴application/pgp-signature 455 bytes</pre>
<div class="code-block"><span style="color:#dc322f;">Subject:</span> headers in top-level MIME object: signed multipart email
<span style="color:#268bd2;">Message-ID:</span> G@memoryhole.example
<span style="color:#268bd2;">Date:</span> Wed, 29 Jul 2015 09:31:44 +0100
<span style="color:#859900;">To:</span> Julia <julia@example.org>
<span style="color:#cb4b16;">From:</span> Winston <winston@example.net>
<span style="color:#268bd2;">MIME-Version:</span> 1.0
<span style="color:#268bd2;">Content-Type:</span> multipart/signed; micalg="pgp-sha256";
 protocol="application/pgp-signature"; boundary="bbbbbbbbbbbb"

<span style="color:#2aa198;">--bbbbbbbbbbbb</span>
<span style="color:#268bd2;">MIME-Version:</span> 1.0
<span style="color:#268bd2;">Content-Type:</span> multipart/alternative; boundary="aaaaaaaaaaaa"
<span style="color:#dc322f;">Subject:</span> headers in top-level MIME object: signed multipart email
<span style="color:#cb4b16;">From:</span> Winston <winston@example.net>

<span style="color:#2aa198;">--aaaaaaaaaaaa</span>
<span style="color:#268bd2;">MIME-Version:</span> 1.0
<span style="color:#268bd2;">Content-Type:</span> text/plain

This message demonstrates including the memoryhole headers inside the
top-level MIME object. The signed Subject and From are headers of the
multipart/alternative part, rather than having their own
rfc822-headers part.

<span style="color:#2aa198;">--aaaaaaaaaaaa</span>
<span style="color:#268bd2;">MIME-Version:</span> 1.0
<span style="color:#268bd2;">Content-Type:</span> text/html

<html>
<head>
<title>titles are usually unrendered</title>
</head>
<body>
<p>This is a test<br/>message on multiple lines</p>
<p>with a silly bit more.</p>
<hr/>
<p>and a .sig here.</p>
</body>
</html>

<span style="color:#2aa198;">--aaaaaaaaaaaa</span>

<span style="color:#2aa198;">--bbbbbbbbbbbb</span>
<span style="color:#268bd2;">MIME-Version:</span> 1.0
<span style="color:#268bd2;">Content-Type:</span> application/pgp-signature

-----BEGIN PGP SIGNATURE-----

iQEcBAABCAAGBQJVuKHQAAoJEBX7TryOLWy3u4EH/i/X51ydnUNU2TWZyVkQCXoq
nF/TO2X7fwyvnaH0+Hxd67sswErwH8oijTGJ7RaGeV8rfCQbk7tZsoWi4SxAfxV+
Kprt2GImqtbm1MHlR0bbHLm9fXB/Sm0LZMSqOxsm4SsKcBGGljBUmubydhUBL6ei
/nDGB1adhg8HYsSgvhbqIsi6ElQkp75GdIoG3FvQgTVEuD8mZSMs5LDpuV/br0wc
bc133d9SCYfxCxnx7MkzScr0zTh9ReKgGvTirlJWXKbbUjwsePkVfLfAnyVRoy7w
qPfDnnF196urRcKnJbqMPEklzDx4wMf1jCqyriXEjuFHCEHEI2GWJm/7wUQfjKk=
=/k9W
-----END PGP SIGNATURE-----

<span style="color:#2aa198;">--bbbbbbbbbbbb</span>
</div>
<h3 id="H" class="mail-example">
Email H: 
</h3>
headers in top-level MIME: tampered subject and from 
<pre>
This email demonstrates including the memoryhole headers inside the
top-level MIME object. The signed Subject and From are headers of the
text/plain part, rather than having their own rfc822-headers part.

This email has been tampered with. It was originally sent by Winston,
who signed the body (including the memoryhole headers). Eve has
fiddled with the From and Subject headers in-flight.

└┬╴multipart/signed 1452 bytes
 ├─╴text/plain 393 bytes
 └─╴application/pgp-signature 455 bytes</pre>
<div class="code-block"><span style="color:#dc322f;">Subject:</span> headers in top-level MIME: tampered subject and from
<span style="color:#268bd2;">Message-ID:</span> H@memoryhole.example
<span style="color:#268bd2;">Date:</span> Wed, 29 Jul 2015 09:31:44 +0100
<span style="color:#859900;">To:</span> Julia <julia@example.org>
<span style="color:#cb4b16;">From:</span> Eve <eve@evilcorp.com>
<span style="color:#268bd2;">MIME-Version:</span> 1.0
<span style="color:#268bd2;">Content-Type:</span> multipart/signed; micalg="pgp-sha256";
 protocol="application/pgp-signature"; boundary="bbbbbbbbbbbb"

<span style="color:#2aa198;">--bbbbbbbbbbbb</span>
<span style="color:#268bd2;">MIME-Version:</span> 1.0
<span style="color:#268bd2;">Content-Type:</span> text/plain; boundary="aaaaaaaaaaaa"
<span style="color:#dc322f;">Subject:</span> headers in top-level MIME: subject restored to original
<span style="color:#cb4b16;">From:</span> Winston <winston@example.net>

This email demonstrates including the memoryhole headers inside the
top-level MIME object. The signed Subject and From are headers of the
text/plain part, rather than having their own rfc822-headers part.

This email has been tampered with. It was originally sent by Winston,
who signed the body (including the memoryhole headers). Eve has
fiddled with the From and Subject headers in-flight.

<span style="color:#2aa198;">--bbbbbbbbbbbb</span>
<span style="color:#268bd2;">MIME-Version:</span> 1.0
<span style="color:#268bd2;">Content-Type:</span> application/pgp-signature

-----BEGIN PGP SIGNATURE-----

iQEcBAABCAAGBQJVuKVJAAoJEBX7TryOLWy3GIUH+gLqXAdsPb7UcfLe5eZ/o5pn
ZiM7dZgaIOD+vXOK6VGMdY10onzleOlyzuYv8nY0pcz3awrHIuz29DsSiVDFtJF8
nNvjIkyLiAfGckdTRJWVDAYiEJ51dyl8EuhRajpCfr+h2to3a6nHdhkX5t+5C0aU
JJGbnSamet2FfDAApE6cAHRUvApcF85/b7X46x+jSgZourNHerlcHUtsXUZP0IC+
FQBFmCsGdW6w3j4q9PjvXzV0+PHrLzqTtf99KVxOkO7jEWGH7us1D+9Kf25Hza5o
EwJn9uAWnCH28nuDSXqcY6oiAWNmYCqyw47uYjTe+LaD3HsyYIzs6iZTbynJ4nA=
=Lpdg
-----END PGP SIGNATURE-----

<span style="color:#2aa198;">--bbbbbbbbbbbb</span>
</div>