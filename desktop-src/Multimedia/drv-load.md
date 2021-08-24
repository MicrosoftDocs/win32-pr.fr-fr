---
title: Message DRV_LOAD (mmsystem. h)
description: Notifie le pilote qu’il a été chargé. Le pilote doit s’assurer que tout le matériel et les pilotes de prise en charge dont il a besoin pour fonctionner correctement sont présents.
ms.assetid: f3642d91-cea8-499d-8d2e-bf01a59a7d72
keywords:
- message DRV_LOAD Windows Multimedia
topic_type:
- apiref
api_name:
- DRV_LOAD
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d74b8d0663e96f0dc700739c7b8b5f9304d478ed02bf9493f24d03a506c14a61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678709"
---
# <a name="drv_load-message"></a>Le \_ message de chargement du DRV

Notifie le pilote qu’il a été chargé. Le pilote doit s’assurer que tout le matériel et les pilotes de prise en charge dont il a besoin pour fonctionner correctement sont présents.

## <a name="parameters"></a>Paramètres

Le paramètre *hdrvr* est toujours égal à zéro. Les paramètres *dwDriverId*, *lParam1* et *lParam2* ne sont pas utilisés.

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur différente de zéro en cas de réussite ou zéro dans le cas contraire.

## <a name="remarks"></a>Remarques

Le message de **\_ chargement du DRV** est toujours le premier message reçu par un pilote de périphérique.

## <a name="requirements"></a>Configuration requise



| Condition requise | Value |
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

 

 





