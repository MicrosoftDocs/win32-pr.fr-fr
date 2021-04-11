---
title: Fonctionnalités de l’API du serveur HTTP
description: Cette rubrique prenait en charge et ne prenait pas en charge les fonctionnalités de l’API du serveur HTTP.
ms.assetid: 448fe5a5-e79f-4c3a-aa76-94cff988f24f
keywords:
- Fonctionnalités de l’API du serveur HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48d5f529811b08999d6e1cfffa99fc85288ec471
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310998"
---
# <a name="http-server-api-features"></a><span data-ttu-id="e7ab0-104">Fonctionnalités de l’API du serveur HTTP</span><span class="sxs-lookup"><span data-stu-id="e7ab0-104">HTTP Server API Features</span></span>

<span data-ttu-id="e7ab0-105">Les listes suivantes décrivent les fonctionnalités prises en charge et non prises en charge de l’API du serveur HTTP.</span><span class="sxs-lookup"><span data-stu-id="e7ab0-105">The following lists describe supported and unsupported features of the HTTP Server API.</span></span>

## <a name="features-supported"></a><span data-ttu-id="e7ab0-106">Fonctionnalités prises en charge</span><span class="sxs-lookup"><span data-stu-id="e7ab0-106">Features Supported</span></span>

<span data-ttu-id="e7ab0-107">HTTP prend en charge les fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="e7ab0-107">HTTP supports the following features:</span></span>

-   <span data-ttu-id="e7ab0-108">Fonctionnalités du serveur HTTP v 1.0 et v 1.1.</span><span class="sxs-lookup"><span data-stu-id="e7ab0-108">HTTP v1.0 and v1.1 server functionality.</span></span>
-   <span data-ttu-id="e7ab0-109">SSL (Secure Sockets Layer) 3,0 (SSL) avec prise en charge des certificats client et serveur.</span><span class="sxs-lookup"><span data-stu-id="e7ab0-109">Secure Sockets Layer 3.0 (SSL) with support for client and server certificates.</span></span>
-   <span data-ttu-id="e7ab0-110">Mise en cache des fragments de données à utiliser dans les réponses suivantes.</span><span class="sxs-lookup"><span data-stu-id="e7ab0-110">Caching of data fragments for use in subsequent responses.</span></span>
-   <span data-ttu-id="e7ab0-111">Prise en charge de l’adressage IPv6 et IPv4.</span><span class="sxs-lookup"><span data-stu-id="e7ab0-111">Support for IPv6 and IPv4 addressing.</span></span>
-   <span data-ttu-id="e7ab0-112">Réservations d’espaces de noms d’URL pour la sécurité de l’application.</span><span class="sxs-lookup"><span data-stu-id="e7ab0-112">URL namespace reservations for application security.</span></span>
-   <span data-ttu-id="e7ab0-113">Handles true pour tous les objets.</span><span class="sxs-lookup"><span data-stu-id="e7ab0-113">True handles for all objects.</span></span>
-   <span data-ttu-id="e7ab0-114">Modèles d’e/s synchrones et asynchrones.</span><span class="sxs-lookup"><span data-stu-id="e7ab0-114">Synchronous and asynchronous I/O models.</span></span>
-   <span data-ttu-id="e7ab0-115">Prise en charge de WOW64 sur les ordinateurs exécutant Windows 64 bits à partir de Windows Server 2003 avec Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="e7ab0-115">Support for WOW64 on computers running on 64-bit Windows starting with Windows Server 2003 with Service Pack 1 (SP1).</span></span>

## <a name="features-not-supported"></a><span data-ttu-id="e7ab0-116">Fonctionnalités non prises en charge</span><span class="sxs-lookup"><span data-stu-id="e7ab0-116">Features Not Supported</span></span>

<span data-ttu-id="e7ab0-117">L’API du serveur HTTP ne prend pas en charge les fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="e7ab0-117">The HTTP Server API does not support the following functionality:</span></span>

-   <span data-ttu-id="e7ab0-118">L’API du serveur HTTP n’effectue pas l’authentification du client ou du serveur en fonction du contenu des en-têtes de requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="e7ab0-118">The HTTP Server API does not perform client or server authentication based on the contents of the HTTP request headers.</span></span> <span data-ttu-id="e7ab0-119">Toute authentification requise doit être implémentée par l’application.</span><span class="sxs-lookup"><span data-stu-id="e7ab0-119">Any required authentication must be implemented by the application.</span></span>
-   <span data-ttu-id="e7ab0-120">WOW64 sur des ordinateurs fonctionnant sous Windows 64 bits n’est pas pris en charge sur Windows Server 2003 et Windows XP avec Service Pack 2 (SP2) et versions antérieures.</span><span class="sxs-lookup"><span data-stu-id="e7ab0-120">WOW64 on computers running on 64-bit Windows is not supported on Windows Server 2003, and Windows XP with Service Pack 2 (SP2) and earlier.</span></span>
-   <span data-ttu-id="e7ab0-121">L’API du serveur HTTP ne prend pas en charge la journalisation des requêtes et des réponses HTTP.</span><span class="sxs-lookup"><span data-stu-id="e7ab0-121">The HTTP Server API does not support logging HTTP requests and responses.</span></span>
-   <span data-ttu-id="e7ab0-122">L’API du serveur HTTP ne segmente pas les réponses HTTP sortantes.</span><span class="sxs-lookup"><span data-stu-id="e7ab0-122">The HTTP Server API does not chunk outgoing HTTP responses.</span></span> <span data-ttu-id="e7ab0-123">L’application doit implémenter la segmentation des réponses si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="e7ab0-123">The application must implement response chunking if required.</span></span>

 

 




