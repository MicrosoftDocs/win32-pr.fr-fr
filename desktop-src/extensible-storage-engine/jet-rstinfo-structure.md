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
ms.openlocfilehash: 76da8fdc7ded6025e2497771622a8e34c3928967
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126917248"
---
# <a name="jet_rstinfo-structure"></a>Structure JET_RSTINFO


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jet_rstinfo-structure"></a>Structure JET_RSTINFO

La structure **JET_RSTINFO** contient les informations de contrôle du processus de récupération, telles que les informations de réadressage de la base de données et la possibilité de contrôler l’arrêt de la récupération.

**Windows Vista :** la structure **JET_RSTINFO** est introduite dans Windows Vista.

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

### <a name="requirements"></a>Spécifications


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implémenté comme <strong>JET_RSTINFO_W</strong> (Unicode) et <strong>JET_RSTINFO_A</strong> (ANSI).</p> | 



### <a name="see-also"></a>Voir aussi

[JetInit3](./jetinit3-function.md)
