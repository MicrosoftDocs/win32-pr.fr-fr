---
title: Structure MPSAMPLE_DATA (MpClient. h)
description: Données de notification transmises à l’exemple de fonction de rappel de soumission.
ms.assetid: 58F348C6-411D-4545-9D4D-A80095FD139B
keywords:
- fonctionnalités d’environnement Windows héritées de la structure MPSAMPLE_DATA
- PMPSAMPLE_DATA des fonctionnalités d’environnement du pointeur de structure Windows hérité
topic_type:
- apiref
api_name:
- MPSAMPLE_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24a894638465c0362069b8fdcbacddf98bfdd2c1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404555"
---
# <a name="mpsample_data-structure"></a>\_Structure de données MPSAMPLE

Données de notification transmises à l’exemple de fonction de rappel de soumission.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagMPSAMPLE_DATA {
  DWORD dwSampleIndex;
} MPSAMPLE_DATA, *PMPSAMPLE_DATA;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwSampleIndex**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Index de l’exemple d’élément pour lequel l’état d’envoi est signalé.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





