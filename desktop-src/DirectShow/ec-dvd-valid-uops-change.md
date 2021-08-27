---
description: Signale que l’ensemble de méthodes d’interface IDvdControl2 disponibles a changé.
ms.assetid: dfe698b9-abe5-44a7-9844-f408f11fd0ce
title: EC_DVD_VALID_UOPS_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_VALID_UOPS_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: fafdbb5443a32a8029ad73d92a2b23c5f05c96d5dfc32375fd05e6d4502484a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051809"
---
# <a name="ec_dvd_valid_uops_change"></a>\_ \_ \_ modification UOPs valide du DVD EC \_

Signale que l’ensemble de méthodes d’interface [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) disponibles a changé.

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Valeur **DWORD** qui contient une combinaison de zéro ou plusieurs indicateurs de l’énumération d' [**\_ \_ indicateur UOP valide**](/windows/win32/api/strmif/ne-strmif-valid_uop_flag) . Les bits indiquent les commandes [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) qui ont été explicitement désactivées par le disque DVD.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zéro.

</dd> </dl>

## <a name="remarks"></a>Remarques

Cet événement indique uniquement les opérations qui sont explicitement désactivées par le contenu sur le disque DVD. Cela ne garantit pas qu’il est valide d’appeler des méthodes qui ne sont pas désactivées. Par exemple, si aucun bouton n’est présent, la méthode [**IDvdControl2 :: ActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activatebutton) ne fonctionnera pas, même si la méthode n’est pas explicitement désactivée.

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

[Notification d’événements dans DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




