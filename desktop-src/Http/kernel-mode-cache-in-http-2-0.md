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
# <a name="kernel-mode-cache"></a>Cache en mode noyau

L’API de la version 2,0 du serveur HTTP permet aux applications de mettre en cache les réponses avec un contenu statique en mode noyau. Des performances accrues sont obtenues lorsque les demandes sont traitées à partir du cache du noyau sans passer au mode utilisateur.

L’API du serveur HTTP applique les configurations de propriétés appropriées à toutes les demandes traitées à partir du cache du noyau, y compris les réponses de journalisation. Toutefois, les demandes qui requièrent une authentification ne seront pas traitées à partir du cache.

L’API du serveur HTTP limite le cache en mode noyau aux demandes qui remplissent les conditions suivantes :

-   Le verbe de requête est obtenir et la requête entière est reçue.
-   La demande ne doit pas avoir de corps d’entité.
-   Le protocole HTTP est la version 1,0 ou une version ultérieure.
-   L’en-tête « Translate : f » n’est pas présent.
-   Les en-têtes attendus autres que « expect : 100-continue » ne sont pas présents.
-   L’en-tête Authorization n’est pas présent.
-   Les en-têtes de plage et de If-Range ne sont pas présents.

Outre les restrictions sur la demande, la réponse doit également remplir les conditions suivantes :

-   La taille de la réponse est limitée à 256 Ko par défaut. Pour modifier la taille de la réponse mise en cache, définissez la valeur de Registre **UriMaxUriBytes** sur le nombre d’octets requis.

    ```
    HKEY_LOCAL_MACHINE
       System
          CurrentControlSet
             Services
                HTTP
                   Parameters
                      UriMaxUriBytes
    ```

-   L’intégralité de la réponse doit être fournie en un seul appel à [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse).
-   L’en-tête de date de la réponse ne doit pas être supprimé.
-   Si l’en-tête Last-modified est présent, la syntaxe de l’en-tête doit être correcte. La valeur de temps de cet en-tête est utilisée pour la vérification du contrôle de cache.
-   Le cache en mode noyau a suffisamment d’espace pour stocker la réponse.

Par défaut, le cache de réponse en mode noyau est activé. Si l’une des conditions de la demande ou de la réponse répertoriées ci-dessus n’est pas remplie, la réponse est envoyée, mais elle n’est pas mise en cache. Dans l’API du serveur HTTP version 2,0, [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) comprend un paramètre *pCachePolicy* facultatif permettant de transmettre la structure de la [**\_ \_ stratégie de cache http**](/windows/desktop/api/Http/ns-http-http_cache_policy) . Les applications utilisent la structure de stratégie de cache pour configurer le cache.

 

 




