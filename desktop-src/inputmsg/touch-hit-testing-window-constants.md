---
title: Constantes de la fenêtre test d’atteinte tactile
description: Indique comment les messages pour le test d’atteinte tactile sont traités par les fenêtres qui sont inscrites via la fonction RegisterTouchHitTestingWindow.
ms.assetid: CC6CCD0B-882F-4DA7-B886-D4BD18D6060C
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
ms.date: 02/03/2020
ms.openlocfilehash: ccc26947241d5d777cacee504a066b7e070faf0a8febc39b86571537c14245f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829749"
---
# <a name="touch-hit-testing-window-constants"></a>Constantes de la fenêtre test d’atteinte tactile

Indique comment les messages pour le test d’atteinte tactile sont traités par les fenêtres qui sont inscrites via la fonction [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) .



| Constante/valeur                                                                                                                                                                                                                                                   | Description                                                                                                                            |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TOUCH_HIT_TESTING_DEFAULT"></span><span id="touch_hit_testing_default"></span><dl> <dt>**TOUCH_HIT_TESTING_DEFAULT**</dt> <dt>0 (0x0)</dt> </dl> | [**WM_TOUCHHITTESTING**](wm-touchhittesting.md) messages ne sont pas envoyés à la fenêtre cible, mais sont envoyés aux fenêtres enfants.<br/> |
| <span id="TOUCH_HIT_TESTING_CLIENT"></span><span id="touch_hit_testing_client"></span><dl> <dt>**TOUCH_HIT_TESTING_CLIENT**</dt> <dt>1 (0x1)</dt> </dl>    | [**WM_TOUCHHITTESTING**](wm-touchhittesting.md) messages sont envoyés à la fenêtre cible.<br/>                                   |
| <span id="TOUCH_HIT_TESTING_NONE"></span><span id="touch_hit_testing_none"></span><dl> <dt>**TOUCH_HIT_TESTING_NONE**</dt> <dt>2 (0X2)</dt> </dl>          | [**WM_TOUCHHITTESTING**](wm-touchhittesting.md) messages ne sont pas envoyés à la fenêtre cible ou aux fenêtres enfants.<br/>              |



## <a name="requirements"></a>Configuration requise



| Condition requise | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes](constants.md)
</dt> <dt>

[**POINTER_INFO**](/previous-versions/windows/desktop/api)
</dt> </dl>

 

