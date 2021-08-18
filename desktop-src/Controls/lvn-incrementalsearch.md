---
title: LVN_INCREMENTALSEARCH le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle List-View qu’une recherche incrémentielle a démarré. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 34517250-a6ba-490b-b87e-b09048543339
keywords:
- LVN_INCREMENTALSEARCH les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- LVN_INCREMENTALSEARCH
- LVN_INCREMENTALSEARCHA
- LVN_INCREMENTALSEARCHW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ec3207fbb16bca23bf44ac61fee58bb6e4fad1ff74c38d7b56910ed52997f39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826119"
---
# <a name="lvn_incrementalsearch-notification-code"></a>\_Code de notification LVN INCREMENTALSEARCH

Avertit la fenêtre parente d’un contrôle List-View qu’une recherche incrémentielle a démarré. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
LVN_INCREMENTALSEARCH
          
    pnmv = (LPNMLVFINDITEM) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) qui décrit le code de notification. L’appelant est chargé d’allouer cette structure, y compris les structures [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) et [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) contenues. Définissez les membres de la structure **NMHDR** . Le membre de **code** doit être défini sur LVN \_ INCREMENTALSEARCH.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Remarques

Le récepteur de notification convertit *lParam* pour récupérer la structure [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) . Le paramètre *wParam* contient l’ID du contrôle qui envoie ce code de notification.

Ce code de notification donne à une application (ou au destinataire de notifications) la possibilité de personnaliser une recherche incrémentielle. Par exemple, si les éléments de recherche sont numériques, l’application peut effectuer une recherche numérique au lieu d’une recherche de chaîne.

L’application définit le membre **lParam** de la structure [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) contenue dans la structure [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) sur le résultat de la recherche, ou sur une autre valeur définie par l’application pour faire échouer la recherche et indiquer au contrôle comment procéder.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl>   |
| Noms Unicode et ANSI<br/>   | **LVN \_ INCREMENTALSEARCHW** (Unicode) et **LVN \_ INCREMENTALSEARCHA** (ANSI)<br/> |



 

 





