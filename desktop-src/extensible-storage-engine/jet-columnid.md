---
description: 'En savoir plus sur : JET_COLUMNID'
title: JET_COLUMNID
TOCTitle: JET_COLUMNID
ms:assetid: d6c74c5c-ba61-4e1c-a1b1-495e925b6b68
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294104(v=EXCHG.10)
ms:contentKeyID: 32765719
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
ms.openlocfilehash: fbdc03342187cfc2adfa1dcd3ed650f532e1dbc0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127095202"
---
# <a name="jet_columnid"></a>JET_COLUMNID


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jet_columnid"></a>JET_COLUMNID

Le type de données **JET_COLUMNID** identifie une colonne dans une table.

```cpp
    typedef unsigned long JET_COLUMNID;
```

### <a name="data-types"></a>Types de données

JET_COLUMNID

Identifie une colonne dans une table.

### <a name="remarks"></a>Notes

Les ID de colonne sont uniques dans une table unique. Une fois qu’une colonne est connue pour avoir un certain ID de colonne, elle aura toujours cet ID de colonne. La restauration à partir d’une sauvegarde ne modifie pas la valeur d’un ID de colonne. Toutefois, si une ou plusieurs colonnes de table, antérieures à une colonne de table spécifique, sont supprimées, une base de données compacte peut alors modifier la valeur d’un ID de colonne.

Dans certains cas, les ID de colonne sont le seul moyen d’identifier les colonnes. Lorsqu’une table temporaire est créée, ses colonnes n’ont pas de noms, mais un tableau d’ID de colonne est retourné par la fonction Create.

Les colonnes de différentes tables peuvent avoir le même ID de colonne.

### <a name="requirements"></a>Spécifications


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 


