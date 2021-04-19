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
ms.openlocfilehash: 61fb49d50ee7c529174fe4c5546efd7de1727892
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534691"
---
# <a name="jetescrowupdate-function"></a>Fonction JetEscrowUpdate


_**S’applique à :** Windows | Serveur Windows_

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

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valeur</p></th>
<th><p>Signification</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitEscrowNoRollback</p></td>
<td><p>Cette mise à jour ne sera pas annulée même si la session effectuant la mise à jour du tiers de confiance a été restaurée. Notez que dans la mesure où les enregistrements du journal ne peuvent pas être vidés sur le disque, les mises à jour de dépôt récentes effectuées avec cet indicateur peuvent être perdues en cas de panne.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Code de retour</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>L’opération s’est terminée avec succès.</p></td>
</tr>
<tr class="even">
<td><p>JET_errAlreadyPrepared</p></td>
<td><p>Le curseur a une mise à jour préparée avec <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données. Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidBufferSize</p></td>
<td><p>Une taille de mémoire tampon non valide a été passée. Actuellement, seul JET_coltypLong est pris en charge. la mémoire tampon doit donc être de 4 octets.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidOperation</p></td>
<td><p>Une colonne non valide a été spécifiée. La colonne doit être créée avec JET_bitColumnEscrowUpdate spécifié. Seules les colonnes fixes de JET_coltypLong peuvent être spécifiées comme pouvant être mises à jour par tiers de confiance.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>Le curseur doit se trouver sur un enregistrement pour pouvoir mettre à jour une colonne.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInTransaction</p></td>
<td><p>Les mises à jour du tiers de confiance ne peuvent être effectuées que par les sessions dans une transaction.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p></td>
</tr>
<tr class="even">
<td><p>JET_errPermissionDenied</p></td>
<td><p>Le curseur ne peut pas être en lecture seule et mettre à jour un enregistrement.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>La même session ne peut pas être utilisée à partir de plusieurs threads en même temps. Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTransReadOnly</p></td>
<td><p>La session doit avoir des autorisations en écriture pour mettre à jour un enregistrement.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errWriteConflict</p></td>
<td><p>L’erreur retournée lorsqu’une mise à jour en conflit est demandée.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Notes

Normalement, si deux sessions tentent de mettre à jour un enregistrement simultanément, la deuxième session reçoit une erreur JET_errWriteConflict, sauf si les sessions sont complètement sérialisées. Pour sérialiser deux sessions qui mettent à jour le même enregistrement, la deuxième session doit démarrer sa transaction une fois que la première transaction a validé sa transaction. Pour plus d’informations, consultez [JetBeginTransaction](./jetbegintransaction-function.md) .

Le tiers de confiance peut mettre à jour plusieurs colonnes dans le même enregistrement. Les mises à jour n’affectent pas les unes les autres.

Seules les opérations **JetEscrowUpdate** sont compatibles les unes avec les autres. Si deux sessions différentes essaient de préparer des mises à jour ou de supprimer le même enregistrement, un conflit d’écriture est généré.

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p></p></th>
<th><p>Session B<br />
<strong>JetEscrowUpdate</strong></p></th>
<th><p><a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a></p></th>
<th><p><a href="gg269315(v=exchg.10).md">JetDelete</a></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><strong>JetEscrowUpdate</strong></p></td>
<td><p>JET_errSuccess</p></td>
<td><p>JET_errWriteConflict</p></td>
<td><p>JET_errWriteConflict</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><a href="gg269288(v=exchg.10).md">JetUpdate</a></p></td>
<td><p>JET_errWriteConflict</p></td>
<td><p>JET_errWriteConflict</p></td>
<td><p>JET_errWriteConflict</p></td>
</tr>
<tr class="odd">
<td><p>Session A</p></td>
<td><p><a href="gg269315(v=exchg.10).md">JetDelete</a></p></td>
<td><p>JET_errWriteConflict</p></td>
<td><p>JET_errWriteConflict</p></td>
<td><p>JET_errWriteConflict</p></td>
</tr>
</tbody>
</table>


Les opérations de dépôt sont gérées par version et sont annulées à l’aide de [JetRollback](./jetrollback-function.md) (sauf si JET_bitEscrowNoRollback a été spécifié). **JetEscrowUpdate** retourne la valeur brute de la colonne stockée dans la base de données, car une application peut souhaiter exécuter une action spéciale quand une valeur de sentinelle est atteinte. [JetRetrieveColumn](./jetretrievecolumn-function.md) retourne la vue de version correcte de la colonne, en ignorant les mises à jour effectuées par les sessions simultanées.

À partir de deux sessions opérant sur la même colonne du même enregistrement, nous pouvons voir comment cela fonctionne. Supposons que la colonne commence par une valeur de 0.

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>session</p></th>
<th><p>Opération</p></th>
<th><p>Valeur stockée</p></th>
<th><p>Valeur renvoyée</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Un</p></td>
<td><p><a href="gg294083(v=exchg.10).md">JetBeginTransation</a></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Un</p></td>
<td><p><a href="gg294083(v=exchg.10).md">JetBeginTransation</a></p></td>
<td><p></p></td>
<td><p>0</p></td>
</tr>
<tr class="odd">
<td><p>Un</p></td>
<td><p><strong>JetEscrowUpdate</strong> (4)</p></td>
<td><p>4</p></td>
<td><p>0</p></td>
</tr>
<tr class="even">
<td><p>Un</p></td>
<td><p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p></td>
<td><p></p></td>
<td><p>4</p></td>
</tr>
<tr class="odd">
<td><p>B</p></td>
<td><p><a href="gg294083(v=exchg.10).md">JetBeginTransaction</a></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>B</p></td>
<td><p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p></td>
<td><p></p></td>
<td><p>0</p></td>
</tr>
<tr class="odd">
<td><p>B</p></td>
<td><p><strong>JetEscrowUpdate</strong> (3)</p></td>
<td><p>7</p></td>
<td><p>4</p></td>
</tr>
<tr class="even">
<td><p>B</p></td>
<td><p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p></td>
<td><p></p></td>
<td><p>3</p></td>
</tr>
<tr class="odd">
<td><p>Un</p></td>
<td><p><strong>JetEscrowUpdate</strong> (2)</p></td>
<td><p>9</p></td>
<td><p>7</p></td>
</tr>
<tr class="even">
<td><p>Un</p></td>
<td><p><strong>JetEscrowUpdate</strong> (-7)</p></td>
<td><p>2</p></td>
<td><p>9</p></td>
</tr>
<tr class="odd">
<td><p>B</p></td>
<td><p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p></td>
<td><p></p></td>
<td><p>3</p></td>
</tr>
<tr class="even">
<td><p>Un</p></td>
<td><p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p></td>
<td><p></p></td>
<td><p>-1</p></td>
</tr>
<tr class="odd">
<td><p>B</p></td>
<td><p><a href="gg269273(v=exchg.10).md">JetRollback</a></p></td>
<td><p>-1</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Un</p></td>
<td><p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p></td>
<td><p></p></td>
<td><p>-1</p></td>
</tr>
</tbody>
</table>


Il n’est pas recommandé de remplacer un enregistrement dans la même transaction qui effectue des mises à jour de dépôt dans un enregistrement. En particulier, si une mise à jour d’un enregistrement est préparée avec un [JET_TABLEID](./jet-tableid.md) et qu’un autre [JET_TABLEID](./jet-tableid.md) est utilisé pour le dépôt de la mise à jour de l’enregistrement, le tiers de confiance mis à jour sera perdu lors de l’appel de [JetUpdate](./jetupdate-function.md) . Cela se produit même si la colonne du tiers de confiance n’a pas été définie lors de la mise à jour.

Quand une colonne pouvant être mise à jour par dépôt a une valeur égale à zéro, un comportement spécial peut être déclenché. Ce comportement se produit uniquement si une opération **JetEscrowUpdate** provoque une valeur de zéro pour la colonne. L’action ne se produit pas immédiatement, mais elle se produit une fois que la transaction qui a provoqué la colonne a une valeur de zéro validations. La colonne doit toujours avoir une valeur égale à zéro (autrement dit, si aucune autre session n’a modifié la colonne). Si la colonne a été créée avec JET_bitColumnDeleteOnZero, l’enregistrement contenant la colonne sera supprimé. Si la colonne a été créée avec JET_bitColumnFinalize, un rappel sera émis. Un incident peut entraîner la non-utilisation de ces actions, mais la maintenance en ligne (à l’aide de la fonction [JetDefragment](./jetdefragment-function.md) ) rétablit correctement les actions.

#### <a name="requirements"></a>Configuration requise

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</p></td>
</tr>
<tr class="even">
<td><p><strong>Serveur</strong></p></td>
<td><p>Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>En-tête</strong></p></td>
<td><p>Déclaré dans esent. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Bibliothèque</strong></p></td>
<td><p>Utilisez ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Requiert ESENT.dll.</p></td>
</tr>
</tbody>
</table>


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
