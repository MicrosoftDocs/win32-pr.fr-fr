---
description: Un service qui est une application console peut inscrire un gestionnaire de contrôle de console pour recevoir une notification lorsqu’un utilisateur se déconnecte.
ms.assetid: 86ace8b8-c1cb-4646-bc92-86bd578a82c5
title: Réception d’événements dans un service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b95f7329383ffc8aea08102a2fe8cf8b49e0ef9d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416344"
---
# <a name="receiving-events-in-a-service"></a>Réception d’événements dans un service

Un service qui est une application console peut inscrire un [Gestionnaire de contrôle de console](/windows/console/console-control-handlers) pour recevoir une notification lorsqu’un utilisateur se déconnecte. Toutefois, aucun événement de console n’est envoyé lorsqu’un utilisateur interactif ouvre une session. Pour plus d’informations sur la réception d’une notification lorsqu’un utilisateur ouvre une session, consultez [création d’un package de notifications Winlogon](/windows/desktop/SecAuthN/creating-a-winlogon-notification-package).

Le système diffuse les événements de changement d’appareil à tous les services. Ces événements peuvent être reçus par un service dans une procédure de fenêtre ou dans son gestionnaire de contrôle de service. Pour spécifier les événements que votre service doit recevoir, utilisez la fonction [**RegisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa) .

Veillez à gérer Plug-and-Play événements d’appareil aussi rapidement que possible. Dans le cas contraire, le système risque de ne plus répondre. Si votre gestionnaire d’événements doit effectuer une opération qui peut bloquer l’exécution (par exemple, les e/s), il est préférable de démarrer un autre thread pour effectuer l’opération de façon asynchrone.

Lorsqu’un service appelle [**RegisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa), le service spécifie également un handle de fenêtre ou un handle d’état de service. Si un service spécifie un handle de fenêtre, la procédure de fenêtre reçoit les événements de notification. Si un service spécifie son descripteur d’État du service, son gestionnaire de contrôle des services reçoit les événements de notification. Pour plus d’informations, consultez [**HandlerEx**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex).

Les descripteurs de notification de périphérique retournés par [**RegisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa) doivent être fermés en appelant la fonction [**UnregisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-unregisterdevicenotification) lorsqu’ils ne sont plus nécessaires.

 

 
