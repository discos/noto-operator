.. _stow:

Parcheggio e messa in sicurezza dell'antenna (STOW)
***************************************************

Per parcheggiare in sicurezza l'antenna eseguire la prima di queste procedure. 
Nel caso in cui non funzionasse, passare alla successiva:

#.  :ref:`Stow mediante ESCS <stowescs>`
#.  :ref:`Stow mediante Local Control Panel <stowlcp>`


.. _stowescs:

STOW mediante ESCS
---------------------

Da ``operator input`` su **escs** eseguire i comandi::

   >goTo=*,90d
   >servoPark
   >asPark


.. _stowlcp:

STOW mediante il Local Control Panel dell'ACU
---------------------------------------------------

Se la procedura di STOW mediante NURAGHE non ha dato buon esito occorre:

- verificare tramite ACU se ci sono condizioni di errori;
- verificare se sono ci sono emergency stop attivi

In caso di errori o emergency stop attivi è necessario analizzare il problema 
e valutare come procedere. 
