# Log4j

## Upplýsingar

Þann 9. desember var opinberaður alvarlegur veikleiki ([CVE-2021-44228](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-44228)) í hugbúnaðarpakka sem kallast Apache Log4j. Þessi hugbúnaður er notaður sem hjálpartól í mörgum þekktum og útbreiddum hugbúnaði. Um er að ræða Java hugbúnað sem finnst á fjölmörgum stöðum á internetinu og innan fyrirtækja.

Hlutverk Log4j sem hjálpartól er að halda utan um og skrá upplýsingar sem geta meðal annars verið upplýsingar sem notendur kerfa t.d. vefkerfa láta frá sér, en getur einnig verið upplýsingar sem geta komið í gegnum tölvupóst eða aðrar leiðir svo lengi sem Log4j er að taka við upplýsingunum.

Gott dæmi gæti verið vefur sem keyrir WordPress en notar Apache Solr til að vinna úr (e. index) og bjóða upp á leitarvél. Þegar notandi slær inn texta í leitarstreng og ef leitarstrengurinn er skráður í gegnum Log4j í log skrá til geymslu þá getur utanaðkomandi aðili slegið inn sérstaka strengi sem Log4j keyrir (e. executes).

Í þeim tilfellum getur utanaðkomandi aðili verið kominn með aðgang að tölvunni eða kerfinu sem um ræðir. Ef utanaðkomandi aðili nær aðgengi að tölvunni eða kerfinu þá getur hann lesið eða hlerað upplýsingar sem geta verið viðkvæmar og mögulega stjórnað tölvunni.

Í flestum tilfellum sem þetta hjálpartól er notað er verið að notast við hugbúnað frá þekktum hugbúnaðarframleiðendum og í þeim tilfellum þurfa þeir að gefa út uppfærslu. Það getur tekið tíma og því getur verið nauðsynlegt að grípa til tímabundinna aðgerða.

## Aðgerðir

### Forgangur 1

* Meta hvort að fyrirtækið þitt sé með kerfi opin fyrir allt internetið. Dæmi geta verið VPN þjónustur, vefkerfi eða myndavélakerfi.
* Er um að ræða Java hugbúnað? Erfitt getur verið að sjá hvort um er að ræða Java hugbúnað, best er að leita að upplýsingum frá framleiðenda.
* Ef ekki er hægt að uppfæra og ganga úr skugga að uppfærslan leysi vandamálið, meta þá hvort hægt sé að takmarka aðgengi strax t.d. loka alveg frá interneti eða opna fyrir takmarkað IP tölu mengi (IP range).
* Möguleiki er að færa vefþjónustuna á bakvið kerfi sem hreinsar mögulega árásir.
* Ekki gleyma innri java kerfum sem mögulega eru að taka við upplýsingum frá aðilum á internetinu og vinna úr (e. process).

### Forgangur 2

* Meta allan innri hugbúnað sem er að nota Java.
* Útbúa uppfærslu eða aðgerðaráætlun til að taka á vandamálinu.
* Fylgjast með tilkynningum frá hugbúnaðarframleiðendum.
* Fylgjast vel með fréttum og tilkynningum um vandamálið.

## Greinar

### Nánari upplýsingar:

* [CVE-2021-44228](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-44228)
* [Fjarskiptastofa – Netöryggssveitin CERT-IS hefur virkjað samhæfingarferli vegna alvarlegs veikleika í algengum hugbúnaði](https://www.fjarskiptastofa.is/fjarskiptastofa/tolfraedi-og-gagnasafn/frettasafn/frett/fr%C3%A9ttir/netoryggssveitin-cert-is-hefur-virkjad-samhaefingarstod-vegna-alvarlegs-veikleika-i-algengum-hugbunadi)

### Ráðleggingar eða yfirlýsingar frá birgjum:

* [Microsoft](https://msrc-blog.microsoft.com/2021/12/11/microsofts-response-to-cve-2021-44228-apache-log4j2/)
* [Nutanix](https://download.nutanix.com/alerts/Security\\\_Advisory\\\_0023.pdf)
* [F5](https://support.f5.com/csp/article/K19026212)
* [Fortinet](https://www.fortiguard.com/psirt/FG-IR-21-245)
* [HPe](https://support.hpe.com/hpesc/public/docDisplay?docLocale=en\\\_US\\&docId=a00120086en\\\_us)
* [Dell](https://www.dell.com/support/kbdoc/en-is/000194372/dsn-2021-007-dell-response-to-apache-log4j-remote-code-execution-vulnerability)
* [Cisco](https://tools.cisco.com/security/center/content/CiscoSecurityAdvisory/cisco-sa-apache-log4j-qRuKNEbd)
* [Red Hat](https://access.redhat.com/security/vulnerabilities/RHSB-2021-009)
* [VMWare](https://www.vmware.com/security/advisories/VMSA-2021-0028.html)
* [Unifi](https://community.ui.com/releases/UniFi-Network-Application-6-5-54/d717f241-48bb-4979-8b10-99db36ddabe1)
* [VEEAM](https://forums.veeam.com/veeam-backup-for-azure-f59/log4j-cve-2021-44228-vulnerability-t78225.html#p438231)
* [Atlassian](https://confluence.atlassian.com/kb/faq-for-cve-2021-44228-1103069406.html)
* [CloudFlare](https://blog.cloudflare.com/cve-2021-44228-log4j-rce-0-day-mitigation/)
