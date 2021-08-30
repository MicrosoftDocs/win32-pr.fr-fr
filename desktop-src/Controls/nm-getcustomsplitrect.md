---
title: NM_GETCUSTOMSPLITRECT le code de notification (commctrl. h)
description: Envoyé par un contrôle bouton à son parent pour obtenir des mesures pour les deux rectangles du bouton partagé. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: ce72778d-3cca-46a4-9d05-40954a18681d
keywords:
- NM_GETCUSTOMSPLITRECT les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- NM_GETCUSTOMSPLITRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ab55083b830ef3ba8a0e22250d4048134fdda100bf798a8b567c13c8a949e57
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088759"
---
# <a name="nm_getcustomsplitrect-notification-code"></a>\_Code de notification GETCUSTOMSPLITRECT nm

Envoyé par un contrôle bouton à son parent pour obtenir des mesures pour les deux rectangles du bouton partagé. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
NM_GETCUSTOMSPLITRECT
        
    nmCustomSplit = (NMCUSTOMSPLITRECTINFO *) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers un [**NMCUSTOMSPLITRECTINFO**](/windows/win32/api/commctrl/ns-commctrl-nmcustomsplitrectinfo) pour recevoir des informations sur les rectangles englobants. La structure **NMCUSTOMSPLITRECTINFO** est envoyée avec le code de notification sous la forme d’une demande pour que le parent fournisse des mesures pour les rectangles du bouton partagé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retournez [**CDRF \_ SKIPDEFAULT**](cdrf-constants.md) pour indiquer au contrôle Button d’utiliser les valeurs retournées dans la structure [**NMCUSTOMSPLITRECTINFO**](/windows/win32/api/commctrl/ns-commctrl-nmcustomsplitrectinfo) ; sinon, retournez la [**valeur de CDRF \_ par défaut**](cdrf-constants.md).

## <a name="remarks"></a>Remarques

Ce code de notification est envoyé par un contrôle Button avant d’être dessiné. Le bouton doit être de style [**BS \_ SPLITBUTTON**](button-styles.md) ou [**BS \_ DEFSPLITBUTTON**](button-styles.md). Si les rectangles retournés au contrôle dans *lParam* ne sont pas valides, ils sont ignorés.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





