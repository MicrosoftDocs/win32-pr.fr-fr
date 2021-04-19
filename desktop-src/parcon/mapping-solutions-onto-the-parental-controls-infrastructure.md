---
description: Mappage de solutions sur l’infrastructure de contrôle parental
ms.assetid: 09677019-2cf9-43fe-b16c-e802767bef3a
title: Mappage de solutions sur l’infrastructure de contrôle parental
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea410663af2e3b2363b7026a6997da5c19a1077a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518673"
---
# <a name="mapping-solutions-onto-the-parental-controls-infrastructure"></a>Mappage de solutions sur l’infrastructure de contrôle parental

Cinq catégories d’offres d’éditeurs de logiciels indépendants et de fournisseurs de services Internet et de portails de contrôle parental sont évidentes :

-   Application cliente autonome. Les clients de messagerie et les lecteurs multimédias en sont des exemples. Bien que les lecteurs multimédias présentent un risque sur Internet et certains disposent de services spécifiques, les contrôles parentaux Windows promeuvent principalement la journalisation et les restrictions sur les activités de lecture uniquement afin de réduire l’impact de la bibliothèque et de consigner les bruits aux administrateurs.
-   Solutions client/serveur. Les exemples les plus évidents sont les solutions de messagerie instantanée.
-   Suites de fournisseurs de services Internet. Il s’agit de collections de solutions client/serveur et d’applications clientes, souvent intégrées dans une interface utilisateur client unique. Notez que la plupart de ces fonctionnalités fournissent également la plupart ou la totalité des fonctionnalités à l’aide de l’accès du navigateur, en passant par les solutions dans le Web uniquement.
-   Solutions Web uniquement. Accessible via le navigateur. Exemples de fonctionnalités de messagerie Web et de messagerie instantanée. L’accès à ces derniers peut être bloqué par des catégories de filtres Web correctement renseignées.
-   Solutions de type pare-feu. Fournit un filtrage au niveau de la pile réseau, et éventuellement d’autres restrictions du système d’exploitation.

Les recommandations pour l’implémentation de solutions conformes pour chaque catégorie sont spécifiées dans le tableau suivant.



| Category                           | Journalisation                                                  | Paramètres des restrictions                                    | Mise en application des restrictions                                 | Remplacement du filtre de contenu Web                                                        | Utilisation d’un lien d’extensibilité pour l’accès à la journalisation et aux paramètres               |
|------------------------------------|----------------------------------------------------------|----------------------------------------------------------|----------------------------------------------------------|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| Client « autonome »<br/>    | Requis sur le client<br/>                            | Requis sur le client<br/>                            | Requis sur le client<br/>                            | N/A<br/>                                                                        | Obligatoire, sera exe. Peut simplement appeler la navigation dans l’interface utilisateur de l’application<br/>   |
| Solution client/serveur<br/>  | Requis sur le client s’il n’est pas effectué par le serveur<br/> | Requis sur le client s’il n’est pas effectué par le serveur<br/> | Requis sur le client s’il n’est pas effectué par le serveur<br/> | N/A<br/>                                                                        | Obligatoire, sera exe<br/>                                        |
| Suite ISP<br/>               | Requis sur le client s’il n’est pas effectué par le serveur<br/> | Requis sur le client s’il n’est pas effectué par le serveur<br/> | Requis sur le client s’il n’est pas effectué par le serveur<br/> | Vous recommandons d’utiliser le filtre WPC, mais d’autoriser le remplacement s’il est robuste pour plusieurs utilisateurs<br/> | Obligatoire, sera exe<br/>                                        |
| Solution Web uniquement<br/>       | Recommandation d’exécution sur le serveur<br/>                | Recommandation d’exécution sur le serveur<br/>                | Recommandation d’exécution sur le serveur<br/>                | N/A<br/>                                                                        | Recommandé. Exposer la journalisation et les paramètres du serveur à l’aide de exe<br/> |
| Solutions de type pare-feu<br/> | Requis sur le client<br/>                            | Requis sur le client<br/>                            | Requis sur le client<br/>                            | Vous recommandons d’utiliser le filtre WPC, mais d’autoriser le remplacement s’il est robuste pour plusieurs utilisateurs<br/> | Obligatoire, sera exe<br/>                                        |



 

 

 




