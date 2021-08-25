---
title: Message PBM_SETSTEP (commctrl. h)
description: Spécifie l’incrément de l’étape d’une barre de progression. L’incrément d’étape correspond à la quantité d’augmentation de la position actuelle de la barre de progression à chaque fois qu’elle reçoit un \_ message PBM STEPIT. Par défaut, l’incrément de l’étape est défini sur 10.
ms.assetid: 75c1085b-6c7a-4c44-9a12-f9bf21f7d945
keywords:
- PBM_SETSTEP les contrôles de Windows de message
topic_type:
- apiref
api_name:
- PBM_SETSTEP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b88508654565cb3af05dd768ef7ef1e54e5ef0ee80e0797bc45631f6e3fe6912
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119798769"
---
# <a name="pbm_setstep-message"></a>\_Message PBM SETSTEP

Spécifie l’incrément de l’étape d’une barre de progression. L’incrément d’étape correspond à la quantité d’augmentation de la position actuelle de la barre de progression à chaque fois qu’elle reçoit un message [**PBM \_ STEPIT**](pbm-stepit.md) . Par défaut, l’incrément de l’étape est défini sur 10.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Nouvel incrément de l’étape.

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’incrément de l’étape précédente.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





