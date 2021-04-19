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
ms.openlocfilehash: 76a763a7153bbb9aa67254ffeb5e994a55426e43
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106537936"
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
| Client minimal pris en charge | Applications de \[ Bureau Windows 8 uniquement\]                                           |
| Serveur minimal pris en charge | Applications de bureau Windows Server 2012 \[ uniquement\]                                 |
| En-tête                   | Winuser. h |

## <a name="see-also"></a>Voir aussi

[Référence d’injection tactile](touch-injection-reference.md)
