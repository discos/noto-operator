.. _descr:


Descrizione Sistema di controllo 
================================

NURAGHE è il sistema di controllo di SRT ed è distribuito su  4 server:

#. nuraghe-mng.srt.inaf.it
#. nuraghe-obs1.srt.inaf.it
#. nuraghe-as.srt.inaf.it
#. nuraghe-lo.srt.inaf.it

nuraghe-mng e nuraghe-obs1 sono accessibili mendiante le rispettive postazioni utente, mentre nuraghe-as e nuraghe-lo sono accessibili 
unicamente tramite ssh. Per tutti i server lo username di riferimento e' ``gavino``
 
NURAGHE ha accesso tramite tcp/ip  ad altre risorse:

- ACU (antenna control unit), che si occupa del controllo dei servo sistemi maggiori (assi di elevazione e azimuth e *cable wrap*)
- MSCU (minor servo control unit) 
- Backends (Total Power, XARCOS, DBBC, SARDARA, DFB)
- Terminali VLBI (DBBC + Mark V)
- schede di controllo dei ricevitori
- Centralina meteo


Postazioni utente
-----------------

Gli SD hanno accesso alle seguenti postazioni utente:

- nuraghe-obs1
- nuraghe-mng
- nuraghe-obs3
- ACU-PCP
- ACU-LCP

Le  prime 4 sono collocate in control room, la quinta nella stanza ALER in antenna. 

nuraghe-obs1
~~~~~~~~~~~~

E' la console operativa di nuraghe, contiene i client testuali dei sotto sistemi di nuraghe e la shell di operator input.
Inoltre ospita la console vlbi

nuraghe-mng
~~~~~~~~~~~

La postazione utente 

- Ospita il manager, ovvero tutti i tool che permettono l'avvio e la gestione dei servizi ACS sui quale si basa NURAGHE
- Consente l'accesso tramite ssh a ``nuraghe-lo`` e ``nuraghe-as``
- Consente l'esecuzione dei tool di diagnostica utili per seguire il corretto svolgimento delle osservazioni

nuraghe-obs3
~~~~~~~~~~~~

Attualmente questo server ha solamente l'utente observer (pw solita) e
viene utilizzato per accedere a nuraghe-obs2 come utente scicom via vnc.

ACU-LCP
~~~~~~~

Local Control Panel.
Situato il ALER, è il pannello di controllo della Antenna Control Unit (ACU), per controllare il comportamento dei servo sistemi principali,
ovvero gli assi di azimuth ed elevazione ed il cable wrap. Eventualmente permette di effettualre la movimentazione se l'ACU è
impostata per il controllo :ref:`locale <antenna>`

ACU-PCP
~~~~~~~

Primary Control Panel, è la replica del ACU_LCP in Control Room. 

Se la modalità di controllo dell'ACU è  impostata su :ref:`remoto <antenna>` 
il pannello è unicamente informativo e pertanto i pulsanti non sortiscono nessuna azione e non aprono finestre informative.
