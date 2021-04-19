---
title: Types de données de l’API du serveur HTTP 2,0
description: Types de données de l’API du serveur HTTP 2,0
ms.assetid: 13a0cac9-9e75-4350-a523-5ad9a57caad7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 670099f3303682f52fdc78397dc7f229577b94d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509610"
---
# <a name="http-server-api-version-20-data-types"></a><span data-ttu-id="c04fe-103">Types de données de l’API du serveur HTTP 2,0</span><span class="sxs-lookup"><span data-stu-id="c04fe-103">HTTP Server API Version 2.0 Data Types</span></span>

<span data-ttu-id="c04fe-104">L’API du serveur HTTP utilise divers types d’identificateurs à usage spécial déclarés dans l’en-tête http. h, comme suit :</span><span class="sxs-lookup"><span data-stu-id="c04fe-104">The HTTP Server API uses various special purpose identifier types declared in the Http.h header as follows:</span></span>

-   <span data-ttu-id="c04fe-105">**UShort** \_ \_ \_ paramètre du délai d’expiration de la configuration du service http \_ , \* PHTTP \_ du service de \_ configuration \_ du service \_</span><span class="sxs-lookup"><span data-stu-id="c04fe-105">**USHORT** HTTP\_SERVICE\_CONFIG\_TIMEOUT\_PARAM, \*PHTTP\_SERVICE\_CONFIG\_TIMEOUT\_PARAM</span></span>
-   <span data-ttu-id="c04fe-106">**ULONGLONG** \_ID opaque http \_ , \* \_ ID opaque \_ PHTTP</span><span class="sxs-lookup"><span data-stu-id="c04fe-106">**ULONGLONG** HTTP\_OPAQUE\_ID, \*PHTTP\_OPAQUE\_ID</span></span>
-   <span data-ttu-id="c04fe-107">**Protocole http \_ ID \_** de requête HTTP de l’ID opaque \_ \_ , ID de la \* \_ demande PHTTP \_</span><span class="sxs-lookup"><span data-stu-id="c04fe-107">**HTTP\_OPAQUE\_ID** HTTP\_REQUEST\_ID, \*PHTTP\_REQUEST\_ID</span></span>
-   <span data-ttu-id="c04fe-108">**Protocole http \_ ID \_** de connexion http de l’ID opaque \_ \_ , \* ID de \_ connexion PHTTP \_</span><span class="sxs-lookup"><span data-stu-id="c04fe-108">**HTTP\_OPAQUE\_ID** HTTP\_CONNECTION\_ID, \*PHTTP\_CONNECTION\_ID</span></span>
-   <span data-ttu-id="c04fe-109">**Protocole http \_ ID \_ opaque** ID \_ \_ de connexion brute http \_ , \* \_ \_ ID de connexion brute PHTTP \_</span><span class="sxs-lookup"><span data-stu-id="c04fe-109">**HTTP\_OPAQUE\_ID** HTTP\_RAW\_CONNECTION\_ID, \*PHTTP\_RAW\_CONNECTION\_ID</span></span>
-   <span data-ttu-id="c04fe-110">**UShort** \_ \_ \_ paramètre du délai d’expiration de la configuration du service http \_ , \* PHTTP \_ du service de \_ configuration \_ du service \_</span><span class="sxs-lookup"><span data-stu-id="c04fe-110">**USHORT** HTTP\_SERVICE\_CONFIG\_TIMEOUT\_PARAM, \*PHTTP\_SERVICE\_CONFIG\_TIMEOUT\_PARAM</span></span>

<span data-ttu-id="c04fe-111">Une application ne doit pas tenter de générer ou de modifier un identificateur qui appartient à l’un de ces types.</span><span class="sxs-lookup"><span data-stu-id="c04fe-111">An application should not attempt to generate or modify any identifier that belongs to one of these types.</span></span>

 

 




