---
title: API serveur HTTP version 2,0, fonctions
description: La version 2,0 de l’API du serveur HTTP fournit les fonctions suivantes.
ms.assetid: 12daffca-b403-4f06-8037-206f90e33252
keywords:
- API serveur HTTP version 2,0, fonctions
- Fonctions HTTP, API serveur HTTP version 2,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92e4d5c09c001caa58d43c1e61d800f66b39706b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127233987"
---
# <a name="http-server-api-version-20-functions"></a>API serveur HTTP version 2,0, fonctions

La version 2,0 de l’API du serveur HTTP fournit les fonctions suivantes.

| Fonction | Description |
|-|-|
| [**HttpDelegateRequestEx**](/windows/win32/api/http/nf-http-httpdelegaterequestex) | Délègue une requête de la file d’attente de demandes source à la file d’attente de demandes cible. |
| [**HttpFindUrlGroupId**](/windows/win32/api/http/nf-http-httpfindurlgroupid) | Récupère un ID de groupe d’URL pour une URL et une file d’attente de demandes. |
| [**HttpIsFeatureSupported**](/windows/win32/api/http/nf-http-httpisfeaturesupported) | Vérifie si une fonctionnalité particulière est prise en charge. |

## <a name="server-session"></a>Session serveur

| Fonction | Description |
|-|-|
| [**HttpCloseServerSession**](/windows/desktop/api/Http/nf-http-httpcloseserversession) | |
| [**HttpCreateServerSession**](/windows/desktop/api/Http/nf-http-httpcreateserversession) | |
| [**HttpQueryServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty) | |
| [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) | |

## <a name="url-groups"></a>Groupes d’URL

| Fonction | Description |
|-|-|
| [**HttpAddUrlToUrlGroup**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup) | |
| [**HttpCreateUrlGroup**](/windows/desktop/api/Http/nf-http-httpcreateurlgroup) | |
| [**HttpCloseUrlGroup**](/windows/desktop/api/Http/nf-http-httpcloseurlgroup) | |
| [**HttpQueryUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty) | |
| [**HttpRemoveUrlFromUrlGroup**](/windows/desktop/api/Http/nf-http-httpremoveurlfromurlgroup) | |
| [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) | |

## <a name="request-queue"></a>File d'attente de requêtes

| Fonction | Description |
|-|-|
| [**HttpCloseRequestQueue**](/windows/desktop/api/Http/nf-http-httpcloserequestqueue) | |
| [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) | |
| [**HttpQueryRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpqueryrequestqueueproperty) | |
| [**HttpSetRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) | |
| [**HttpShutdownRequestQueue**](/windows/desktop/api/Http/nf-http-httpshutdownrequestqueue) | |
| [**HttpWaitForDemandStart**](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) | |

## <a name="related-topics"></a>Rubriques connexes

[Structures de la version 2,0 de l’API du serveur HTTP](http-server-api-version-2-0-structures.md)
