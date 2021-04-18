---
title: Types de données de l’API du serveur HTTP 1,0
description: L’API du serveur HTTP utilise divers types d’identificateurs à usage spécial déclarés dans le fichier d’en-tête http. h comme des entiers non signés 64 bits.
ms.assetid: bec1d41e-0c80-49bc-84e1-b16c409cd0f3
keywords:
- Type de HTTP_CONNECTION_ID HTTP
- Type de HTTP_RAW_CONNECTION_ID HTTP
- Type de HTTP_REQUEST_ID HTTP
- Type de HTTP_URL_CONTEXT HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 681e24c06334a9010287e2084d9d6a04428ca6a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511849"
---
# <a name="http-server-api-version-10-data-types"></a><span data-ttu-id="48bf6-107">Types de données de l’API du serveur HTTP 1,0</span><span class="sxs-lookup"><span data-stu-id="48bf6-107">HTTP Server API Version 1.0 Data Types</span></span>

<span data-ttu-id="48bf6-108">L’API du serveur HTTP utilise divers types d’identificateurs à usage spécial déclarés dans le fichier d’en-tête http. h comme des entiers non signés 64 bits (**ULONGLONGs**) :</span><span class="sxs-lookup"><span data-stu-id="48bf6-108">The HTTP Server API uses various special purpose identifier types declared in the Http.h header file as 64-bit unsigned integers (**ULONGLONGs**):</span></span>

-   <span data-ttu-id="48bf6-109">\_ID de connexion http \_</span><span class="sxs-lookup"><span data-stu-id="48bf6-109">HTTP\_CONNECTION\_ID</span></span>
-   <span data-ttu-id="48bf6-110">\_ID de \_ connexion \_ brute http</span><span class="sxs-lookup"><span data-stu-id="48bf6-110">HTTP\_RAW\_CONNECTION\_ID</span></span>
-   <span data-ttu-id="48bf6-111">ID de la \_ requête HTTP \_</span><span class="sxs-lookup"><span data-stu-id="48bf6-111">HTTP\_REQUEST\_ID</span></span>
-   <span data-ttu-id="48bf6-112">\_contexte d’URL http \_</span><span class="sxs-lookup"><span data-stu-id="48bf6-112">HTTP\_URL\_CONTEXT</span></span>

<span data-ttu-id="48bf6-113">Une application ne doit pas tenter de générer ou de modifier un identificateur qui appartient à l’un de ces types.</span><span class="sxs-lookup"><span data-stu-id="48bf6-113">An application should not attempt to generate or modify any identifier that belongs to one of these types.</span></span>

 

 




