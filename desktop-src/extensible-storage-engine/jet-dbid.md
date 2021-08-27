---
description: 'En savoir plus sur : JET_DBID'
title: JET_DBID
TOCTitle: JET_DBID
ms:assetid: 516acb79-aa75-4609-81b6-3b2e4e0c95af
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269248(v=EXCHG.10)
ms:contentKeyID: 32765550
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
ms.openlocfilehash: 988dd14ca96a5818254602b5ab6dcaeab4952669
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470905"
---
# <a name="jet_dbid"></a>JET_DBID


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jet_dbid"></a>JET_DBID

Le type de données **JET_DBID** contient le descripteur de la base de données. Un descripteur de base de données est utilisé pour gérer le schéma d’une base de données. Il peut également être utilisé pour gérer les tables à l’intérieur de cette base de données.

```cpp
    typedef unsigned long JET_DBID;
```

### <a name="data-types"></a>Types de données

JET_DBID

Handle de la base de données.

La valeur JET_dbidNil indique que le handle n’est pas valide.

### <a name="remarks"></a>Remarques

Un descripteur de base de données est créé au moyen d’un appel à [JetCreateDatabase](./jetcreatedatabase-function.md) ou [JetOpenDatabase](./jetopendatabase-function.md).

Un descripteur de base de données peut être explicitement fermé par [JetCloseDatabase](./jetclosedatabase-function.md) ou fermé implicitement par [JetEndSession](./jetendsession-function.md) ou [JetTerm](./jetterm-function.md).

Un descripteur de base de données peut être utilisé uniquement dans la session dans laquelle il a été créé. L’existence d’un descripteur de base de données correspond à l’ouverture logique d’une base de données. Une ouverture logique est différente de l’ouverture physique d’une base de données, qui se produit lorsqu’une base de données est attachée au système.

### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 



### <a name="see-also"></a>Voir aussi

[JetCreateDatabase](./jetcreatedatabase-function.md)  
[JetOpenDatabase](./jetopendatabase-function.md)  
[JetCloseDatabase](./jetclosedatabase-function.md)  
[JetEndSession](./jetendsession-function.md)
