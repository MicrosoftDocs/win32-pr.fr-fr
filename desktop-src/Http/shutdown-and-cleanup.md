---
title: Arrêt et nettoyage
description: Pour qu’une application s’arrête normalement, elle doit effectuer les opérations de nettoyage suivantes.
ms.assetid: fc07adb8-103c-42d8-8187-3f5ee083c6d8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebf1c59534b73fee21489439c7818c286874185d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029315"
---
# <a name="shutdown-and-cleanup"></a><span data-ttu-id="35f20-103">Arrêt et nettoyage</span><span class="sxs-lookup"><span data-stu-id="35f20-103">Shutdown and Cleanup</span></span>

<span data-ttu-id="35f20-104">Pour qu’une application s’arrête normalement, elle doit effectuer les opérations de nettoyage suivantes :</span><span class="sxs-lookup"><span data-stu-id="35f20-104">For an application to terminate gracefully, it must perform the following cleanup operations:</span></span>

-   <span data-ttu-id="35f20-105">Supprimez toutes les URL inscrites du groupe d’URL en appelant la fonction [**HttpRemoveUrlFromUrlGroup**](/windows/desktop/api/Http/nf-http-httpremoveurlfromurlgroup) pour annuler l’inscription des URL précédemment inscrites dans l’appel à [**HttpAddUrlToUrlGroup**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup).</span><span class="sxs-lookup"><span data-stu-id="35f20-105">Remove all registered URLs from the URL group by calling the [**HttpRemoveUrlFromUrlGroup**](/windows/desktop/api/Http/nf-http-httpremoveurlfromurlgroup) function to deregister URLs previously registered in the call to [**HttpAddUrlToUrlGroup**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup).</span></span>
-   <span data-ttu-id="35f20-106">Fermez le groupe d’URL en appelant la fonction [**HttpCloseUrlGroup**](/windows/desktop/api/Http/nf-http-httpcloseurlgroup) .</span><span class="sxs-lookup"><span data-stu-id="35f20-106">Close the URL Group by calling the [**HttpCloseUrlGroup**](/windows/desktop/api/Http/nf-http-httpcloseurlgroup) function.</span></span> <span data-ttu-id="35f20-107">Tous les groupes d’URL créés sous une session serveur doivent être fermés avant de fermer la session serveur.</span><span class="sxs-lookup"><span data-stu-id="35f20-107">All the URL groups created under a server session must be closed before closing the server session.</span></span>
-   <span data-ttu-id="35f20-108">Fermez la session serveur en appelant [**HttpCloseServerSession**](/windows/desktop/api/Http/nf-http-httpcloseserversession).</span><span class="sxs-lookup"><span data-stu-id="35f20-108">Close the server session by calling [**HttpCloseServerSession**](/windows/desktop/api/Http/nf-http-httpcloseserversession).</span></span>
-   <span data-ttu-id="35f20-109">Fermez le descripteur de la file d’attente de demandes en appelant [**HttpCloseRequestQueue**](/windows/desktop/api/Http/nf-http-httpcloserequestqueue).</span><span class="sxs-lookup"><span data-stu-id="35f20-109">Close the handle to the request queue by calling [**HttpCloseRequestQueue**](/windows/desktop/api/Http/nf-http-httpcloserequestqueue).</span></span>
-   <span data-ttu-id="35f20-110">Arrêtez les ressources créées par l’API du serveur HTTP en appelant la fonction [**HttpTerminate**](/windows/desktop/api/Http/nf-http-httpterminate) avec les paramètres d’indicateur correspondants pour chaque appel de l’application initialement effectuée à [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize).</span><span class="sxs-lookup"><span data-stu-id="35f20-110">Terminate the resources created by the HTTP Server API by calling the [**HttpTerminate**](/windows/desktop/api/Http/nf-http-httpterminate) function with matching flag settings for each call the application originally made to [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize).</span></span> <span data-ttu-id="35f20-111">Chacun de ces appels met fin à toutes les ressources créées dans l’appel à [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize).</span><span class="sxs-lookup"><span data-stu-id="35f20-111">Each of these calls terminates all resources created in the call to [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize).</span></span>

 

 




