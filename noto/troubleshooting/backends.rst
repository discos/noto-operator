====================================
Backends
====================================

.. index:: pair: Backends; Crash container 


Crash del TotalPower Container
===============================

In caso di crash del TotalPower container, è necessario riavviare anche i FitsZillaContainer e ManagementContainer
Pertanto per ripristinare l'operatività è necessario:

 #. Prendere nota dei messaggi di errore da ``jlog``
 #. Chiudere ogni console (nuragheConsole -stop su nuraghe-obs1 o nuraghe-mng a seconda del server sul quale è aperta)
 #. Chiudere  ``FitsZillaContainer``
 #. Chiudere  ``ManagementContainer``
 #. Riavviare  ``FitsZillaContainer``
 #. Riavviare  ``ManagementContainer``
 #. Riavviare ``TotalPowerContainer``
 #. Riavviare la console

Problemi con backend XARCOS. 
===============================

Se durante le osservazioni jlog mostra errori connessi con il backend, verificare che il container XContainer sia vivo.

In caso di crash del container XContainer, è necessario riavviare anche i FitsZillaContainer e ManagementContainer
Pertanto per ripristinare l'operatività è necessario:  

#. Prendere nota dei messaggi di errore da ''jlog''
#. Chiudere ogni console (nuragheConsole -stop su nuraghe-obs1 o nuraghe-mng a seconda del server sul quale è aperta)
#. Chiudere  ``ManagementContainer``
#. Chiudere  ``FitsZillaContainer``
#. Attendere che il numero dei container attivi sia diminuito di 3 container. 
#. Riavviare  ``FitsZillaContainer``
#. Riavviare  ``ManagementContainer``
#. Riavviare ``XContainer``
#. Riavviare la console


