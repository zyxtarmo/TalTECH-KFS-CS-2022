### Ex1.pcap

Selle faili avame Wiresharkiga:

- esmalt vaatame mis paketid meil seal on
- tuletame meelde neid erinevaid "kihte" mida loengus mainiti
- töövahendiga tuttavaks saamiseks teeme harjutuse mille käigus me võtame välja kõik failid mis veebilehitseja kasutamise käigus võrgu vahendusel liikusid, selleks vali - File -> Export Objects -> HTTP ja vajuta Save all. Loo uus kataloog, terminaliaknas mine sinna kataloogi ja leia kõik failid mille tüübiks "PE32 executable (GUI) Intel 80386, for MS Windows", vt ka linke sissejuhatavalt praktikumi loengult , vihjeid leiab ka: https://www.geeksforgeeks.org/grep-command-in-unixlinux https://www.geeksforgeeks.org/file-command-in-linux-with-examples
- arvuta leitud failide räsi (vt shasum, sha256sum) ja kontrolli töövahendi virustotal.com otsingut kasutades faili "pahadust"


Mis peaks tegema edasi? Ilmselt aru saama kelle arvuti nakatus, mis kaudu / kuidas nakatus, mis edasi juhtus ... aga see jäägu meile lahti harutamiseks järgmistel kordadel :)


Selle praktikumi kodune töö on lisatud, võid kasutada nii kooli kui koduarvutit neile vastamiseks.



Kuidas saada shasum windowsi all käivituvate failide kohta kätte "ühe reaga":

	for i in $( file * | grep -i exe | awk -F':' '{print $1}' ) ; do sha256sum $i ; done


