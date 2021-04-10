---
title: Cache en mode noyau
description: .
ms.assetid: f9a46ff4-779b-4b3a-b8f5-1ae10a3c0a61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9264535a58c033d66fd3fcc39988a292afc2a27f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029750"
---
# <a name="kernel-mode-cache"></a><span data-ttu-id="b537a-103">Cache en mode noyau</span><span class="sxs-lookup"><span data-stu-id="b537a-103">Kernel Mode Cache</span></span>

<span data-ttu-id="b537a-104">L’API de la version 2,0 du serveur HTTP permet aux applications de mettre en cache les réponses avec un contenu statique en mode noyau.</span><span class="sxs-lookup"><span data-stu-id="b537a-104">The HTTP Server version 2.0 API allows applications to cache responses with static content in kernel mode.</span></span> <span data-ttu-id="b537a-105">Des performances accrues sont obtenues lorsque les demandes sont traitées à partir du cache du noyau sans passer au mode utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b537a-105">Increased performance is achieved when requests are served from the kernel cache without transitioning to user mode.</span></span>

<span data-ttu-id="b537a-106">L’API du serveur HTTP applique les configurations de propriétés appropriées à toutes les demandes traitées à partir du cache du noyau, y compris les réponses de journalisation.</span><span class="sxs-lookup"><span data-stu-id="b537a-106">The HTTP Server API applies the appropriate property configurations to all requests served from the kernel cache, including logging responses.</span></span> <span data-ttu-id="b537a-107">Toutefois, les demandes qui requièrent une authentification ne seront pas traitées à partir du cache.</span><span class="sxs-lookup"><span data-stu-id="b537a-107">Requests that require authentication, however, will not be served from the cache.</span></span>

<span data-ttu-id="b537a-108">L’API du serveur HTTP limite le cache en mode noyau aux demandes qui remplissent les conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="b537a-108">The HTTP Server API limits the kernel mode cache to requests that meet the following conditions:</span></span>

-   <span data-ttu-id="b537a-109">Le verbe de requête est obtenir et la requête entière est reçue.</span><span class="sxs-lookup"><span data-stu-id="b537a-109">The request verb is GET and the entire request is received.</span></span>
-   <span data-ttu-id="b537a-110">La demande ne doit pas avoir de corps d’entité.</span><span class="sxs-lookup"><span data-stu-id="b537a-110">The request must not have an entity body.</span></span>
-   <span data-ttu-id="b537a-111">Le protocole HTTP est la version 1,0 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="b537a-111">The HTTP protocol is version 1.0 or later.</span></span>
-   <span data-ttu-id="b537a-112">L’en-tête « Translate : f » n’est pas présent.</span><span class="sxs-lookup"><span data-stu-id="b537a-112">The "Translate: f " header is not present.</span></span>
-   <span data-ttu-id="b537a-113">Les en-têtes attendus autres que « expect : 100-continue » ne sont pas présents.</span><span class="sxs-lookup"><span data-stu-id="b537a-113">Expect headers other than "Expect: 100-Continue" are not present.</span></span>
-   <span data-ttu-id="b537a-114">L’en-tête Authorization n’est pas présent.</span><span class="sxs-lookup"><span data-stu-id="b537a-114">The authorization header is not present.</span></span>
-   <span data-ttu-id="b537a-115">Les en-têtes de plage et de If-Range ne sont pas présents.</span><span class="sxs-lookup"><span data-stu-id="b537a-115">The Range and If-Range headers are not present.</span></span>

<span data-ttu-id="b537a-116">Outre les restrictions sur la demande, la réponse doit également remplir les conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="b537a-116">In addition to the restrictions on the request, the response must also meet the following conditions:</span></span>

-   <span data-ttu-id="b537a-117">La taille de la réponse est limitée à 256 Ko par défaut.</span><span class="sxs-lookup"><span data-stu-id="b537a-117">Response size is limited to 256 KB, by default.</span></span> <span data-ttu-id="b537a-118">Pour modifier la taille de la réponse mise en cache, définissez la valeur de Registre **UriMaxUriBytes** sur le nombre d’octets requis.</span><span class="sxs-lookup"><span data-stu-id="b537a-118">To change the size of the response that is cached, set the **UriMaxUriBytes** registry value to the required number of bytes.</span></span>

    ```
    HKEY_LOCAL_MACHINE
       System
          CurrentControlSet
             Services
                HTTP
                   Parameters
                      UriMaxUriBytes
    ```

-   <span data-ttu-id="b537a-119">L’intégralité de la réponse doit être fournie en un seul appel à [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse).</span><span class="sxs-lookup"><span data-stu-id="b537a-119">The entire response must be provided in a single call to [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse).</span></span>
-   <span data-ttu-id="b537a-120">L’en-tête de date de la réponse ne doit pas être supprimé.</span><span class="sxs-lookup"><span data-stu-id="b537a-120">The date header on the response must not be suppressed.</span></span>
-   <span data-ttu-id="b537a-121">Si l’en-tête Last-modified est présent, la syntaxe de l’en-tête doit être correcte.</span><span class="sxs-lookup"><span data-stu-id="b537a-121">If the last-modified header is present, the value of the header must have the correct syntax.</span></span> <span data-ttu-id="b537a-122">La valeur de temps de cet en-tête est utilisée pour la vérification du contrôle de cache.</span><span class="sxs-lookup"><span data-stu-id="b537a-122">The time value in this header is used for cache control verification.</span></span>
-   <span data-ttu-id="b537a-123">Le cache en mode noyau a suffisamment d’espace pour stocker la réponse.</span><span class="sxs-lookup"><span data-stu-id="b537a-123">The kernel mode cache has enough space left to store the response.</span></span>

<span data-ttu-id="b537a-124">Par défaut, le cache de réponse en mode noyau est activé.</span><span class="sxs-lookup"><span data-stu-id="b537a-124">By default, kernel mode response cache is enabled.</span></span> <span data-ttu-id="b537a-125">Si l’une des conditions de la demande ou de la réponse répertoriées ci-dessus n’est pas remplie, la réponse est envoyée, mais elle n’est pas mise en cache.</span><span class="sxs-lookup"><span data-stu-id="b537a-125">If any of the conditions for the request or response listed above are not met, the response will be sent, but it will not be cached.</span></span> <span data-ttu-id="b537a-126">Dans l’API du serveur HTTP version 2,0, [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) comprend un paramètre *pCachePolicy* facultatif permettant de transmettre la structure de la [**\_ \_ stratégie de cache http**](/windows/desktop/api/Http/ns-http-http_cache_policy) .</span><span class="sxs-lookup"><span data-stu-id="b537a-126">In HTTP Server version 2.0 API, [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) includes an optional *pCachePolicy* parameter to pass the [**HTTP\_CACHE\_POLICY**](/windows/desktop/api/Http/ns-http-http_cache_policy) structure.</span></span> <span data-ttu-id="b537a-127">Les applications utilisent la structure de stratégie de cache pour configurer le cache.</span><span class="sxs-lookup"><span data-stu-id="b537a-127">Applications use the cache policy structure to configure the cache.</span></span>

 

 




