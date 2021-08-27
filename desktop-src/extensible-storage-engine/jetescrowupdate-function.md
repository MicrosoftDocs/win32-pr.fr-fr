---
description: 'En savoir plus sur : fonction JetEscrowUpdate'
title: Fonction JetEscrowUpdate
TOCTitle: JetEscrowUpdate Function
ms:assetid: e509b6c9-a8ce-4898-a426-485e286869fa
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294125(v=EXCHG.10)
ms:contentKeyID: 32765739
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEscrowUpdate
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e9f037b8c26829d7b1f3a10b05e1d4bd83bd186a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469796"
---
# <a name="jetescrowupdate-function"></a>Fonction JetEscrowUpdate


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetescrowupdate-function"></a>Fonction JetEscrowUpdate

La fonction **JetEscrowUpdate** effectue une opération d’addition atomique sur une colonne. Cette fonction permet à plusieurs sessions de mettre à jour le même enregistrement simultanément sans conflits.

```cpp
    JET_ERR JET_API JetEscrowUpdate(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_COLUMNID columnid,
      __in          void* pv,
      __in          unsigned long cbMax,
      __out_opt     void* pvOld,
      __in          unsigned long cbOldMax,
      __out_opt     unsigned long* pcbOldActual,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Session à utiliser pour cet appel.

*TableID*

Curseur à utiliser pour cet appel.

*ColumnID*

*ColumnID* de la colonne à mettre à jour.

*va*

Pointeur vers une mémoire tampon contenant le addend pour la colonne.

*cbMax*

Taille de la mémoire tampon contenant le addend.

*pvOld*

Mémoire tampon de sortie qui recevra la valeur actuelle de la colonne telle qu’elle est stockée dans la base de données (le contrôle de version est ignoré).

*cbOldMax*

Taille maximale de la mémoire tampon de sortie qui recevra la valeur actuelle de la colonne. Actuellement JET_coltypLong est pris en charge, la mémoire tampon doit avoir une longueur de 4 octets ou de 0 octets. Si *pvOld* a la valeur null, *cbOldMax* doit être égal à 0.

*pcbOldActual*

Reçoit le volume réel de données de valeur brute reçues dans la mémoire tampon de sortie.

*grbit*

Groupe de bits spécifiant zéro ou plusieurs des options suivantes.


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>JET_bitEscrowNoRollback</p> | <p>Cette mise à jour ne sera pas annulée même si la session effectuant la mise à jour du tiers de confiance a été restaurée. Notez que dans la mesure où les enregistrements du journal ne peuvent pas être vidés sur le disque, les mises à jour de dépôt récentes effectuées avec cet indicateur peuvent être perdues en cas de panne.</p> | 



### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errAlreadyPrepared</p> | <p>Le curseur a une mise à jour préparée avec <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données. cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p> | 
| <p>JET_errInvalidBufferSize</p> | <p>Une taille de mémoire tampon non valide a été passée. Actuellement, seul JET_coltypLong est pris en charge. la mémoire tampon doit donc être de 4 octets.</p> | 
| <p>JET_errInvalidOperation</p> | <p>Une colonne non valide a été spécifiée. La colonne doit être créée avec JET_bitColumnEscrowUpdate spécifié. Seules les colonnes fixes de JET_coltypLong peuvent être spécifiées comme pouvant être mises à jour par tiers de confiance.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>Le curseur doit se trouver sur un enregistrement pour pouvoir mettre à jour une colonne.</p> | 
| <p>JET_errNotInTransaction</p> | <p>Les mises à jour du tiers de confiance ne peuvent être effectuées que par les sessions dans une transaction.</p> | 
| <p>JET_errNotInitialized</p> | <p>Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p> | 
| <p>JET_errPermissionDenied</p> | <p>Le curseur ne peut pas être en lecture seule et mettre à jour un enregistrement.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La même session ne peut pas être utilisée à partir de plusieurs threads en même temps. cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p> | 
| <p>JET_errTermInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</p> | 
| <p>JET_errTransReadOnly</p> | <p>La session doit avoir des autorisations en écriture pour mettre à jour un enregistrement.</p> | 
| <p>JET_errWriteConflict</p> | <p>L’erreur retournée lorsqu’une mise à jour en conflit est demandée.</p> | 



#### <a name="remarks"></a>Remarques

Normalement, si deux sessions tentent de mettre à jour un enregistrement simultanément, la deuxième session reçoit une erreur JET_errWriteConflict, sauf si les sessions sont complètement sérialisées. Pour sérialiser deux sessions qui mettent à jour le même enregistrement, la deuxième session doit démarrer sa transaction une fois que la première transaction a validé sa transaction. Pour plus d’informations, consultez [JetBeginTransaction](./jetbegintransaction-function.md) .

Le tiers de confiance peut mettre à jour plusieurs colonnes dans le même enregistrement. Les mises à jour n’affectent pas les unes les autres.

Seules les opérations **JetEscrowUpdate** sont compatibles les unes avec les autres. Si deux sessions différentes essaient de préparer des mises à jour ou de supprimer le même enregistrement, un conflit d’écriture est généré.


| <p></p> | <p></p> | <p>Session B<br /><strong>JetEscrowUpdate</strong></p> | <p><a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a></p> | <p><a href="gg269315(v=exchg.10).md">JetDelete</a></p> | 
|---------|---------|--------------------------------------------------------|---------------------------------------------------------------|--------------------------------------------------------|
| <p></p> | <p><strong>JetEscrowUpdate</strong></p> | <p>JET_errSuccess</p> | <p>JET_errWriteConflict</p> | <p>JET_errWriteConflict</p> | 
| <p></p> | <p><a href="gg269288(v=exchg.10).md">JetUpdate</a></p> | <p>JET_errWriteConflict</p> | <p>JET_errWriteConflict</p> | <p>JET_errWriteConflict</p> | 
| <p>Session A</p> | <p><a href="gg269315(v=exchg.10).md">JetDelete</a></p> | <p>JET_errWriteConflict</p> | <p>JET_errWriteConflict</p> | <p>JET_errWriteConflict</p> | 



Les opérations de dépôt sont gérées par version et sont annulées à l’aide de [JetRollback](./jetrollback-function.md) (sauf si JET_bitEscrowNoRollback a été spécifié). **JetEscrowUpdate** retourne la valeur brute de la colonne stockée dans la base de données, car une application peut souhaiter exécuter une action spéciale quand une valeur de sentinelle est atteinte. [JetRetrieveColumn](./jetretrievecolumn-function.md) retourne la vue de version correcte de la colonne, en ignorant les mises à jour effectuées par les sessions simultanées.

À partir de deux sessions opérant sur la même colonne du même enregistrement, nous pouvons voir comment cela fonctionne. Supposons que la colonne commence par une valeur de 0.


| <p>Session</p> | <p>Opération</p> | <p>Valeur stockée</p> | <p>Valeur renvoyée</p> | 
|----------------|------------------|---------------------|-----------------------|
| <p>A</p> | <p><a href="gg294083(v=exchg.10).md">JetBeginTransation</a></p> | <p></p> | <p></p> | 
| <p>A</p> | <p><a href="gg294083(v=exchg.10).md">JetBeginTransation</a></p> | <p></p> | <p>0</p> | 
| <p>A</p> | <p><strong>JetEscrowUpdate</strong> (4)</p> | <p>4</p> | <p>0</p> | 
| <p>A</p> | <p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p> | <p></p> | <p>4</p> | 
| <p>B</p> | <p><a href="gg294083(v=exchg.10).md">JetBeginTransaction</a></p> | <p></p> | <p></p> | 
| <p>B</p> | <p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p> | <p></p> | <p>0</p> | 
| <p>B</p> | <p><strong>JetEscrowUpdate</strong> (3)</p> | <p>7</p> | <p>4</p> | 
| <p>B</p> | <p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p> | <p></p> | <p>3</p> | 
| <p>A</p> | <p><strong>JetEscrowUpdate</strong> (2)</p> | <p>9</p> | <p>7</p> | 
| <p>A</p> | <p><strong>JetEscrowUpdate</strong> (-7)</p> | <p>2</p> | <p>9</p> | 
| <p>B</p> | <p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p> | <p></p> | <p>3</p> | 
| <p>A</p> | <p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p> | <p></p> | <p>-1</p> | 
| <p>B</p> | <p><a href="gg269273(v=exchg.10).md">JetRollback</a></p> | <p>-1</p> | <p></p> | 
| <p>A</p> | <p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p> | <p></p> | <p>-1</p> | 



Il n’est pas recommandé de remplacer un enregistrement dans la même transaction qui effectue des mises à jour de dépôt dans un enregistrement. En particulier, si une mise à jour d’un enregistrement est préparée avec un [JET_TABLEID](./jet-tableid.md) et qu’un autre [JET_TABLEID](./jet-tableid.md) est utilisé pour le dépôt de la mise à jour de l’enregistrement, le tiers de confiance mis à jour sera perdu lors de l’appel de [JetUpdate](./jetupdate-function.md) . Cela se produit même si la colonne du tiers de confiance n’a pas été définie lors de la mise à jour.

Quand une colonne pouvant être mise à jour par dépôt a une valeur égale à zéro, un comportement spécial peut être déclenché. Ce comportement se produit uniquement si une opération **JetEscrowUpdate** provoque une valeur de zéro pour la colonne. L’action ne se produit pas immédiatement, mais elle se produit une fois que la transaction qui a provoqué la colonne a une valeur de zéro validations. La colonne doit toujours avoir une valeur égale à zéro (autrement dit, si aucune autre session n’a modifié la colonne). Si la colonne a été créée avec JET_bitColumnDeleteOnZero, l’enregistrement contenant la colonne sera supprimé. Si la colonne a été créée avec JET_bitColumnFinalize, un rappel sera émis. Un incident peut entraîner la non-utilisation de ces actions, mais la maintenance en ligne (à l’aide de la fonction [JetDefragment](./jetdefragment-function.md) ) rétablit correctement les actions.

#### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | | <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 



#### <a name="see-also"></a>Voir aussi

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetBeginTransaction](./jetbegintransaction-function.md)  
[JetDefragment](./jetdefragment-function.md)  
[JetPrepareUpdate](./jetprepareupdate-function.md)  
[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetStopService](./jetstopservice-function.md)  
[JetUpdate](./jetupdate-function.md)
