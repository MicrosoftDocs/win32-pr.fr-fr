---
description: 'En savoir plus sur : JET_TABLEID'
title: JET_TABLEID
TOCTitle: JET_TABLEID
ms:assetid: 09705c32-97d8-460c-8b58-921497e29c13
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269182(v=EXCHG.10)
ms:contentKeyID: 32765485
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
ms.openlocfilehash: f3221fcb23e6c512ff7b5a2ade7abad0791b9449
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465436"
---
# <a name="jet_tableid"></a>JET_TABLEID


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jet_tableid"></a>JET_TABLEID

Le type de données JET_TABLEID contient un handle vers le curseur de base de données à utiliser pour un appel à l’API JET. Un curseur ne peut être utilisé qu’avec la session qui a été utilisée pour ouvrir ce curseur.

```cpp
    typedef JET_API_PTR JET_TABLEID;
```

### <a name="data-types"></a>Types de données

JET_TABLEID

La **valeur null** ou [JET_tableidNil](./invalid-handle-constants.md) peut être utilisée pour indiquer un handle de curseur non valide.

### <a name="remarks"></a>Remarques

Un curseur gère l’utilisation d’une table pour le moteur de base de données. Un curseur peut effectuer les tâches suivantes :

  - Analyser les enregistrements

  - Rechercher des enregistrements

  - Choisir l’ordre de tri et la visibilité effectifs de ces enregistrements

  - Créer, mettre à jour ou supprimer des enregistrements

  - Modifier le schéma de la table

Les fonctionnalités prises en charge du curseur peuvent changer à mesure que l’État ou le type de la table sous-jacente change. Par exemple, une table temporaire peut ne pas autoriser la recherche de données lorsqu’elle est ouverte avec certaines options. Le curseur est toujours entièrement connecté à la table sous-jacente et interagit directement avec ces données, sans aucune mise en cache. Presque toutes les fonctionnalités ISAM principales exposées par ce moteur de base de données fonctionnent par le biais du curseur.

Un curseur peut être créé à l’aide de [JetOpenTable](./jetopentable-function.md) ou [JetOpenTempTable](./jetopentemptable-function.md). Un curseur peut être dupliqué à l’aide de [JetDupCursor](./jetdupcursor-function.md). Un curseur peut être explicitement fermé à l’aide de [JetCloseTable](./jetclosetable-function.md) ou d’une fermeture implicite à l’aide de [JetEndSession](./jetendsession-function.md) ou [JetTerm](./jetterm-function.md). Un curseur peut également être fermé implicitement par [JetRollback](./jetrollback-function.md) s’il a été ouvert dans la transaction qui a été abandonnée. Le nombre maximal de curseurs qui peuvent être créés à un moment donné est contrôlé par [JET_paramMaxCursors](./resource-parameters.md), qui peut être configuré à l’aide de [JetSetSystemParameter](./jetsetsystemparameter-function.md).

### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 



### <a name="see-also"></a>Voir aussi

[JET_paramMaxSessions](./resource-parameters.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetDupCursor](./jetdupcursor-function.md)  
[JetEndSession](./jetendsession-function.md)  
[JetOpenTable](./jetopentable-function.md)  
[JetOpenTempTable](./jetopentemptable-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetTerm](./jetterm-function.md)
