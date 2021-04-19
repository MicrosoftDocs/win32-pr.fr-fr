---
description: 'En savoir plus sur : structure JET_RECPOS'
title: Structure JET_RECPOS
TOCTitle: JET_RECPOS Structure
ms:assetid: 7c335120-4b84-4095-8f13-e5315d4996b1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269308(v=EXCHG.10)
ms:contentKeyID: 32765598
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
ms.openlocfilehash: e24e16aaac4228f35350f55f57a14f2820add0cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522105"
---
# <a name="jet_recpos-structure"></a>Structure JET_RECPOS


_**S’applique à :** Windows | Serveur Windows_

## <a name="jet_recpos-structure"></a>Structure JET_RECPOS

La structure **JET_RECPOS** contient une collection d’entiers représentant une position fractionnaire dans un index. **centriesLT** est le nombre d’entrées d’index inférieures à la clé d’index actuelle. **centriesInRange** est le nombre d’entrées d’index égales à la clé actuelle. **centriesInRange** n’est pas pris en charge et est toujours retourné en tant que 1. **centriesTotal** est le nombre d’entrées d’index dans l’index. Toutes les valeurs sont des approximations sans garantie de précision.

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long centriesLT;
      unsigned long centriesInRange;
      unsigned long centriesTotal;
    } JET_RECPOS;
```

### <a name="members"></a>Membres

**cbStruct**

Taille de la structure [JET_RETINFO](./jet-retinfo-structure.md) , en octets. Cette valeur confirme la présence des champs suivants.

**centriesLT**

Nombre approximatif d’entrées d’index inférieures à la clé actuelle.

**centriesInRange**

Nombre approximatif d’entrées d’index égales à la clé actuelle. Ce champ a toujours la valeur 1, quel que soit le nombre d’entrées d’index qui sont réellement égales à la clé actuelle.

**centriesTotal**

Nombre approximatif d’entrées dans l’index.

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

[JET_RETINFO](./jet-retinfo-structure.md)  
[JetGetRecordPosition](./jetgetrecordposition-function.md)
