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
ms.openlocfilehash: ed374030bd3ab577b209d326d21110482c9cf37a
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122989112"
---
# <a name="jet_recpos-structure"></a>Structure JET_RECPOS


_**S’applique à :** Windows | Windows Serveurs_

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


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 



### <a name="see-also"></a>Voir aussi

[JET_RETINFO](./jet-retinfo-structure.md)  
[JetGetRecordPosition](./jetgetrecordposition-function.md)
