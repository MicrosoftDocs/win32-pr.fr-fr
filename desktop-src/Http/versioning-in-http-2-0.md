---
title: Contrôle de version (API serveur HTTP)
description: L’API du serveur HTTP version 2,0 applique le contrôle de version de portée objet pour déterminer la version de l’API.
ms.assetid: 2c2d7501-85e0-44ec-aa42-01372b29266e
keywords:
- Contrôle de version dans l’API du serveur HTTP version 2,0
- API version 2,0 du serveur HTTP, contrôle de version
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc7a84af7de439cdd13cc1e9ff66fff367370fa963882077904ad656b856511
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829689"
---
# <a name="versioning-http-server-api"></a>Contrôle de version (API serveur HTTP)

L’API de la version 2,0 du serveur HTTP rend obsolètes les files d’attente de demandes de version 1,0 et les associations d’URL avec la file d’attente des demandes. Le contrôle de version de portée objet permet aux applications de fournir des informations de version spécifiques à l’application. Une application peut automatiquement appeler la version correcte des structures pour le système d’exploitation sur lequel elle s’exécute.

## <a name="request-queues"></a>Files d’attente de demandes

À partir de l’API du serveur HTTP version 2,0, les files d’attente des demandes sont créées avec [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) , ce qui rend obsolète la fonction [**HttpCreateHttpHandle**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle) version 1,0. Les groupes d’URL sont introduits dans la version 2,0 avec la fonction [**HttpCreateUrlGroup**](/windows/desktop/api/Http/nf-http-httpcreateurlgroup) . Les URL sont ajoutées au groupe à l’aide de [**HttpAddUrlToUrlGroup**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup) , ce qui rend obsolète la fonction [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl) version 1,0. Les groupes d’URL de la version 2,0 ne doivent pas être utilisés avec les files d’attente de demandes 1,0.

À partir de la version 2,0, les fonctions suivantes de la version 1,0 sont obsolètes et ne peuvent pas être utilisées avec les files d’attente de demandes de la version 2,0 :

-   [**HttpCreateHttpHandle**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle)
-   [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl)
-   [**HttpRemoveUrl**](/windows/desktop/api/Http/nf-http-httpremoveurl)

Pour plus d’informations sur la configuration des groupes d’URL, consultez la rubrique [configuration du groupe d’URL](configuring-the-url-group.md) . Pour plus d’informations sur les files d’attente de demandes de la version 2,0, consultez la rubrique [file d’attente des demandes nommée](named-request-queue.md) .

## <a name="object-scoped-versioning"></a>Gestion des versions de Object-Scoped

Dans la version 1,0, l’application fournit la version de l’API du serveur HTTP dans l’appel à [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize). Les informations de version sont uniquement acceptées à partir de la première application qui a appelé **HttpInitialize** et sont appliquées à toutes les applications API du serveur http dans le même processus. À partir de la version 2,0 de l’API, les informations de version globales fournies dans l’appel à **HttpInitialize** ne sont pas utilisées. Pour les applications de la version 2,0, la version de l’API du serveur HTTP est passée dans le paramètre version lorsque la file d’attente de demandes ou la session serveur est créée par [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) ou [**HttpCreateServerSession**](/windows/desktop/api/Http/nf-http-httpcreateserversession). Lorsque la file d’attente des demandes est créée avec la version 1,0 [**HttpCreateHttpHandle**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle), elle est automatiquement marquée comme version 1,0. Les applications version 1,0 et version 2,0 peuvent s’exécuter dans le même processus.

Les structures de [**\_ requête http**](/previous-versions/windows/desktop/legacy/aa364545(v=vs.85)) et de [**\_ réponse http**](http-response.md) sont mises à jour pour inclure les informations d’authentification dans l’API du serveur http version 2,0. [**Protocole http \_ Les demandes \_ v1**](/windows/desktop/api/Http/ns-http-http_request_v1) et [**http \_ Request \_ v2**](/windows/desktop/api/Http/ns-http-http_request_v2) sont spécifiques à la version de l’API utilisée par l’application. Toutefois, les applications ne doivent pas utiliser ces structures directement dans leur code ; au lieu de cela, ils doivent utiliser la **\_ requête http** pour obtenir la version correcte en fonction de la version de la file d’attente de demandes sur laquelle la demande a été reçue. Sachez également que la taille de la structure de la **\_ requête http** est basée sur la version du système d’exploitation sous lequel le code est compilé.

 

 
