---
title: Message PBM_STEPIT (commctrl. h)
description: Avance la position actuelle d’une barre de progression à l’aide de l’incrément de l’étape et redessine la barre pour refléter la nouvelle position. Une application définit l’incrément d’étape en envoyant le \_ message PBM SETSTEP.
ms.assetid: fd9947f6-7a48-4207-b691-b7db78eb8a85
keywords:
- PBM_STEPIT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- PBM_STEPIT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa0d4aee387e8f929aaaaf19d947422b95ca9528
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127117682"
---
# <a name="pbm_stepit-message"></a>\_Message PBM STEPIT

Avance la position actuelle d’une barre de progression à l’aide de l’incrément de l’étape et redessine la barre pour refléter la nouvelle position. Une application définit l’incrément d’étape en envoyant le message [**PBM \_ SETSTEP**](pbm-setstep.md) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la position précédente.

## <a name="remarks"></a>Notes

Lorsque la position dépasse la valeur de plage maximale, ce message réinitialise la position actuelle afin que l’indicateur de progression recommence à partir du début.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





