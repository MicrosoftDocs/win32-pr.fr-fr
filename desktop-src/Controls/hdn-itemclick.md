---
title: HDN_ITEMCLICK le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle header que l’utilisateur a cliqué sur le contrôle. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 25ed0070-5891-4f36-9ae0-fc04e064401f
keywords:
- HDN_ITEMCLICK les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- HDN_ITEMCLICK
- HDN_ITEMCLICKA
- HDN_ITEMCLICKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca49cd4fd77425f202c5d8ee06cb0b3d7712e610
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999919"
---
# <a name="hdn_itemclick-notification-code"></a>\_Code de notification HDN ITEMCLICK

Avertit la fenêtre parente d’un contrôle header que l’utilisateur a cliqué sur le contrôle. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
HDN_ITEMCLICK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) qui identifie le contrôle d’en-tête et spécifie l’index de l’élément d’en-tête sur lequel l’utilisateur a cliqué et le bouton de la souris utilisé pour cliquer sur l’élément. Le membre **pItem** a la valeur **null**.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Un contrôle header envoie ce code de notification lorsque l’utilisateur relâche le bouton gauche de la souris.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **HDN \_ ITEMCLICKW** (Unicode) et **HDN \_ ITEMCLICKA** (ANSI)<br/>               |



 

 





