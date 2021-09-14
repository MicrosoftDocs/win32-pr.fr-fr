---
title: Message TBM_GETPAGESIZE (commctrl. h)
description: Récupère le nombre de positions logiques du curseur de la barre de défilement en réponse à l’entrée au clavier, comme les touches ou, ou l’entrée de la souris, comme les clics dans le canal de la barre de défilement.
ms.assetid: f0c5feac-2723-440e-96c0-dac37b0531ed
keywords:
- TBM_GETPAGESIZE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TBM_GETPAGESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac58c0b935b468cf8af565fba2db67c88418ee4f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116466"
---
# <a name="tbm_getpagesize-message"></a>\_Message TBM GETPAGESIZE

Récupère le nombre de positions logiques du curseur de la barre de défilement en réponse à l’entrée au clavier, comme les touches ou, ou l’entrée de la souris, comme les clics dans le canal de la barre de défilement. Les positions logiques sont les incréments de l’entier dans la plage de la plage de la barre de défilement minimale à la position maximale du curseur.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur 32 bits qui spécifie la taille de page du TrackBar.

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

[**TBM \_ SETPAGESIZE**](tbm-setpagesize.md)
</dt> </dl>

 

 





