.. _backends:


********
Backends
********

 
--------------------------------------------
Total Power
--------------------------------------------

.. index:: single: Total Power


Il backend ``Total Power`` è raggiungibile all'ip 192.168.200.129

Per verificare se tale backend è acceso, da una shell di ``nuraghe-mng`` effettuare ping al suo indirizzo ip::

   $> ping 192.168.200.129

++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
Riavvio
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. index:: pair: Total Power; riavvio
 
Se è necessario riavviare il backend, occorre effetuare login con username root. Da ``nuraghe-mng``::

   $> ssh root@192.168.200.129

Inserita l'apposita password si ha accesso alla shell del pc di controllo del TotalPower. Per il riavvio, eseguire il comando::

   #> reboot

+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
Spegnimento del Total Power
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. index:: pair: Total Power; Shutdown


Il sistema operativo del backend TotalPower è installato su una scheda SD, pertanto eventuali spegnimenti dell'alimentazione del backend
senza una procedura di shutdown del sistema operativo possono essere dannosi. 

Innanzitutto è necessario disconnettere il backend dal sistema di controllo del telescopio. Pertanto è necessario:


- chiudere la console di Nuraghe
- chiudere i seguenti container:

    - TotalPowerContainer
    - FitsZillaContainer


Poi, è necessario accedere al backend  con username root. Da ``nuraghe-mng``::



   $> ssh root@192.168.200.129
  

Infine è necessario eseguire il comando:: 

   #> poweroff


Attendere circa 60 secondi prima di togliere l'alimentazione al backend.


++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
Sincronizzazione Clock
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
.. index:: pair: Total Power; Sincronizzazione Orologi


Non è necessario sincronizzare il *clock* della CPU del Total Power. Tale sincronizzazione avviene all'avvio. 


++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
Controllo del backend senza ausilio di NURAGHE
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
.. index:: pair: Total Power; Sincronizzazione Orologi

Prima di operare sul backend  è necessario chiudere ogni connessione con il backend: 

- chiudere la console di Nuraghe
- chiudere i seguenti container:

  - TotalPowerContainer
  - FitsZillaContainer

------------------------------------------------------------------
DBBC
------------------------------------------------------------------

.. index:: single: DBBC


+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
Setup modalità ''spettrometro''
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

Si accede al **DBBC** mediante remote desktop da **nuraghe-obs**.
 
Se la finestra del remote desktop non è aperta, occore andare nel workspace  **VLBI** di **nuraghe-obs1** 
e cliccare sull'icona **DBBC** sul Desktop.

Una volta dentro occorre chiudere la shell C:\\DBBC\\bin\\DBBC2ControlDDC
v105_1.exe. A questo punto bisogna aprire la cartella Spectrometer e
lanciare i seguenti eseguibili:

* Server_CM.exe
* Server_FPGA_Impact.exe

Ci vogliono circa due minuti per configurare le FPGA. 

Con un setup corretto, il remote desktop apparirà come nella figura sottostante, con 
*spectrometer* presente nel titolo delle due shell.


.. figure:: images/dbbc_spectrometer.png
    :width: 50%
    :align: center
    :alt: dbbc

.. warning:: le due shell "Server_CM.exe" e "Server_FPGA_Impact.exe" devono rimanere
     aperte. Non chiuderle. 


Il sistema permette pertanto la commutazione del percorso della IF per i backend basati
su ROACH (ROACH-1 e SARDARA). L'utente dovrà selezionare dalla console **nuraghe-obs1**, il percorso
adatto al ricevitore in uso. I comandi, da shell, sono:

* setupIFPathPCK  (ricevitori P, C, e K)
* setupIFPathL    (ricevitore L)

Si aprirà un plot che consente di visualizzare la banda IF che arriva al DBBC.


