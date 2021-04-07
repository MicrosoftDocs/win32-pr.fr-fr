---
title: Appels de procédure distante à l’aide de RPC sur HTTP
description: Les programmes de navigation Internet emploient généralement le protocole HTTP (Hypertext Transport Protocol) comme moyen principal de parcourir les World Wide Web.
ms.assetid: f87262f6-fd82-4e8c-bf83-8f93791deec0
keywords:
- Appel de procédure distante RPC, tâches, à l’aide de RPC/http
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c84551500af712b1126d8f9a65cb3d02eba8c9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939559"
---
# <a name="remote-procedure-calls-using-rpc-over-http"></a>Appels de procédure distante à l’aide de RPC sur HTTP

Les programmes de navigation Internet emploient généralement le protocole HTTP (Hypertext Transport Protocol) comme moyen principal de parcourir les World Wide Web. HTTP, par conséquent, voit une utilisation intensive sur la plupart des ordinateurs dès aujourd’hui. Microsoft a étendu les fonctionnalités de son Internet Information Server (IIS) pour fournir des services d’appel de procédure distante à l’aide de HTTP.

L’implémentation Microsoft RPC sur http (RPC sur HTTP) permet aux clients RPC de se connecter en toute sécurité et de manière efficace via Internet à des programmes serveur RPC et d’exécuter des appels de procédure distante. Cela s’effectue à l’aide d’un intermédiaire appelé proxy RPC sur HTTP, ou simplement du proxy RPC.

Le proxy RPC s’exécute sur un ordinateur IIS. Il accepte les demandes RPC provenant d’Internet, effectue des vérifications d’authentification, de validation et d’accès sur ces requêtes et, si la demande réussit tous les tests, le proxy RPC transfère la demande au serveur RPC qui effectue le traitement réel. Avec RPC sur HTTP, le client et le serveur RPC ne communiquent pas directement ; au lieu de cela, ils utilisent le proxy RPC comme intermédiaire. Ce modèle a été choisi pour de nombreuses raisons. Pour plus d’informations, consultez [RPC sur la sécurité http](rpc-over-http-security.md).

Cette section fournit une vue d’ensemble de RPC sur HTTP dans les rubriques suivantes :

-   [Utilisation de HTTP comme transport RPC](using-http-as-an-rpc-transport.md)
-   [Sécurité RPC sur HTTP](rpc-over-http-security.md)
-   [Configuration système requise et interopérabilité pour RPC sur HTTP](system-requirements-and-interoperability-for-rpc-over-http.md)
-   [Configuration des ordinateurs pour RPC sur HTTP](configuring-computers-for-rpc-over-http.md)
-   [Recommandations relatives au déploiement de RPC sur HTTP](rpc-over-http-deployment-recommendations.md)

Pour plus d’informations sur les scénarios RPC sur HTTP volumineux, consultez [équilibrage de charge Microsoft RPC](rpc-load-balancing.md).

 

 




