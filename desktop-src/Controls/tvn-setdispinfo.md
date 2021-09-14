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
ms.openlocfilehash: 9b03e60ba7d8e6d7851c62fac030bd252cf957d3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115481"
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

## <a name="return-value"></a>Valeur de retour

La valeur de retour est ignorée.

## <a name="remarks"></a>Notes

Si le membre **pszText** de la structure [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) de l’élément est la \_ valeur de TEXTCALLBACK LPSTR, le contrôle envoie cette notification pour définir le texte de l’élément. Dans ce cas, l’indicateur de texte TVIF est défini pour le membre de **masque** de *lParam* \_ .

Si le membre **IImage** ou **iSelectedImage** de la structure [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) de l’élément est la \_ valeur I IMAGECALLBACK, le contrôle envoie cette notification pour récupérer l’index de l’image d’icône à afficher. Dans ce cas, le membre **Mask** de *lParam* aura l’indicateur TVIF \_ image ou TVIF \_ SELECTEDIMAGE défini.

## <a name="requirements"></a>Spécifications



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

 

 





