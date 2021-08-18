---
description: Le système diffuse un ensemble d’événements de changement d’appareil par défaut à l’ensemble des applications et services.
ms.assetid: 672ad753-210b-41c3-b8c7-e041ce7b1671
title: Notifications de l’appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12186ab6349057258d723f7e690e889b7e79af4abe47f714055599cb6f648333
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636619"
---
# <a name="device-notifications"></a>Notifications de l’appareil

Le système diffuse un ensemble d’événements de changement d’appareil par défaut à l’ensemble des applications et services. Vous n’avez pas besoin de vous inscrire pour recevoir ces événements par défaut. Pour plus d’informations, consultez la section Notes dans [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) . Pour spécifier d’autres événements que votre application ou service doit recevoir, utilisez la fonction **RegisterDeviceNotification** .

Lorsqu’une application ou un service appelle [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa), elle spécifie également la fenêtre qui recevra les événements de notification. Les services peuvent spécifier un handle d’état de service au lieu d’un handle de fenêtre. Si un service spécifie son descripteur d’État du service, son gestionnaire de contrôle des services recevra les événements de notification. Pour plus d’informations, consultez [**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex).

Veillez à gérer Plug-and-Play événements d’appareil aussi rapidement que possible. Dans le cas contraire, le système risque de ne plus répondre. Si votre gestionnaire d’événements doit effectuer une opération qui peut bloquer l’exécution (par exemple, les e/s), il est préférable de démarrer un autre thread pour effectuer l’opération de façon asynchrone.

Les descripteurs de notification de périphérique retournés par [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) doivent être fermés en appelant la fonction [**UnregisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-unregisterdevicenotification) lorsqu’ils ne sont plus nécessaires.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Inscription aux notifications de l’appareil](registering-for-device-notification.md)
</dt> </dl>

 

 
