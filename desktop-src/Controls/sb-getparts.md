---
title: Message SB_GETPARTS (commctrl. h)
description: Récupère le nombre de parties dans une fenêtre d’État. Le message récupère également la coordonnée du bord droit du nombre spécifié de parties.
ms.assetid: 2535f490-4d6b-468a-b13c-096941e61bf4
keywords:
- SB_GETPARTS les contrôles de message Windows
topic_type:
- apiref
api_name:
- SB_GETPARTS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cee0f33331c579490cf66a38b9ce6655215ae673
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509021"
---
# <a name="sb_getparts-message"></a>\_Message SB GETPARTS

Récupère le nombre de parties dans une fenêtre d’État. Le message récupère également la coordonnée du bord droit du nombre spécifié de parties.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Nombre de parties pour lesquelles récupérer les coordonnées. Si ce paramètre est supérieur au nombre de parties dans la fenêtre, le message récupère les coordonnées des parties existantes uniquement.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers un tableau d’entiers qui a le même nombre d’éléments que les éléments spécifiés par *wParam*. Chaque élément du tableau reçoit la coordonnée cliente du bord droit du composant correspondant. Si un élément a la valeur-1, la position du bord droit de cette partie s’étend jusqu’au bord droit de la fenêtre. Pour récupérer le nombre actuel de parties, définissez ce paramètre sur zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le nombre de parties dans la fenêtre.

## <a name="remarks"></a>Notes

Ce message retourne toujours le nombre de parties dans la barre d’État.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





