---
title: Message PGM_SETCHILD (commctrl. h)
description: Définit la fenêtre contenue pour le contrôle de pagineur.
ms.assetid: 717e6720-aa42-4ecd-9520-4618a04dc28d
keywords:
- PGM_SETCHILD les contrôles de message Windows
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
ms.openlocfilehash: 5c934c3c5688ac79b5c5ce67aef68e28ad3627ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103476"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





