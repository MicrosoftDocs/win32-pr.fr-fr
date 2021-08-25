---
title: DL_DROPPED le code de notification (commctrl. h)
description: Signale que l’utilisateur a terminé une opération glisser-déplacer en relâchant le bouton gauche de la souris. Une zone de liste de glissement envoie ce code de notification à sa fenêtre parente sous la forme d’un message de liste de glissement. Pour plus d’informations, consultez faire glisser des messages de zone de liste.
ms.assetid: 81b9b424-2735-407d-bac9-f03ea2f48b4e
keywords:
- DL_DROPPED les contrôles de Windows de code de notification
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
ms.openlocfilehash: 4c245cbb85a4e67845bd86a25b4cccb2f2aa0dc1d9d9613afd1d685037c5e1ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002719"
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

## <a name="remarks"></a>Remarques

Ce code de notification est normalement traité en insérant l’élément déplacé dans la liste devant l’élément sous le curseur. Pour récupérer l’index de l’élément à la position du curseur, utilisez la fonction [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) . Notez que le code de notification de la liste de distribution \_ supprimée est envoyé même si le curseur ne se trouve pas sur un élément de liste. Dans ce cas, **LBItemFromPt** retourne-1.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





