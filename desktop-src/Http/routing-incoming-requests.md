---
title: Routage des demandes entrantes
description: L’API du serveur HTTP gère une base de données de routage pour déterminer l’application qui reçoit une demande entrante.
ms.assetid: 7c613137-66bd-4375-93cb-b5562823bc12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da483030441f3a9239eef153da59212166bce9eb
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "104383208"
---
# <a name="routing-incoming-requests"></a><span data-ttu-id="12db1-103">Routage des demandes entrantes</span><span class="sxs-lookup"><span data-stu-id="12db1-103">Routing Incoming Requests</span></span>

<span data-ttu-id="12db1-104">L’API du serveur HTTP gère une base de données de routage pour déterminer l’application qui reçoit une demande entrante.</span><span class="sxs-lookup"><span data-stu-id="12db1-104">The HTTP Server API maintains a routing database to determine which application receives an incoming request.</span></span> <span data-ttu-id="12db1-105">La table de routage est créée à partir de la base de données de réservation et contient des entrées de réservation ainsi que des inscriptions actuelles.</span><span class="sxs-lookup"><span data-stu-id="12db1-105">The routing table is built from the reservation database and contains reservation entries as well as current registrations.</span></span> <span data-ttu-id="12db1-106">Lorsqu’une inscription ou une réservation est effectuée, elle est placée dans le compartiment de la base de données de routage qui correspond au type d’hôte comme suit :</span><span class="sxs-lookup"><span data-stu-id="12db1-106">When a registration or reservation is made, it is placed into the routing database bucket that corresponds to the host type as follows:</span></span>

-   <span data-ttu-id="12db1-107">\+ : les inscriptions de port sont placées dans le compartiment « caractère générique fort ».</span><span class="sxs-lookup"><span data-stu-id="12db1-107">\+ : port registrations are placed in the "Strong Wildcard" bucket</span></span>

-   <span data-ttu-id="12db1-108">hôte : les inscriptions de port sont placées dans le compartiment « explicite »</span><span class="sxs-lookup"><span data-stu-id="12db1-108">host : port registrations are placed in the "Explicit" bucket</span></span>

-   <span data-ttu-id="12db1-109">IP : les inscriptions de port sont placées dans le compartiment « caractère générique faible lié à IP »</span><span class="sxs-lookup"><span data-stu-id="12db1-109">IP : port registrations are placed in the "IP-bound Weak Wildcard" bucket</span></span>

-   <span data-ttu-id="12db1-110">\* : les inscriptions de port sont placées dans le compartiment « caractère générique faible »</span><span class="sxs-lookup"><span data-stu-id="12db1-110">\* : port registrations are placed in the "Weak Wildcard" bucket</span></span>

<span data-ttu-id="12db1-111">Ces étapes font également référence à l’ordre de traitement des demandes HTTP entrantes.</span><span class="sxs-lookup"><span data-stu-id="12db1-111">These steps also refer to the order incoming HTTP requests are processed.</span></span> <span data-ttu-id="12db1-112">En premier lieu, les réservations à caractères génériques fortes sont vérifiées, suivies du caractère générique faible lié à IP et du caractère générique faible.</span><span class="sxs-lookup"><span data-stu-id="12db1-112">The strong wildcard reservations first, then the explicit reservation are checked followed by the IP-bound weak wildcard and weak wildcard.</span></span> <span data-ttu-id="12db1-113">La recherche s’arrête lorsqu’une correspondance est trouvée afin que les inscriptions dans l’un des compartiments restants soient introuvables.</span><span class="sxs-lookup"><span data-stu-id="12db1-113">The search stops when a match is found so that registrations in any of the remaining buckets are not found.</span></span>

<span data-ttu-id="12db1-114">L’algorithme de routage de l’API du serveur HTTP localise la meilleure correspondance pour le [URLPrefix](urlprefix-strings.md) en effectuant une recherche dans les entrées d’inscription et les entrées de réservation de la base de données de routage, en commençant par le compartiment à caractères génériques renforcé et en terminant par la plage de caractères génériques faibles.</span><span class="sxs-lookup"><span data-stu-id="12db1-114">The HTTP Server API routing algorithm locates the best match for the [UrlPrefix](urlprefix-strings.md) by searching both the registration entries and the reservation entries of the routing database, starting with the strong wildcard bucket and ending with the weak wildcard bucket.</span></span> <span data-ttu-id="12db1-115">La meilleure correspondance, au sein d’un compartiment, est la correspondance la plus longue dans la partie URI relative du UrlPrefix (en supposant une correspondance exacte pour les parties hôte, port et schéma de l’URL).</span><span class="sxs-lookup"><span data-stu-id="12db1-115">The best match, within a bucket, is the longest match in the relative URI portion of the UrlPrefix (assuming an exact match for the host, port and scheme portions of the URL).</span></span> <span data-ttu-id="12db1-116">Une fois qu’une correspondance a été trouvée dans un compartiment, l’algorithme de routage arrête sa recherche et ignore tous les compartiments de priorité inférieure.</span><span class="sxs-lookup"><span data-stu-id="12db1-116">After a match is found in a bucket, the routing algorithm stops its search and skips all lower priority buckets.</span></span>

<span data-ttu-id="12db1-117">Par exemple, considérez les inscriptions suivantes (classées par ordre de priorité décroissant selon les types de compartiments :</span><span class="sxs-lookup"><span data-stu-id="12db1-117">For example, consider the following registrations (listed in descending order of priority based on bucket types:</span></span>

-   <span data-ttu-id="12db1-118">Inscription : `https://+:80/vroot/` est inscrit par l’application 1</span><span class="sxs-lookup"><span data-stu-id="12db1-118">Registration: `https://+:80/vroot/` is registered by application 1</span></span>

-   <span data-ttu-id="12db1-119">Inscription : `https://adatum.com:80/` est inscrit par l’application 2</span><span class="sxs-lookup"><span data-stu-id="12db1-119">Registration: `https://adatum.com:80/` is registered by application 2</span></span>

-   <span data-ttu-id="12db1-120">Inscription : `https://\*:80/` est inscrit par l’application 3</span><span class="sxs-lookup"><span data-stu-id="12db1-120">Registration: `https://\*:80/` is registered by application 3</span></span>

<span data-ttu-id="12db1-121">Une demande entrante pour `https://adatum.com:80/vroot/subdir/file.htm/` est remise à l’application 1.</span><span class="sxs-lookup"><span data-stu-id="12db1-121">An incoming request for `https://adatum.com:80/vroot/subdir/file.htm/` is delivered to application 1.</span></span> <span data-ttu-id="12db1-122">Une demande entrante pour `https://adatum.com:80/default.htm/` est remise à l’application 2.</span><span class="sxs-lookup"><span data-stu-id="12db1-122">An incoming request for `https://adatum.com:80/default.htm/` is delivered to application 2.</span></span> <span data-ttu-id="12db1-123">Une demande entrante pour `https://otheradatum.com:80/file.htm/` est remise à l’application 3.</span><span class="sxs-lookup"><span data-stu-id="12db1-123">An incoming request for `https://otheradatum.com:80/file.htm/` is delivered to application 3.</span></span>

<span data-ttu-id="12db1-124">Si la meilleure correspondance est une entrée de réservation, cela signifie que l’application qui doit recevoir la demande n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="12db1-124">If the best match is a reservation entry, this means that the application that should receive the request is not running.</span></span> <span data-ttu-id="12db1-125">Par exemple, considérez l’inscription et la réservation suivantes :</span><span class="sxs-lookup"><span data-stu-id="12db1-125">For example, consider the following registration and reservation:</span></span>

-   <span data-ttu-id="12db1-126">Inscription : `https://\*:80/vroot/` est inscrit par l’application 1, utilisateur a</span><span class="sxs-lookup"><span data-stu-id="12db1-126">Registration: `https://\*:80/vroot/` is registered by application 1, user A</span></span>

-   <span data-ttu-id="12db1-127">Réservation : `https://adatum.com:80/` a été réservé pour l’utilisateur B</span><span class="sxs-lookup"><span data-stu-id="12db1-127">Reservation: `https://adatum.com:80/` has been reserved for user B</span></span>

<span data-ttu-id="12db1-128">Une demande entrante pour `https://adatum.com:80/vroot/file.htm/` n’est pas remise à l’application 1 car la meilleure correspondance correspond à l’entrée de réservation pour l’utilisateur B. Dans ce cas, les règles de précédence sont appliquées à la réservation qui a une priorité plus élevée.</span><span class="sxs-lookup"><span data-stu-id="12db1-128">An incoming request for `https://adatum.com:80/vroot/file.htm/` is not delivered to application 1 because the best match leads to the reservation entry for user B. The precedence rules are applied in this case to the reservation which has a higher priority.</span></span> <span data-ttu-id="12db1-129">Si aucun processus actif n’est autorisé et inscrit aux demandes de service pour l’URL reçue, la demande est rejetée avec un code d’état 400 (demande incorrecte).</span><span class="sxs-lookup"><span data-stu-id="12db1-129">If no process is active that is authorized and registered to service requests for the URL received, the request is rejected with a 400 status code (Bad Request).</span></span>

 

 




