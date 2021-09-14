---
title: Message PGM_SETBUTTONSIZE (commctrl. h)
description: Définit la taille actuelle du bouton pour le contrôle de pagineur. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de radiomessagerie \_ SetButtonSize.
ms.assetid: b31960f8-87c2-4209-8213-df75ac883e11
keywords:
- PGM_SETBUTTONSIZE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- PGM_SETBUTTONSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecf8c164ed960675c1a68be36acfe0eff40f972f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127117641"
---
# <a name="pgm_setbuttonsize-message"></a>\_Message SETBUTTONSIZE PGM

Définit la taille actuelle du bouton pour le contrôle de pagineur. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de [**radiomessagerie \_ SetButtonSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbuttonsize) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Valeur de type **int** qui contient la nouvelle taille de bouton, en pixels.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur **int** qui contient la taille de bouton précédente, en pixels.

## <a name="remarks"></a>Notes

Si le contrôle de pagineur a le style [**PG \_ horiment**](pager-control-styles.md) , la taille du bouton détermine la largeur des boutons du pagineur. Si le contrôle de pagineur a le style [**PG \_ vert**](pager-control-styles.md) , la taille du bouton détermine la hauteur des boutons du pagineur. Par défaut, le contrôle pager définit sa taille de bouton sur trois-quarts de la largeur de la barre de défilement.

La taille minimale du bouton du pagineur est actuellement de 12 pixels. Toutefois, cela peut changer par conséquent, vous ne devez pas dépendre de cette valeur.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_GETBUTTONSIZE PGM**](pgm-getbuttonsize.md)
</dt> </dl>

 

 





