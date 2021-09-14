---
title: TBN_QUERYINSERT le code de notification (commctrl. h)
description: Avertit la fenêtre parente de la barre d’outils qu’un bouton peut être inséré à gauche du bouton spécifié pendant que l’utilisateur personnalise une barre d’outils. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: d389fabb-16f6-43aa-a4b6-abb80723345b
keywords:
- TBN_QUERYINSERT les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- TBN_QUERYINSERT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1a21e9ade8f54ffe27ebffdfc2a8b535b4b3630
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116274"
---
# <a name="tbn_queryinsert-notification-code"></a>\_Code de notification TBN QUERYINSERT

Avertit la fenêtre parente de la barre d’outils qu’un bouton peut être inséré à gauche du bouton spécifié pendant que l’utilisateur personnalise une barre d’outils. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
TBN_QUERYINSERT 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) . Le membre **iItem** contient l’index de base zéro du bouton à insérer.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne **true** pour autoriser l’insertion d’un bouton devant le bouton donné, ou **false** pour empêcher l’insertion du bouton.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





