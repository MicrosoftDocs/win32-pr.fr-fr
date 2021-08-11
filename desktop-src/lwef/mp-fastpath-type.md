---
title: Énumération MP_FASTPATH_TYPE (MpClient. h)
description: Type de FastPath.
ms.assetid: BD72228F-DCC0-435E-A408-BD7FB02E55E1
keywords:
- MP_FASTPATH_TYPE énumération des fonctionnalités d’environnement Windows héritées
- PMP_FASTPATH_TYPE de l’héritage des Windows fonctionnalités d’environnement du pointeur d’énumération
topic_type:
- apiref
api_name:
- MP_FASTPATH_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7bd9a8ce26f930a35c9c4fa547234b0d55b0b588b60881cf8aae31621e9a83a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118247444"
---
# <a name="mp_fastpath_type-enumeration"></a>\_ \_ Énumération de type FASTPATH MP

Type de FastPath.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum tagMP_FASTPATH_TYPE { 
  MP_FASTPATH_UNKNOWN   = 0,
  MP_FASTPATH_VDM       = 1,
  MP_FASTPATH_DISABLED  = 2
} MP_FASTPATH_TYPE, *PMP_FASTPATH_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MP_FASTPATH_UNKNOWN"></span><span id="mp_fastpath_unknown"></span>**FASTPATH de point de gestion \_ \_ inconnu**
</dt> <dd>

Inconnu.

</dd> <dt>

<span id="MP_FASTPATH_VDM"></span><span id="mp_fastpath_vdm"></span>**\_ \_ machine virtuelle FASTPATH MP**
</dt> <dd>

Mise à jour de VDM.

</dd> <dt>

<span id="MP_FASTPATH_DISABLED"></span><span id="mp_fastpath_disabled"></span>**\_FASTPATH MP \_ désactivé**
</dt> <dd>

Notification de désactivation de signature.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





