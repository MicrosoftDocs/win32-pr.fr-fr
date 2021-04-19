---
title: LVN_INCREMENTALSEARCH le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle List-View qu’une recherche incrémentielle a démarré. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 34517250-a6ba-490b-b87e-b09048543339
keywords:
- Contrôles Windows de code de notification LVN_INCREMENTALSEARCH
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
ms.openlocfilehash: e4784ed8f2a9df664b203f776dc1102702d2861e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513239"
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

## <a name="remarks"></a>Notes

Le récepteur de notification convertit *lParam* pour récupérer la structure [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) . Le paramètre *wParam* contient l’ID du contrôle qui envoie ce code de notification.

Ce code de notification donne à une application (ou au destinataire de notifications) la possibilité de personnaliser une recherche incrémentielle. Par exemple, si les éléments de recherche sont numériques, l’application peut effectuer une recherche numérique au lieu d’une recherche de chaîne.

L’application définit le membre **lParam** de la structure [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) contenue dans la structure [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) sur le résultat de la recherche, ou sur une autre valeur définie par l’application pour faire échouer la recherche et indiquer au contrôle comment procéder.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl>   |
| Noms Unicode et ANSI<br/>   | **LVN \_ INCREMENTALSEARCHW** (Unicode) et **LVN \_ INCREMENTALSEARCHA** (ANSI)<br/> |



 

 





