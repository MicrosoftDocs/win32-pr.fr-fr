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
ms.openlocfilehash: 46d577e03eaf918e4f2ea40aae30a2ab5112b630
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385032"
---
# <a name="touch-hit-testing-window-constants"></a>Constantes de la fenêtre test d’atteinte tactile

Indique comment les messages pour le test d’atteinte tactile sont traités par les fenêtres qui sont inscrites via la fonction [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) .



| Constante/valeur                                                                                                                                                                                                                                                   | Description                                                                                                                            |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TOUCH_HIT_TESTING_DEFAULT"></span><span id="touch_hit_testing_default"></span><dl> <dt>**TOUCH_HIT_TESTING_DEFAULT**</dt> <dt>0 (0x0)</dt> </dl> | [**WM_TOUCHHITTESTING**](wm-touchhittesting.md) messages ne sont pas envoyés à la fenêtre cible, mais sont envoyés aux fenêtres enfants.<br/> |
| <span id="TOUCH_HIT_TESTING_CLIENT"></span><span id="touch_hit_testing_client"></span><dl> <dt>**TOUCH_HIT_TESTING_CLIENT**</dt> <dt>1 (0x1)</dt> </dl>    | [**WM_TOUCHHITTESTING**](wm-touchhittesting.md) messages sont envoyés à la fenêtre cible.<br/>                                   |
| <span id="TOUCH_HIT_TESTING_NONE"></span><span id="touch_hit_testing_none"></span><dl> <dt>**TOUCH_HIT_TESTING_NONE**</dt> <dt>2 (0X2)</dt> </dl>          | [**WM_TOUCHHITTESTING**](wm-touchhittesting.md) messages ne sont pas envoyés à la fenêtre cible ou aux fenêtres enfants.<br/>              |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes](constants.md)
</dt> <dt>

[**POINTER_INFO**](/previous-versions/windows/desktop/api)
</dt> </dl>

 

