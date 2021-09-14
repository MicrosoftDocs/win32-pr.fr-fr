---
title: TBN_DRAGOUT le code de notification (commctrl. h)
description: Envoyé par un contrôle de barre d’outils lorsque l’utilisateur clique sur un bouton, puis déplace le curseur en dehors du bouton. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 3566ad60-9744-494f-bb02-d30b41d06351
keywords:
- TBN_DRAGOUT les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- TBN_DRAGOUT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54fa61ef183b56b882c6ecdcb9d0d59edbf13e80
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116329"
---
# <a name="tbn_dragout-notification-code"></a>\_Code de notification TBN DRAGOUT

Envoyé par un contrôle de barre d’outils lorsque l’utilisateur clique sur un bouton, puis déplace le curseur en dehors du bouton. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
TBN_DRAGOUT

    lpnmtb = (LPNMTOOLBAR) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) qui contient des informations sur ce code de notification. Pour ce code de notification, seuls les membres **HDR** et **iItem** de cette structure sont valides. Le membre **iItem** de cette structure contient l’identificateur de commande du bouton qui est glissé.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La valeur de retour est ignorée.

## <a name="remarks"></a>Notes

Ce code de notification permet à une application d’implémenter la fonctionnalité glisser-déplacer pour les boutons de barre d’outils. Lors du traitement de ce code de notification, l’application commence l’opération de glisser-déplacer.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





