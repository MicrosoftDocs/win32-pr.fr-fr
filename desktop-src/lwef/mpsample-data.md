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
ms.openlocfilehash: aafafd2ff7162dcb50bd5e2ea92cd56ab9f073332238dc0742845f9c48c5a588
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747412"
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

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





