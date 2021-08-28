---
description: 'En savoir plus sur : JET_SESID'
title: JET_SESID
TOCTitle: JET_SESID
ms:assetid: 56b53532-e0a8-4255-8442-bb90184d91da
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269253(v=EXCHG.10)
ms:contentKeyID: 32765555
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 60920995e72fdc1f45dcc6c083be7bcc1a91b3fa
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466406"
---
# <a name="jet_sesid"></a>JET_SESID


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jet_sesid"></a>JET_SESID

Le type de données **JET_SESID** contient un descripteur de la session à utiliser pour un appel à l’API jet.

```cpp
    typedef JET_API_PTR JET_SESID;
```

### <a name="data-types"></a>Types de données

JET_SESID

La **valeur null** ou [JET_sesidNil](./invalid-handle-constants.md) peut être utilisée pour indiquer un handle de session non valide.

### <a name="remarks"></a>Remarques

Une session est le contexte de transaction du moteur de base de données. Il peut être utilisé pour commencer, valider ou abandonner des transactions qui affectent la visibilité et la durabilité des modifications apportées par ce ou d’autres sessions.

Une transaction peut être démarrée à l’aide de [JetBeginTransaction](./jetbegintransaction-function.md). Une session peut être créée à l’aide de [JetBeginSession](./jetbeginsession-function.md). Le nombre maximal de sessions qui peuvent être créées à un moment donné est contrôlé par [JET_paramMaxSessions](./resource-parameters.md), ce qui peut être configuré au moyen de [JetSetSystemParameter](./jetsetsystemparameter-function.md).

Une session est explicitement terminée par un appel à [JetEndSession](./jetendsession-function.md) ou est terminée implicitement par un appel à [JetTerm](./jetterm-function.md).

Chaque session ne peut être utilisée que par un seul thread à la fois. En outre, le comportement par défaut du moteur consiste à limiter l’utilisation d’une session au même thread à partir du moment où le premier appel à [JetBeginTransaction](./jetbegintransaction-function.md) est effectué jusqu’au moment où l’appel correspondant à [JetCommitTransaction](./jetcommittransaction-function.md) ou [JetRollback](./jetrollback-function.md) est effectué. Ce comportement peut être modifié pour supprimer cette deuxième restriction en définissant un contexte de session personnalisé à l’aide de [JetSetSessionContext](./jetsetsessioncontext-function.md) et [JetResetSessionContext](./jetresetsessioncontext-function.md).

### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 



### <a name="see-also"></a>Voir aussi

[JET_paramMaxSessions](./resource-parameters.md)  
[JetBeginSession](./jetbeginsession-function.md)  
[JetBeginTransaction](./jetbegintransaction-function.md)  
[JetCommitTransaction](./jetcommittransaction-function.md)  
[JetEndSession](./jetendsession-function.md)  
[JetResetSessionContext](./jetresetsessioncontext-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSetSessionContext](./jetsetsessioncontext-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetTerm](./jetterm-function.md)
