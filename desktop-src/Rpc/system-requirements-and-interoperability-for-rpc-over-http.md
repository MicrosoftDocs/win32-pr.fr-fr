---
title: Configuration système requise pour RPC sur HTTP, interopérabilité
description: Microsoft RPC prend en charge RPC sur HTTP, comme indiqué dans le tableau suivant.
ms.assetid: 1815315c-1286-4e60-b3a2-a02cb3016fca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 880f078ea481be59448612b5024bbec4d2f54fa5
ms.sourcegitcommit: b95a94ffffda33f9ebbdd41787c01866444b4cf4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/27/2019
ms.locfileid: "104030652"
---
# <a name="rpc-over-http-system-requirements-interoperability"></a>Configuration système requise pour RPC sur HTTP, interopérabilité

Microsoft RPC prend en charge RPC sur HTTP, comme indiqué dans le tableau suivant.



| Plateforme                             | Prise en charge                       | Commentaires                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Server 2003                  | Clients, serveurs et proxy RPC | Prend en charge RPC sur HTTP v1 et RPC sur le client et le serveur HTTP v2. Le proxy RPC prend en charge RPC sur HTTP v2 quand IIS s’exécute en mode IIS 6,0. Le proxy RPC prend en charge RPC sur HTTP v1 et RPC sur HTTP v2 quand IIS s’exécute en mode IIS 5,0. Toutefois, l’exécution en mode IIS 5,0 n’est pas recommandée. Pour plus d’informations, consultez [recommandations relatives au déploiement de RPC sur http](rpc-over-http-deployment-recommendations.md) . Le serveur RPC sur HTTP et le proxy RPC peuvent se trouver sur des ordinateurs différents. |
| Windows XP avec Service Pack 1 (SP1) | Clients et serveurs            | Prend en charge RPC sur HTTP v1 et RPC sur le client et le serveur HTTP v2. Ne prend pas en charge le proxy RPC.                                                                                                                                                                                                                                                                                                                                                                                         |
| Windows XP                           | Clients et serveurs            | Prend en charge RPC sur le client et le serveur HTTP v1 uniquement. Ne prend pas en charge le proxy RPC.                                                                                                                                                                                                                                                                                                                                                                                                         |
| Windows 2000                         | Clients, serveurs et proxy RPC | Le programme serveur RPC sur HTTP et le proxy RPC peuvent s’exécuter sur des ordinateurs différents. Le client RPC sur HTTP, le serveur et le proxy RPC prennent uniquement en charge RPC sur HTTP v1.                                                                                                                                                                                                                                                                                                                   |



 

En outre, les conditions suivantes s’appliquent :

-   Windows 2000 et versions ultérieures requièrent l’utilisation d’IIS 4,0 ou version ultérieure.
-   Le proxy RPC sur HTTP s’exécute uniquement sur les éditions Windows Server.
-   Si IIS s’exécute sur une version serveur de Windows, le programme serveur RPC sur HTTP peut s’exécuter sur n’importe quel ordinateur sur lequel le proxy RPC est configuré pour transférer le trafic. Par conséquent, il peut s’exécuter sur le même ordinateur que le proxy RPC ou sur un autre ordinateur.

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



 

Par exemple, imaginez un client Windows 2000, un proxy Windows Server 2003 avec IIS exécuté en mode IIS 6,0 et un serveur Windows Server 2003 RPC sur HTTP. Le premier tableau de cette page de référence indique que Windows 2000 prend en charge uniquement RPC sur HTTP v1. La même table révèle qu’un serveur Windows Server 2003 avec IIS s’exécutant en mode IIS 6,0 prend en charge uniquement RPC sur HTTP v2 et qu’un serveur Windows Server 2003 RPC sur HTTP prend en charge RPC sur HTTP v1 et RPC sur HTTP v2. Ce scénario est décrit dans la ligne 6 de la deuxième table de cette page de référence, où il indique qu’une connexion RPC sur HTTP ne peut pas être établie. En outre, la deuxième table révèle que deux options existent pour ce scénario :

-   Si la sécurité et la robustesse ne sont pas prises en compte, IIS peut être basculé vers le mode IIS 5,0 où il prend en charge à la fois RPC sur HTTP v1 et RPC sur HTTP v2. Cela permet d’établir une connexion RPC sur HTTP v1.
-   Mettez à niveau le client Windows 98 vers Windows XP avec SP1 et procurez-vous la puissance, la sécurité et la robustesse d’une connexion RPC sur HTTP v2.

 

 




