---
title: Cohérence de thread
description: Toutes les fonctions de cette API peuvent être appelées en toute sécurité à partir de différents threads. Toutefois, chaque objet passé en tant que paramètre aux fonctions a un comportement de thread spécifique, comme décrit ci-dessous.
ms.assetid: 712d6750-884e-421a-8ecf-efcd4ec9b21d
keywords:
- Services Web de sécurité des threads pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fed84cac9634148742c92f1b0d4b4ecdb905ac42
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103734852"
---
# <a name="thread-safety"></a>Cohérence de thread

Toutes les fonctions de cette API peuvent être appelées en toute sécurité à partir de différents threads. Toutefois, chaque objet passé en tant que paramètre aux fonctions a un comportement de thread spécifique, comme décrit ci-dessous.


Les descripteurs suivants sont à thread unique et ne prennent pas en charge les opérations simultanées pour une instance particulière :

-   [\_tas WS](ws-heap.md)
-   [\_message WS](ws-message.md)
-   [\_ \_ mémoire tampon XML WS](ws-xml-buffer.md)
-   [\_lecteur XML \_ WS](ws-xml-reader.md)
-   [\_enregistreur XML \_ WS](ws-xml-writer.md)
-   [\_erreur WS](ws-error.md)
-   [contexte de l' \_ opération WS \_](ws-operation-context.md)
-   [\_stratégie WS](ws-policy.md)
-   [\_métadonnées WS](ws-metadata.md)
-   [\_jeton de sécurité WS \_](ws-security-token.md)
-   [\_contexte de sécurité WS \_](ws-security-context.md)

Les handles suivants sont des threads libres et prennent en charge les opérations simultanées pour une instance particulière :

-   [\_canal WS](ws-channel.md)
-   [\_écouteur WS](ws-listener.md)
-   [\_hôte de service WS \_](ws-service-host.md)
-   [\_proxy WS service \_](ws-service-proxy.md)

Pour tous ces handles, le Threading est défini en termes d’opérations (pas d’appels de fonction). Une opération est définie différemment pour les fonctions appelées de façon synchrone par rapport aux fonctions appelées de façon asynchrone :

-   Pour les fonctions appelées de façon synchrone, l’opération est en attente pendant l’exécution de la fonction.
-   Pour les fonctions appelées de façon asynchrone, si la fonction retourne un code de retour autre que **WS \_ S \_ Async** , l’opération est en attente pendant l’exécution de la fonction. Toutefois, si la fonction retourne **WS \_ S \_ Async** , l’opération est en attente jusqu’à ce que le [**\_ \_ rappel WS Async**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback) soit appelé. Pour plus d’informations sur l’appel de fonctions de manière asynchrone, consultez la rubrique [modèle asynchrone](asynchronous-model.md) . Pour les codes d’erreur, consultez [valeurs de retour des services Web Windows](windows-web-services-return-values.md).

Le fait de ne pas suivre le contrat de thread d’un objet entraîne un comportement indéfini.

 

 




