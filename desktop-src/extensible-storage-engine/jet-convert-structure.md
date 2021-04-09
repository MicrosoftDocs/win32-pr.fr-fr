---
description: 'En savoir plus sur : structure JET_CONVERT'
title: Structure JET_CONVERT
TOCTitle: JET_CONVERT Structure
ms:assetid: 33a0ff95-e9af-44c0-bf80-03d785771d5e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269220(v=EXCHG.10)
ms:contentKeyID: 32765523
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
ms.openlocfilehash: c4e39548b6bcb0a4742b926c1b618b9cc899c2e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863185"
---
# <a name="jet_convert-structure"></a>Structure JET_CONVERT


_**S’applique à :** Windows | Serveur Windows_

## <a name="jet_convert-structure"></a>Structure JET_CONVERT

La structure **JET_CONVERT** contient le nom d’une dll de version ESE antérieure qui est utilisée pour lire les bases de données créées avec cette version antérieure. En outre, d’autres indicateurs sont fournis pour contrôler la nature de la conversion.

**Windows Server 2003 :** La fonctionnalité de [JetCompact](./jetcompact-function.md) qui a effectué une conversion a été supprimée du produit dans Windows Server 2003. Il est uniquement pris en charge dans Windows 2000 et Windows XP.

```cpp
    typedef struct tagCONVERT {
      tchar* SzOldDll;
      union {
        unsigned long fFlags;
        struct {
          unsigned long fSchemaChangesOnly  :1;
        };
      };
    } JET_CONVERT;
```

### <a name="members"></a>Membres

**SzOldDll**

Nom, y compris les informations de chemin d’accès, à la version antérieure de la DLL ESE.

**fFlags**

Réservé pour le système.

**fSchemaChangesOnly**

Réservé pour le système.

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implémenté comme <strong>JET_CONVERT_W</strong> (Unicode) et <strong>JET_CONVERT_A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Voir aussi

[JetCompact](./jetcompact-function.md)
