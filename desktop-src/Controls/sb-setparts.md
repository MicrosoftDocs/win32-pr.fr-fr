---
title: Message SB_SETPARTS (commctrl. h)
description: Définit le nombre de parties dans une fenêtre d’État et la coordonnée du bord droit de chaque partie.
ms.assetid: e29e8b09-c018-4ea4-8b47-6f3713113427
keywords:
- SB_SETPARTS les contrôles de message Windows
topic_type:
- apiref
api_name:
- SB_SETPARTS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 062058fa3778cd0394cadd9d76b363a0353ffb2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509014"
---
# <a name="sb_setparts-message"></a>\_Message SB SETPARTS

Définit le nombre de parties dans une fenêtre d’État et la coordonnée du bord droit de chaque partie.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Nombre de parties à définir (ne peut pas être supérieur à 256).

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers un tableau d’entiers. Le nombre d’éléments est spécifié dans *wParam*. Chaque élément spécifie la position, dans les coordonnées clientes, du bord droit de la partie correspondante. Si un élément est-1, le bord droit de la partie correspondante s’étend jusqu’à la bordure de la fenêtre.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





