---
title: Message TBM_SETPAGESIZE (commctrl. h)
description: Définit le nombre de positions logiques du curseur de la barre de défilement en réponse à l’entrée au clavier, comme les touches ou, ou l’entrée de la souris, comme les clics dans le canal de la barre de défilement.
ms.assetid: 34edb868-4b6b-4b3f-b315-3ce39346b134
keywords:
- TBM_SETPAGESIZE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TBM_SETPAGESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec5d8a396bb605b4276346e84e7b46bfbefe0657
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116406"
---
# <a name="tbm_setpagesize-message"></a>\_Message TBM SETPAGESIZE

Définit le nombre de positions logiques du curseur de la barre de défilement en réponse à l’entrée au clavier, comme les touches ou, ou l’entrée de la souris, comme les clics dans le canal de la barre de défilement. Les positions logiques sont les incréments de l’entier dans la plage de la plage de la barre de défilement minimale à la position maximale du curseur.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Nouvelle taille de page.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur 32 bits qui spécifie la taille de page précédente.

## <a name="remarks"></a>Notes

La barre de défilement envoie également un message [**WM \_ HSCROLL**](wm-hscroll.md) ou [**WM \_ VSCROLL**](wm-vscroll.md) avec les \_ codes de \_ notification PG. préc et to PageDown à sa fenêtre parente lorsqu’elle reçoit une entrée de clavier ou de souris qui fait défiler la page.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TBM \_ GETPAGESIZE**](tbm-getpagesize.md)
</dt> </dl>

 

 





