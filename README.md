# DNS
Dieses Git enthält die Zonendatei für [ffslfl.community](https://ffslfl.community).<br>
Sowie zusätzliche Reverseeinträge für IPs welche über keinen Hostnamen aufgelöst werden oder werden sollen, aber dennoch einen Namen bei Reverseauflösung anzeigen sollen (z.B. `traceroute`).

## empfohlenes Schema
Es ist zu empfehlen auf Redundanz im Namen zu verzichten (z.B. `ffslfl` im Hostnamen).

Es bietet sich an für die einzelnen Hoods oder auch zusammenhängende Abdeckungsbereiche eigene Subdomains zu nutzen, an denen der Ort oder die Ortschaft erkennbar ist (z.B. Würzburg -> `wue`). Diese Subdomain kann dann auch mit weiteren Subdomains genauer beschreiben werden und es macht eine Umstellung einfacher, sollte man sich entscheiden diese Subdomain später selbst zu hosten (siehe [DNS](https://wiki.freifunk-franken.de/w/DNS#eigener_rekursiver_Resolver_als_authorativer_DNS)).

Für Gateways kann anhand der Nutzung unterschieden werden. Handelt es sich beispielsweise um ein Gateway der l3-firmware und dieses bedient nur eine Hood oder dient das Gateway hauptsächlich für eine Hood so ist empfehlenswert dieses mit `gw<Nummer>.<Hood>` zu bezeichnen und hier alle IP-Adressen anzugeben.<br>
Handelt es sich eher um ein Gateway welches gleichberechtigt mehrere Hoods bedient kann man es zusätzlich mit seinem Eigennamen in die Subdomain `gw` aufnehmen (z.B. `aquarius.gw`). Es ist zu empfehlen dennoch die jeweiligen `gw<Nummer>.<Hood>` Einträge mit den Hood-eigenen Adressen aus dem privaten IP-Bereich zu setzen, dann funktioniert auch die Reverseauflösung.

## Zone extern
siehe [Wiki](https://wiki.freifunk-franken.de/w/DNS#Zone_extern)

