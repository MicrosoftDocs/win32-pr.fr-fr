---
title: API serveur HTTP version 1,0, fonctions
description: L’API du serveur HTTP fournit les fonctions suivantes pour l’écriture d’applications.
ms.assetid: 1da9907d-a09d-41e1-aca1-9a8e2b91296f
keywords:
- API serveur HTTP version 1,0, fonctions
- Fonctions HTTP, API serveur HTTP version 1,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 050821e40695268d6e3fa2c946d2e8859748db2b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127234029"
---
# <a name="http-server-api-version-10-functions"></a>API serveur HTTP version 1,0, fonctions

L’API du serveur HTTP fournit les fonctions suivantes pour l’écriture d’applications.

## <a name="general"></a>Général



| Fonction                                             | Description                                                                                                                       |
|------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**HttpCreateHttpHandle**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle) | Crée une file d’attente de requêtes HTTP et retourne un descripteur à celle-ci.                                                                         |
| [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize)             | Initialise l’API du serveur HTTP pour une utilisation par le processus appelant.                                                                   |
| [**HttpPrepareUrl**](/windows/desktop/api/Http/nf-http-httpprepareurl)             | Analyse, analyse et normalise une URL Unicode ou Punycode non normalisée afin qu’elle soit sûre et valide à utiliser dans d’autres fonctions HTTP. |
| [**HttpTerminate**](/windows/desktop/api/Http/nf-http-httpterminate)               | Dirige l’API du serveur HTTP pour nettoyer toutes les ressources associées à un processus particulier.                                       |



 

## <a name="cache-management"></a>Gestion du cache



| Fonction                                                       | Description                                                                                            |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**HttpAddFragmentToCache**](/windows/desktop/api/Http/nf-http-httpaddfragmenttocache)       | Met en cache un fragment de données afin qu’il puisse être utilisé pour composer une réponse dynamique sans lire à partir du disque. |
| [**HttpFlushResponseCache**](/windows/desktop/api/Http/nf-http-httpflushresponsecache)       | Supprime les fragments mis en cache spécifiés du cache HTTP.                                                |
| [**HttpReadFragmentFromCache**](/windows/desktop/api/Http/nf-http-httpreadfragmentfromcache) | Récupère un fragment de réponse mis en cache spécifié.                                                        |



 

## <a name="configuration"></a>Configuration



| Fonction                                                                 | Description                                                       |
|--------------------------------------------------------------------------|-------------------------------------------------------------------|
| [**HttpDeleteServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpdeleteserviceconfiguration) | Supprime les informations spécifiées du magasin de configuration HTTP.  |
| [**HttpQueryServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration)   | Interroge le magasin de configuration HTTP pour obtenir les informations spécifiées.   |
| [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration)       | Définit les valeurs spécifiées dans le magasin de configuration de l’API du serveur HTTP. |



 

## <a name="input-and-output"></a>Entrées et sorties



| Fonction                                                             | Description                                                    |
|----------------------------------------------------------------------|----------------------------------------------------------------|
| [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest)             | Récupère une requête HTTP à partir d’une file d’attente de demandes spécifiée.      |
| [**HttpReceiveRequestEntityBody**](/windows/desktop/api/Http/nf-http-httpreceiverequestentitybody) | Récupère les données de corps d’entité d’une requête HTTP particulière.       |
| [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse)                 | Envoie une réponse HTTP pour une requête HTTP particulière.          |
| [**HttpSendResponseEntityBody**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody)     | Envoie des données de corps d’entité d’une réponse HTTP.                    |
| [**HttpWaitForDisconnect**](/windows/desktop/api/Http/nf-http-httpwaitfordisconnect)               | Avertit l’application lorsqu’un client HTTP est déconnecté. |



 

## <a name="ssl"></a>SSL



| Fonction                                                             | Description                                             |
|----------------------------------------------------------------------|---------------------------------------------------------|
| [**HttpReceiveClientCertificate**](/windows/desktop/api/Http/nf-http-httpreceiveclientcertificate) | Récupère le certificat client pour une connexion SSL. |



 

## <a name="url-registration"></a>Inscription d’URL



| Fonction                               | Description                                                                                     |
|----------------------------------------|-------------------------------------------------------------------------------------------------|
| [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl)       | Inscrit une URL afin que les requêtes HTTP pour celle-ci soient acheminées vers une file d’attente de demandes spécifiée.           |
| [**HttpRemoveUrl**](/windows/desktop/api/Http/nf-http-httpremoveurl) | Annule l’inscription d’une URL spécifiée, afin que les demandes pour celle-ci ne soient plus routées vers une file d’attente spécifiée. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Structures de la version 1,0 de l’API du serveur HTTP](http-server-api-version-1-0-structures.md)
</dt> </dl>

 

 




