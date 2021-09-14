---
title: Énumération MP_REMOVAL_REASON (MpClient. h)
description: Raison de la suppression de la signature FastPath.
ms.assetid: A09B4903-E53C-4DA1-BD0B-6DE0124FCAB3
keywords:
- MP_REMOVAL_REASON énumération des fonctionnalités d’environnement Windows héritées
- PMP_REMOVAL_REASON de l’héritage des Windows fonctionnalités d’environnement du pointeur d’énumération
topic_type:
- apiref
api_name:
- MP_REMOVAL_REASON
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03ce70f46bd95d4183343990b40594326ed5d3b5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127196851"
---
# <a name="mp_removal_reason-enumeration"></a>Énumération des raisons de suppression du pack d' \_ installation \_

Raison de la suppression de la signature FastPath.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum tagMP_REMOVAL_REASON { 
  MP_REMOVAL_UNKNOWN    = 0,
  MP_REMOVAL_MANUAL     = 1,
  MP_REMOVAL_AUTOMATIC  = 2
} MP_REMOVAL_REASON, *PMP_REMOVAL_REASON;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MP_REMOVAL_UNKNOWN"></span><span id="mp_removal_unknown"></span>**suppression du pack d' \_ installation \_ inconnue**
</dt> <dd>

Inconnu.

</dd> <dt>

<span id="MP_REMOVAL_MANUAL"></span><span id="mp_removal_manual"></span>**Manuel de suppression du pack d' \_ installation \_**
</dt> <dd>

Manuelles.

</dd> <dt>

<span id="MP_REMOVAL_AUTOMATIC"></span><span id="mp_removal_automatic"></span>**désinstallation automatique du pack d' \_ installation \_**
</dt> <dd>

Automatique.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





