---
title: LVN_GETEMPTYMARKUP le code de notification (commctrl. h)
description: Envoyé par le contrôle List-View à sa fenêtre parente lorsque le contrôle n’a pas d’éléments. Le \_ Code de notification LVN GETEMPTYMARKUP est une demande pour que la fenêtre parente fournisse du texte de balisage. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 5ea74120-f347-493a-af14-6bda5b8f6082
keywords:
- LVN_GETEMPTYMARKUP les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- LVN_GETEMPTYMARKUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dea693475ca42f962be07936f980cd3f5d52479c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012314"
---
# <a name="lvn_getemptymarkup-notification-code"></a>\_Code de notification LVN GETEMPTYMARKUP

Envoyé par le contrôle List-View à sa fenêtre parente lorsque le contrôle n’a pas d’éléments. Le \_ Code de notification LVN GETEMPTYMARKUP est une demande pour que la fenêtre parente fournisse du texte de balisage. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
LVN_GETEMPTYMARKUP
        
    pnmMarkup = (NMLVEMPTYMARKUP*) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMLVEMPTYMARKUP**](/windows/win32/api/commctrl/ns-commctrl-nmlvemptymarkup) . Définissez les membres de cette structure pour fournir le texte de balisage pour le contrôle de vue de liste.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la **valeur true** pour définir le texte de balisage dans le contrôle d’affichage de liste, ou **false** dans le cas contraire.

## <a name="remarks"></a>Notes

Le récepteur de notification convertit *lParam* pour récupérer la structure [**NMLVEMPTYMARKUP**](/windows/win32/api/commctrl/ns-commctrl-nmlvemptymarkup) . Le paramètre *wParam* contient l’ID du contrôle qui envoie ce message.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





