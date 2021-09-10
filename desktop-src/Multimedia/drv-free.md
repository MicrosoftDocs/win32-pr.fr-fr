---
title: Message DRV_FREE (mmsystem. h)
description: Avertit le pilote qu’il est en cours de suppression de la mémoire. Le pilote doit libérer la mémoire et les autres ressources système qu’il a allouées.
ms.assetid: 0447f8e9-4c4d-4be5-ab1f-ecd3e8cd2e67
keywords:
- message DRV_FREE Windows Multimedia
topic_type:
- apiref
api_name:
- DRV_FREE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abb9d70d269cb84e0d6ef0881618b67cfef11068
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364135"
---
# <a name="drv_free-message"></a>\_Message Free DRV

Avertit le pilote qu’il est en cours de suppression de la mémoire. Le pilote doit libérer la mémoire et les autres ressources système qu’il a allouées.

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*
</dt> <dd>

Handle de l’instance du pilote installable.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Pas de valeur de retour.

## <a name="remarks"></a>Remarques

Les paramètres *dwDriverId*, *lParam1* et *lParam2* ne sont pas utilisés.

Le **message \_ Free DRV** est toujours le dernier message reçu par un pilote de périphérique.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Mmsystem. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Pilotes installables](installable-drivers.md)
</dt> <dt>

[Messages de pilote installables](installable-driver-messages.md)
</dt> </dl>

 

 





