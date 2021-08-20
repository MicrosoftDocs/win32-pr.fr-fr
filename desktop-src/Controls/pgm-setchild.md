---
title: Message PGM_SETCHILD (commctrl. h)
description: Définit la fenêtre contenue pour le contrôle de pagineur.
ms.assetid: 717e6720-aa42-4ecd-9520-4618a04dc28d
keywords:
- PGM_SETCHILD les contrôles de Windows de message
topic_type:
- apiref
api_name:
- PGM_SETCHILD
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da3424eabfb87d587ac8cd33802dfc03b3c3868d881b131360bfee2e8bc26730
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830170"
---
# <a name="pgm_setchild-message"></a>\_Message SETCHILD PGM

Définit la fenêtre contenue pour le contrôle de pagineur. Ce message ne change pas le parent de la fenêtre contenue. Il assigne uniquement un handle de fenêtre au contrôle de pagineur pour le défilement. Dans la plupart des cas, la fenêtre contenue est une fenêtre enfant. Si c’est le cas, la fenêtre contenue doit être un enfant du contrôle pager. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de [**radiomessagerie \_ SetChild**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setchild) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Handle de la fenêtre à contenu.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour n’est pas utilisée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





