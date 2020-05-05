Kest Lokaverkefni.


Það er ekki mikið sem hægt er að sega hér. Ég eyddi ekki miklum tíma í þetta verkefni. Í rauninni ætlaði ég ekki einu sinni að skila því þar sem að ég hafði eitt heilli viku í að gera VESM verkefnið og þegar ég ætlaði loksinns að vinda mér í KEST þá var nánast enginn tími.
En svo kom hann Einar til bjargar á síðasta klukkutímanum og fór með mér yfir allt saman og hjálpaði mér að klára.

Hann hjálpaði mér að skilja alltasaman bæði packet tracer og kóðan. Ég er honum afar þakklátur.

Hér er kóðinn.

$Notendur = Import-Csv -Path C:\notendur.csv

foreach ($Notandi in $Notendur) {

New-LocalUser -Name $Notandi.notendanafn -Fullname $Notandi.nafn -NoPassword

Add-LocalGroupMember -Group $Notandi.hopur -Member $Notandi.notendanafn

Add-LocalGroupMember -Group "Allir" -Member $Notandi.notendanafn

Add-LocalGroupMember -Group "Users" -Member $Notandi.notendanafn }
