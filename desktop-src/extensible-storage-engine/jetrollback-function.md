---
description: 'En savoir plus sur : fonction JetRollback'
title: JetRollback fonction)
TOCTitle: JetRollback Function
ms:assetid: 685c51f4-8fe4-47cc-8a8e-c42014431b8b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269273(v=EXCHG.10)
ms:contentKeyID: 32765575
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRollback
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f7918d1d9568848dfcd77a09ea777dba93bb2ab2
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475805"
---
# <a name="jetrollback-function"></a>JetRollback fonction)


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetrollback-function"></a>JetRollback fonction)

La fonction **JetRollback** annule les modifications apportées à l’état de la base de données et retourne au dernier point d’enregistrement. **JetRollback** ferme également tous les curseurs ouverts pendant le point d’enregistrement. Si le point d’enregistrement le plus à l’extérieur est annulé, la session va quitter la transaction.

```cpp
    JET_ERR JET_API JetRollback(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Session à utiliser pour cet appel.

*grbit*

Groupe de bits qui contiennent les options à utiliser pour cet appel, qui incluent zéro ou plusieurs des éléments suivants :


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>JET_bitRollbackAll</p> | <p>Cette option demande que toutes les modifications apportées à l’état de la base de données au cours de tous les points d’enregistrement soient annulées. Par conséquent, la session va quitter la transaction.</p> | 



### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données. cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p> | 
| <p>JET_errNotInitialized</p> | <p>Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p> | 
| <p>JET_errNotInTransaction</p> | <p>L’opération a échoué, car la session spécifiée n’est pas dans une transaction.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p> | 
| <p>JET_errRollbackError</p> | <p>Il n’était pas possible de restaurer les modifications en raison d’une erreur irrécupérable.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La même session ne peut pas être utilisée simultanément pour plusieurs threads. cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p> | 
| <p>JET_errTermInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</p> | 



En cas de réussite, toute modification apportée à la base de données pendant le point d’enregistrement actuel pour la session donnée est annulée et le point d’enregistrement est terminé. Si le dernier point d’enregistrement de la session a été interrompu, la session quitte la transaction.

En cas d’échec, l’état transactionnel de la session reste inchangé. Aucune modification de l’état de la base de données ne se produit. Un échec lors de la restauration est considéré comme une erreur catastrophique de la base de données.

#### <a name="remarks"></a>Remarques

Il doit y avoir un appel à [JetCommitTransaction](./jetcommittransaction-function.md) ou **JetRollback** pour qu’il corresponde à chaque appel à [JetBeginTransaction](./jetbegintransaction-function.md) pour une session donnée.

Si des curseurs ont été ouverts (à l’aide de [JetOpenTable](./jetopentable-function.md), par exemple) au cours d’un point d’enregistrement en cours de restauration, ce curseur est fermé.

#### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | | <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 



#### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginTransaction](./jetbegintransaction-function.md)  
[JetCommitTransaction](./jetcommittransaction-function.md)
