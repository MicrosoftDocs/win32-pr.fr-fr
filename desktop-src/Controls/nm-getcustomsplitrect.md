---
title: NM_GETCUSTOMSPLITRECT le code de notification (commctrl. h)
description: Envoyé par un contrôle bouton à son parent pour obtenir des mesures pour les deux rectangles du bouton partagé. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: ce72778d-3cca-46a4-9d05-40954a18681d
keywords:
- Contrôles Windows de code de notification NM_GETCUSTOMSPLITRECT
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
ms.openlocfilehash: 97b839540da7e07069fdf56ed656ed8772d029eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102880"
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

## <a name="remarks"></a>Notes

Ce code de notification est envoyé par un contrôle Button avant d’être dessiné. Le bouton doit être de style [**BS \_ SPLITBUTTON**](button-styles.md) ou [**BS \_ DEFSPLITBUTTON**](button-styles.md). Si les rectangles retournés au contrôle dans *lParam* ne sont pas valides, ils sont ignorés.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





