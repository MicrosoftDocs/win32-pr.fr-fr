---
title: Configuration de la session serveur
description: Configuration de la session serveur
ms.assetid: 1e4e9440-8d70-44df-90a7-2d5e25b2f680
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d41c1606cce397c49a15c62dae10531edfde93f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090937"
---
# <a name="configuring-the-server-session"></a><span data-ttu-id="b1195-103">Configuration de la session serveur</span><span class="sxs-lookup"><span data-stu-id="b1195-103">Configuring the Server Session</span></span>

<span data-ttu-id="b1195-104">L’ID de session du serveur est créé avec la fonction [**HttpCreateServerSession**](/windows/desktop/api/Http/nf-http-httpcreateserversession) et utilisé dans l’appel à [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty).</span><span class="sxs-lookup"><span data-stu-id="b1195-104">The server session ID is created with the [**HttpCreateServerSession**](/windows/desktop/api/Http/nf-http-httpcreateserversession) function, and used in the call to [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty).</span></span> <span data-ttu-id="b1195-105">Le paramètre *pPropertyInformation* pointe vers la structure de configuration pour le type de propriété défini.</span><span class="sxs-lookup"><span data-stu-id="b1195-105">The *pPropertyInformation* parameter points to the configuration structure for the property type that is set.</span></span> <span data-ttu-id="b1195-106">Le paramètre *PropertyInformationLength* spécifie la taille, en octets, de la structure de configuration.</span><span class="sxs-lookup"><span data-stu-id="b1195-106">The *PropertyInformationLength* parameter specifies the size, in bytes, of the configuration structure.</span></span> <span data-ttu-id="b1195-107">Par exemple, lors de la définition du **HttpServerTimeoutsProperty** , le paramètre **pPropertyInformation** doit pointer vers une mémoire tampon qui correspond au moins à la taille de la structure d' [**informations de limite du délai d' \_ expiration \_ \_ http**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) .</span><span class="sxs-lookup"><span data-stu-id="b1195-107">For example, when setting the **HttpServerTimeoutsProperty** the **pPropertyInformation** parameter must point to a buffer that is at least the size of the [**HTTP\_TIMEOUT\_LIMIT\_INFO**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) structure.</span></span>

<span data-ttu-id="b1195-108">En général, une application HTTP crée une session de serveur unique et peut définir des propriétés à l’échelle de l’application, telles que la limite de limitation de bande passante globale, ou activer la journalisation centralisée sur cette session serveur.</span><span class="sxs-lookup"><span data-stu-id="b1195-108">Typically an HTTP application creates a single server session and may set application wide properties such as global bandwidth throttling limit or enable centralized logging on this server session.</span></span> <span data-ttu-id="b1195-109">[**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) remplace les configurations de l’API du serveur http pour l’application appelante ; elle n’affecte pas les propriétés de l’API du serveur HTTP.</span><span class="sxs-lookup"><span data-stu-id="b1195-109">[**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) overrides the HTTP Server API configurations for the calling application; it does not affect the HTTP Server API-wide properties.</span></span> <span data-ttu-id="b1195-110">Les configurations de session serveur sont interrogées en appelant [**HttpQueryServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty).</span><span class="sxs-lookup"><span data-stu-id="b1195-110">The server session configurations are queried by calling [**HttpQueryServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty).</span></span>

 

 




