---
description: 'En savoir plus sur : structure JET_INDEXID'
title: Structure JET_INDEXID
TOCTitle: JET_INDEXID Structure
ms:assetid: 8b1d90f0-bc93-4b30-90d1-b9e93ad26654
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269327(v=EXCHG.10)
ms:contentKeyID: 32765617
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
ms.openlocfilehash: e1a9c6a971e44604240d750163f0570937f9d4db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522242"
---
# <a name="jet_indexid-structure"></a>Structure JET_INDEXID


_**S’applique à :** Windows | Serveur Windows_

## <a name="jet_indexid-structure"></a>Structure JET_INDEXID

La structure **JET_INDEXID** contient un ID d’index. Un ID d’index est un indicateur utilisé pour accélérer la sélection de l’index actuel à l’aide de [JetSetCurrentIndex](./jetsetcurrentindex-function.md). Elle est particulièrement utile lorsqu’il existe un très grand nombre d’index sur une table. L’ID d’index peut être récupéré à l’aide de [JetGetIndexInfo](./jetgetindexinfo-function.md) ou [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).

```cpp
    typedef struct tagJET_INDEXID {
      unsigned long cbStruct;
      char rgbIndexId[sizeof(JET_API_PRT) + sizeof(unsigned long) + sizeof(unsigned long)];
    } JET_INDEXID;
```

### <a name="members"></a>Membres

**cbStruct**

Taille, en octets, de l’ID d’index.

Il s’agit de la taille réelle de l’ID d’index qui est retourné dans la mémoire tampon de sortie à partir de [JetGetIndexInfo](./jetgetindexinfo-function.md) ou [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).

**rgbIndexId**

Objet BLOB opaque d’informations utilisé par le moteur pour identifier rapidement un index dans son cache de schéma.

N’essayez pas d’interpréter l’objet BLOB d’informations. Il ne s’agit pas d’une taille définie.

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


### <a name="see-also"></a>Voir aussi

[JetGetIndexInfo](./jetgetindexinfo-function.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)  
[JetGetTableInfo](./jetgettableinfo-function.md)  
[JetSetCurrentIndex](./jetsetcurrentindex-function.md)
