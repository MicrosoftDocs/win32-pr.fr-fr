---
title: Message PGM_SETPOS (commctrl. h)
description: Définit la position de défilement actuelle pour le contrôle de pagineur. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de radiomessagerie \_ SetPos.
ms.assetid: b882ea2d-9dab-4d36-9201-29522141f779
keywords:
- PGM_SETPOS les contrôles de message Windows
topic_type:
- apiref
api_name:
- PGM_SETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5af4497e97a8263fa9ec8e454d367bb57e830c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741221"
---
# <a name="pgm_setpos-message"></a>\_Message SetPos PGM

Définit la position de défilement actuelle pour le contrôle de pagineur. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de [**radiomessagerie \_ SetPos**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setpos) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Valeur de type **int** qui contient la nouvelle position de défilement, en pixels.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour n’est pas utilisée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





