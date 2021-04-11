---
title: Autorisation du service
description: Une application peut implémenter une autorisation personnalisée pour les messages entrants sur un hôte de service.
ms.assetid: 75bcf051-3983-48fc-8121-0984ac9cdcb9
keywords:
- Services Web d’autorisation de service pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c296dc6b4900bd20df7d1e70631e758599a0028d
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104102557"
---
# <a name="service-authorization"></a><span data-ttu-id="14a2a-106">Autorisation du service</span><span class="sxs-lookup"><span data-stu-id="14a2a-106">Service Authorization</span></span>

<span data-ttu-id="14a2a-107">Une application peut implémenter une autorisation personnalisée pour les messages entrants sur un hôte de service.</span><span class="sxs-lookup"><span data-stu-id="14a2a-107">An application can implement custom authorization for incoming messages on a service host .</span></span>


<span data-ttu-id="14a2a-108">Un hôte de service reçoit un rappel de sécurité de [**service Web de rappel \_ \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback) de sécurité dans le cadre du [**\_ point de \_ terminaison de service WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) qui est passé à la fonction [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) .</span><span class="sxs-lookup"><span data-stu-id="14a2a-108">A service host receives a security callback [**WS\_SERVICE\_SECURITY\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback) as part of the [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) which is passed to the [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) function.</span></span> <span data-ttu-id="14a2a-109">Ce rappel est appelé lors de la réception du [ \_ message WS](ws-message.md) .</span><span class="sxs-lookup"><span data-stu-id="14a2a-109">This callback is invoked when the [WS\_MESSAGE](ws-message.md) is received.</span></span>

<span data-ttu-id="14a2a-110">L’application peut s’appuyer sur ce rappel pour implémenter l’autorisation personnalisée pour les messages entrants sur l’hôte de service.</span><span class="sxs-lookup"><span data-stu-id="14a2a-110">The application can rely on this callback to implement custom authorization for incoming messages on the service host.</span></span> <span data-ttu-id="14a2a-111">Si l’autorisation échoue, la fonction de rappel de sécurité retourne un échec HR et l’hôte de service abandonne le canal.</span><span class="sxs-lookup"><span data-stu-id="14a2a-111">If the authorization fails the security callback function returns a failure HR, and the service host aborts the channel.</span></span>

<span data-ttu-id="14a2a-112">Pour obtenir un exemple d’implémentation, consultez l’exemple nom d’utilisateur sur SSL [HttpCalculatorWithUserNameOverSslServiceExample](httpcalculatorwithusernameoversslserviceexample.md).</span><span class="sxs-lookup"><span data-stu-id="14a2a-112">See the user name over SSL example, [HttpCalculatorWithUserNameOverSslServiceExample](httpcalculatorwithusernameoversslserviceexample.md), for an example implementation.</span></span>

 

 




