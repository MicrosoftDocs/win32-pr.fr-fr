---
title: PSN_QUERYCANCEL le code de notification (Prsht. h)
description: Indique que l’utilisateur a annulé la feuille de propriétés. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 4a789e08-065a-485c-87e3-f7958e2dc544
keywords:
- PSN_QUERYCANCEL les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- PSN_QUERYCANCEL
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bff5ed6203d255a18c40044febb2f7afd9ab42e15c5a9d8ae9fa1a1a56518693
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119798619"
---
# <a name="psn_querycancel-notification-code"></a>\_Code de notification PSN QUERYCANCEL

Indique que l’utilisateur a annulé la feuille de propriétés. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
PSN_QUERYCANCEL 

    lppsn = (LPPSHNOTIFY) lParam;  
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) qui contient des informations sur le code de notification. Cette structure contient une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) en tant que premier membre, **HDR**. Le membre **hwndFrom** de cette structure **NMHDR** contient le handle de la feuille de propriétés. Le membre **lParam** de la structure **PSHNOTIFY** ne contient aucune information.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** pour empêcher l’opération d’annulation, ou **false** pour l’autoriser.

## <a name="remarks"></a>Remarques

Ce code de notification est généralement envoyé lorsqu’un utilisateur clique sur le bouton **Annuler** . Elle est également envoyée lorsqu’un utilisateur clique sur le bouton **X** dans l’angle supérieur droit de la feuille de propriétés ou appuie sur la touche ÉCHAP. Une page de feuille de propriétés peut gérer ce code de notification pour demander à l’utilisateur de vérifier l’opération d’annulation.

Pour définir une valeur de retour, la procédure de la boîte de dialogue de la page doit appeler la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) avec la valeur de retour de la fonction \_ MSGRESULT. La procédure de la boîte de dialogue doit retourner **true**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

