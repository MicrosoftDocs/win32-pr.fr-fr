---
title: DL_DRAGGING le code de notification (commctrl. h)
description: Signale que l’utilisateur a déplacé la souris tout en faisant glisser un élément.
ms.assetid: 87fc4c24-8e88-4e3c-8f54-ecc7f80de5d7
keywords:
- DL_DRAGGING les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- DL_DRAGGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f5c9f3f6cec3ef95745eed88ec0208dff581ada
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127124093"
---
# <a name="dl_dragging-notification-code"></a>DL- \_ glissement du code de notification

Signale que l’utilisateur a déplacé la souris tout en faisant glisser un élément. \_La fonction de glisser-déplacer est également envoyée périodiquement lors du glissement, même si la souris n’est pas déplacée. Une zone de liste de glissement envoie ce code de notification à sa fenêtre parente sous la forme d’un message de liste de glissement. Pour plus d’informations, consultez [faire glisser des messages de zone de liste](about-list-boxes.md).


```C++
DL_DRAGGING

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Identificateur de contrôle de la zone de liste de glissement.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) qui contient la liste de distribution \_ faisant glisser le code de notification, le handle vers la zone de liste de glissement et la position du curseur.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La valeur de retour détermine le type de curseur de la souris que doit définir la liste de glissement. Il peut s’agir de la \_ valeur DL STOPCURSOR, DL \_ COPYCURSOR ou DL \_ MOVECURSOR. Si une autre valeur est retournée, le curseur ne change pas.

## <a name="remarks"></a>Notes

Une procédure de fenêtre traite généralement la LD \_ en faisant glisser le code de notification en déterminant l’élément sous le curseur, puis en dessinant une icône d’insertion. Pour récupérer l’élément sous le curseur, utilisez la fonction [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) , en spécifiant **true** pour le paramètre *bAutoScroll* . Cette option permet de faire défiler régulièrement la zone de liste glisser si le curseur se trouve au-dessus ou au-dessous de sa zone cliente. Pour dessiner l’icône d’insertion, utilisez la fonction [**DrawInsert**](/windows/desktop/api/Commctrl/nf-commctrl-drawinsert) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





