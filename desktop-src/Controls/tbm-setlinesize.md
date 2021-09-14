---
title: Message TBM_SETLINESIZE (commctrl. h)
description: Définit le nombre de positions logiques du curseur de la barre de défilement en réponse à une entrée au clavier à partir des touches de direction, telles que les touches ou. Les positions logiques sont les incréments de l’entier dans la plage de la plage de la barre de défilement minimale à la position maximale du curseur.
ms.assetid: 7fe3f9b8-2ddf-4460-882f-6be439f83daa
keywords:
- TBM_SETLINESIZE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TBM_SETLINESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec898ed09b20f15023ef04a399f5644df746e495
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116413"
---
# <a name="tbm_setlinesize-message"></a>\_Message TBM SETLINESIZE

Définit le nombre de positions logiques du curseur de la barre de défilement en réponse à une entrée au clavier à partir des touches de direction, telles que les touches ou. Les positions logiques sont les incréments de l’entier dans la plage de la plage de la barre de défilement minimale à la position maximale du curseur.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Nouvelle taille de ligne.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur 32 bits qui spécifie la taille de ligne précédente.

## <a name="remarks"></a>Notes

La valeur par défaut de la taille de ligne est 1.

Le TrackBar envoie également un message [**WM \_ HSCROLL**](wm-hscroll.md) ou [**WM \_ VSCROLL**](wm-vscroll.md) avec les \_ codes de notification de la programmation to et de to \_ LINEDOWN à sa fenêtre parente quand l’utilisateur appuie sur les touches de direction.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TBM \_ GETLINESIZE**](tbm-getlinesize.md)
</dt> </dl>

 

 





