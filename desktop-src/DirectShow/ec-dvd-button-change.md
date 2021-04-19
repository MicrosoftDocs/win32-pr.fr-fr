---
description: Signale que le nombre de boutons de menu DVD a changé ou que la sélection du bouton a été modifiée.
ms.assetid: af6c841d-ca06-4535-b418-14409fa78c81
title: EC_DVD_BUTTON_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_BUTTON_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 8647c1100e5cca6897e2068b2a20119a8f047396
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540607"
---
# <a name="ec_dvd_button_change"></a>\_changement du \_ bouton \_ DVD EC

Signale que le nombre de boutons de menu DVD a changé ou que la sélection du bouton a été modifiée.

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Valeur **DWORD** indiquant le nombre de boutons disponibles.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Valeur **DWORD** indiquant le numéro de bouton actuellement sélectionné. Le numéro de bouton sélectionné zéro signifie qu’aucun bouton n’est sélectionné.

</dd> </dl>

## <a name="remarks"></a>Notes

Les numéros de bouton vont de 1 à 36.

Le bouton actuellement sélectionné peut changer automatiquement à l’aide d’une commande de navigation créée sur le disque, ainsi que via le contrôle d’application à l’aide de l’interface [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) .

Cet événement peut signaler n’importe quel numéro de bouton disponible. Ces nombres ne correspondent pas toujours aux numéros de bouton utilisés pour [**IDvdControl2 :: SelectAndActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectandactivatebutton) , car cette méthode ne peut activer qu’un sous-ensemble de boutons.

Cet événement est déclenché dans tous les domaines.

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

[Notification d’événement dans DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




