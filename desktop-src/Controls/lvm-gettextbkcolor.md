---
title: Message LVM_GETTEXTBKCOLOR (commctrl. h)
description: Récupère la couleur d’arrière-plan du texte d’un contrôle d’affichage de liste. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView GetTextBkColor.
ms.assetid: 3d2c8be8-d7f9-4aa7-b358-f7effc6dbb25
keywords:
- LVM_GETTEXTBKCOLOR les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_GETTEXTBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88bc7d22766f2d1bed304c5e9780faf05808513312b744ae54bc2d6cfab6dffc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958258"
---
# <a name="lvm_gettextbkcolor-message"></a>\_Message GETTEXTBKCOLOR LVM

Récupère la couleur d’arrière-plan du texte d’un contrôle d’affichage de liste. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ GetTextBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettextbkcolor) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la couleur d’arrière-plan du texte.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





