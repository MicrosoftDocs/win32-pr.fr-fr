---
description: 'En savoir plus sur : fonction JetDupSession'
title: JetDupSession fonction)
TOCTitle: JetDupSession Function
ms:assetid: fa8fbaca-fe48-401e-9700-1303f4842ad9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294141(v=EXCHG.10)
ms:contentKeyID: 32765755
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDupSession
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7aa320c329032f5867f5f762351277cc4567baef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867553"
---
# <a name="jetdupsession-function"></a>JetDupSession fonction)


_**S’applique à :** Windows | Serveur Windows_

## <a name="jetdupsession-function"></a>JetDupSession fonction)

La fonction **JetDupSession** démarre une session, puis initialise et retourne un handle de session ESE ([JET_SESID](./jet-sesid.md)). Les sessions contrôlent tous les accès à la base de données et sont utilisées pour contrôler l’étendue des transactions. La session peut être utilisée pour commencer, valider ou abandonner des transactions. La session est également utilisée pour attacher, créer ou ouvrir une base de données. La session est utilisée comme contexte pour toutes les opérations DDL et DML. Pour augmenter l’accès concurrentiel et l’accès parallèle à la base de données, plusieurs sessions peuvent être démarrées.

**Remarque** Cette API agira de la même manière qu’un [JetBeginSession](./jetbeginsession-function.md) appelé sur l’instance de la session passée. Cette fonction n’est pas recommandée, [JetBeginSession](./jetbeginsession-function.md) est préféré.

```cpp
    JET_ERR JET_API JetDupSession(
      __in          JET_SESID sesid,
      __out         JET_SESID* psesid
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Session à utiliser comme source pour la duplication ou le début de la session.

*psesid*

Pointeur vers la variable que le handle de session Initialise lors d’un retour réussi.

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
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</p>
<p>Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>L’un des paramètres fournis contenait une valeur inattendue ou contenait une valeur qui n’a pas de sens lorsqu’elle était associée à la valeur d’un autre paramètre.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfMemory</p></td>
<td><p>L’opération a échoué car la mémoire n’a pas pu être allouée.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfSessions</p></td>
<td><p>Le nombre de sessions que le moteur autorise le client à démarrer est limité. Cette valeur peut être modifiée à l’aide de <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> avec la constante <em>JET_paramMaxSessions</em> . Le nombre de sessions par défaut est 16. Pour plus d’informations sur la <em>JET_paramMaxSessions</em>, consultez <a href="gg294139(v=exchg.10).md">paramètres système</a> .</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</p></td>
</tr>
</tbody>
</table>


En cas de réussite, le descripteur de session est initialisé et peut être utilisé pour les opérations de base de données.

En cas d’échec, aucune session n’est disponible ou une nouvelle session n’a pas pu être initialisée.

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

[JET_SESID](./jet-sesid.md)  
[JetBeginSession](./jetbeginsession-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Paramètres système](./extensible-storage-engine-system-parameters.md)
