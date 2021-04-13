---
title: Création et liaison à une file d’attente de demandes
description: Une file d’attente de demandes est une file d’attente de service qui contient les demandes en attente pour une application spécifique.
ms.assetid: 93f8b230-af0a-4582-b35b-d65f6841e525
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 945b8451f9128357b7da0ddc64600b74deffd0d7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380185"
---
# <a name="creating-and-binding-to-a-request-queue"></a><span data-ttu-id="d068d-103">Création et liaison à une file d’attente de demandes</span><span class="sxs-lookup"><span data-stu-id="d068d-103">Creating and Binding to a Request Queue</span></span>

<span data-ttu-id="d068d-104">Une file d’attente de demandes est une file d’attente de service qui contient les demandes en attente pour une application spécifique.</span><span class="sxs-lookup"><span data-stu-id="d068d-104">A request queue is a service queue that holds pending requests for a specific application.</span></span> <span data-ttu-id="d068d-105">Une application crée la file d’attente de demandes indépendamment du groupe d’URL ou de la session serveur en appelant la fonction [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) et définit les propriétés de la file d’attente des demandes en appelant la fonction [**HttpSetRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) .</span><span class="sxs-lookup"><span data-stu-id="d068d-105">An application creates the request queue independently of the URL group or server session by calling the [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) function, and sets the request queue properties by calling the [**HttpSetRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) function.</span></span> <span data-ttu-id="d068d-106">Ces propriétés sont les commentaires des réponses 503, la longueur maximale de la file d’attente et l’état de l’activité.</span><span class="sxs-lookup"><span data-stu-id="d068d-106">These properties are the verbosity of 503 responses, the maximum length of the queue, and the activity state.</span></span>

<span data-ttu-id="d068d-107">Pour que les demandes soient acheminées vers sa file d’attente de demandes, l’application lie le groupe d’URL qu’il a créé dans le cadre de la configuration de l' [exécution](run-time-configuration.md) à la file d’attente en appelant [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) avec **HttpServerBindingProperty** spécifié dans le paramètre *Property* .</span><span class="sxs-lookup"><span data-stu-id="d068d-107">To cause requests to be routed to its request queue, the application binds the URL group it created as part of [run-time configuration](run-time-configuration.md) to the queue by calling [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) with **HttpServerBindingProperty** specified in the *Property* parameter.</span></span> <span data-ttu-id="d068d-108">Les demandes entrantes des URL dans le groupe sont ensuite acheminées vers la file d’attente de demandes spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d068d-108">Incoming requests from the URLs in the group are then routed to the specified request queue.</span></span>

 

 




