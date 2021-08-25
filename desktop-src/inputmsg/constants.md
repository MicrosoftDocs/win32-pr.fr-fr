---
title: Messages d’entrée de pointeur et constantes de notifications
description: Les rubriques de cette section fournissent les spécifications de référence pour les messages d’entrée de pointeur et les constantes de notifications.
ms.assetid: 2224DCD0-DAE1-4AC2-AB36-23D114803138
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 600ae37234c64ab313d38666b83f926795b08e21d91f23eeaec68aa68b24b9db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829769"
---
# <a name="pointer-input-messages-and-notifications-constants"></a>Messages d’entrée de pointeur et constantes de notifications

Les rubriques de cette section fournissent les spécifications de référence pour les [messages d’entrée de pointeur et](messages-and-notifications-portal.md) les constantes de notifications.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                             | Description                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**État de la touche de modification**](modifier-key-states-constants.md)<br/>            | Indique les touches de modification du clavier qui ont été activées lors de la génération de l’entrée.<br/>                                                                                                       |
| [**Indicateurs de stylet**](pen-flags-constants.md)<br/>                               | Valeurs qui peuvent apparaître dans le champ **penFlags** de la structure [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) .<br/>                                                                         |
| [**Masque du stylet**](pen-mask-constants.md)<br/>                                 | Valeurs qui peuvent apparaître dans le champ **penMask** de la structure [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) .<br/>                                                                          |
| [**Modification de l’appareil pointeur**](pointer-device-change-constants.md)<br/>       | Valeurs qui peuvent être passées dans le paramètre *wParam* du message [**WM_POINTERDEVICECHANGE**](wm-pointerdevicechange.md) .<br/>                                                                    |
| [**Indicateurs de pointeur**](pointer-flags-contants.md)<br/>                        | Valeurs qui peuvent apparaître dans le champ **pointerFlags** de la structure [**POINTER_INFO**](/previous-versions/windows/desktop/api) .<br/>                                                                              |
| [**Indicateurs de message de pointeur**](pointer-message-flags.md)<br/>                 | Valeurs utilisées dans différentes macros de pointeur (consultez [macros](macros.md)).<br/>                                                                                                                       |
| [**Indicateurs tactiles**](touch-flags-constants.md)<br/>                           | Valeurs qui peuvent apparaître dans le champ **touchFlags** de la structure [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) .<br/>                                                                   |
| [**Fenêtre test d’atteinte tactile**](touch-hit-testing-window-constants.md)<br/> | Indique comment les messages pour le test d’atteinte tactile sont traités par les fenêtres qui sont inscrites via la fonction [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) .<br/> |
| [**Masque tactile**](touch-mask-constants.md)<br/>                             | Valeurs qui peuvent apparaître dans le champ **touchMask** de la structure [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) .<br/>                                                                    |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence de message d’entrée de pointeur](wmpointer-reference.md)
</dt> </dl>

 

