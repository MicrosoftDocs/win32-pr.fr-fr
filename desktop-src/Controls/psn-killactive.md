---
title: PSN_KILLACTIVE le code de notification (Prsht. h)
description: Avertit une page qu’il va perdre l’activation soit parce qu’une autre page est activée, soit parce que l’utilisateur a cliqué sur le bouton OK. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 470cd6ff-73ad-451a-a861-4d3324a8a8db
keywords:
- Contrôles Windows de code de notification PSN_KILLACTIVE
topic_type:
- apiref
api_name:
- PSN_KILLACTIVE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ae5f90670c79797ef8576c5e6e3911255ab5fe1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942021"
---
# <a name="psn_killactive-notification-code"></a>\_Code de notification PSN KILLACTIVE

Avertit une page qu’il va perdre l’activation soit parce qu’une autre page est activée, soit parce que l’utilisateur a cliqué sur le bouton OK. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
PSN_KILLACTIVE 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) qui contient des informations sur le code de notification. Cette structure contient une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) en tant que premier membre, **HDR**. Le membre **hwndFrom** de cette structure **NMHDR** contient le handle de la feuille de propriétés. Le membre **lParam** de la structure **PSHNOTIFY** ne contient aucune information.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** pour empêcher la page de perdre l’activation, ou **false** pour l’autoriser.

## <a name="remarks"></a>Notes

Une application gère ce code de notification pour valider les informations entrées par l’utilisateur.

> [!Note]  
> La feuille de propriétés est en cours de manipulation de la liste de pages lorsque le \_ Code de notification PSN KILLACTIVE est envoyé. N’essayez pas d’ajouter, de supprimer ou d’insérer des pages lors de la gestion de ce code de notification. Vous obtiendrez des résultats imprévisibles.

 

Pour définir une valeur de retour, la procédure de la boîte de dialogue de la page doit appeler la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) avec une valeur MSGRESULT de l’DWL \_ définie sur la valeur de retour. La procédure de la boîte de dialogue doit retourner **true**.

Si la procédure de la boîte de dialogue affecte la \_ **valeur true** à DWL MSGRESULT, une boîte de message doit s’afficher pour expliquer le problème à l’utilisateur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

