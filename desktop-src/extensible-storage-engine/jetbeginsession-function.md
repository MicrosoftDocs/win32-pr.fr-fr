---
description: 'En savoir plus sur : fonction JetBeginSession'
title: Fonction JetBeginSession
TOCTitle: JetBeginSession Function
ms:assetid: f1c33b78-f2d1-44ea-8ec9-94b729b94e24
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294131(v=EXCHG.10)
ms:contentKeyID: 32765745
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginSessionA
- JetBeginSession
- JetBeginSessionW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3e6263916211e5d21e0032ba6de8d98e46fedfa9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127531361"
---
# <a name="jetbeginsession-function"></a>Fonction JetBeginSession


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetbeginsession-function"></a>Fonction JetBeginSession

La fonction **JetBeginSession** démarre une session et initialise et retourne un handle de session ESE ([JET_SESID](./jet-sesid.md)). Les sessions contrôlent tous les accès à la base de données et sont utilisées pour contrôler l’étendue des transactions. La session peut être utilisée pour commencer, valider ou abandonner des transactions. La session est également utilisée pour attacher, créer ou ouvrir une base de données. La session est utilisée comme contexte pour toutes les opérations DDL et DML. Pour augmenter l’accès concurrentiel et l’accès parallèle à la base de données, plusieurs sessions peuvent être démarrées.

```cpp
    JET_ERR JET_API JetBeginSession(
      __in          JET_INSTANCE instance,
      __out         JET_SESID* psesid,
      __in_opt      JET_PCSTR szUserName,
      __in_opt      JET_PCSTR szPassword
    );
```

### <a name="parameters"></a>Paramètres

*instancié*

Instance de base de données à utiliser pour cet appel.

*psesid*

Pointeur vers la variable que le handle de session Initialise lors d’un retour réussi.

*szUserName*

Ce paramètre est réservé.

*szPassword*

Ce paramètre est réservé.

### <a name="return-value"></a>Valeur renvoyée

Cette fonction permet le retour de tout [JET_ERR](./jet-err.md)s qui sont définis dans cette API. pour plus d’informations sur les erreurs Jet, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</p><p>cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p> | 
| <p>JET_errInvalidParameter</p> | <p>L’un des paramètres fournis contenait une valeur inattendue ou contenait une valeur qui n’a pas de sens lorsqu’elle était associée à la valeur d’un autre paramètre.</p> | 
| <p>JET_errNotInitialized</p> | <p>Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p> | 
| <p>JET_errOutOfMemory</p> | <p>L’opération a échoué car la mémoire n’a pas pu être allouée.</p> | 
| <p>JET_errOutOfSessions</p> | <p>Le nombre de sessions que le moteur autorise le client à démarrer est limité. Cette valeur peut être modifiée à l’aide de <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> avec la constante JET_paramMaxSessions. Le nombre de sessions par défaut est 16. Pour plus d’informations sur la JET_paramMaxSessions, consultez <a href="gg294139(v=exchg.10).md">paramètres système</a> .</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p> | 
| <p>JET_errTermInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</p> | 



En cas de réussite, le descripteur de session est initialisé et peut être utilisé pour les opérations de base de données.

En cas d’échec, aucune session n’est disponible ou une nouvelle session n’a pas pu être initialisée.

#### <a name="remarks"></a>Notes

Une attention particulière doit être utilisée lors de l’utilisation de sessions sur différents threads. Une session suit le thread sur lequel elle a été utilisée pendant [JetBeginTransaction](./jetbegintransaction-function.md), [JetCommitTransaction](./jetcommittransaction-function.md)ou [JetRollback](./jetrollback-function.md), et génère une erreur si elle est utilisée sur plusieurs threads avec une transaction ouverte. Le [JetResetSessionContext](./jetresetsessioncontext-function.md), [JetSetSessionContext](./jetsetsessioncontext-function.md) peut modifier ce comportement. Étant donné que la session est toujours un contexte sérialisé, plusieurs opérations de base de données ne peuvent pas être exécutées simultanément sur une seule session, en série uniquement. Toutefois, vous pouvez utiliser plusieurs sessions pour obtenir un accès simultané à la base de données. Les sessions peuvent être utilisées à l’intérieur d’une transaction entre les threads en définissant et en réinitialisant les contextes de session.

Le descripteur de session doit être fermé avec [JetEndSession](./jetendsession-function.md).

#### <a name="requirements"></a>Spécifications


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 
| <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implémenté en tant que <strong>JetBeginSessionW</strong> (Unicode) et <strong>JetBeginSessionA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginTransaction](./jetbegintransaction-function.md)  
[JetCommitTransaction](./jetcommittransaction-function.md)  
[JetDupSession](./jetdupsession-function.md)  
[JetEndSession](./jetendsession-function.md)  
[JetResetSessionContext](./jetresetsessioncontext-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSetSessionContext](./jetsetsessioncontext-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Paramètres système](./extensible-storage-engine-system-parameters.md)
