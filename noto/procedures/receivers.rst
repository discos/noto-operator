**********
Ricevitori
**********

Controllo Temperatura criogenica
================================
Per controllare la temperatura criogenica degli LNA, da una shell di
``nuraghe-obs1`` si dia il comando::

    > tail -f ~/logs/receivers/receivers.log

Verranno visualizzate le temperature. Per chiudere ``tail``, si digiti la
combinazione di caratteri ``CTRL-C`` da tastiera.

L'aggiornamento delle temperature avviene ogni 2 minuti, pertanto nel caso in
siano trascorsi più di due minuti dall'ultimo aggiornamento, è possibile che
nuraghe non sia avviato, o che lo script non sia in esecuzione. In questo
ultimo caso, si riavvi lo script aprendo un terminale su ``nuraghe-obs1``, e
dando il comando::

   > receiversmonitor.py &

E' possibile che venga mostrato il seguente messaggio::

    > receiversmonitor.py
    receiversmonitor.py already running, everything is OK

Significa semplicemente che lo script era già in esecuzione, e tutto sta
andando come dovrebbe.

Per chiudere la shell in cui è stato avviato ``receiversmonitor.py``, si digiti
la combinazione di tasti ``CTRL-D``, oppure si dia il comando ``exit`` nel
terminale. **NON chiudere la shell cliccando sulla 'x'** in alto a destra,
altrimenti ``receiversmonitor.py`` terminerà la sua esecuzione.

