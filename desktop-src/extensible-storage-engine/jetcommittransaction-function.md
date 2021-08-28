---
description: 'En savoir plus sur : fonction JetCommitTransaction'
title: Fonction JetCommitTransaction
TOCTitle: JetCommitTransaction Function
ms:assetid: 140ca76a-b3a7-4ae8-bc7e-73941fbfc759
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269191(v=EXCHG.10)
ms:contentKeyID: 32765494
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCommitTransaction
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 01e95d9a96ed59853eb167e8a0003fe756968b90d100fb8ee7a738c1f163673b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119832359"
---
# <a name="jetcommittransaction-function"></a>Fonction JetCommitTransaction


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetcommittransaction-function"></a>Fonction JetCommitTransaction

La fonction **JetCommitTransaction** valide les modifications apportées à l’état de la base de données pendant le point d’enregistrement en cours et les migre vers le point d’enregistrement précédent. Si le point d’enregistrement le plus à l’extérieur est validé, les modifications apportées pendant ce point d’enregistrement sont validées à l’état de la base de données et la session quitte la transaction.

```cpp
    JET_ERR JET_API JetCommitTransaction(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Session à utiliser pour cet appel.

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
<td><p>JET_bitCommitLazyFlush</p></td>
<td><p>La transaction est validée normalement, mais cette API n’attend pas que la transaction soit vidée dans le fichier journal des transactions avant de retourner à l’appelant. Cela réduit considérablement la durée d’une opération de validation au détriment de la durabilité. Toute transaction qui n’est pas vidée dans le journal avant un incident est automatiquement abandonnée lors de la récupération après incident lors du prochain appel à <a href="gg294068(v=exchg.10).md">JetInit</a>.</p>
<p>Si JET_bitWaitLastLevel0Commit ou JET_bitWaitAllLevel0Commit sont spécifiés, cette option est ignorée.</p>
<p>Si cet appel à <strong>JetCommitTransaction</strong> ne correspond pas au premier appel à <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a> pour cette session, cette option est ignorée. Cela est dû au fait que la dernière action qui se produit sur le point d’enregistrement le plus à l’extérieur est le facteur déterminant si l’intégralité de la transaction est réellement validée sur le disque.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitWaitAllLevel0Commit</p></td>
<td><p>Toutes les transactions précédemment validées par une session qui n’ont pas encore été vidées dans le fichier journal des transactions seront vidées immédiatement. Cette API attend que les transactions aient été vidées avant de retourner à l’appelant.</p>
<p>Cette option peut être utilisée même si la session n’est pas actuellement dans une transaction.</p>
<p>Cette option ne peut pas être utilisée conjointement avec une autre option.</p>
<p>cette option est disponible uniquement à partir de Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitWaitLastLevel0Commit</p></td>
<td><p>Si la session a précédemment validé des transactions et qu’elles n’ont pas encore été vidées dans le fichier journal des transactions, elles doivent être vidées immédiatement. Cette API attend que les transactions aient été vidées avant de retourner à l’appelant. Cela est utile si l’application a précédemment validé plusieurs transactions à l’aide de JET_bitCommitLazyFlush et souhaite maintenant les vider sur le disque.</p>
<p>Cette option peut être utilisée même si la session n’est pas actuellement dans une transaction.</p>
<p>Cette option ne peut pas être utilisée conjointement avec une autre option.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).

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
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</p>
<p>cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>L’une des options demandées n’est pas valide ou n’est pas implémentée. Cette erreur est retournée par <strong>JetCommitTransaction</strong> quand :</p>
<ul>
<li><p>Un <em>Grbit</em> illégal est spécifié.</p></li>
<li><p>JET_bitWaitLastLevel0Commit a été spécifié en combinaison avec un autre <em>Grbit</em>.</p></li>
<li><p>JET_bitWaitAllLevel0Commit a été spécifié en combinaison avec un autre <em>Grbit</em>.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInTransaction</p></td>
<td><p>L’opération a échoué, car la session spécifiée n’est pas dans une transaction.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>La même session ne peut pas être utilisée simultanément pour plusieurs threads.</p>
<p>cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</p></td>
</tr>
</tbody>
</table>


En cas de réussite, toute modification apportée à la base de données pendant le point d’enregistrement actuel pour la session donnée est validée et le point d’enregistrement est terminé. Si le dernier point d’enregistrement de la session a été interrompu, la transaction est éventuellement vidée dans le fichier journal des transactions et la session quitte la transaction.

En cas d’échec, l’état transactionnel de la session reste inchangé. Aucune modification de l’état de la base de données ne se produit. L’application doit appeler [JetRollback](./jetrollback-function.md) pour abandonner la transaction.

#### <a name="remarks"></a>Remarques

Il doit y avoir un appel à **JetCommitTransaction** ou [JetRollback](./jetrollback-function.md) pour qu’il corresponde à chaque appel à [JetBeginTransaction](./jetbegintransaction-function.md) pour une session donnée.

#### <a name="requirements"></a>Configuration requise

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Serveur</strong></p></td>
<td><p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p></td>
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

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginTransaction](./jetbegintransaction-function.md)  
[JetCommitTransaction]()  
[JetRollback](./jetrollback-function.md)  
[JetStopService](./jetstopservice-function.md)
