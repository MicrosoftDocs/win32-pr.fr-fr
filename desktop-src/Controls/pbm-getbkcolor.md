---
title: Message PBM_GETBKCOLOR (commctrl. h)
description: Obtient la couleur d’arrière-plan de la barre de progression.
ms.assetid: 9526ed78-08d9-468f-831b-72bb7c8c92d1
keywords:
- PBM_GETBKCOLOR les contrôles de Windows de message
topic_type:
- apiref
api_name:
- PBM_GETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1462d864df0440cd0567e6d6b1d04261818bb98ab4a6b5a803272e63abcb8d5d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919519"
---
# <a name="pbm_getbkcolor-message"></a>\_Message PBM GETBKCOLOR

Obtient la couleur d’arrière-plan de la barre de progression.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la couleur d’arrière-plan de la barre de progression.

## <a name="remarks"></a>Remarques

Il s’agit de la couleur définie par le message [**PBM \_ SETBKCOLOR**](pbm-setbkcolor.md) . La valeur par défaut est CLR \_ par défaut, qui est définie dans commctrl. h.

Cette fonction affecte uniquement le mode classique, et non aucun style visuel.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





