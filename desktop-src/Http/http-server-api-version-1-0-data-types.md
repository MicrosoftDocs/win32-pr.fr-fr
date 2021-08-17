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
ms.openlocfilehash: 151ef975470ca21c6e82e5bc7bd7bd8b99a70573385375e8552b6660ce78f631
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950798"
---
# <a name="http-server-api-version-10-data-types"></a>Types de données de l’API du serveur HTTP 1,0

L’API du serveur HTTP utilise divers types d’identificateurs à usage spécial déclarés dans le fichier d’en-tête http. h comme des entiers non signés 64 bits (**ULONGLONGs**) :

-   \_ID de connexion http \_
-   \_ID de \_ connexion \_ brute http
-   ID de la \_ requête HTTP \_
-   \_contexte d’URL http \_

Une application ne doit pas tenter de générer ou de modifier un identificateur qui appartient à l’un de ces types.

 

 




