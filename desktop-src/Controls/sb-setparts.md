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
ms.openlocfilehash: 062058fa3778cd0394cadd9d76b363a0353ffb2e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127117070"
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

## <a name="return-value"></a>Valeur de retour

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





