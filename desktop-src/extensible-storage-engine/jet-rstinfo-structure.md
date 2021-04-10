---
description: 'En savoir plus sur : structure JET_RSTINFO'
title: Structure JET_RSTINFO
TOCTitle: JET_RSTINFO Structure
ms:assetid: 2f144d68-dcd9-4d0d-9d9e-a7d2a5c350fe
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269216(v=EXCHG.10)
ms:contentKeyID: 32765519
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
ms.openlocfilehash: 3a776c84d89dfc97272c65bb0c0684faba814fdf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112550"
---
# <a name="jet_rstinfo-structure"></a>Structure JET_RSTINFO


_**S’applique à :** Windows | Serveur Windows_

## <a name="jet_rstinfo-structure"></a>Structure JET_RSTINFO

La structure **JET_RSTINFO** contient les informations de contrôle du processus de récupération, telles que les informations de réadressage de la base de données et la possibilité de contrôler l’arrêt de la récupération.

**Windows Vista :** La structure **JET_RSTINFO** est introduite dans Windows Vista.

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_RSTMAP* rgrstmap;
      long crstmap;
      JET_LGPOS lgposStop;
      JET_LOGTIME logtimeStop;
      JET_PFNSTATUS pfnStatus;
    } JET_RSTINFO;
```

### <a name="members"></a>Membres

**cbStruct**

Taille de la structure.

**rgrstmap**

Structure qui décrit l’ancien et le nouveau chemin d’accès d’une base de données restaurée.

**crstmap**

Nombre d’entrées de tableau dans le rgrstmap.

**lgposStop**

Position du journal sur laquelle arrêter la récupération. Aucune annulation n’est effectuée.

**logtimeStop**

Réservé pour un usage futur.

**pfnStatus**

Fonction d’État pour signaler l’état de la récupération.

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
<td><p>Implémenté comme <strong>JET_RSTINFO_W</strong> (Unicode) et <strong>JET_RSTINFO_A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Voir aussi

[JetInit3](./jetinit3-function.md)
