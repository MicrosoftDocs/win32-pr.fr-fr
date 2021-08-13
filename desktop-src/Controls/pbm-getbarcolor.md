---
title: Message PBM_GETBARCOLOR (commctrl. h)
description: Obtient la couleur de la barre de progression.
ms.assetid: d046f7e4-e21e-4dd9-a7be-2bf820c3c492
keywords:
- PBM_GETBARCOLOR les contrôles de Windows de message
topic_type:
- apiref
api_name:
- PBM_GETBARCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cb42d878840ad05f0854ec7ca9cb50dc1b3be2a55b3b65ddf652d961b6d818b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119312439"
---
# <a name="pbm_getbarcolor-message"></a>\_Message PBM GETBARCOLOR

Obtient la couleur de la barre de progression.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la couleur de la barre de progression.

## <a name="remarks"></a>Remarques

Il s’agit de la couleur définie par le message [**PBM \_ SETBARCOLOR**](pbm-setbarcolor.md) . La valeur par défaut est CLR \_ par défaut, qui est définie dans commctrl. h.

Cette fonction affecte uniquement le mode classique, et non aucun style visuel.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





