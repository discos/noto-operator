*************************************
Azioni propedeutiche all'osservazione
*************************************
Prima che inizi l'osservazione, il SD *deve sempre*:

-  :ref:`nuraghe-is-ready`, altrimenti :ref:`lo si avvii <nuraghe>`
- verificare che non siano attivi emergency stop.

Se sono attivi emergency stop:

- verificare qual è la natura dell'emergency e perché è stato premuto il pulsante
- se l'emergenza si è risolta:

  - rilasciare l'emergecy stop
  - riconoscere che  la condizione di emergenza è stata superata tramite:

    - il comando **antennaReset** se l'ACU è in modalità `remote <antenna>`
    - il pulsante **Interlock Acknowledge**, nel pannello ECP in :ref:`ALER <antenna>` 
      se l'ACU è in modalità :ref:`locale <antenna>`


All'inizio di una sessione osservativa è necessario verificare qual è la tipologia di osservazione
prevista: *VLBI* o *Single Dish*.

In caso di osservazione *VLBI*, si rimanda alla documentazione relativa e non presente in questo manuale.
Per le osservazioni *single dish* occorre verificare che il DBBC sia in modalità spettrometro. 

Per la configurazione si rimanda alla apposita sezione dei :ref:`backends <backends>` .




.. important:: Il SoD non deve partire dall'assunzione che il sistema 
   sia funzionante nemmeno nel caso in cui il SoD che ha appena terminato il 
   turno gli garantisca che tutto è OK.
   Quindi **prima che inizi l'osservazione** deve sempre seguire scrupolosamente
   la procedura appena descritta, accertandosi che tutti gli step diano 
   esito positivo.

.. toctree::
   :maxdepth: 2

   is_ready.rst
  
