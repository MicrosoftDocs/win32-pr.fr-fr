---
title: LVN_GETEMPTYMARKUP le code de notification (commctrl. h)
description: Envoyé par le contrôle List-View à sa fenêtre parente lorsque le contrôle n’a pas d’éléments. Le \_ Code de notification LVN GETEMPTYMARKUP est une demande pour que la fenêtre parente fournisse du texte de balisage. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 5ea74120-f347-493a-af14-6bda5b8f6082
keywords:
- Contrôles Windows de code de notification LVN_GETEMPTYMARKUP
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844477"
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

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** pour définir le texte de balisage dans le contrôle d’affichage de liste, ou **false** dans le cas contraire.

## <a name="remarks"></a>Notes

Le récepteur de notification convertit *lParam* pour récupérer la structure [**NMLVEMPTYMARKUP**](/windows/win32/api/commctrl/ns-commctrl-nmlvemptymarkup) . Le paramètre *wParam* contient l’ID du contrôle qui envoie ce message.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





