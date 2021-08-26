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
ms.openlocfilehash: 8e9952c040540e78c76d81babbb4c7b326fe92f8
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465856"
---
# <a name="jet_rstmap-structure"></a>Structure JET_RSTMAP


_**S’applique à :** Windows | Windows Serveurs_

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


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | | <p><strong>Unicode</strong></p> | <p>Implémenté comme <strong>JET_RSTMAP_W</strong> (Unicode) et <strong>JET_RSTMAP_A</strong> (ANSI).</p> | 



### <a name="see-also"></a>Voir aussi

[JetExternalRestore](./jetexternalrestore-function.md)  
[JetInit](./jetinit-function.md)
