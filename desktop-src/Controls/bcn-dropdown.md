---
title: BCN_DROPDOWN le code de notification (winuser. h)
description: Envoyé lorsque l’utilisateur clique sur une flèche de déroulement sur un bouton. La fenêtre parente du contrôle reçoit ce code de notification sous la forme d’un \_ message WM Notify.
ms.assetid: 61503b8d-193e-4855-b9eb-35c0dc636c02
keywords:
- BCN_DROPDOWN les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- BCN_DROPDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e78512419f62beaa82aff42ccaf951d34130fe3a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126920383"
---
# <a name="bcn_dropdown-notification-code"></a>\_Code de notification de liste déroulante BCN

Envoyé lorsque l’utilisateur clique sur une flèche de déroulement sur un bouton. La fenêtre parente du contrôle reçoit ce code de notification sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
BCN_DROPDOWN
        
    pnmdropdown = (NMBCDROPDOWN*) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMBCDROPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmbcdropdown) . Le membre **rcButton** est défini pour décrire la zone de liste déroulante.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Le récepteur de notification convertit **lParam** pour récupérer la structure [**NMBCDROPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmbcdropdown) . **WParam** contient l’ID du contrôle qui envoie ce message. Le contrôle Button doit avoir un style de bouton déroulant.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



 

 





