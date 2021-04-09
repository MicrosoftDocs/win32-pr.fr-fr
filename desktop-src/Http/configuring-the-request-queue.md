---
title: Configuration de la file d’attente des demandes
description: Configuration de la file d’attente des demandes
ms.assetid: ab03089c-2ef1-457d-a5f5-a4d400f3a7f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42ed397ffbcb42d887d519bc4492bd167dd98c57
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840013"
---
# <a name="configuring-the-request-queue"></a><span data-ttu-id="d9803-103">Configuration de la file d’attente des demandes</span><span class="sxs-lookup"><span data-stu-id="d9803-103">Configuring the Request Queue</span></span>

<span data-ttu-id="d9803-104">Lorsque la file d’attente de demandes est ouverte ou créée, l’application appelante reçoit un descripteur qui peut être utilisé pour envoyer des demandes ou configurer la file d’attente de demandes.</span><span class="sxs-lookup"><span data-stu-id="d9803-104">When the request queue is opened or created, the calling application receives a handle to it that can be used to send requests or configure the request queue.</span></span> <span data-ttu-id="d9803-105">L’appel de [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) avec **HttpServerBindingProperty** et la spécification du descripteur de la file d’attente des demandes dans la structure des [**\_ \_ informations de liaison http**](/windows/desktop/api/Http/ns-http-http_binding_info) , spécifiée dans le paramètre *pPropertyInformation* , associe le groupe d’URL à la file d’attente de demandes.</span><span class="sxs-lookup"><span data-stu-id="d9803-105">Calling [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) with **HttpServerBindingProperty** and supplying the request queue handle in the [**HTTP\_BINDING\_INFO**](/windows/desktop/api/Http/ns-http-http_binding_info) structure, specified in the *pPropertyInformation* parameter, associates the URL group with the request queue.</span></span> <span data-ttu-id="d9803-106">Les propriétés de la file d’attente des demandes sont définies uniquement par l’application qui crée la file d’attente des demandes.</span><span class="sxs-lookup"><span data-stu-id="d9803-106">Request queue properties are set only by the application that creates the request queue.</span></span> <span data-ttu-id="d9803-107">Par exemple, pour définir la propriété longueur de la file d’attente du serveur, l’application Creator appelle [**HttpSetRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) en spécifiant **HttpServerQueueLengthProperty** dans le paramètre *Property* .</span><span class="sxs-lookup"><span data-stu-id="d9803-107">For example, to set the server queue length property, the creator application calls [**HttpSetRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) specifying **HttpServerQueueLengthProperty** in the *Property* parameter.</span></span>

 

 




