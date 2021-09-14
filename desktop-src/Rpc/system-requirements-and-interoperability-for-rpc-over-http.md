---
title: Configuration système requise pour RPC sur HTTP, interopérabilité
description: Microsoft RPC prend en charge RPC sur HTTP, comme indiqué dans le tableau suivant.
ms.assetid: 1815315c-1286-4e60-b3a2-a02cb3016fca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 880f078ea481be59448612b5024bbec4d2f54fa5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416598"
---
# <a name="rpc-over-http-system-requirements-interoperability"></a>Configuration système requise pour RPC sur HTTP, interopérabilité

Microsoft RPC prend en charge RPC sur HTTP, comme indiqué dans le tableau suivant.



| Plateforme                             | Prise en charge                       | Commentaires                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Server 2003                  | Clients, serveurs et proxy RPC | Prend en charge RPC sur HTTP v1 et RPC sur le client et le serveur HTTP v2. Le proxy RPC prend en charge RPC sur HTTP v2 quand IIS s’exécute en mode IIS 6,0. Le proxy RPC prend en charge RPC sur HTTP v1 et RPC sur HTTP v2 quand IIS s’exécute en mode IIS 5,0. Toutefois, l’exécution en mode IIS 5,0 n’est pas recommandée. pour plus d’informations, consultez [Recommandations de déploiement de RPC sur HTTP](rpc-over-http-deployment-recommendations.md) . Le serveur RPC sur HTTP et le proxy RPC peuvent se trouver sur des ordinateurs différents. |
| Windows XP avec Service Pack 1 (SP1) | Clients et serveurs            | Prend en charge RPC sur HTTP v1 et RPC sur le client et le serveur HTTP v2. Ne prend pas en charge le proxy RPC.                                                                                                                                                                                                                                                                                                                                                                                         |
| Windows XP                           | Clients et serveurs            | Prend en charge RPC sur le client et le serveur HTTP v1 uniquement. Ne prend pas en charge le proxy RPC.                                                                                                                                                                                                                                                                                                                                                                                                         |
| Windows 2000                         | Clients, serveurs et proxy RPC | Le programme serveur RPC sur HTTP et le proxy RPC peuvent s’exécuter sur des ordinateurs différents. Le client RPC sur HTTP, le serveur et le proxy RPC prennent uniquement en charge RPC sur HTTP v1.                                                                                                                                                                                                                                                                                                                   |



 

En outre, les conditions suivantes s’appliquent :

-   Windows 2000 et versions ultérieures requièrent l’utilisation d’IIS 4,0 ou version ultérieure.
-   le proxy RPC sur HTTP s’exécute uniquement sur les éditions Windows server.
-   si IIS s’exécute sur une version serveur de Windows, le programme serveur rpc sur HTTP peut s’exécuter sur n’importe quel ordinateur sur lequel le Proxy rpc est configuré pour transférer le trafic. Par conséquent, il peut s’exécuter sur le même ordinateur que le proxy RPC ou sur un autre ordinateur.

Pour qu’une connexion RPC sur HTTP soit établie, tout le client RPC sur http, le serveur RPC sur HTTP et le proxy RPC doivent s’accorder sur la version de RPC sur HTTP utilisée. S’il n’existe aucune version courante de RPC sur HTTP qui prend en charge les trois (client, serveur et proxy RPC), il n’est pas possible d’établir une connexion RPC sur HTTP. Le tableau suivant résume cette interopérabilité pour les différentes versions de RPC sur HTTP.



| Client RPC sur HTTP | Proxy RPC      | Serveur RPC sur HTTP | Fonctionne?                                      | Version utilisée     |
|----------------------|----------------|----------------------|---------------------------------------------|------------------|
| v1 uniquement              | v1 uniquement        | v1 uniquement              | Oui, avec des limitations v1                    | RPC sur HTTP v1 |
| v1 uniquement              | v1 uniquement        | V1 et v2       | Oui, avec des limitations v1                    | RPC sur HTTP v1 |
| v1 uniquement              | V1 et v2 | v1 uniquement              | Oui, avec des limitations v1                    | RPC sur HTTP v1 |
| v1 uniquement              | V1 et v2 | V1 et v2       | Oui, avec des limitations v1                    | RPC sur HTTP v1 |
| v1 uniquement              | v2 uniquement        | v1 uniquement              | Non                                          |                  |
| v1 uniquement              | v2 uniquement        | V1 et v2       | Non                                          |                  |
| V1 et v2       | v1 uniquement        | v1 uniquement              | Oui, avec des limitations v1                    | RPC sur HTTP v1 |
| V1 et v2       | v1 uniquement        | V1 et v2       | Oui, avec des limitations v1                    | RPC sur HTTP v1 |
| V1 et v2       | V1 et v2 | v1 uniquement              | Oui, avec des limitations v1                    | RPC sur HTTP v1 |
| V1 et v2       | V1 et v2 | V1 et v2       | Oui                                         | RPC sur HTTP v2 |
| V1 et v2       | v2 uniquement        | v1 uniquement              | Non                                          |                  |
| V1 et v2       | v2 uniquement        | V1 et v2       | Oui. Il s'agit de la configuration recommandée. | RPC sur HTTP v2 |



 

par exemple, imaginez un client Windows 2000, un proxy Windows Server 2003 avec iis s’exécutant en mode iis 6,0 et un serveur Windows RPC sur HTTP du 2003 serveur. le premier tableau de cette page de référence indique que Windows 2000 prend en charge uniquement RPC sur HTTP v1. la même table révèle qu’un Windows Server 2003 avec iis s’exécutant en mode iis 6,0 prend en charge uniquement rpc sur http v2 et qu’un serveur Windows 2003 rpc sur http prend en charge rpc sur http v1 et rpc sur http v2. Ce scénario est décrit dans la ligne 6 de la deuxième table de cette page de référence, où il indique qu’une connexion RPC sur HTTP ne peut pas être établie. En outre, la deuxième table révèle que deux options existent pour ce scénario :

-   Si la sécurité et la robustesse ne sont pas prises en compte, IIS peut être basculé vers le mode IIS 5,0 où il prend en charge à la fois RPC sur HTTP v1 et RPC sur HTTP v2. Cela permet d’établir une connexion RPC sur HTTP v1.
-   mettez à niveau le client Windows 98 vers Windows XP avec SP1 et obtenez la puissance, la sécurité et la robustesse d’une connexion RPC sur HTTP v2.

 

 




