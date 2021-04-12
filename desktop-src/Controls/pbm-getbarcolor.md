---
title: Message PBM_GETBARCOLOR (commctrl. h)
description: Obtient la couleur de la barre de progression.
ms.assetid: d046f7e4-e21e-4dd9-a7be-2bf820c3c492
keywords:
- PBM_GETBARCOLOR les contrôles de message Windows
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
ms.openlocfilehash: 35586d3483d1d487f740a1a3d991c884c814f452
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104800"
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

## <a name="remarks"></a>Notes

Il s’agit de la couleur définie par le message [**PBM \_ SETBARCOLOR**](pbm-setbarcolor.md) . La valeur par défaut est CLR \_ par défaut, qui est définie dans commctrl. h.

Cette fonction affecte uniquement le mode classique, et non aucun style visuel.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





