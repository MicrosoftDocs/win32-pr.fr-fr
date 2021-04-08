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
ms.openlocfilehash: be5b8bb64dc9e0fc42055cf5e4d4f67caa7654bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861962"
---
# <a name="jet_columnid"></a>JET_COLUMNID


_**S’applique à :** Windows | Serveur Windows_

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

### <a name="requirements"></a>Configuration requise

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
</tbody>
</table>

