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
# <a name="http-server-api-version-10-data-types"></a>Types de données de l’API du serveur HTTP 1,0

L’API du serveur HTTP utilise divers types d’identificateurs à usage spécial déclarés dans le fichier d’en-tête http. h comme des entiers non signés 64 bits (**ULONGLONGs**) :

-   \_ID de connexion http \_
-   \_ID de \_ connexion \_ brute http
-   ID de la \_ requête HTTP \_
-   \_contexte d’URL http \_

Une application ne doit pas tenter de générer ou de modifier un identificateur qui appartient à l’un de ces types.

 

 




