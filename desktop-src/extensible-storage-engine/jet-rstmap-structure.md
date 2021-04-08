---
description: 'En savoir plus sur : structure JET_RSTMAP'
title: Structure JET_RSTMAP
TOCTitle: JET_RSTMAP Structure
ms:assetid: bddf95e4-1bd4-4e3a-ad3e-d01f6564e33b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294077(v=EXCHG.10)
ms:contentKeyID: 32765692
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
ms.openlocfilehash: 646a055230b6476abf70abcde582fc2015cb241c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750556"
---
# <a name="jet_rstmap-structure"></a>Structure JET_RSTMAP


_**S’applique à :** Windows | Serveur Windows_

## <a name="jet_rstmap-structure"></a>Structure JET_RSTMAP

La structure **JET_RSTMAP** permet le remappage des chemins d’accès aux fichiers de base de données qui sont stockés dans les journaux de transactions pendant la récupération, lorsqu’ils sont utilisés par les fonctions [JetInit](./jetinit-function.md) et [JetExternalRestore](./jetexternalrestore-function.md) . Cela permet aux bases de données d’être déplacées hors connexion ou en cas de restauration à partir d’une sauvegarde.

```cpp
    typedef struct {
      xRPC_STRING tchar* szDatabaseName;
      xRPC_STRING tchar* szNewDatabaseName;
    } JET_RSTMAP;
```

### <a name="members"></a>Membres

**szDatabaseName**

Chemin d’accès absolu actuel d’une base de données associée aux journaux des transactions qui sont relus lors de la récupération.

**szNewDatabaseName**

Nouveau chemin d’accès absolu de la base de données.

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
<td><p>Implémenté comme <strong>JET_RSTMAP_W</strong> (Unicode) et <strong>JET_RSTMAP_A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Voir aussi

[JetExternalRestore](./jetexternalrestore-function.md)  
[JetInit](./jetinit-function.md)
