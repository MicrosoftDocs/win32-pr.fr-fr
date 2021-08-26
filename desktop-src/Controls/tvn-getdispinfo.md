---
title: TVN_GETDISPINFO le code de notification (commctrl. h)
description: Demande qu’une fenêtre parente d’un contrôle Tree-View fournisse les informations nécessaires pour afficher ou trier un élément. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 2dfe41d8-1164-481b-ac07-8faba43c562a
keywords:
- TVN_GETDISPINFO les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- TVN_GETDISPINFO
- TVN_GETDISPINFOA
- TVN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59728c816ee3fe7dac46c12d7e62da6c18cfdad8387f03d3861e63792d9c8f66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120059909"
---
# <a name="tvn_getdispinfo-notification-code"></a>\_Code de notification TVN GETDISPINFO

Demande qu’une fenêtre parente d’un contrôle Tree-View fournisse les informations nécessaires pour afficher ou trier un élément. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
TVN_GETDISPINFO 

    lptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) . Le membre de l' **élément** est une structure [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) dont les membres **Mask**, **hitem**, **State** et **lParam** spécifient le type d’informations requis. Vous devez remplir les membres de la structure avec les informations appropriées.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est ignorée.

## <a name="remarks"></a>Remarques

Ce code de notification est envoyé dans les circonstances suivantes :

-   Si le membre **pszText** de la structure [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) de l’élément est la \_ valeur de TEXTCALLBACK LPSTR, le contrôle envoie ce code de notification pour récupérer le texte de l’élément. Dans ce cas, l’indicateur de texte TVIF est défini pour le membre de **masque** de *lParam* \_ .
-   Si le membre **IImage** ou **iSelectedImage** de la structure [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) de l’élément est la \_ valeur I IMAGECALLBACK, le contrôle envoie ce code de notification pour récupérer l’index des icônes d’un élément dans la liste d’images du contrôle. Dans ce cas, si l’élément est sélectionné, l’indicateur TVIF SELECTEDIMAGE est défini pour le membre **Mask** de *lParam* \_ . Si l’élément n’est pas sélectionné, l’indicateur d’image TVIF est défini pour le membre **Mask** de *lParam* \_ .
-   Si le membre **cChildren** de la structure [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) de l’élément est la \_ valeur I CHILDRENCALLBACK, le contrôle envoie ce code de notification pour récupérer une valeur qui indique si l’élément a des éléments enfants. Dans ce cas, le membre **Mask** de *lParam* aura l’indicateur TVIF \_ Children Set.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **TVN \_ GETDISPINFOW** (Unicode) et **TVN \_ GETDISPINFOA** (ANSI)<br/>           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[TVN \_ SETDISPINFO](tvn-setdispinfo.md)
</dt> </dl>

 

 





