---
title: PSN_RESET le code de notification (Prsht. h)
description: Avertit une page que la feuille de propriétés va être détruite. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 75448852-8a5e-41a7-92b6-00692e771a06
keywords:
- PSN_RESET les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- PSN_RESET
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb9f14b037d8757469497e644d870a887e6db36172b171f31b00d5615ff39532
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118409810"
---
# <a name="psn_reset-notification-code"></a>\_Code de notification de réinitialisation PSN

Avertit une page que la feuille de propriétés va être détruite. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
PSN_RESET 

    lppsn = (LPPSHNOTIFY) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) qui contient des informations sur le code de notification.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Remarques

Toutes les modifications apportées depuis le dernier code de notification d' [ \_ application PSN](psn-apply.md) sont annulées, sauf dans le cas de [**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2), qui ne prend pas en charge ce code de notification.

Le membre **lParam** de la structure [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) vers laquelle pointe *lParam* prend la valeur **true** si l’utilisateur a cliqué sur le bouton **X** dans l’angle supérieur droit de la feuille de propriétés. La valeur est **false** si l’utilisateur a cliqué sur le bouton **Annuler** . La structure **PSHNOTIFY** contient une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) en tant que premier membre, **HDR**. Le membre **hwndFrom** de cette structure **NMHDR** contient le handle de la feuille de propriétés.

Une application peut utiliser ce code de notification comme opportunité d’effectuer des opérations de nettoyage.

> [!Note]  
> La feuille de propriétés est en cours de manipulation de la liste de pages lorsque le \_ Code de notification de réinitialisation PSN est envoyé. N’essayez pas d’ajouter, de supprimer ou d’insérer des pages lors de la gestion de ce code de notification. Vous obtiendrez des résultats imprévisibles.

 

N’appelez pas la fonction [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) lors du traitement de ce code de notification.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

