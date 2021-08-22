---
title: TVN_SETDISPINFO le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle Tree-View qu’elle doit mettre à jour les informations qu’elle gère à propos d’un élément. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 40fa61bc-c043-4001-ada9-b627d68bd737
keywords:
- TVN_SETDISPINFO les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- TVN_SETDISPINFO
- TVN_SETDISPINFOA
- TVN_SETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e88a9b5fed4260fa88f5f40431113456950d99985ad2f2e0e97c2e951dce96bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957768"
---
# <a name="tvn_setdispinfo-notification-code"></a>\_Code de notification TVN SETDISPINFO

Avertit la fenêtre parente d’un contrôle Tree-View qu’elle doit mettre à jour les informations qu’elle gère à propos d’un élément. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
TVN_SETDISPINFO 

    lptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) qui décrit l’élément en cours de mise à jour. Le membre **hitem** de la structure [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) spécifie l’élément en cours de mise à jour et le membre **Mask** spécifie les attributs de l’élément à mettre à jour.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est ignorée.

## <a name="remarks"></a>Remarques

Si le membre **pszText** de la structure [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) de l’élément est la \_ valeur de TEXTCALLBACK LPSTR, le contrôle envoie cette notification pour définir le texte de l’élément. Dans ce cas, l’indicateur de texte TVIF est défini pour le membre de **masque** de *lParam* \_ .

Si le membre **IImage** ou **iSelectedImage** de la structure [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) de l’élément est la \_ valeur I IMAGECALLBACK, le contrôle envoie cette notification pour récupérer l’index de l’image d’icône à afficher. Dans ce cas, le membre **Mask** de *lParam* aura l’indicateur TVIF \_ image ou TVIF \_ SELECTEDIMAGE défini.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **TVN \_ SETDISPINFOW** (Unicode) et **TVN \_ SETDISPINFOA** (ANSI)<br/>           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema)
</dt> <dt>

[**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa)
</dt> <dt>

[TVN \_ GETDISPINFO](tvn-getdispinfo.md)
</dt> </dl>

 

 





