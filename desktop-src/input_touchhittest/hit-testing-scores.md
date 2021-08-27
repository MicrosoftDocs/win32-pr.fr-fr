---
title: Scores de test d’atteinte tactile
description: Les constantes suivantes identifient les scores de test de positionnement possibles pour un objet, par rapport aux autres objets qui croisent la zone de contact tactile.
ms.assetid: EACDE6DB-ADBD-4F0C-8C31-7321AB6A73EA
topic_type:
- apiref
api_name:
- TOUCH_HIT_TESTING_PROXIMITY_CLOSEST
- TOUCH_HIT_TESTING_PROXIMITY_FARTHEST
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 18b321272637f4e6931bdc9115e64f8b0553e90e94d8013147ca7a577bad1eb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118758011"
---
# <a name="touch-hit-testing-scores"></a>Scores de test d’atteinte tactile

Les constantes suivantes identifient les scores de test de positionnement possibles pour un objet, par rapport aux autres objets qui croisent la zone de contact tactile.

| Constante/valeur | Description |
|---|---|
| **TOUCH_HIT_TESTING_PROXIMITY_CLOSEST** 0x0      | L’objet est la cible la plus probable.<br/>  |
| **TOUCH_HIT_TESTING_PROXIMITY_FARTHEST** 0xFFF | L’objet est la cible la moins probable.<br/> |

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                            |
| En-tête<br/>                   | Winuser. h |
