---
title: Utilisation de Transport-Level sécurité sur le client
description: Le client spécifie comment le serveur emprunte l’identité du client lorsque le client établit la liaison de chaîne.
ms.assetid: 0d02b7f2-4dcb-41e8-829c-6942dfdcd4c6
keywords:
- Appel de procédure distante RPC, tâches, à l’aide de la sécurité au niveau du transport sur le client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c10360d5b8d11640803e31ee1d1d0490a6edfdf7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941287"
---
# <a name="using-transport-level-security-on-the-client"></a>Utilisation de Transport-Level sécurité sur le client

Le client spécifie comment le serveur emprunte l’identité du client lorsque le client établit la liaison de chaîne. Ces informations de QOS sont fournies en tant qu’option de point de terminaison dans la liaison de chaîne. Le client peut spécifier le niveau d’emprunt d’identité, le suivi dynamique ou statique et l’indicateur d’efficacité uniquement.

**Pour fournir des informations de qualité de service pour le serveur**

1.  Le client appelle [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) pour créer les chaînes du composant, y compris les options de point de terminaison, dans le contexte de liaison de chaîne correct.
2.  Le client appelle [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) pour obtenir un nouveau handle de liaison et appliquer les informations de qualité de service pour le client.
3.  Le client effectue des appels de procédure distante à l’aide du descripteur.

Microsoft RPC prend en charge les fonctionnalités de sécurité Windows uniquement sur [**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np) et [**Ncalrpc**](/windows/desktop/Midl/ncalrpc). Les options de sécurité pour les autres transports sont ignorées.

Le client peut associer les paramètres de sécurité suivants à la liaison pour le transport de canal nommé [**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np) ou [**Ncalrpc**](/windows/desktop/Midl/ncalrpc):

-   Identification, emprunt d’identité ou anonyme. Spécifie le type de sécurité utilisé. La valeur par défaut est emprunt d’identité.
-   Dynamique ou statique. Détermine si les informations de sécurité associées à un thread sont une copie des informations de sécurité créées au moment où l’appel de procédure distante est effectué (statique) ou un pointeur vers les informations de sécurité (dynamique).

    Les informations de sécurité statiques ne changent pas. Le paramètre dynamique reflète les paramètres de sécurité actuels, y compris les modifications apportées après l’appel de procédure distante. Pour [**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np), la valeur par défaut pour les connexions de canaux nommés distants est statique, pour les connexions de canaux nommés locales, la valeur par défaut est dynamique.

-   **True** ou **false**. Spécifie la valeur de l’indicateur d’efficacité uniquement. La valeur **true** indique que seuls les privilèges de jeton activés au moment de l’appel sont effectifs. La valeur **false** indique que tous les privilèges sont disponibles et que l’application peut les modifier.

Une combinaison de ces paramètres peut être assignée à la liaison, comme illustré dans l’exemple suivant :

``` syntax
"Security=Identification Dynamic True"
"Security=Anonymous Static True"
"Security=Impersonation Static False"
```

Les paramètres de sécurité par défaut varient en fonction du protocole de transport.

Pour plus d’informations sur la syntaxe des options de point de terminaison, consultez [point de terminaison](/windows/desktop/Midl/endpoint).

 

 