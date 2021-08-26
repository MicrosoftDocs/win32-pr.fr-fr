---
title: DL_BEGINDRAG le code de notification (commctrl. h)
description: Avertit la fenêtre parente de la zone de liste de glissement que l’utilisateur a cliqué avec le bouton gauche de la souris sur un élément. Une zone de liste de glissement envoie ce code de notification sous la forme d’un message de liste de glissement. Pour plus d’informations, consultez faire glisser des messages de zone de liste.
ms.assetid: ccf66818-e5f7-4165-8d0d-4d279944f70e
keywords:
- DL_BEGINDRAG les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- DL_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e2c843398b21ad51df51ae706a515c2e6f9831b89d32092b87148598b4bed5f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119968329"
---
# <a name="dl_begindrag-notification-code"></a>\_Code de notification DL BEGINDRAG

Avertit la fenêtre parente de la zone de liste de glissement que l’utilisateur a cliqué avec le bouton gauche de la souris sur un élément. Une zone de liste de glissement envoie ce code de notification sous la forme d’un message de liste de glissement. Pour plus d’informations, consultez [faire glisser des messages de zone de liste](about-list-boxes.md).


```C++
DL_BEGINDRAG

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) qui contient le code de \_ notification DL BEGINDRAG, le handle de la zone de liste de glissement et la position du curseur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne **true** pour commencer l’opération glisser ou **false** pour empêcher l’opération glisser.

## <a name="remarks"></a>Remarques

Lors du traitement de ce code de notification, une procédure de fenêtre détermine généralement l’élément de liste à la position de curseur spécifiée à l’aide de la fonction [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) . Elle retourne ensuite **true** ou **false**, selon que l’élément doit ou non être glissé. Avant de retourner **true**, la procédure de fenêtre doit enregistrer l’index de l’élément de liste afin que l’application sache quel élément déplacer ou copier lorsque l’opération glisser est terminée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





