---
description: 'En savoir plus sur : structure JET_LGPOS'
title: Structure JET_LGPOS
TOCTitle: JET_LGPOS Structure
ms:assetid: dbce1a60-b32b-40c1-a215-e93bb77cd8c1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294113(v=EXCHG.10)
ms:contentKeyID: 32765727
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
ms.openlocfilehash: abf3ca2996e75d2abfe6fc766ec6f5bbd30054eeb9dd8406fe2747307a00c4a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119109256"
---
# <a name="jet_lgpos-structure"></a>Structure JET_LGPOS


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jet_lgpos-structure"></a>Structure JET_LGPOS

La structure **JET_LGPOS** contient des données qui sont internes au mécanisme de journalisation du moteur de base de données. Cette structure est considérée comme interne.

```cpp
    typedef struct {
      unsigned short ib;
      unsigned short isec;
      long lGeneration;
    } JET_LGPOS;
```

### <a name="members"></a>Membres

**IB**

Prend en charge l’infrastructure ESE et ne peut pas être utilisé à partir de votre code.

**ISEC**

Prend en charge l’infrastructure ESE et ne peut pas être utilisé à partir de votre code.

**lGeneration**

Prend en charge l’infrastructure ESE et ne peut pas être utilisé à partir de votre code.

### <a name="requirements"></a>Configuration requise

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Serveur</strong></p></td>
<td><p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>En-tête</strong></p></td>
<td><p>Déclaré dans esent. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Voir aussi

[JET_BKINFO](./jet-bkinfo-structure.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)
