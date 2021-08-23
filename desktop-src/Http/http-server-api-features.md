---
title: Fonctionnalités de l’API du serveur HTTP
description: Cette rubrique prenait en charge et ne prenait pas en charge les fonctionnalités de l’API du serveur HTTP.
ms.assetid: 448fe5a5-e79f-4c3a-aa76-94cff988f24f
keywords:
- Fonctionnalités de l’API du serveur HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eaf567d4576618b07ef5ad8dec91b360f37ab46eb820ff52e2bca896ca91a36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014777"
---
# <a name="http-server-api-features"></a>Fonctionnalités de l’API du serveur HTTP

Les listes suivantes décrivent les fonctionnalités prises en charge et non prises en charge de l’API du serveur HTTP.

## <a name="features-supported"></a>Fonctionnalités prises en charge

HTTP prend en charge les fonctionnalités suivantes :

-   Fonctionnalités du serveur HTTP v 1.0 et v 1.1.
-   SSL (Secure Sockets Layer) 3,0 (SSL) avec prise en charge des certificats client et serveur.
-   Mise en cache des fragments de données à utiliser dans les réponses suivantes.
-   Prise en charge de l’adressage IPv6 et IPv4.
-   Réservations d’espaces de noms d’URL pour la sécurité de l’application.
-   Handles true pour tous les objets.
-   Modèles d’e/s synchrones et asynchrones.
-   la prise en charge de WOW64 sur les ordinateurs qui exécutent des Windows 64 bits à partir de Windows Server 2003 avec Service Pack 1 (SP1).

## <a name="features-not-supported"></a>Fonctionnalités non prises en charge

L’API du serveur HTTP ne prend pas en charge les fonctionnalités suivantes :

-   L’API du serveur HTTP n’effectue pas l’authentification du client ou du serveur en fonction du contenu des en-têtes de requête HTTP. Toute authentification requise doit être implémentée par l’application.
-   WOW64 sur les ordinateurs s’exécutant sur les Windows 64 bits n’est pas pris en charge sur Windows Server 2003 et Windows XP avec Service Pack 2 (SP2) et versions antérieures.
-   L’API du serveur HTTP ne prend pas en charge la journalisation des requêtes et des réponses HTTP.
-   L’API du serveur HTTP ne segmente pas les réponses HTTP sortantes. L’application doit implémenter la segmentation des réponses si nécessaire.

 

 




