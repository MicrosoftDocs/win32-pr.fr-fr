---
title: Journalisation Server-Side
description: La journalisation côté serveur est disponible sur un groupe d’URL ou une session de serveur.
ms.assetid: e1fcd87f-382a-42bf-b53f-1e1cb1dbbfc5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b76548b296bcdbd343e4e259e0cf3c87537ef5d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840377"
---
# <a name="server-side-logging"></a><span data-ttu-id="229df-103">Journalisation Server-Side</span><span class="sxs-lookup"><span data-stu-id="229df-103">Server-Side Logging</span></span>

<span data-ttu-id="229df-104">La journalisation côté serveur est disponible sur un groupe d’URL ou une session de serveur.</span><span class="sxs-lookup"><span data-stu-id="229df-104">Server-side logging is available on a URL group or server session.</span></span> <span data-ttu-id="229df-105">Lorsque la journalisation est activée sur une session de serveur, elle fonctionne comme une forme centralisée de journalisation pour tous les groupes d’URL sous la session serveur.</span><span class="sxs-lookup"><span data-stu-id="229df-105">When logging is enabled on a server session, it functions as centralized form of logging for all the URL groups under the server session.</span></span> <span data-ttu-id="229df-106">Lorsque la journalisation est activée sur un groupe d’URL, la journalisation est exécutée uniquement sur les demandes routées vers le groupe d’URL.</span><span class="sxs-lookup"><span data-stu-id="229df-106">When logging is enabled on a URL group, logging is performed only on requests that are routed to the URL Group.</span></span> <span data-ttu-id="229df-107">Les types de journalisation suivants sont pris en charge par l’API du serveur HTTP :</span><span class="sxs-lookup"><span data-stu-id="229df-107">The following types of logging are supported by the HTTP Server API:</span></span>

-   <span data-ttu-id="229df-108">[Journalisation W3C](w3c-logging.md): disponible sur la session du serveur et le groupe d’URL.</span><span class="sxs-lookup"><span data-stu-id="229df-108">[W3C logging](w3c-logging.md): Available on the server session and URL group.</span></span>
-   <span data-ttu-id="229df-109">[Journalisation du NCSA](ncsa-logging.md): disponible sur le groupe d’URL.</span><span class="sxs-lookup"><span data-stu-id="229df-109">[NCSA logging](ncsa-logging.md): Available on the URL group.</span></span>
-   <span data-ttu-id="229df-110">[Journalisation IIS](iis-logging.md): disponible sur le groupe d’URL.</span><span class="sxs-lookup"><span data-stu-id="229df-110">[IIS logging](iis-logging.md): Available on the URL group.</span></span>
-   <span data-ttu-id="229df-111">[Journalisation centralisée binaire](centralized-binary-logging.md): disponible sur la session serveur.</span><span class="sxs-lookup"><span data-stu-id="229df-111">[Centralized binary logging](centralized-binary-logging.md): Available on the server session.</span></span>

<span data-ttu-id="229df-112">Pour tirer parti de la fonctionnalité de journalisation HTTP, l’application active et configure un type de journalisation sur la session serveur ou le groupe d’URL.</span><span class="sxs-lookup"><span data-stu-id="229df-112">To take advantage of the HTTP logging feature, the application enables and configures one type of logging on the server session or URL group.</span></span> <span data-ttu-id="229df-113">Pour plus d’informations, consultez [configuration et activation de la journalisation côté serveur](configuring-and-enabling-server-side-logging.md) .</span><span class="sxs-lookup"><span data-stu-id="229df-113">For more information, see [Configuring and Enabling Server Side Logging](configuring-and-enabling-server-side-logging.md)</span></span>

 

 




