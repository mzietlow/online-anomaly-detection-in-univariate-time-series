# Transferleistung-LaTeX
Dieses Markdown-File ist Schmu. Ich werde, irgendwann, versuchen es nach LaTeX
zu migrieren - und vor allem zu vervollständigen.


Typesetting ist eine Sache für sich. Studenten dazu zu zwingen, das Rad stets
neu zu erfinden, ist eine schlechte Idee. Der folgende Guide richtet sich,
entsprechend, an Studenten, die bisher noch keine Erfahrungen auf diesem Gebiet
angesammelt haben. Einen sehr viel Umfassenderen Ansatz verfolgt TheMegaTB unter
https://github.com/TexNAK/Science-Paper-Template. Dieser Guide entspringt
persönlicher Erfahrung, den Arbeiten meines Bruders sowie den Arbeiten von
FWellers (https://gitlab.com/fwellers/texfornak) und OleKoring
(https://gitlab2.nordakademie.de/OleKoring-I16/LaTeX-Transferleistung/)
Ziel ist es letztlich, Minimalbeispiele für die häufigsten Problemstellungen
bieten zu können und diese übersichtlich aufzubereiten.


Softwarestack: VSCode, TeX Live, LuaLaTeX
Entwicklungsumgebung

### Aussprache: LaTeX: Latech < - 'frech'.

### LaTeX & Entwicklungsumgebung

Das Anfang der 80.-Jahre von Leslie Lamport entwickelte LaTeX (Lamport Tex) ist
eine Erweiterung des ursprünglichen Textsatzsystems TeX. Für LaTeX selbst
existieren ebenfalls zahllose Zusatzprogramme, die von unterschiedlichen Gruppen
zu Distributionen zusammengefasst wurden. Deren bekannteste MikTeX und TeX Live.
Weiterführend hierzu: https://www.schlosser.info/miktex-vs-texlive/ Im Folgenden
soll die Installation von TeX Live unter Win10 durchexerziert werden.

Weitere Informationen über https://www.latexbuch.de/latex-windows-installieren/

### TeX Live Installation

Es ist unbedingt auf eine Stabile Internetverbindung zu achten, da der Setup
bei einem Disconnect komplett abbricht.
http://www.tug.org/texlive/ -> download -> install-tl-windows.exe
oder direkt: http://mirror.ctan.org/systems/texlive/tlnet/install-tl-windows.exe
Optional auch als zip verfügbar, das Archiv entpacken und install-tl-windows.bat
ausführen.

Standard-Papierformat: A4
TeXworks wird in dieser Einleitung nicht benötigt, als Editor wird VSCode genutzt.

Da Tex Live ursprünglich per CD vertrieben wurde (und auch weiterhin wird),
fehlen der Distribution einige grundsätzlich kostenlose Fonts (Schriftarten).
Diese werden im nächsten Schritt nachgeladen.
1. Hierzu install-getnonfreefonts
(http://tug.org/fonts/getnonfreefonts/) herunterladen.
2. Kommandozeile öffnen (win+r: cmd oder win+x->Kommandozeile/Command Prompt)
3. cd '<download-pfad>'
4. texlua install-getnonfreefonts
   getnonfreefonts --sys --all (falls keine Admin-Rechte, statt --sys:--user)
5.

### VSCode Installation und Setup

Da mich hässliche Editoren deprimieren (bin da oberflächlich), nutze ich VSCode.
Als ich mich das erste Mal mit LaTeX Editoren auseinandergesetzt hatte, bin ich
bei Atom gelandet. 2018 war das eine schlechte Wahl, wie es heute ist, kann
ich nicht beurteilen. Mit VSCode bin ich allerdings sehr glücklich.

### Das einbinden von Grafiken, Installation von Ghostscript
https://www.latexbuch.de/latex-windows-installieren/#x1-70002 (Postscript)

### Hinweise zu Schriftarten

Mit \usepackage{fontspec} können die auf dem PC verwendeten Schriftarten
verwendet werden. \setmainfont{Arial} wählt dann Arial als Schriftart aus. So
kann auch Times New Roman ausgewählt werden.

Alternativ kann auch \usepackage{lmodern} genutzt werden. Damit werden
Schriftarten genutzt, die eigentlich wie Arial und Times New Roman aussehen.
Standardmäßig ist eine Schrift mit Serifen ausgewählt.
\renewcommand*\familydefault{\sfdefault} setzt dann eine serifenlose Schriftart.

### Hinweise zum Zitieren

\usepackage[backend=biber, style=apa, citestyle=authoryear-ibid]{biblatex}
Die Option style setzt den Stil des Literaturverzeichnisses, citestlye setzt den
Stil bei Zitaten.

Zitiert werden kann dann zum Beispiel mit \cite{bibid} oder mit
\footcite{bibid}. Wenn noch ein Vgl. davor und eine Seitenangabe dahinter soll
geht das mit \cite[Vgl.][150]{bibid}.

Dokumentation Biblatex:
https://mirror.hmc.edu/ctan/info/translations/biblatex/de/biblatex-de-Benutzerhandbuch.pdf

### Hinweise für Tabellen
Todo

### Absätze

Mit \par können Absätze eingefügt werden.
