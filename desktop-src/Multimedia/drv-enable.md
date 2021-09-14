---
title: Message DRV_ENABLE (mmsystem. h)
description: Active le pilote. Le pilote doit initialiser toutes les variables et localiser les appareils avec l’interface d’entrée et de sortie (e/s).
ms.assetid: 8aa36f3d-b36c-4460-859c-108a7a450ae5
keywords:
- message DRV_ENABLE Windows Multimedia
topic_type:
- apiref
api_name:
- DRV_ENABLE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 569b4ca5f3d0dc5f439b1e2b0e25887ffd1da4ac
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011764"
---
# <a name="drv_enable-message"></a>DRV- \_ activer le message

Active le pilote. Le pilote doit initialiser toutes les variables et localiser les appareils avec l’interface d’entrée et de sortie (e/s).

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

Les pilotes sont considérés comme activés à partir du moment où ils reçoivent ce message jusqu’à ce qu’ils soient désactivés à l’aide du message de [**\_ désactivation DRV**](drv-disable.md) .

## <a name="requirements"></a>Configuration requise



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

 

 





