---
title: Message SB_SETPARTS (commctrl. h)
description: Définit le nombre de parties dans une fenêtre d’État et la coordonnée du bord droit de chaque partie.
ms.assetid: e29e8b09-c018-4ea4-8b47-6f3713113427
keywords:
- SB_SETPARTS les contrôles de Windows de message
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
ms.openlocfilehash: a63694ba40eb77cd887454b634ba8cdd2bff2c6ee7bb75beb9a7230eb3d1e1d0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637029"
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
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





