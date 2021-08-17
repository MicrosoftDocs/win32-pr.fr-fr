---
title: Types de données de l’API du serveur HTTP 2,0
description: Types de données de l’API du serveur HTTP 2,0
ms.assetid: 13a0cac9-9e75-4350-a523-5ad9a57caad7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61a347b58a97ad89e499136c07f85e18ee2ce1bddc31b5c6d67b8f14a2348a44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950768"
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

 

 




