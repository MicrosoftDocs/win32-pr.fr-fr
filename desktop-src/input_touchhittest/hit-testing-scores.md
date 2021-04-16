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
ms.openlocfilehash: f6590e7d56c1c9d92f0ff20524b6e4222d8655b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508469"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                            |
| En-tête<br/>                   | Winuser. h |
