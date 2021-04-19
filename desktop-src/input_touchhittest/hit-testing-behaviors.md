---
title: Comportements de test de positionnement tactile
description: Les constantes suivantes sont utilisées par les applications ou les infrastructures d’interface utilisateur pour identifier la façon dont les messages pour le test d’atteinte tactile sont traités par les fenêtres inscrites via la fonction RegisterTouchHitTestingWindow.
ms.assetid: D1ECCBFA-CD01-401E-A42E-4F954F5F0A32
topic_type:
- apiref
api_name:
- TOUCH_HIT_TESTING_DEFAULT
- TOUCH_HIT_TESTING_CLIENT
- TOUCH_HIT_TESTING_NONE
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 9b49f61870c6c7041d73d6fa8d5c078887360359
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510770"
---
# <a name="touch-hit-testing-behaviors"></a>Comportements de test de positionnement tactile

Les constantes suivantes sont utilisées par les applications ou les infrastructures d’interface utilisateur pour identifier la façon dont les messages pour le test d’atteinte tactile sont traités par les fenêtres inscrites via la fonction [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) .

| Constante/valeur | Description |
|---|---|
| **TOUCH_HIT_TESTING_DEFAULT** </dt> <dt>0 (0x0) | Indique que les messages de [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) ne sont pas envoyés à la fenêtre cible, mais sont envoyés aux fenêtres enfants.<br/> |
| **TOUCH_HIT_TESTING_CLIENT** </dt> <dt>1 (0x1)    | Indique que les messages de [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) sont envoyés à la fenêtre cible.<br/>                                   |
| **TOUCH_HIT_TESTING_NONE** </dt> <dt>2 (0X2)          | Indique que les messages de [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) ne sont pas envoyés à la fenêtre cible ou aux fenêtres enfants.<br/>              |

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                            |
| En-tête<br/>                   | <dl> <dt>Winuser. h |

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes](constants.md)
