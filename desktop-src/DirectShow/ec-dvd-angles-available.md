---
description: Indique si un bloc angle est lu et si des modifications d’angle peuvent être effectuées.
ms.assetid: 15593841-3162-4598-86bc-1debca22b284
title: EC_DVD_ANGLES_AVAILABLE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_ANGLES_AVAILABLE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: e95c692aed8ac6c709ff0db1d6056fc59219fa73f5aa2e4cfb9b31b2c1a03d94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015987"
---
# <a name="ec_dvd_angles_available"></a>\_angles de DVD EC \_ \_ disponibles

Indique si un bloc angle est lu et si des modifications d’angle peuvent être effectuées.

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Valeur booléenne (**bool**) qui indique si un bloc angle est lu. Zéro (0) indique que la lecture n’est pas dans un bloc angle et que les angles ne sont pas disponibles, un (1) indique qu’un bloc angle est lu et que des changements d’angle peuvent être effectués.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zéro.

</dd> </dl>

## <a name="remarks"></a>Remarques

Les changements d’angle ne sont pas limités aux blocs d’angle et la détection de la modification d’angle ne peut être vue que dans un bloc angle.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Dvdevcode. h (inclure DShow. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Applications DVD](dvd-applications.md)
</dt> <dt>

[Codes de notification des événements DVD](dvd-notification-codes.md)
</dt> <dt>

[Notification d’événements dans DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




