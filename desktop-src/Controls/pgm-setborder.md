---
title: Message PGM_SETBORDER (commctrl. h)
description: Définit la taille de bordure actuelle pour le contrôle de pagineur. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de radiomessagerie \_ setBorder.
ms.assetid: 073a1f9e-f05b-4203-9035-8106e87e55cd
keywords:
- PGM_SETBORDER les contrôles de message Windows
topic_type:
- apiref
api_name:
- PGM_SETBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a987246a56da213098ba8632044af97ae51462df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032756"
---
# <a name="pgm_setborder-message"></a>\_Message SETBORDER PGM

Définit la taille de bordure actuelle pour le contrôle de pagineur. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de [**radiomessagerie \_ setBorder**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setborder) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Nouvelle taille de la bordure, en pixels. Cette valeur ne doit pas être supérieure au bouton du pagineur ou inférieure à zéro. Si *lParam* est trop grand, la bordure est dessinée avec la même taille que le bouton. Si *lParam* est négatif, la taille de la bordure sera définie sur zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur INT qui contient la taille de bordure précédente, en pixels.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





