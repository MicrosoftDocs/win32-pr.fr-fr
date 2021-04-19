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
# <a name="http-server-api-version-20-data-types"></a>Types de données de l’API du serveur HTTP 2,0

L’API du serveur HTTP utilise divers types d’identificateurs à usage spécial déclarés dans l’en-tête http. h, comme suit :

-   **UShort** \_ \_ \_ paramètre du délai d’expiration de la configuration du service http \_ , \* PHTTP \_ du service de \_ configuration \_ du service \_
-   **ULONGLONG** \_ID opaque http \_ , \* \_ ID opaque \_ PHTTP
-   **Protocole http \_ ID \_** de requête HTTP de l’ID opaque \_ \_ , ID de la \* \_ demande PHTTP \_
-   **Protocole http \_ ID \_** de connexion http de l’ID opaque \_ \_ , \* ID de \_ connexion PHTTP \_
-   **Protocole http \_ ID \_ opaque** ID \_ \_ de connexion brute http \_ , \* \_ \_ ID de connexion brute PHTTP \_
-   **UShort** \_ \_ \_ paramètre du délai d’expiration de la configuration du service http \_ , \* PHTTP \_ du service de \_ configuration \_ du service \_

Une application ne doit pas tenter de générer ou de modifier un identificateur qui appartient à l’un de ces types.

 

 




