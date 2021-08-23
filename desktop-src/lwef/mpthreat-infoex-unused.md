---
title: Structure MPTHREAT_INFOEX_UNUSED (MpClient. h)
description: Structure factice pour les menaces de type modification de non-comportement.
ms.assetid: 3C5305CD-D533-47B5-ADD3-BD8DA05F2046
keywords:
- fonctionnalités d’environnement Windows héritées de la structure MPTHREAT_INFOEX_UNUSED
- PMPTHREAT_INFOEX_UNUSED des fonctionnalités d’environnement du pointeur de structure Windows hérité
topic_type:
- apiref
api_name:
- MPTHREAT_INFOEX_UNUSED
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8def13a6f6aff010b9854055abd4636d19f77ef1f0e9867ec5e4d7562baff4f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119601099"
---
# <a name="mpthreat_infoex_unused-structure"></a>MPTHREAT \_ INFOEX, \_ structure inutilisée

Structure factice pour les menaces de type modification de non-comportement.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagMPTHREAT_INFOEX_UNUSED {
  DWORD dwNone;
} MPTHREAT_INFOEX_UNUSED, *PMPTHREAT_INFOEX_UNUSED;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwNone**
</dt> <dd>

Type : **DWORD**

</dd> <dd></dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





