---
description: Signale que le nombre d’angles disponibles a changé ou que le numéro d’angle actuel a changé.
ms.assetid: 0564b0e3-6434-448b-80fb-5362ab67fef7
title: EC_DVD_ANGLE_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_ANGLE_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 08914e3fcb93d38ccad25053f7c33480e900ad93
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999169"
---
# <a name="ec_dvd_angle_change"></a>\_changement d' \_ angle de DVD EC \_

Signale que le nombre d’angles disponibles a changé ou que le numéro d’angle actuel a changé.

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Valeur **DWORD** indiquant le nombre d’angles disponibles. Lorsque le nombre d’angles disponibles est 1, la vidéo actuelle n’est pas multiangle.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Valeur **DWORD** indiquant le nombre d’angles en cours.

</dd> </dl>

## <a name="remarks"></a>Notes

Les nombres en angle sont compris entre 1 et 9.

Le numéro d’angle actuel peut changer automatiquement à l’aide d’une commande de navigation créée sur le disque, ainsi que via le contrôle d’application à l’aide de l’interface [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) .

Cet événement est déclenché dans tous les domaines.

## <a name="requirements"></a>Spécifications



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

 

 




