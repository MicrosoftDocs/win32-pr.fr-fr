---
title: DL_DROPPED le code de notification (commctrl. h)
description: Signale que l’utilisateur a terminé une opération glisser-déplacer en relâchant le bouton gauche de la souris. Une zone de liste de glissement envoie ce code de notification à sa fenêtre parente sous la forme d’un message de liste de glissement. Pour plus d’informations, consultez faire glisser des messages de zone de liste.
ms.assetid: 81b9b424-2735-407d-bac9-f03ea2f48b4e
keywords:
- Contrôles Windows de code de notification DL_DROPPED
topic_type:
- apiref
api_name:
- DL_DROPPED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1b2480360ea38a00c4dd8efe6eb84eed8999890
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844497"
---
# <a name="dl_dropped-notification-code"></a>Code de notification de DL \_ supprimé

Signale que l’utilisateur a terminé une opération glisser-déplacer en relâchant le bouton gauche de la souris. Une zone de liste de glissement envoie ce code de notification à sa fenêtre parente sous la forme d’un message de liste de glissement. Pour plus d’informations, consultez [faire glisser des messages de zone de liste](about-list-boxes.md).


```C++
DL_DROPPED

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) qui contient le code de \_ notification supprimé DL, le handle de la zone de liste de glissement et la position du curseur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Ce code de notification est normalement traité en insérant l’élément déplacé dans la liste devant l’élément sous le curseur. Pour récupérer l’index de l’élément à la position du curseur, utilisez la fonction [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) . Notez que le code de notification de la liste de distribution \_ supprimée est envoyé même si le curseur ne se trouve pas sur un élément de liste. Dans ce cas, **LBItemFromPt** retourne-1.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





