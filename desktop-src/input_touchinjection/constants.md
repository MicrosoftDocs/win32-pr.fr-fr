---
title: Constantes d’injection tactile
description: Cette section fournit les spécifications de référence pour les constantes d’injection tactile.
ms.assetid: 52941DF1-88AF-452B-BF3E-838ADBDBC9B2
topic_type:
- apiref
api_name:
- MAX_TOUCH_COUNT
- TOUCH_FEEDBACK_DEFAULT
- TOUCH_FEEDBACK_INDIRECT
- TOUCH_FEEDBACK_NONE
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/06/2020
ms.openlocfilehash: d86af0d67c48218e8cb3f5909b647ff59d8b0cdddddef24057e02521a7f253ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451739"
---
# <a name="touch-injection-constants"></a>Constantes d’injection tactile

Cette section fournit les spécifications de référence pour les constantes d' [injection tactile](touch-injection-portal.md) .

| Constante/valeur | Description |
|---|---|
| **MAX_TOUCH_COUNT** 256                            | Spécifie le nombre maximal de contacts simultanés.<br/> |
| **TOUCH_FEEDBACK_DEFAULT** 0x1    | Spécifie les visualisations tactiles par défaut.<br/>                |
| **TOUCH_FEEDBACK_INDIRECT** 0X2 | Spécifie des visualisations tactiles indirectes.<br/>               |
| **TOUCH_FEEDBACK_NONE** 0x3             | Ne spécifie aucune visualisation tactile.<br/>                     |

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge | Windows 8 \[ applications de bureau uniquement\]                                           |
| Serveur minimal pris en charge | Windows Server 2012 \[ applications de bureau uniquement\]                                 |
| En-tête                   | Winuser. h |

## <a name="see-also"></a>Voir aussi

[Référence d’injection tactile](touch-injection-reference.md)
