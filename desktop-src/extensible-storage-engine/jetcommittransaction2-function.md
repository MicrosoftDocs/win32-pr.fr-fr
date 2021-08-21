---
description: 'En savoir plus sur : fonction JetCommitTransaction2'
title: JetCommitTransaction2 fonction)
TOCTitle: JetCommitTransaction2 Function
ms:assetid: 55b89f8e-7073-4fc2-bf97-103b4bc45e1c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835041(v=EXCHG.10)
ms:contentKeyID: 49894663
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetCommitTransaction2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8ad6c3584f27421b14ef44ed86b423778a570b63
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465846"
---
# <a name="jetcommittransaction2-function"></a>JetCommitTransaction2 fonction)


_**S’applique à :** Windows | Windows Serveurs_

La fonction **JetCommitTransaction2** valide les modifications apportées à l’état de la base de données pendant le point d’enregistrement en cours et les migre vers le point d’enregistrement précédent. Si le point d’enregistrement le plus à l’extérieur est validé, les modifications apportées pendant ce point d’enregistrement sont validées à l’état de la base de données et la session quitte la transaction.

la fonction **JetCommitTransaction2** a été introduite dans le système d’exploitation Windows 8.

``` c++
JET_ERR JET_API JetCommitTransaction2(
  __in          JET_SESID sesid,
  __in          JET_GRBIT grbit,
  __in          DWORD cmsecDurableCommit,
  __out         JET_COMMIT_ID pCommitID
);
```

### <a name="parameters"></a>Paramètres

*sesid*

Session à utiliser pour cet appel.

*grbit*

Groupe de bits qui spécifient zéro, une ou plusieurs des valeurs énumérées dans le tableau suivant.


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>JET_bitCommitLazyFlush</p> | <p>La transaction est validée normalement, mais cette API n’attend pas que la transaction soit vidée dans le fichier journal des transactions avant de retourner à l’appelant. Cela réduit considérablement la durée d’une opération de validation au détriment de la durabilité. Toute transaction qui n’est pas vidée dans le journal avant un incident est automatiquement abandonnée lors de la récupération après incident lors du prochain appel à la fonction <a href="gg294068(v=exchg.10).md">JetInit</a> .</p><p>Si JET_bitWaitLastLevel0Commit ou JET_bitWaitAllLevel0Commit sont spécifiés, cette option est ignorée.</p><p>Si cet appel à <strong>JetCommitTransaction2</strong> ne correspond pas au premier appel à la fonction <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a> pour cette session, cette option est ignorée. Cela est dû au fait que la dernière action qui se produit sur le point d’enregistrement le plus à l’extérieur est le facteur déterminant si l’intégralité de la transaction est réellement validée sur le disque.</p> | 
| <p>JET_bitWaitAllLevel0Commit</p> | <p>Toutes les transactions précédemment validées par une session qui n’ont pas encore été vidées dans le fichier journal des transactions seront vidées immédiatement. Cette API attend que les transactions aient été vidées avant de retourner à l’appelant.</p><p>Cette option peut être utilisée même si la session n’est pas actuellement dans une transaction.</p><p>Cette option ne peut pas être utilisée conjointement avec une autre option.</p><p>cette option est disponible dans les versions du système d’exploitation Windows server à partir de Windows server 2003.</p> | 
| <p>JET_bitWaitLastLevel0Commit</p> | <p>Si la session a précédemment validé des transactions et qu’elles n’ont pas encore été vidées dans le fichier journal des transactions, elles doivent être vidées immédiatement. Cette API attend que les transactions aient été vidées avant de retourner à l’appelant. Cela est utile si l’application a précédemment validé plusieurs transactions à l’aide de JET_bitCommitLazyFlush et souhaite maintenant les vider sur le disque.</p><p>Cette option peut être utilisée même si la session n’est pas actuellement dans une transaction.</p><p>Cette option ne peut pas être utilisée conjointement avec une autre option.</p> | 



*cmsecDurableCommit*

Durée de validation d’une transaction paresseuse.

*pCommitID*

ID de validation associé à cet enregistrement de validation.

### <a name="return-value"></a>Valeur de retour

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour énumérés dans le tableau suivant. pour plus d’informations sur les erreurs ESE (extensible Stockage engine) possibles, consultez [erreurs du moteur de Stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a cessé à la suite d’un appel à la fonction <a href="gg269240(v=exchg.10).md">JetStopService</a> .</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</p><p>cette erreur est renvoyée uniquement par les versions du système d’exploitation Windows à partir de Windows XP.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>L’une des options demandées n’est pas valide ou n’est pas implémentée. Cette erreur est retournée par la fonction <strong>JetCommitTransaction2</strong> dans les cas suivants :</p><ul><li><p>Un <em>Grbit</em> illégal est spécifié.</p></li><li><p>JET_bitWaitLastLevel0Commit a été spécifié en combinaison avec un autre <em>Grbit</em>.</p></li><li><p>JET_bitWaitAllLevel0Commit a été spécifié en combinaison avec un autre <em>Grbit</em>.</p></li></ul> | 
| <p>JET_errNotInitialized</p> | <p>Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p> | 
| <p>JET_errNotInTransaction</p> | <p>L’opération a échoué, car la session spécifiée n’est pas dans une transaction.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La même session ne peut pas être utilisée simultanément pour plusieurs threads.</p><p>cette erreur est renvoyée uniquement par les versions du système d’exploitation Windows à partir de Windows XP.</p> | 
| <p>JET_errTermInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</p> | 



En cas de réussite, toute modification apportée à la base de données pendant le point d’enregistrement actuel pour la session donnée est validée et le point d’enregistrement est terminé. Si le dernier point d’enregistrement de la session est terminé, la transaction est éventuellement vidée dans le fichier journal des transactions et la session quitte la transaction.

En cas d’échec, l’état transactionnel de la session reste inchangé. Aucune modification de l’état de la base de données ne se produit. L’application doit appeler la fonction [JetRollback](./jetrollback-function.md) pour abandonner la transaction.

#### <a name="remarks"></a>Remarques

Il doit y avoir un appel à **JetCommitTransaction2** ou [JetRollback](./jetrollback-function.md) pour qu’il corresponde à chaque appel à [JetBeginTransaction](./jetbegintransaction-function.md) pour une session donnée.

#### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>Requiert Windows 8.</p> | | <p><strong>Serveur</strong></p> | <p>Requiert Windows Server 2012.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | | <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 



#### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginTransaction](./jetbegintransaction-function.md)  
[JetCommitTransaction](./jetcommittransaction-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetStopService](./jetstopservice-function.md)
