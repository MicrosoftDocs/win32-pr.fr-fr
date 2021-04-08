---
description: L’une des méthodes les plus courantes pour recevoir un événement consiste à utiliser une application en cours d’exécution, telle qu’une application de gestion qui recueille et affiche des événements à un utilisateur.
ms.assetid: 380ac556-ba0a-4fae-8b76-0645d99e8583
ms.tgt_platform: multiple
title: Réception d’événements pendant la durée de votre application
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fd6b9731dd662a92296a86910a6cf8cb231cca1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034258"
---
# <a name="receiving-events-for-the-duration-of-your-application"></a><span data-ttu-id="c5847-103">Réception d’événements pendant la durée de votre application</span><span class="sxs-lookup"><span data-stu-id="c5847-103">Receiving Events for the Duration of Your Application</span></span>

<span data-ttu-id="c5847-104">L’une des méthodes les plus courantes pour recevoir un événement consiste à utiliser une application en cours d’exécution, telle qu’une application de gestion qui recueille et affiche des événements à un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c5847-104">One of the most common ways to receive an event is through a running application, such as a management application that collects and displays events to a user.</span></span> <span data-ttu-id="c5847-105">Ces applications sont appelées « temporaires », car un consommateur temporaire ne reçoit pas de notifications d’événements lorsqu’il est arrêté.</span><span class="sxs-lookup"><span data-stu-id="c5847-105">Such applications are called "temporary" because a temporary consumer does not receive event notifications when shut down.</span></span>

<span data-ttu-id="c5847-106">Un consommateur temporaire appelle [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) dans le script ou [**IWbemServices.ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) en C++ pour s’abonner aux événements d’un espace de noms.</span><span class="sxs-lookup"><span data-stu-id="c5847-106">A temporary consumer calls [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) in script or [**IWbemServices.ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) in C++ to subscribe to events in a namespace.</span></span> <span data-ttu-id="c5847-107">L’identité associée à cet abonnement est l’appelant.</span><span class="sxs-lookup"><span data-stu-id="c5847-107">The identity associated with this subscription is the caller.</span></span>

<span data-ttu-id="c5847-108">Un consommateur d’événements temporaire peut recevoir des notifications de manière asynchrone ou semisynchronously dans les scripts et C++.</span><span class="sxs-lookup"><span data-stu-id="c5847-108">A temporary event consumer can receive notifications either asynchronously or semisynchronously in both scripts and C++.</span></span>

> [!Note]  
> <span data-ttu-id="c5847-109">Pour des raisons de sécurité, il est important de noter que les notifications d’événements asynchrones ne sont pas recommandées.</span><span class="sxs-lookup"><span data-stu-id="c5847-109">For security reasons, it is important to note that asynchronous event notifications are not recommended.</span></span> <span data-ttu-id="c5847-110">Pour plus d’informations, consultez [définition de la sécurité sur un appel asynchrone](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="c5847-110">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span> <span data-ttu-id="c5847-111">Les consommateurs d’événements ont des problèmes de sécurité particuliers.</span><span class="sxs-lookup"><span data-stu-id="c5847-111">Event consumers have special security concerns.</span></span> <span data-ttu-id="c5847-112">Pour plus d’informations, consultez [sécurisation des événements WMI](securing-wmi-events.md).</span><span class="sxs-lookup"><span data-stu-id="c5847-112">For more information, see [Securing WMI Events](securing-wmi-events.md).</span></span>

 

<span data-ttu-id="c5847-113">Pour plus d’informations sur la réception de notifications d’événements asynchrones et semi-synchrones, consultez réception de notifications d' [événements asynchrones](receiving-asynchronous-event-notifications.md) et [réception de notifications d’événements semi](receiving-synchronous-and-semisynchronous-event-notifications.md)</span><span class="sxs-lookup"><span data-stu-id="c5847-113">For more information about receiving asynchronous and semisynchronous event notifications, see [Receiving Asynchronous Event Notifications](receiving-asynchronous-event-notifications.md) and [Receiving Semisynchronous Event Notifications](receiving-synchronous-and-semisynchronous-event-notifications.md).</span></span>

 

 



