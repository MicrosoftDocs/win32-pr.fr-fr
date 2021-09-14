---
title: HDN_ENDDRAG le code de notification (commctrl. h)
description: Envoyé par un contrôle header lorsqu’une opération glisser est terminée sur l’un de ses éléments. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify. Seuls les contrôles d’en-tête définis sur le \_ style HDS DRAGDROP envoient ce code de notification.
ms.assetid: a28df985-73f1-4fc7-a1db-81a86a131c06
keywords:
- HDN_ENDDRAG les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- HDN_ENDDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eef628dd8ff748829542ace76642e20ad97786f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999937"
---
# <a name="hdn_enddrag-notification-code"></a>\_Code de notification HDN ENDDRAG

Envoyé par un contrôle header lorsqu’une opération glisser est terminée sur l’un de ses éléments. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) . Seuls les contrôles d’en-tête définis sur le style [**HDS \_ DRAGDROP**](header-control-styles.md) envoient ce code de notification.


```C++
HDN_ENDDRAG

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) contenant des informations sur l’élément d’en-tête qui a été glissé.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Pour permettre au contrôle de placer et de réorganiser automatiquement l’élément, retournez **false**. Pour empêcher l’élément d’être placé, retournez la **valeur true**.

## <a name="remarks"></a>Notes

Si le propriétaire effectue une gestion par glisser-déplacer externe (manuelle), il doit retourner la **valeur false**. Le propriétaire doit ensuite réorganiser manuellement les éléments d’en-tête en envoyant [**HDM \_ SETITEM**](hdm-setitem.md) ou [**HDM \_ SETORDERARRAY**](hdm-setorderarray.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





