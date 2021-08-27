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
ms.openlocfilehash: 3b120ed4bd6b7090621e09dd24b9e6a23b037fb5aed83e7ac6fc43254393330e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046789"
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

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **int** qui contient la taille de bouton précédente, en pixels.

## <a name="remarks"></a>Remarques

Si le contrôle de pagineur a le style [**PG \_ horiment**](pager-control-styles.md) , la taille du bouton détermine la largeur des boutons du pagineur. Si le contrôle de pagineur a le style [**PG \_ vert**](pager-control-styles.md) , la taille du bouton détermine la hauteur des boutons du pagineur. Par défaut, le contrôle pager définit sa taille de bouton sur trois-quarts de la largeur de la barre de défilement.

La taille minimale du bouton du pagineur est actuellement de 12 pixels. Toutefois, cela peut changer par conséquent, vous ne devez pas dépendre de cette valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_GETBUTTONSIZE PGM**](pgm-getbuttonsize.md)
</dt> </dl>

 

 





