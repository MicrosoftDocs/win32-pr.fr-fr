---
description: L’une des méthodes les plus courantes pour recevoir un événement consiste à utiliser une application en cours d’exécution, telle qu’une application de gestion qui recueille et affiche des événements à un utilisateur.
ms.assetid: 380ac556-ba0a-4fae-8b76-0645d99e8583
ms.tgt_platform: multiple
title: Réception d’événements pendant la durée de votre application
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6815c2ddd7725ccd12dd65b0047874ddce1038b2a2c07f90a40d6f87e6af3a06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118554217"
---
# <a name="receiving-events-for-the-duration-of-your-application"></a>Réception d’événements pendant la durée de votre application

L’une des méthodes les plus courantes pour recevoir un événement consiste à utiliser une application en cours d’exécution, telle qu’une application de gestion qui recueille et affiche des événements à un utilisateur. Ces applications sont appelées « temporaires », car un consommateur temporaire ne reçoit pas de notifications d’événements lorsqu’il est arrêté.

Un consommateur temporaire appelle [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) dans le script ou [**IWbemServices.ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) en C++ pour s’abonner aux événements d’un espace de noms. L’identité associée à cet abonnement est l’appelant.

Un consommateur d’événements temporaire peut recevoir des notifications de manière asynchrone ou semisynchronously dans les scripts et C++.

> [!Note]  
> Pour des raisons de sécurité, il est important de noter que les notifications d’événements asynchrones ne sont pas recommandées. Pour plus d’informations, consultez [définition de la sécurité sur un appel asynchrone](setting-security-on-an-asynchronous-call.md). Les consommateurs d’événements ont des problèmes de sécurité particuliers. Pour plus d’informations, consultez [sécurisation des événements WMI](securing-wmi-events.md).

 

Pour plus d’informations sur la réception de notifications d’événements asynchrones et semi-synchrones, consultez réception de notifications d' [événements asynchrones](receiving-asynchronous-event-notifications.md) et [réception de notifications d’événements semi](receiving-synchronous-and-semisynchronous-event-notifications.md)

 

 



