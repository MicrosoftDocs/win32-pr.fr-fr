---
title: DL_CANCELDRAG le code de notification (commctrl. h)
description: Signale que l’utilisateur a annulé une opération glisser en cliquant sur le bouton droit de la souris ou en appuyant sur la touche ÉCHAP.
ms.assetid: 62c1377f-41b6-449f-a95e-2689dc1913c6
keywords:
- Contrôles Windows de code de notification DL_CANCELDRAG
topic_type:
- apiref
api_name:
- DL_CANCELDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab10f7c31184c44fabdffd4f611847e550b62cc7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106690"
---
# <a name="dl_canceldrag-notification-code"></a>\_Code de notification DL CANCELDRAG

Signale que l’utilisateur a annulé une opération glisser en cliquant sur le bouton droit de la souris ou en appuyant sur la touche ÉCHAP. Une zone de liste de glissement envoie ce code de notification à sa fenêtre parente sous la forme d’un message de liste de glissement. Pour plus d’informations, consultez [faire glisser des messages de zone de liste](about-list-boxes.md).


```C++
DL_CANCELDRAG

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) qui contient le code de \_ notification DL CANCELDRAG, le handle de la zone de liste de glissement et la position du curseur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

En traitant le \_ Code de notification DL CANCELDRAG, une application peut réinitialiser son état interne pour indiquer que le glissement n’est pas appliqué.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





