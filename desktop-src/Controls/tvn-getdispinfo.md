---
title: TVN_GETDISPINFO le code de notification (commctrl. h)
description: Demande qu’une fenêtre parente d’un contrôle Tree-View fournisse les informations nécessaires pour afficher ou trier un élément. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 2dfe41d8-1164-481b-ac07-8faba43c562a
keywords:
- Contrôles Windows de code de notification TVN_GETDISPINFO
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
ms.openlocfilehash: 2a09bcc683ba9cf2d89a796e63812381254588a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508609"
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

## <a name="remarks"></a>Notes

Ce code de notification est envoyé dans les circonstances suivantes :

-   Si le membre **pszText** de la structure [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) de l’élément est la \_ valeur de TEXTCALLBACK LPSTR, le contrôle envoie ce code de notification pour récupérer le texte de l’élément. Dans ce cas, l’indicateur de texte TVIF est défini pour le membre de **masque** de *lParam* \_ .
-   Si le membre **IImage** ou **iSelectedImage** de la structure [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) de l’élément est la \_ valeur I IMAGECALLBACK, le contrôle envoie ce code de notification pour récupérer l’index des icônes d’un élément dans la liste d’images du contrôle. Dans ce cas, si l’élément est sélectionné, l’indicateur TVIF SELECTEDIMAGE est défini pour le membre **Mask** de *lParam* \_ . Si l’élément n’est pas sélectionné, l’indicateur d’image TVIF est défini pour le membre **Mask** de *lParam* \_ .
-   Si le membre **cChildren** de la structure [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) de l’élément est la \_ valeur I CHILDRENCALLBACK, le contrôle envoie ce code de notification pour récupérer une valeur qui indique si l’élément a des éléments enfants. Dans ce cas, le membre **Mask** de *lParam* aura l’indicateur TVIF \_ Children Set.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **TVN \_ GETDISPINFOW** (Unicode) et **TVN \_ GETDISPINFOA** (ANSI)<br/>           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[TVN \_ SETDISPINFO](tvn-setdispinfo.md)
</dt> </dl>

 

 





