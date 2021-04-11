---
title: Clients multithread et handles de contexte
description: Quand vous avez un client multithread où plusieurs threads utilisent la même instance de handle de contexte, l’accès à l’instance de handle de contexte est sérialisé par défaut sur le serveur.
ms.assetid: 192be467-b1e0-422b-878a-738cb7d72b5b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67c621d75d8cc48ca1f71719066f455e0efce39f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031553"
---
# <a name="multithreaded-clients-and-context-handles"></a>Clients multithread et handles de contexte

Quand vous avez un client multithread où plusieurs threads utilisent la même instance de handle de contexte, l’accès à l’instance de handle de contexte est sérialisé par défaut sur le serveur. Cela évite au gestionnaire de serveur d’avoir à se prémunir contre un autre thread du même client en modifiant le contexte ou le contexte qui s’est exécuté pendant la distribution d’un appel. Toutefois, dans certains cas, la sérialisation peut avoir un impact sur les performances.

Considérez les éléments suivants : deux threads clients appellent un appel de procédure distante qui ne modifie pas l’état du contexte (par exemple, l’appel obtient simplement des valeurs à partir de celui-ci). De tels appels n’ont pas besoin d’être sérialisés.

Dans ce cas, Windows XP offre un modèle de sérialisation en mode mixte, où chaque méthode peut être déclarée comme disposant d’un accès exclusif ou partagé à un handle de contexte. Pour plus d’informations, consultez [ \_ \_ sérialisation de handle de contexte](/windows/desktop/Midl/context-handle-serialize) et handle de [contexte \_ \_ noserialize](/windows/desktop/Midl/context-handle-noserialize) .

Dans les versions de Windows antérieures à Windows XP, le seul moyen d’autoriser l’accès simultané à un handle de contexte consiste à appeler la fonction [**RpcSsDontSerializeContext**](/previous-versions/aa378473(v=vs.80)) pour permettre la distribution de plusieurs appels sur un seul handle de contexte. L’appel de la fonction **RpcSsDontSerializeContext** ne désactive pas entièrement la sérialisation ; Lorsqu’une exécution de contexte se produit, la routine d’exécution de contexte s’exécute uniquement lorsque toutes les demandes de client en suspens sont terminées. Un appel à **RpcScDontSerializeContext** affecte l’ensemble du processus et n’est pas réversible. L’utilisation de **RpcScDontSerializeContext** dans Windows XP et les versions ultérieures n’est pas recommandée. Cela rend le code du serveur très compliqué lorsqu’il s’agit d’une gestion fiable des conditions de concurrence inhérentes à des environnements totalement non sérialisés.

 

 