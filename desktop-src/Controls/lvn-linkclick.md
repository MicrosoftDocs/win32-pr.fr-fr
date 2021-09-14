---
title: LVN_LINKCLICK le code de notification (commctrl. h)
description: Avertit une fenêtre parente d’un contrôle List-View qu’un lien a été activé sur un lien. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: de8f40d6-b79e-4324-af67-9a3c0915609d
keywords:
- LVN_LINKCLICK les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- LVN_LINKCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd69fb463e71523fcbd4eeb65a6a718d27847c09
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012306"
---
# <a name="lvn_linkclick-notification-code"></a>\_Code de notification LVN LINKCLICK

Avertit une fenêtre parente d’un contrôle List-View qu’un lien a été activé sur un lien. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
LVN_LINKCLICK
        
    pLinkInfo = (NMLVLINK*) lParam;         
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMLVLINK**](/windows/win32/api/commctrl/ns-commctrl-nmlvlink) . L’identificateur du groupe contenant le lien se trouve dans le membre **iSubItem** .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Pas de valeur de retour.

## <a name="remarks"></a>Notes

L’exemple suivant montre comment une application peut répondre à ce code de notification dans son gestionnaire de messages [**WM \_ Notify**](wm-notify.md) . L’exemple bascule l’État réduit du groupe et définit le texte de lien approprié.

``` syntax
case LVN_LINKCLICK:
{
    NMLVLINK* pLinkInfo = (NMLVLINK*)lParam;
    HWND hList = pLinkInfo->hdr.hwndFrom;
    LVGROUP groupInfo;
    groupInfo.cbSize = sizeof(groupInfo);
    groupInfo.mask = LVGF_TASK;
    int groupIndex = pLinkInfo->iSubItem;
    if (ListView_GetGroupState(hList, groupIndex, LVGS_COLLAPSED))
    {
        ListView_SetGroupState(hList, groupIndex, LVGS_COLLAPSED, 0);
        groupInfo.pszTask = L"Hide";
    }
    else
    {
        ListView_SetGroupState(hList, groupIndex, LVGS_COLLAPSED, LVGS_COLLAPSED);
        groupInfo.pszTask = L"Show";
     }
      ListView_SetGroupInfo(hList, groupIndex, &groupInfo);
      break;
}
```

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





