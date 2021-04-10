---
title: Mise en cache (Windows Internet)
description: Les fonctions WinINet disposent d’une prise en charge de la mise en cache intégrée simple, mais flexible.
ms.assetid: 44c268c9-a745-432a-8540-60d7e7d2cb2d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e753d826ec3abe580b94158296562208dcbed44
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102680"
---
# <a name="caching-windows-internet"></a><span data-ttu-id="40714-103">Mise en cache (Windows Internet)</span><span class="sxs-lookup"><span data-stu-id="40714-103">Caching (Windows Internet)</span></span>

<span data-ttu-id="40714-104">Les fonctions WinINet disposent d’une prise en charge de la mise en cache intégrée simple, mais flexible.</span><span class="sxs-lookup"><span data-stu-id="40714-104">The WinINet functions have simple, yet flexible, built-in caching support.</span></span> <span data-ttu-id="40714-105">Toutes les données récupérées à partir du réseau sont mises en cache sur le disque dur et récupérées pour les demandes suivantes.</span><span class="sxs-lookup"><span data-stu-id="40714-105">Any data retrieved from the network is cached on the hard disk and retrieved for subsequent requests.</span></span> <span data-ttu-id="40714-106">L’application peut contrôler la mise en cache à chaque requête.</span><span class="sxs-lookup"><span data-stu-id="40714-106">The application can control the caching on each request.</span></span> <span data-ttu-id="40714-107">Pour les requêtes http provenant du serveur, la plupart des en-têtes reçus sont également mis en cache.</span><span class="sxs-lookup"><span data-stu-id="40714-107">For http requests from the server, most headers received are also cached.</span></span> <span data-ttu-id="40714-108">Quand une requête HTTP est satisfaite à partir du cache, les en-têtes mis en cache sont également retournés à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="40714-108">When an http request is satisfied from the cache, the cached headers are also returned to the caller.</span></span> <span data-ttu-id="40714-109">Cela rend le téléchargement des données transparent, que les données proviennent du cache ou du réseau.</span><span class="sxs-lookup"><span data-stu-id="40714-109">This makes data download seamless, whether the data is coming from the cache or from the network.</span></span>

<span data-ttu-id="40714-110">Les applications doivent allouer correctement un tampon afin d’obtenir les résultats souhaités lors de l’utilisation des fonctions de mise en cache des URL persistantes.</span><span class="sxs-lookup"><span data-stu-id="40714-110">Applications must properly allocate a buffer in order to get the desired results when using the persistent URL caching functions.</span></span> <span data-ttu-id="40714-111">Pour plus d’informations, consultez [utilisation de mémoires tampons](appendix-b-using-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="40714-111">For more information, see [Using Buffers](appendix-b-using-buffers.md).</span></span>

## <a name="cache-behavior-during-response-processing"></a><span data-ttu-id="40714-112">Comportement du cache pendant le traitement de la réponse</span><span class="sxs-lookup"><span data-stu-id="40714-112">Cache Behavior During Response Processing</span></span>

<span data-ttu-id="40714-113">Le cache WinINet est conforme aux directives de contrôle de cache HTTP décrites dans le document RFC 2616.</span><span class="sxs-lookup"><span data-stu-id="40714-113">The WinINet cache is compliant with the HTTP cache-control directives described in RFC 2616.</span></span> <span data-ttu-id="40714-114">Les directives de contrôle de cache et les indicateurs de jeu d’applications déterminent ce qui peut être mis en cache ; Toutefois, WinINet détermine ce qui est réellement mis en cache en fonction du critère suivant :</span><span class="sxs-lookup"><span data-stu-id="40714-114">The cache-control directives and application set flags determine what may be cached; however, WinINet determines what is actually cached based on the following criterion:</span></span>

-   <span data-ttu-id="40714-115">WinINet met uniquement en cache les réponses HTTP et FTP.</span><span class="sxs-lookup"><span data-stu-id="40714-115">WinINet only caches HTTP and FTP responses.</span></span>
-   <span data-ttu-id="40714-116">Seules les réponses bien comportent peuvent être stockées par un cache et utilisées dans une réponse à une demande ultérieure.</span><span class="sxs-lookup"><span data-stu-id="40714-116">Only well behaved responses may be stored by a cache and used in a reply to a subsequent Request.</span></span> <span data-ttu-id="40714-117">Les réponses correctes sont définies comme des réponses qui renvoient correctement.</span><span class="sxs-lookup"><span data-stu-id="40714-117">Well behaved responses are defined as responses that return successfully.</span></span>
-   <span data-ttu-id="40714-118">Par défaut, WinINet met en cache les réponses réussies, sauf si une directive Cache-Control du serveur ou un indicateur défini par l’application indique spécifiquement que la réponse ne peut pas être mise en cache.</span><span class="sxs-lookup"><span data-stu-id="40714-118">By default, WinINet will cache successful responses unless either a cache-control directive from the server, or an application-defined flag specifically denote that the response may not be cached.</span></span>
-   <span data-ttu-id="40714-119">En général, les réponses au verbe obtenir sont mises en cache si les spécifications répertoriées ci-dessus sont remplies.</span><span class="sxs-lookup"><span data-stu-id="40714-119">In general, responses to the GET verb are cached if the requirements listed above are met.</span></span> <span data-ttu-id="40714-120">Les réponses aux verbes PUT et POSTCONNEXION ne sont en aucun cas mises en cache.</span><span class="sxs-lookup"><span data-stu-id="40714-120">Responses to PUT and POST verbs are not cached under any circumstances.</span></span>
-   <span data-ttu-id="40714-121">Les éléments sont mis en cache même lorsque le cache est saturé.</span><span class="sxs-lookup"><span data-stu-id="40714-121">Items will be cached even when the cache is full.</span></span> <span data-ttu-id="40714-122">Si un élément ajouté met le cache sur la limite de taille, le nettoyage du cache est planifié.</span><span class="sxs-lookup"><span data-stu-id="40714-122">If an added item is puts the cache over the size limit, the cache scavenger is scheduled.</span></span> <span data-ttu-id="40714-123">Par défaut, il n’est pas garanti que les éléments restent dans le cache plus de 10 minutes.</span><span class="sxs-lookup"><span data-stu-id="40714-123">By default, items are not guaranteed to remain more than 10 minutes in the cache.</span></span> <span data-ttu-id="40714-124">Pour plus d’informations, consultez la section [cache de nettoyage](#cache-scavenger) ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="40714-124">For more information, see the [Cache Scavenger](#cache-scavenger) section below.</span></span>
-   <span data-ttu-id="40714-125">HTTPS est mis en cache par défaut.</span><span class="sxs-lookup"><span data-stu-id="40714-125">Https is cached by default.</span></span> <span data-ttu-id="40714-126">Cela est géré par un paramètre global qui ne peut pas être substitué par les directives de cache définies par l’application.</span><span class="sxs-lookup"><span data-stu-id="40714-126">This is managed by a global setting that cannot be overridden by application-defined cache directives.</span></span> <span data-ttu-id="40714-127">Pour remplacer le paramètre global, sélectionnez l’applet options Internet dans le panneau de configuration, puis accédez à l’onglet Avancé. Cochez la case « ne pas enregistrer les pages chiffrées sur le disque » sous la section « sécurité ».</span><span class="sxs-lookup"><span data-stu-id="40714-127">To override the global setting, select the Internet Options applet in the control panel, and go to the advanced tab. Check the "Do not save encrypted pages to disk" box under the "Security" section.</span></span>

## <a name="cache-scavenger"></a><span data-ttu-id="40714-128">Nettoyage du cache</span><span class="sxs-lookup"><span data-stu-id="40714-128">Cache Scavenger</span></span>

<span data-ttu-id="40714-129">Le nettoyage du cache nettoie régulièrement les éléments du cache.</span><span class="sxs-lookup"><span data-stu-id="40714-129">The cache scavenger periodically cleans items from the cache.</span></span> <span data-ttu-id="40714-130">Si un élément est ajouté au cache et que le cache est plein, l’élément est ajouté au cache et le nettoyage du cache est planifié.</span><span class="sxs-lookup"><span data-stu-id="40714-130">If an item is added to the cache and the cache is full, the item is added to the cache and the cache scavenger is scheduled.</span></span> <span data-ttu-id="40714-131">Si le nettoyage du cache termine un nettoyage et que le cache n’a pas atteint la limite du cache, le nettoyage est planifié pour un autre arrondi lorsqu’un autre élément est ajouté au cache.</span><span class="sxs-lookup"><span data-stu-id="40714-131">If the cache scavenger completes a round of scavenging and the cache has not reached the cache limit, the scavenger is scheduled for another round when another item is added to the cache.</span></span> <span data-ttu-id="40714-132">En général, le nettoyage est planifié lorsqu’un élément ajouté place le cache au-dessus de sa taille limite.</span><span class="sxs-lookup"><span data-stu-id="40714-132">In general, the scavenger is scheduled when an added item puts the cache over its size limit.</span></span> <span data-ttu-id="40714-133">Par défaut, la durée de vie minimale du cache est définie à 10 minutes, sauf indication contraire dans une directive Cache-Control.</span><span class="sxs-lookup"><span data-stu-id="40714-133">By default, the minimum time to live in the cache is set to 10 minutes unless otherwise specified in a cache-control directive.</span></span> <span data-ttu-id="40714-134">Lorsque le nettoyage du cache est initié, il n’y a aucune garantie que les éléments les plus anciens sont les premiers à être supprimés du cache.</span><span class="sxs-lookup"><span data-stu-id="40714-134">When the cache scavenger is initiated, there is no guarantee that the oldest items are the first to be deleted from the cache.</span></span>

<span data-ttu-id="40714-135">Le cache est partagé entre toutes les applications WinINet sur l’ordinateur pour le même utilisateur.</span><span class="sxs-lookup"><span data-stu-id="40714-135">The cache is shared across all WinINet applications on the computer for the same user.</span></span> <span data-ttu-id="40714-136">À compter de Windows Vista et de Windows Server 2008, la taille du cache est définie à 1/32e la taille du disque, avec une taille minimale de 8 Mo et une taille maximale de 50 Mo.</span><span class="sxs-lookup"><span data-stu-id="40714-136">Starting with Windows Vista and Windows Server 2008 the cache size is set to 1/32nd the size of the disk, with a minimum size of 8MB and a maximum size of 50MB.</span></span>

## <a name="using-flags-to-control-caching"></a><span data-ttu-id="40714-137">Utilisation d’indicateurs pour contrôler la mise en cache</span><span class="sxs-lookup"><span data-stu-id="40714-137">Using Flags to Control Caching</span></span>

<span data-ttu-id="40714-138">Les indicateurs de mise en cache permettent à une application de contrôler le moment et la façon dont elle utilise le cache.</span><span class="sxs-lookup"><span data-stu-id="40714-138">The caching flags allow an application to control when and how it uses the cache.</span></span> <span data-ttu-id="40714-139">Ces indicateurs peuvent être utilisés seuls ou en association avec le paramètre *dwFlags* dans des fonctions qui accèdent à des informations ou à des ressources sur Internet.</span><span class="sxs-lookup"><span data-stu-id="40714-139">These flags can be used alone or in combination with the *dwFlags* parameter in functions that access information or resources on the Internet.</span></span> <span data-ttu-id="40714-140">Par défaut, les fonctions stockent toutes les données téléchargées à partir d’Internet.</span><span class="sxs-lookup"><span data-stu-id="40714-140">By default, the functions store all data downloaded from the Internet.</span></span>

<span data-ttu-id="40714-141">Les indicateurs suivants peuvent être utilisés pour contrôler la mise en cache.</span><span class="sxs-lookup"><span data-stu-id="40714-141">The following flags can be used to control caching.</span></span>



| <span data-ttu-id="40714-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="40714-142">Value</span></span>                                                                                                                                                  | <span data-ttu-id="40714-143">Signification</span><span class="sxs-lookup"><span data-stu-id="40714-143">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="40714-144">**\_cache d’indicateur Internet \_ \_ asynchrone**</span><span class="sxs-lookup"><span data-stu-id="40714-144">**INTERNET\_FLAG\_CACHE\_ASYNC**</span></span>](api-flags.md)                                                                            | <span data-ttu-id="40714-145">Cet indicateur est sans effet.</span><span class="sxs-lookup"><span data-stu-id="40714-145">This flag has no effect.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="40714-146">**INTERNET \_ Flag \_ cache en \_ cas d' \_ \_ échec net**</span><span class="sxs-lookup"><span data-stu-id="40714-146">**INTERNET\_FLAG\_CACHE\_IF\_NET\_FAIL**</span></span>](api-flags.md)                                                              | <span data-ttu-id="40714-147">Retourne la ressource à partir du cache en cas d’échec de la demande réseau de la ressource en raison d’une [erreur de \_ \_ \_ réinitialisation de la connexion Internet](wininet-errors.md) ou d’une erreur [ \_ Internet \_ ne peut pas \_ se connecter](wininet-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="40714-147">Returns the resource from the cache if the network request for the resource fails due to an [ERROR\_INTERNET\_CONNECTION\_RESET](wininet-errors.md) or [ERROR\_INTERNET\_CANNOT\_CONNECT](wininet-errors.md) error.</span></span> <span data-ttu-id="40714-148">Cet indicateur est utilisé par [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span><span class="sxs-lookup"><span data-stu-id="40714-148">This flag is used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span>                                                                                                              |
| [<span data-ttu-id="40714-149">**\_cache sans indicateur Internet \_ \_**</span><span class="sxs-lookup"><span data-stu-id="40714-149">**INTERNET\_FLAG\_DONT\_CACHE**</span></span>](api-flags.md)                                                                              | <span data-ttu-id="40714-150">Ne met pas en cache les données, localement ou dans les passerelles.</span><span class="sxs-lookup"><span data-stu-id="40714-150">Does not cache the data, either locally or in any gateways.</span></span> <span data-ttu-id="40714-151">Identique à la valeur par défaut [**, \_ indicateur \_ Internet \_ sans \_ écriture**](api-flags.md)dans le cache.</span><span class="sxs-lookup"><span data-stu-id="40714-151">Identical to the preferred value, [**INTERNET\_FLAG\_NO\_CACHE\_WRITE**](api-flags.md).</span></span>                                                                                                                                                                                                                                                                                 |
|                                                                                                                                                        | <span data-ttu-id="40714-152">Indique qu’il s’agit d’une soumission de formulaires.</span><span class="sxs-lookup"><span data-stu-id="40714-152">Indicates that this is a Forms submission.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="40714-153">[**Internet \_ indicateur \_ du \_ cache**](api-flags.md)[**Internet \_ Flag \_ Forms \_ Submit**](api-flags.md)</span><span class="sxs-lookup"><span data-stu-id="40714-153">[**INTERNET\_FLAG\_FROM\_CACHE**](api-flags.md)[**INTERNET\_FLAG\_FORMS\_SUBMIT**](api-flags.md)</span></span> | <span data-ttu-id="40714-154">N’effectue pas de demandes réseau.</span><span class="sxs-lookup"><span data-stu-id="40714-154">Does not make network requests.</span></span> <span data-ttu-id="40714-155">Toutes les entités sont retournées à partir du cache.</span><span class="sxs-lookup"><span data-stu-id="40714-155">All entities are returned from the cache.</span></span> <span data-ttu-id="40714-156">Si l’élément demandé n’est pas dans le cache, une erreur appropriée, telle qu’un fichier d’erreur \_ \_ \_ introuvable, est retournée.</span><span class="sxs-lookup"><span data-stu-id="40714-156">If the requested item is not in the cache, a suitable error, such as ERROR\_FILE\_NOT\_FOUND, is returned.</span></span> <span data-ttu-id="40714-157">Seule la fonction [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) utilise cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="40714-157">Only the [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) function uses this flag.</span></span>                                                                                                                                                                                                       |
| [<span data-ttu-id="40714-158">**\_indicateur de \_ \_ retour sur Internet**</span><span class="sxs-lookup"><span data-stu-id="40714-158">**INTERNET\_FLAG\_FWD\_BACK**</span></span>](api-flags.md)                                                                                  | <span data-ttu-id="40714-159">Indique que la fonction doit utiliser la copie de la ressource qui se trouve actuellement dans le cache Internet.</span><span class="sxs-lookup"><span data-stu-id="40714-159">Indicates that the function should use the copy of the resource that is currently in the Internet cache.</span></span> <span data-ttu-id="40714-160">La date d’expiration et les autres informations relatives à la ressource ne sont pas vérifiées.</span><span class="sxs-lookup"><span data-stu-id="40714-160">The expiration date and other information about the resource is not checked.</span></span> <span data-ttu-id="40714-161">Si l’élément demandé est introuvable dans le cache Internet, le système tente de localiser la ressource sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="40714-161">If the requested item is not found in the Internet cache, the system attempts to locate the resource on the network.</span></span> <span data-ttu-id="40714-162">Cette valeur a été introduite dans Microsoft Internet Explorer 5 et est associée aux opérations de bouton **suivant** et **précédent** d’Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="40714-162">This value was introduced in Microsoft Internet Explorer 5 and is associated with the **Forward** and **Back** button operations of Internet Explorer.</span></span> |
| [<span data-ttu-id="40714-163">**\_ \_ lien hypertexte indicateur Internet**</span><span class="sxs-lookup"><span data-stu-id="40714-163">**INTERNET\_FLAG\_HYPERLINK**</span></span>](api-flags.md)                                                                                 | <span data-ttu-id="40714-164">Force l’application à recharger une ressource si aucune heure d’expiration et aucune heure de dernière modification n’ont été retournées lorsque la ressource a été stockée dans le cache.</span><span class="sxs-lookup"><span data-stu-id="40714-164">Forces the application to reload a resource if no expire time and no last-modified time were returned when the resource was stored in the cache.</span></span>                                                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="40714-165">**\_indicateur Internet \_ rendre \_ persistant**</span><span class="sxs-lookup"><span data-stu-id="40714-165">**INTERNET\_FLAG\_MAKE\_PERSISTENT**</span></span>](api-flags.md)                                                                    | <span data-ttu-id="40714-166">N'est plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="40714-166">No longer supported.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="40714-167">**l' \_ indicateur Internet \_ doit mettre \_ en cache la \_ demande**</span><span class="sxs-lookup"><span data-stu-id="40714-167">**INTERNET\_FLAG\_MUST\_CACHE\_REQUEST**</span></span>](api-flags.md)                                                             | <span data-ttu-id="40714-168">Entraîne la création d’un fichier temporaire si le fichier ne peut pas être mis en cache.</span><span class="sxs-lookup"><span data-stu-id="40714-168">Causes a temporary file to be created if the file cannot be cached.</span></span> <span data-ttu-id="40714-169">Cela est identique à la valeur par défaut, le [**\_ \_ \_ fichier indicateur Internet requis**](api-flags.md).</span><span class="sxs-lookup"><span data-stu-id="40714-169">This is identical to the preferred value, [**INTERNET\_FLAG\_NEED\_FILE**](api-flags.md).</span></span>                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="40714-170">**fichier de l' \_ indicateur Internet \_ requis \_**</span><span class="sxs-lookup"><span data-stu-id="40714-170">**INTERNET\_FLAG\_NEED\_FILE**</span></span>](api-flags.md)                                                                                | <span data-ttu-id="40714-171">Entraîne la création d’un fichier temporaire si le fichier ne peut pas être mis en cache.</span><span class="sxs-lookup"><span data-stu-id="40714-171">Causes a temporary file to be created if the file cannot be cached.</span></span>                                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="40714-172">**\_indicateur Internet \_ sans \_ \_ écriture dans le cache**</span><span class="sxs-lookup"><span data-stu-id="40714-172">**INTERNET\_FLAG\_NO\_CACHE\_WRITE**</span></span>](api-flags.md)                                                                     | <span data-ttu-id="40714-173">Rejette toute tentative par la fonction de stocker des données téléchargées à partir d’Internet dans le cache.</span><span class="sxs-lookup"><span data-stu-id="40714-173">Rejects any attempt by the function to store data downloaded from the Internet in the cache.</span></span> <span data-ttu-id="40714-174">Cet indicateur est nécessaire si l’application ne souhaite pas que les ressources téléchargées soient stockées localement.</span><span class="sxs-lookup"><span data-stu-id="40714-174">This flag is necessary if the application does not want any downloaded resources to be stored locally.</span></span>                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="40714-175">**\_indicateur Internet \_ sans \_ interface utilisateur**</span><span class="sxs-lookup"><span data-stu-id="40714-175">**INTERNET\_FLAG\_NO\_UI**</span></span>](api-flags.md)                                                                                        | <span data-ttu-id="40714-176">Désactive la boîte de dialogue cookie.</span><span class="sxs-lookup"><span data-stu-id="40714-176">Disables the cookie dialog box.</span></span> <span data-ttu-id="40714-177">Cet indicateur peut être utilisé par [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) et [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (requêtes http uniquement).</span><span class="sxs-lookup"><span data-stu-id="40714-177">This flag can be used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (HTTP requests only).</span></span>                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="40714-178">**\_indicateur Internet \_ hors connexion**</span><span class="sxs-lookup"><span data-stu-id="40714-178">**INTERNET\_FLAG\_OFFLINE**</span></span>](api-flags.md)                                                                                     | <span data-ttu-id="40714-179">Empêche l’application d’envoyer des demandes au réseau.</span><span class="sxs-lookup"><span data-stu-id="40714-179">Prevents the application from sending requests to the network.</span></span> <span data-ttu-id="40714-180">Toutes les requêtes sont résolues à l’aide des ressources stockées dans le cache.</span><span class="sxs-lookup"><span data-stu-id="40714-180">All requests are resolved using the resources stored in the cache.</span></span> <span data-ttu-id="40714-181">Si la ressource ne se trouve pas dans le cache, une erreur appropriée, telle qu’un fichier d’erreur \_ \_ \_ introuvable, est retournée.</span><span class="sxs-lookup"><span data-stu-id="40714-181">If the resource is not in the cache, a suitable error, such as ERROR\_FILE\_NOT\_FOUND, is returned.</span></span>                                                                                                                                                                                                                            |
| [<span data-ttu-id="40714-182">**\_indicateur Internet \_ pragma \_ NoCache**</span><span class="sxs-lookup"><span data-stu-id="40714-182">**INTERNET\_FLAG\_PRAGMA\_NOCACHE**</span></span>](api-flags.md)                                                                      | <span data-ttu-id="40714-183">Force la résolution de la demande par le serveur d’origine, même si une copie mise en cache existe sur le proxy.</span><span class="sxs-lookup"><span data-stu-id="40714-183">Forces the request to be resolved by the origin server, even if a cached copy exists on the proxy.</span></span> <span data-ttu-id="40714-184">La fonction [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (sur les requêtes HTTP et HTTPS uniquement) et la fonction [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) utilisent cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="40714-184">The [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) function (on HTTP and HTTPS requests only) and [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) function use this flag.</span></span>                                                                                                                                                                                               |
| [<span data-ttu-id="40714-185">**\_REchargement des indicateurs Internet \_**</span><span class="sxs-lookup"><span data-stu-id="40714-185">**INTERNET\_FLAG\_RELOAD**</span></span>](api-flags.md)                                                                                       | <span data-ttu-id="40714-186">Force la fonction à récupérer la ressource demandée directement à partir d’Internet.</span><span class="sxs-lookup"><span data-stu-id="40714-186">Forces the function to retrieve the requested resource directly from the Internet.</span></span> <span data-ttu-id="40714-187">Les informations téléchargées sont stockées dans le cache.</span><span class="sxs-lookup"><span data-stu-id="40714-187">The information that is downloaded is stored in the cache.</span></span>                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="40714-188">**resynchronisation des \_ indicateurs Internet \_**</span><span class="sxs-lookup"><span data-stu-id="40714-188">**INTERNET\_FLAG\_RESYNCHRONIZE**</span></span>](api-flags.md)                                                                         | <span data-ttu-id="40714-189">Fait en sorte qu’une application effectue un téléchargement conditionnel de la ressource à partir d’Internet.</span><span class="sxs-lookup"><span data-stu-id="40714-189">Causes an application to perform a conditional download of the resource from the Internet.</span></span> <span data-ttu-id="40714-190">Si la version stockée dans le cache est à jour, les informations sont téléchargées à partir du cache.</span><span class="sxs-lookup"><span data-stu-id="40714-190">If the version stored in the cache is current, the information is downloaded from the cache.</span></span> <span data-ttu-id="40714-191">Dans le cas contraire, les informations sont rechargées à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="40714-191">Otherwise, the information is reloaded from the server.</span></span>                                                                                                                                                                                                                   |



 

## <a name="persistent-caching-functions"></a><span data-ttu-id="40714-192">Fonctions de mise en cache persistantes</span><span class="sxs-lookup"><span data-stu-id="40714-192">Persistent Caching Functions</span></span>

<span data-ttu-id="40714-193">Les clients qui ont besoin de services de mise en cache persistants utilisent les fonctions de mise en cache permanentes pour permettre à leurs applications d’enregistrer des données dans le système de fichiers local pour une utilisation ultérieure, par exemple dans les situations où une liaison à faible bande passante limite l’accès aux données, ou si l’accès n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="40714-193">Clients that need persistent caching services use the persistent caching functions to allow their applications to save data in the local file system for subsequent use, such as in situations where a low-bandwidth link limits access to the data, or the access is not available at all.</span></span>

<span data-ttu-id="40714-194">Les fonctions de cache fournissent une mise en cache persistante et une navigation hors connexion.</span><span class="sxs-lookup"><span data-stu-id="40714-194">The cache functions provide persistent caching and offline browsing.</span></span> <span data-ttu-id="40714-195">À moins que l’indicateur d' [**\_ écriture de \_ \_ cache \_ Internet ne**](api-flags.md) spécifie explicitement aucune mise en cache, les fonctions cachent toutes les données téléchargées à partir du réseau.</span><span class="sxs-lookup"><span data-stu-id="40714-195">Unless the [**INTERNET\_FLAG\_NO\_CACHE\_WRITE**](api-flags.md) flag explicitly specifies no caching, the functions cache all data downloaded from the network.</span></span> <span data-ttu-id="40714-196">Les réponses aux données publiées ne sont pas mises en cache.</span><span class="sxs-lookup"><span data-stu-id="40714-196">The responses to POST data are not cached.</span></span>

## <a name="using-the-persistent-url-cache-functions"></a><span data-ttu-id="40714-197">Utilisation des fonctions de cache des URL persistantes</span><span class="sxs-lookup"><span data-stu-id="40714-197">Using the Persistent URL Cache Functions</span></span>

<span data-ttu-id="40714-198">Les fonctions de cache d’URL persistantes suivantes permettent à une application d’accéder à des informations stockées dans le cache et de les manipuler.</span><span class="sxs-lookup"><span data-stu-id="40714-198">The following persistent URL cache functions allow an application to access and manipulate information stored in the cache.</span></span>



| <span data-ttu-id="40714-199">Fonction</span><span class="sxs-lookup"><span data-stu-id="40714-199">Function</span></span>                                                           | <span data-ttu-id="40714-200">Description</span><span class="sxs-lookup"><span data-stu-id="40714-200">Description</span></span>                                                                                                                                                   |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="40714-201">**CommitUrlCacheEntryA**</span><span class="sxs-lookup"><span data-stu-id="40714-201">**CommitUrlCacheEntryA**</span></span>](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya)               | <span data-ttu-id="40714-202">Met en cache les données du fichier spécifié dans le stockage du cache et les associe à l’URL donnée.</span><span class="sxs-lookup"><span data-stu-id="40714-202">Caches data in the specified file in the cache storage and associates it with the given URL.</span></span>                                                                  |
| [<span data-ttu-id="40714-203">**CommitUrlCacheEntryW**</span><span class="sxs-lookup"><span data-stu-id="40714-203">**CommitUrlCacheEntryW**</span></span>](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentryw)               | <span data-ttu-id="40714-204">Met en cache les données du fichier spécifié dans le stockage du cache et les associe à l’URL donnée.</span><span class="sxs-lookup"><span data-stu-id="40714-204">Caches data in the specified file in the cache storage and associates it with the given URL.</span></span>                                                                  |
| [<span data-ttu-id="40714-205">**CreateUrlCacheEntry**</span><span class="sxs-lookup"><span data-stu-id="40714-205">**CreateUrlCacheEntry**</span></span>](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya)                 | <span data-ttu-id="40714-206">Alloue le stockage de cache demandé et crée un nom de fichier local pour enregistrer l’entrée de cache qui correspond au nom de la source.</span><span class="sxs-lookup"><span data-stu-id="40714-206">Allocates the requested cache storage and creates a local file name for saving the cache entry that corresponds to the source name.</span></span>                           |
| [<span data-ttu-id="40714-207">**CreateUrlCacheGroup**</span><span class="sxs-lookup"><span data-stu-id="40714-207">**CreateUrlCacheGroup**</span></span>](/windows/desktop/api/Wininet/nf-wininet-createurlcachegroup)                 | <span data-ttu-id="40714-208">Génère une identification du groupe de caches.</span><span class="sxs-lookup"><span data-stu-id="40714-208">Generates a cache group identification.</span></span>                                                                                                                       |
| [<span data-ttu-id="40714-209">**DeleteUrlCacheEntry**</span><span class="sxs-lookup"><span data-stu-id="40714-209">**DeleteUrlCacheEntry**</span></span>](/windows/desktop/api/Wininet/nf-wininet-deleteurlcacheentry)                 | <span data-ttu-id="40714-210">Supprime le fichier associé au nom de la source du cache, si ce fichier existe.</span><span class="sxs-lookup"><span data-stu-id="40714-210">Removes the file associated with the source name from the cache, if the file exists.</span></span>                                                                          |
| [<span data-ttu-id="40714-211">**DeleteUrlCacheGroup**</span><span class="sxs-lookup"><span data-stu-id="40714-211">**DeleteUrlCacheGroup**</span></span>](/windows/desktop/api/Wininet/nf-wininet-deleteurlcachegroup)                 | <span data-ttu-id="40714-212">Libère un **GROUPID** et tout état associé dans le fichier d’index du cache.</span><span class="sxs-lookup"><span data-stu-id="40714-212">Releases a **GROUPID** and any associated state in the cache index file.</span></span>                                                                                      |
| [<span data-ttu-id="40714-213">**FindCloseUrlCache**</span><span class="sxs-lookup"><span data-stu-id="40714-213">**FindCloseUrlCache**</span></span>](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache)                     | <span data-ttu-id="40714-214">Ferme le handle d’énumération spécifié.</span><span class="sxs-lookup"><span data-stu-id="40714-214">Closes the specified enumeration handle.</span></span>                                                                                                                      |
| [<span data-ttu-id="40714-215">**FindFirstUrlCacheEntry**</span><span class="sxs-lookup"><span data-stu-id="40714-215">**FindFirstUrlCacheEntry**</span></span>](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya)           | <span data-ttu-id="40714-216">Commence l’énumération du cache.</span><span class="sxs-lookup"><span data-stu-id="40714-216">Begins the enumeration of the cache.</span></span>                                                                                                                          |
| [<span data-ttu-id="40714-217">**FindFirstUrlCacheEntryEx**</span><span class="sxs-lookup"><span data-stu-id="40714-217">**FindFirstUrlCacheEntryEx**</span></span>](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentryexa)       | <span data-ttu-id="40714-218">Commence une énumération filtrée du cache.</span><span class="sxs-lookup"><span data-stu-id="40714-218">Begins a filtered enumeration of the cache.</span></span>                                                                                                                   |
| [<span data-ttu-id="40714-219">**FindNextUrlCacheEntry**</span><span class="sxs-lookup"><span data-stu-id="40714-219">**FindNextUrlCacheEntry**</span></span>](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya)             | <span data-ttu-id="40714-220">Récupère l’entrée suivante dans le cache.</span><span class="sxs-lookup"><span data-stu-id="40714-220">Retrieves the next entry in the cache.</span></span>                                                                                                                        |
| [<span data-ttu-id="40714-221">**FindNextUrlCacheEntryEx**</span><span class="sxs-lookup"><span data-stu-id="40714-221">**FindNextUrlCacheEntryEx**</span></span>](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentryexa)         | <span data-ttu-id="40714-222">Récupère l’entrée suivante dans une énumération de cache filtrée.</span><span class="sxs-lookup"><span data-stu-id="40714-222">Retrieves the next entry in a filtered cache enumeration.</span></span>                                                                                                     |
| [<span data-ttu-id="40714-223">**GetUrlCacheEntryInfo**</span><span class="sxs-lookup"><span data-stu-id="40714-223">**GetUrlCacheEntryInfo**</span></span>](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa)               | <span data-ttu-id="40714-224">Récupère des informations sur une entrée du cache.</span><span class="sxs-lookup"><span data-stu-id="40714-224">Retrieves information about a cache entry.</span></span>                                                                                                                    |
| [<span data-ttu-id="40714-225">**GetUrlCacheEntryInfoEx**</span><span class="sxs-lookup"><span data-stu-id="40714-225">**GetUrlCacheEntryInfoEx**</span></span>](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoexa)           | <span data-ttu-id="40714-226">Recherche l’URL après avoir traduit toutes les redirections mises en cache qui seraient appliquées en mode hors connexion par [**HTTPSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span><span class="sxs-lookup"><span data-stu-id="40714-226">Searches for the URL after translating any cached redirections that would be applied in offline mode by [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span></span>           |
| [<span data-ttu-id="40714-227">**ReadUrlCacheEntryStream**</span><span class="sxs-lookup"><span data-stu-id="40714-227">**ReadUrlCacheEntryStream**</span></span>](/windows/desktop/api/Wininet/nf-wininet-readurlcacheentrystream)         | <span data-ttu-id="40714-228">Lit les données mises en cache à partir d’un flux qui a été ouvert à l’aide de [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama).</span><span class="sxs-lookup"><span data-stu-id="40714-228">Reads the cached data from a stream that has been opened using [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama).</span></span>                            |
| [<span data-ttu-id="40714-229">**RetrieveUrlCacheEntryFile**</span><span class="sxs-lookup"><span data-stu-id="40714-229">**RetrieveUrlCacheEntryFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea)     | <span data-ttu-id="40714-230">Récupère une entrée de cache du cache sous la forme d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="40714-230">Retrieves a cache entry from the cache in the form of a file.</span></span>                                                                                                 |
| [<span data-ttu-id="40714-231">**RetrieveUrlCacheEntryStream**</span><span class="sxs-lookup"><span data-stu-id="40714-231">**RetrieveUrlCacheEntryStream**</span></span>](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama) | <span data-ttu-id="40714-232">Offre le moyen le plus efficace et indépendant de l’implémentation d’accéder aux données du cache.</span><span class="sxs-lookup"><span data-stu-id="40714-232">Provides the most efficient and implementation-independent way of accessing the cache data.</span></span>                                                                   |
| [<span data-ttu-id="40714-233">**SetUrlCacheEntryGroup**</span><span class="sxs-lookup"><span data-stu-id="40714-233">**SetUrlCacheEntryGroup**</span></span>](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup)             | <span data-ttu-id="40714-234">Ajoute ou supprime des entrées d’un groupe de cache.</span><span class="sxs-lookup"><span data-stu-id="40714-234">Adds or removes entries from a cache group.</span></span>                                                                                                                   |
| [<span data-ttu-id="40714-235">**SetUrlCacheEntryInfo**</span><span class="sxs-lookup"><span data-stu-id="40714-235">**SetUrlCacheEntryInfo**</span></span>](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentryinfoa)               | <span data-ttu-id="40714-236">Définit les membres spécifiés de la structure d' [**\_ \_ \_ informations d’entrée du cache Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) .</span><span class="sxs-lookup"><span data-stu-id="40714-236">Sets the specified members of the [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) structure.</span></span>                                                |
| [<span data-ttu-id="40714-237">**UnlockUrlCacheEntryFile**</span><span class="sxs-lookup"><span data-stu-id="40714-237">**UnlockUrlCacheEntryFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile)         | <span data-ttu-id="40714-238">Déverrouille l’entrée de cache qui a été verrouillée lors de la récupération du fichier pour une utilisation à partir du cache par [**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea).</span><span class="sxs-lookup"><span data-stu-id="40714-238">Unlocks the cache entry that was locked when the file was retrieved for use from the cache by [**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea).</span></span> |
| [<span data-ttu-id="40714-239">**UnlockUrlCacheEntryStream**</span><span class="sxs-lookup"><span data-stu-id="40714-239">**UnlockUrlCacheEntryStream**</span></span>](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentrystream)     | <span data-ttu-id="40714-240">Ferme le flux qui a été récupéré à l’aide de [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama).</span><span class="sxs-lookup"><span data-stu-id="40714-240">Closes the stream that has been retrieved using [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama).</span></span>                                           |



 

### <a name="enumerating-the-cache"></a><span data-ttu-id="40714-241">Énumération du cache</span><span class="sxs-lookup"><span data-stu-id="40714-241">Enumerating the Cache</span></span>

<span data-ttu-id="40714-242">Les fonctions [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) et [**FindNextUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya) énumèrent les informations stockées dans le cache.</span><span class="sxs-lookup"><span data-stu-id="40714-242">The [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) and [**FindNextUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya) functions enumerate the information stored in the cache.</span></span> <span data-ttu-id="40714-243">[**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) démarre l’énumération en adoptant un modèle de recherche, une mémoire tampon et une taille de mémoire tampon pour créer un handle et retourner la première entrée du cache.</span><span class="sxs-lookup"><span data-stu-id="40714-243">[**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) starts the enumeration by taking a search pattern, a buffer, and a buffer size to create a handle and return the first cache entry.</span></span> <span data-ttu-id="40714-244">[**FindNextUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya) prend le handle créé par [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya), une mémoire tampon et une taille de mémoire tampon pour retourner la prochaine entrée de cache.</span><span class="sxs-lookup"><span data-stu-id="40714-244">[**FindNextUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya) takes the handle created by [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya), a buffer, and a buffer size to return the next cache entry.</span></span>

<span data-ttu-id="40714-245">Les deux fonctions stockent une structure d' [**\_ informations d' \_ entrée \_ de cache Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="40714-245">Both functions store an [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) structure in the buffer.</span></span> <span data-ttu-id="40714-246">La taille de cette structure varie pour chaque entrée.</span><span class="sxs-lookup"><span data-stu-id="40714-246">The size of this structure varies for each entry.</span></span> <span data-ttu-id="40714-247">Si la taille de la mémoire tampon passée à l’une ou l’autre des fonctions est insuffisante, la fonction échoue et [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne l’erreur \_ mémoire tampon insuffisante \_ .</span><span class="sxs-lookup"><span data-stu-id="40714-247">If the buffer size passed to either function is insufficient, the function fails and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="40714-248">La variable de taille de la mémoire tampon contient la taille de la mémoire tampon nécessaire pour récupérer cette entrée de cache.</span><span class="sxs-lookup"><span data-stu-id="40714-248">The buffer size variable contains the buffer size that was needed to retrieve that cache entry.</span></span> <span data-ttu-id="40714-249">Une mémoire tampon de la taille indiquée par la variable de taille de mémoire tampon doit être allouée, et la fonction doit être appelée à nouveau avec la nouvelle mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="40714-249">A buffer of the size indicated by the buffer size variable should be allocated, and the function should be called again with the new buffer.</span></span>

<span data-ttu-id="40714-250">La structure des informations d' [**\_ entrée du cache \_ \_ Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) contient la taille de la structure, l’URL des informations mises en cache, le nom du fichier local, le type d’entrée du cache, le nombre d’utilisations, le taux d’accès, la taille, l’heure de la dernière modification, l’expiration, l’heure de la dernière synchronisation, les informations d’en-tête et l’extension de nom</span><span class="sxs-lookup"><span data-stu-id="40714-250">The [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) structure contains the structure size, URL of the cached information, local file name, cache entry type, use count, hit rate, size, last modified time, expiration, last access, last synchronized time, header information, header information size, and file name extension.</span></span>

<span data-ttu-id="40714-251">La fonction [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) prend un modèle de recherche, une mémoire tampon qui stocke la structure d’informations d' [**entrée du \_ cache \_ \_ Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) et la taille de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="40714-251">The [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) function takes a search pattern, a buffer that stores the [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) structure, and the buffer size.</span></span> <span data-ttu-id="40714-252">Actuellement, seul le modèle de recherche par défaut, qui retourne toutes les entrées de cache, est implémenté.</span><span class="sxs-lookup"><span data-stu-id="40714-252">Currently, only the default search pattern, which returns all cache entries, is implemented.</span></span>

<span data-ttu-id="40714-253">Une fois le cache énuméré, l’application doit appeler [**FindCloseUrlCache**](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache) pour fermer le descripteur d’énumération du cache.</span><span class="sxs-lookup"><span data-stu-id="40714-253">After the cache is enumerated, the application should call [**FindCloseUrlCache**](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache) to close the cache enumeration handle.</span></span>

<span data-ttu-id="40714-254">L’exemple suivant affiche l’URL de chaque entrée de cache dans une zone de liste, **IDC \_ CacheList**.</span><span class="sxs-lookup"><span data-stu-id="40714-254">The following example displays each cache entry's URL in a list box, **IDC\_CacheList**.</span></span> <span data-ttu-id="40714-255">Elle utilise \_ \_ \_ la taille maximale des informations d’entrée du cache \_ pour allouer initialement une mémoire tampon, puisque les versions antérieures de l’API WinInet n’énumèrent pas correctement le cache.</span><span class="sxs-lookup"><span data-stu-id="40714-255">It uses MAX\_CACHE\_ENTRY\_INFO\_SIZE to initially allocate a buffer, since early versions of the WinINet API do not enumerate the cache properly otherwise.</span></span> <span data-ttu-id="40714-256">Les versions ultérieures énumèrent le cache correctement et il n’y a aucune limite de taille de cache.</span><span class="sxs-lookup"><span data-stu-id="40714-256">Later versions do enumerate the cache properly and there is no cache size limit.</span></span> <span data-ttu-id="40714-257">Toutes les applications qui s’exécutent sur des ordinateurs avec la version de l’API WinINet d’Internet Explorer 4,0 doivent allouer une mémoire tampon de la taille requise.</span><span class="sxs-lookup"><span data-stu-id="40714-257">All applications that run on computers with the version of the WinINet API from Internet Explorer 4.0 must allocate a buffer of the required size.</span></span> <span data-ttu-id="40714-258">Pour plus d’informations, consultez [utilisation de mémoires tampons](appendix-b-using-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="40714-258">For more information, see [Using Buffers](appendix-b-using-buffers.md).</span></span>


```C++
int WINAPI EnumerateCacheOld(HWND hX)
{
    DWORD dwEntrySize;
    LPINTERNET_CACHE_ENTRY_INFO lpCacheEntry;
    DWORD MAX_CACHE_ENTRY_INFO_SIZE = 4096;
    HANDLE hCacheDir;
    int nCount=0;

    SendDlgItemMessage(hX,IDC_CacheList,LB_RESETCONTENT,0,0);
    
    SetCursor(LoadCursor(NULL,IDC_WAIT));

    dwEntrySize = MAX_CACHE_ENTRY_INFO_SIZE;
    lpCacheEntry = (LPINTERNET_CACHE_ENTRY_INFO) new char[dwEntrySize];
    lpCacheEntry->dwStructSize = dwEntrySize;

again:

    hCacheDir = FindFirstUrlCacheEntry(NULL,
                                       lpCacheEntry,
                                       &dwEntrySize);
    if (!hCacheDir)                                             
    {
        delete[]lpCacheEntry;
        switch(GetLastError())
        {
            case ERROR_NO_MORE_ITEMS: 
                TCHAR tempout[80];
                _stprintf_s(tempout, 
                            80,   
                            TEXT("The number of cache entries = %d \n"),
                            nCount);
                MessageBox(hX,tempout,TEXT("Cache Enumeration"),MB_OK);
                FindCloseUrlCache(hCacheDir);
                SetCursor(LoadCursor(NULL,IDC_ARROW));
                return TRUE;
                break;
            case ERROR_INSUFFICIENT_BUFFER:
                lpCacheEntry = (LPINTERNET_CACHE_ENTRY_INFO) 
                                new char[dwEntrySize];
                lpCacheEntry->dwStructSize = dwEntrySize;
                goto again;
                break;
            default:
                ErrorOut( hX,GetLastError(),
                          TEXT("FindNextUrlCacheEntry Init"));
                FindCloseUrlCache(hCacheDir);
                SetCursor(LoadCursor(NULL,IDC_ARROW));
                return FALSE;
        }
    }

    SendDlgItemMessage(hX,IDC_CacheList,LB_ADDSTRING,
                       0,(LPARAM)(lpCacheEntry->lpszSourceUrlName));
    nCount++;
    delete (lpCacheEntry);

    do 
    {
        dwEntrySize = MAX_CACHE_ENTRY_INFO_SIZE;
        lpCacheEntry = (LPINTERNET_CACHE_ENTRY_INFO) new char[dwEntrySize];
        lpCacheEntry->dwStructSize = dwEntrySize;

retry:
        if (!FindNextUrlCacheEntry(hCacheDir,
                                   lpCacheEntry, 
                                   &dwEntrySize))
        {
            delete[]lpCacheEntry;
            switch(GetLastError())
            {
                case ERROR_NO_MORE_ITEMS: 
                    TCHAR tempout[80];
                    _stprintf_s(tempout,
                                80,
                                TEXT("The number of cache entries = %d \n"),nCount);
                    MessageBox(hX,
                               tempout,
                               TEXT("Cache Enumeration"),MB_OK);
                    FindCloseUrlCache(hCacheDir);
                    return TRUE;
                    break;
                case ERROR_INSUFFICIENT_BUFFER:
                    lpCacheEntry = 
                             (LPINTERNET_CACHE_ENTRY_INFO) 
                              new char[dwEntrySize];
                    lpCacheEntry->dwStructSize = dwEntrySize;
                    goto retry;
                    break;
                default:
                    ErrorOut(hX,
                             GetLastError(),
                             TEXT("FindNextUrlCacheEntry Init"));
                    FindCloseUrlCache(hCacheDir);
                    return FALSE;
            }
        }

        SendDlgItemMessage(hX,
                           IDC_CacheList,LB_ADDSTRING,
                           0,
                          (LPARAM)(lpCacheEntry->lpszSourceUrlName));
        nCount++;
        delete[] lpCacheEntry;        
    }  while (TRUE);

    SetCursor(LoadCursor(NULL,IDC_ARROW));
    return TRUE;        
}
```



### <a name="retrieving-cache-entry-information"></a><span data-ttu-id="40714-259">Récupération des informations d’entrée du cache</span><span class="sxs-lookup"><span data-stu-id="40714-259">Retrieving Cache Entry Information</span></span>

<span data-ttu-id="40714-260">La fonction [**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) vous permet de récupérer la structure d’informations d' [**entrée du \_ cache \_ \_ Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) pour l’URL spécifiée.</span><span class="sxs-lookup"><span data-stu-id="40714-260">The [**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) function lets you retrieve the [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) structure for the specified URL.</span></span> <span data-ttu-id="40714-261">Cette structure contient la taille de la structure, l’URL des informations mises en cache, le nom du fichier local, le type d’entrée du cache, le nombre d’utilisations, le taux d’accès, la taille, l’heure de la dernière modification, l’expiration, l’heure de la dernière synchronisation, les informations d’en-tête, la taille des informations d’en-tête et l’extension</span><span class="sxs-lookup"><span data-stu-id="40714-261">This structure contains the structure size, URL of the cached information, local file name, cache entry type, use count, hit rate, size, last modified time, expiration, last access, last synchronized time, header information, header information size, and file name extension.</span></span>

<span data-ttu-id="40714-262">[**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) accepte une URL, une mémoire tampon pour une structure d' [**\_ \_ \_ informations d’entrée du cache Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) et la taille de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="40714-262">[**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) accepts a URL, a buffer for an [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) structure, and the buffer size.</span></span> <span data-ttu-id="40714-263">Si l’URL est trouvée, les informations sont copiées dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="40714-263">If the URL is found, the information is copied into the buffer.</span></span> <span data-ttu-id="40714-264">Dans le cas contraire, la fonction échoue et [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne le fichier d’erreur \_ \_ \_ introuvable.</span><span class="sxs-lookup"><span data-stu-id="40714-264">Otherwise, the function fails and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_FILE\_NOT\_FOUND.</span></span> <span data-ttu-id="40714-265">Si la taille de la mémoire tampon est insuffisante pour stocker les informations d’entrée du cache, la fonction échoue et [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne une erreur de \_ mémoire tampon insuffisante \_ .</span><span class="sxs-lookup"><span data-stu-id="40714-265">If the buffer size is insufficient to store the cache entry information, the function fails and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="40714-266">La taille requise pour récupérer les informations est stockée dans la variable de taille de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="40714-266">The size required to retrieve the information is stored in the buffer size variable.</span></span>

<span data-ttu-id="40714-267">[**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) n’effectue aucune analyse d’URL ; par conséquent, une URL qui contient une ancre ( \# ) ne se trouve pas dans le cache, même si la ressource est mise en cache.</span><span class="sxs-lookup"><span data-stu-id="40714-267">[**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) does not do any URL parsing, so a URL that contains an anchor (\#) will not be found in the cache, even if the resource is cached.</span></span> <span data-ttu-id="40714-268">Par exemple, si l’URL « https://example.com/example.htm\#sample » est passée, la fonction retourne le \_ fichier \_ \_ d’erreur introuvable même si « https://example.com/example.htm » se trouve dans le cache.</span><span class="sxs-lookup"><span data-stu-id="40714-268">For example, if the URL "https://example.com/example.htm\#sample" is passed, the function returns ERROR\_FILE\_NOT\_FOUND even if "https://example.com/example.htm" is in the cache.</span></span>

<span data-ttu-id="40714-269">L’exemple suivant récupère les informations d’entrée de cache pour l’URL spécifiée.</span><span class="sxs-lookup"><span data-stu-id="40714-269">The following example retrieves the cache entry information for the specified URL.</span></span> <span data-ttu-id="40714-270">La fonction affiche ensuite les informations d’en-tête dans la zone d’édition **IDC \_ CacheDump** .</span><span class="sxs-lookup"><span data-stu-id="40714-270">The function then displays the header information in the **IDC\_CacheDump** edit box.</span></span>


```C++
int WINAPI GetCacheEntryInfo(HWND hX,LPTSTR lpszUrl)
{
    DWORD dwEntrySize=0;
    LPINTERNET_CACHE_ENTRY_INFO lpCacheEntry;

    SetCursor(LoadCursor(NULL,IDC_WAIT));
    if (!GetUrlCacheEntryInfo(lpszUrl,NULL,&dwEntrySize))
    {
        if (GetLastError()!=ERROR_INSUFFICIENT_BUFFER)
        {
            ErrorOut(hX,GetLastError(),TEXT("GetUrlCacheEntryInfo"));
            SetCursor(LoadCursor(NULL,IDC_ARROW));
            return FALSE;
        }
        else
            lpCacheEntry = (LPINTERNET_CACHE_ENTRY_INFO) 
                            new char[dwEntrySize];
    }
    else
        return FALSE; // should not be successful w/ NULL buffer
                      // and 0 size

    if (!GetUrlCacheEntryInfo(lpszUrl,lpCacheEntry,&dwEntrySize))
    {
        ErrorOut(hX,GetLastError(),TEXT("GetUrlCacheEntryInfo"));
        SetCursor(LoadCursor(NULL,IDC_ARROW));
        return FALSE;
    }
    else
    {
        if ((lpCacheEntry->dwHeaderInfoSize)!=0)
        {
            LPSTR(lpCacheEntry->lpHeaderInfo)
                                [lpCacheEntry->dwHeaderInfoSize]=TEXT('\0');
            SetDlgItemText(hX,IDC_Headers,
                           lpCacheEntry->lpHeaderInfo);
        }
        else
        {
            SetDlgItemText(hX,IDC_Headers,TEXT("None"));
        }

        SetCursor(LoadCursor(NULL,IDC_ARROW));
        return TRUE;
    }
        
}
```



### <a name="creating-a-cache-entry"></a><span data-ttu-id="40714-271">Création d’une entrée de cache</span><span class="sxs-lookup"><span data-stu-id="40714-271">Creating a Cache Entry</span></span>

<span data-ttu-id="40714-272">Une application utilise les fonctions [**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya) et [**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya) pour créer une entrée de cache.</span><span class="sxs-lookup"><span data-stu-id="40714-272">An application uses the [**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya) and [**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya) functions to create a cache entry.</span></span>

<span data-ttu-id="40714-273">[**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya) accepte l’URL, la taille de fichier attendue et l’extension de nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="40714-273">[**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya) accepts the URL, expected file size, and file name extension.</span></span> <span data-ttu-id="40714-274">La fonction crée ensuite un nom de fichier local pour enregistrer l’entrée de cache qui correspond à l’URL et à l’extension de nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="40714-274">The function then creates a local file name for saving the cache entry that corresponds to the URL and file name extension.</span></span>

<span data-ttu-id="40714-275">À l’aide du nom de fichier local, écrivez les données dans le fichier local.</span><span class="sxs-lookup"><span data-stu-id="40714-275">Using the local file name, write the data into the local file.</span></span> <span data-ttu-id="40714-276">Une fois que les données ont été écrites dans le fichier local, l’application doit appeler [**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya).</span><span class="sxs-lookup"><span data-stu-id="40714-276">After the data has been written to the local file, the application should call [**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya).</span></span>

<span data-ttu-id="40714-277">[**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya) accepte l’URL, le nom de fichier local, l’expiration, l’heure de dernière modification, le type d’entrée du cache, les informations d’en-tête, la taille des informations d’en-tête et l’extension de nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="40714-277">[**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya) accepts the URL, local file name, expiration, last modified time, cache entry type, header information, header information size, and file name extension.</span></span> <span data-ttu-id="40714-278">La fonction met ensuite en cache les données dans le fichier spécifié dans le stockage du cache et les associe à l’URL donnée.</span><span class="sxs-lookup"><span data-stu-id="40714-278">The function then caches data in the file specified in the cache storage and associates it with the given URL.</span></span>

<span data-ttu-id="40714-279">L’exemple suivant utilise le nom de fichier local, créé par un appel précédent à [**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya), stocké dans la zone de texte, par **IDC \_ fichier_local**, pour stocker le texte de la zone de texte, **IDC \_ CacheDump**, dans l’entrée de cache.</span><span class="sxs-lookup"><span data-stu-id="40714-279">The following example uses the local file name, created by a previous call to [**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya), stored in the text box, **IDC\_LocalFile**, to store the text from the text box, **IDC\_CacheDump**, in the cache entry.</span></span> <span data-ttu-id="40714-280">Une fois que les données ont été écrites dans le fichier à l’aide de **fopen**, **fprintf** et **fclose**, l’entrée est validée à l’aide de [**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya).</span><span class="sxs-lookup"><span data-stu-id="40714-280">After the data has been written to the file using **fopen**, **fprintf**, and **fclose**, the entry is committed using [**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya).</span></span>


```C++
int WINAPI CommitEntry(HWND hX)
{
    LPTSTR lpszUrl, lpszExt, lpszFileName;
    LPTSTR lpszData,lpszSize;
    DWORD dwSize;
    DWORD dwEntryType=0;
    FILE *lpfCacheEntry;
    LPFILETIME lpdtmExpire, lpdtmLastModified;
    LPSYSTEMTIME lpdtmSysTime;
    errno_t err;

    if( SendDlgItemMessage(hX,IDC_RBNormal,BM_GETCHECK,0,0) )
    {
        dwEntryType = dwEntryType + NORMAL_CACHE_ENTRY;
    }
    else if( SendDlgItemMessage(hX,IDC_RBSticky, BM_GETCHECK,0,0) )
    {
        dwEntryType = dwEntryType + STICKY_CACHE_ENTRY;
    }
    else if(SendDlgItemMessage( hX,IDC_RBSparse, BM_GETCHECK,0,0) )
    {
        dwEntryType = dwEntryType + SPARSE_CACHE_ENTRY;
    }
 

    if( SendDlgItemMessage(hX,IDC_RBCookie, BM_GETCHECK,0,0))
    {
            dwEntryType = dwEntryType + COOKIE_CACHE_ENTRY;
    }
    else if( SendDlgItemMessage(hX,IDC_RBUrl, BM_GETCHECK,0,0) )
    {
        dwEntryType = dwEntryType + URLHISTORY_CACHE_ENTRY;
    }


    if( SendDlgItemMessage(hX,IDC_RBNone, BM_GETCHECK,0,0) )
    {
        dwEntryType=0;
    }
        
    lpdtmSysTime = new SYSTEMTIME;
    lpdtmExpire = new FILETIME;
    lpdtmLastModified = new FILETIME;

    GetLocalTime(lpdtmSysTime);
    SystemTimeToFileTime(lpdtmSysTime,lpdtmExpire);
    SystemTimeToFileTime(lpdtmSysTime,lpdtmLastModified);
    delete(lpdtmSysTime);

    lpszUrl = new TCHAR[MAX_PATH];
    lpszFileName = new TCHAR[MAX_PATH];
    lpszExt = new TCHAR[5];
    lpszSize = new TCHAR[10];

    GetDlgItemText(hX,IDC_SourceURL,lpszUrl,MAX_PATH);
    GetDlgItemText(hX,IDC_LocalFile,lpszFileName,MAX_PATH);
    GetDlgItemText(hX,IDC_FileExt,lpszExt,5);

    GetDlgItemText(hX,IDC_SizeLow,lpszSize,10);
    dwSize = (DWORD)_ttol(lpszSize);
    delete(lpszSize);

    if (dwSize==0)
    {
        if((MessageBox(hX,
                       TEXT("Incorrect File Size.\nUsing 8000 characters, Okay?\n"),
                       TEXT("Commit Entry"),MB_YESNO))
                        ==IDYES)
        {
            dwSize = 8000;
        }
        else
        {
            return FALSE;
        }
    }

    lpszData = new TCHAR[dwSize];
    GetDlgItemText(hX,IDC_CacheDump,lpszData,dwSize);
        
     err = _tfopen_s(&lpfCacheEntry,lpszFileName,_T("w"));
     if (err)
        return FALSE;
    fprintf(lpfCacheEntry,"%s",lpszData);
    fclose(lpfCacheEntry);
    delete(lpszData);

    if ( !CommitUrlCacheEntry( lpszUrl, 
                               lpszFileName, 
                               *lpdtmExpire,
                               *lpdtmLastModified, 
                               dwEntryType,
                               NULL,
                               0,
                               lpszExt,
                               0) )
    {
        ErrorOut(hX,GetLastError(),TEXT("Commit Cache Entry"));
        delete(lpszUrl);
        delete(lpszFileName);
        delete(lpszExt);
        delete(lpdtmExpire);
        delete(lpdtmLastModified);
        return FALSE;
    }
    else
    {
        delete(lpszUrl);
        delete(lpszFileName);
        delete(lpszExt);
        delete(lpdtmExpire);
        delete(lpdtmLastModified);
        return TRUE;
    }
}
```



### <a name="deleting-a-cache-entry"></a><span data-ttu-id="40714-281">Suppression d’une entrée de cache</span><span class="sxs-lookup"><span data-stu-id="40714-281">Deleting a Cache Entry</span></span>

<span data-ttu-id="40714-282">La fonction [**DeleteUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-deleteurlcacheentry) prend une URL et supprime le fichier cache qui lui est associé.</span><span class="sxs-lookup"><span data-stu-id="40714-282">The [**DeleteUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-deleteurlcacheentry) function takes a URL and removes the cache file associated with it.</span></span> <span data-ttu-id="40714-283">Si le fichier cache n’existe pas, la fonction échoue et [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne le \_ fichier d’erreur \_ \_ introuvable.</span><span class="sxs-lookup"><span data-stu-id="40714-283">If the cache file does not exist, the function fails and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_FILE\_NOT\_FOUND.</span></span> <span data-ttu-id="40714-284">Si le fichier cache est actuellement verrouillé ou en cours d’utilisation, la fonction échoue et [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne l’erreur \_ accès \_ refusé.</span><span class="sxs-lookup"><span data-stu-id="40714-284">If the cache file is currently locked or in use, the function fails and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_ACCESS\_DENIED.</span></span> <span data-ttu-id="40714-285">Le fichier est supprimé lorsqu’il est déverrouillé.</span><span class="sxs-lookup"><span data-stu-id="40714-285">The file is deleted when unlocked.</span></span>

### <a name="retrieving-cache-entry-files"></a><span data-ttu-id="40714-286">Récupération des fichiers d’entrée du cache</span><span class="sxs-lookup"><span data-stu-id="40714-286">Retrieving Cache Entry Files</span></span>

<span data-ttu-id="40714-287">Pour les applications qui requièrent le nom de fichier d’une ressource, utilisez les fonctions [**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea) et [**UnlockUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile) .</span><span class="sxs-lookup"><span data-stu-id="40714-287">For applications that require the file name of a resource, use the [**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea) and [**UnlockUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile) functions.</span></span> <span data-ttu-id="40714-288">Les applications qui n’ont pas besoin du nom de fichier doivent utiliser les fonctions [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama), [**ReadUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-readurlcacheentrystream)et [**UnlockUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentrystream) pour récupérer les informations dans le cache.</span><span class="sxs-lookup"><span data-stu-id="40714-288">Applications that do not require the file name should use the [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama), [**ReadUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-readurlcacheentrystream), and [**UnlockUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentrystream) functions to retrieve the information in the cache.</span></span>

<span data-ttu-id="40714-289">[**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama) n’effectue aucune analyse d’URL ; par conséquent, une URL qui contient une ancre ( \# ) ne se trouve pas dans le cache, même si la ressource est mise en cache.</span><span class="sxs-lookup"><span data-stu-id="40714-289">[**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama) does not do any URL parsing, so a URL that contains an anchor (\#) will not be found in the cache, even if the resource is cached.</span></span> <span data-ttu-id="40714-290">Par exemple, si l’URL « https://example.com/example.htm\#sample » est passée, la fonction retourne le \_ fichier \_ \_ d’erreur introuvable même si « https://example.com/example.htm » se trouve dans le cache.</span><span class="sxs-lookup"><span data-stu-id="40714-290">For example, if the URL "https://example.com/example.htm\#sample" is passed, the function returns ERROR\_FILE\_NOT\_FOUND even if "https://example.com/example.htm" is in the cache.</span></span>

<span data-ttu-id="40714-291">[**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea) accepte une URL, une mémoire tampon qui stocke la structure des [**\_ informations d' \_ entrée \_ du cache Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) et la taille de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="40714-291">[**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea) accepts a URL, a buffer that stores the [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) structure, and the buffer size.</span></span> <span data-ttu-id="40714-292">La fonction est récupérée et verrouillée pour l’appelant.</span><span class="sxs-lookup"><span data-stu-id="40714-292">The function is retrieved and locked for the caller.</span></span>

<span data-ttu-id="40714-293">Une fois que les informations du fichier ont été utilisées, l’application doit appeler [**UnlockUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile) pour déverrouiller le fichier.</span><span class="sxs-lookup"><span data-stu-id="40714-293">After the information in the file has been used, the application should call [**UnlockUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile) to unlock the file.</span></span>

### <a name="cache-groups"></a><span data-ttu-id="40714-294">Groupes de cache</span><span class="sxs-lookup"><span data-stu-id="40714-294">Cache Groups</span></span>

<span data-ttu-id="40714-295">Pour créer un groupe de caches, la fonction [**CreateUrlCacheGroup**](/windows/desktop/api/Wininet/nf-wininet-createurlcachegroup) doit être appelée pour générer un **GROUPID** pour le groupe de cache.</span><span class="sxs-lookup"><span data-stu-id="40714-295">To create a cache group, the [**CreateUrlCacheGroup**](/windows/desktop/api/Wininet/nf-wininet-createurlcachegroup) function must be called to generate a **GROUPID** for the cache group.</span></span> <span data-ttu-id="40714-296">Les entrées peuvent être ajoutées au groupe de cache en fournissant l’URL de l’entrée du cache et \_ l' \_ indicateur ajouter du groupe de cache Internet \_ à la fonction [**SetUrlCacheEntryGroup**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup) .</span><span class="sxs-lookup"><span data-stu-id="40714-296">Entries can be added to the cache group by supplying the cache entry's URL and the INTERNET\_CACHE\_GROUP\_ADD flag to the [**SetUrlCacheEntryGroup**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup) function.</span></span> <span data-ttu-id="40714-297">Pour supprimer une entrée de cache d’un groupe, transmettez l’URL de l’entrée de cache et l' \_ \_ indicateur de suppression du groupe de cache Internet \_ à [**SetUrlCacheEntryGroup**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup).</span><span class="sxs-lookup"><span data-stu-id="40714-297">To remove a cache entry from a group, pass the cache entry's URL and the INTERNET\_CACHE\_GROUP\_REMOVE flag to [**SetUrlCacheEntryGroup**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup).</span></span>

<span data-ttu-id="40714-298">Les fonctions [**FindFirstUrlCacheEntryEx**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentryexa) et [**FindNextUrlCacheEntryEx**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentryexa) peuvent être utilisées pour énumérer les entrées dans un groupe de caches spécifié.</span><span class="sxs-lookup"><span data-stu-id="40714-298">The [**FindFirstUrlCacheEntryEx**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentryexa) and [**FindNextUrlCacheEntryEx**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentryexa) functions can be used to enumerate the entries in a specified cache group.</span></span> <span data-ttu-id="40714-299">Une fois l’énumération terminée, la fonction doit appeler [**FindCloseUrlCache**](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache).</span><span class="sxs-lookup"><span data-stu-id="40714-299">After the enumeration is complete, the function should call [**FindCloseUrlCache**](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache).</span></span>

## <a name="handling-structures-with-variable-size-information"></a><span data-ttu-id="40714-300">Gestion des structures avec des informations sur la taille des variables</span><span class="sxs-lookup"><span data-stu-id="40714-300">Handling Structures with Variable Size Information</span></span>

<span data-ttu-id="40714-301">Le cache peut contenir des informations sur la taille des variables pour chaque URL stockée.</span><span class="sxs-lookup"><span data-stu-id="40714-301">The cache can contain variable size information for each URL stored.</span></span> <span data-ttu-id="40714-302">Cela se répercute dans la structure des [**\_ \_ \_ informations d’entrée du cache Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) .</span><span class="sxs-lookup"><span data-stu-id="40714-302">This is reflected in the [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) structure.</span></span> <span data-ttu-id="40714-303">Lorsque les fonctions de cache retournent cette structure, elles créent une mémoire tampon qui correspond toujours à la taille des informations d' [**\_ entrée de cache \_ \_ Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) plus toute information de taille de variable.</span><span class="sxs-lookup"><span data-stu-id="40714-303">When the cache functions return this structure, they create a buffer that is always the size of [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) plus any variable size information.</span></span> <span data-ttu-id="40714-304">Si un membre pointeur n’a pas la **valeur null**, il pointe vers la zone mémoire immédiatement après la structure.</span><span class="sxs-lookup"><span data-stu-id="40714-304">If a pointer member is not **NULL**, it points to the memory area immediately after the structure.</span></span> <span data-ttu-id="40714-305">Lors de la copie de la mémoire tampon retournée par une fonction dans une autre mémoire tampon, les membres du pointeur doivent être corrigés pour pointer vers l’emplacement approprié dans la nouvelle mémoire tampon, comme le montre l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="40714-305">While copying the buffer returned by a function into another buffer, the pointer members should be fixed to point to the appropriate place in the new buffer, as the following example shows.</span></span>

``` syntax
lpDstCEInfo->lpszSourceUrlName = 
    (LPINTERNET_CACHE_ENTRY_INFO) ((LPBYTE) lpSrcCEInfo + 
       ((DWORD)(lpOldCEInfo->lpszSourceUrlName) - (DWORD)lpOldCEInfo));
```

<span data-ttu-id="40714-306">Certaines fonctions de cache échouent avec le message d’erreur erreur de \_ mémoire tampon insuffisante \_ si vous spécifiez une mémoire tampon qui est trop petite pour contenir les informations d’entrée de cache récupérées par la fonction.</span><span class="sxs-lookup"><span data-stu-id="40714-306">Some cache functions fail with the ERROR\_INSUFFICIENT\_BUFFER error message if you specify a buffer that is too small to contain the cache entry information retrieved by the function.</span></span> <span data-ttu-id="40714-307">Dans ce cas, la fonction retourne également la taille requise de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="40714-307">In this case, the function also returns the required size of the buffer.</span></span> <span data-ttu-id="40714-308">Vous pouvez ensuite allouer une mémoire tampon de la taille appropriée et appeler à nouveau la fonction.</span><span class="sxs-lookup"><span data-stu-id="40714-308">You can then allocate a buffer of the appropriate size and call the function again.</span></span>

> [!Note]  
> <span data-ttu-id="40714-309">WinINet ne prend pas en charge les implémentations de serveur.</span><span class="sxs-lookup"><span data-stu-id="40714-309">WinINet does not support server implementations.</span></span> <span data-ttu-id="40714-310">En outre, il ne doit pas être utilisé à partir d’un service.</span><span class="sxs-lookup"><span data-stu-id="40714-310">In addition, it should not be used from a service.</span></span> <span data-ttu-id="40714-311">Pour les implémentations de serveur ou les services, utilisez les [services http Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="40714-311">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 
