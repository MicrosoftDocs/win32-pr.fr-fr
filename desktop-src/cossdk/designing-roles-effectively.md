---
description: Dans de nombreux scénarios, la sécurité basée sur les rôles est un mécanisme très efficace, mais dans certains cas, il est moins efficace.
ms.assetid: 6a1e6cf3-7a8c-4249-926d-675a54061adf
title: Conception efficace des rôles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 134b1caa68c06aef14a21963bb01ee4dfd12f43153ea917487598d76b0e36d5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991119"
---
# <a name="designing-roles-effectively"></a>Conception efficace des rôles

Dans de nombreux scénarios, la sécurité basée sur les rôles est un mécanisme très efficace, mais dans certains cas, il est moins efficace. Vous devez tenir compte d’un certain nombre de facteurs lorsque vous décidez de l’emplacement et de l’application de la sécurité basée sur les rôles à une application particulière.

## <a name="user-and-data-characteristics-and-the-suitability-of-roles"></a>Caractéristiques des utilisateurs et des données et de l’adéquation des rôles

Les rôles fonctionnent très bien pour caractériser des groupes d’utilisateurs et, sur cette base, filtrer les actions que ces utilisateurs peuvent effectuer. souvent, cela est effectué en pratique en créant des rôles qui reflètent l’emplacement d’un utilisateur au sein d’une organisation, par exemple, les rôles « gestionnaires » et « responsables », « administrateurs » et « lecteurs », « Project un employé » et « Project deux employés ». Dans ce cas, lorsque les données qui sont accessibles sont relativement génériques par rapport aux utilisateurs, les rôles peuvent être utilisés efficacement pour appliquer des règles d’entreprise telles que les suivantes :

-   «Les responsables peuvent transférer n’importe quel montant d’argent. Les raconteurs peuvent transférer uniquement jusqu’à $10 000.»

-   «Les administrateurs peuvent modifier quoi que ce soit. Tout le monde peut uniquement lire.»

-   «Project un employé peut accéder à une certaine base de données. Personne d’autre ne peut le faire.»

Les utilisateurs peuvent tomber naturellement dans plusieurs rôles, en fonction de la façon dont les rôles modélisent la structure organisationnelle d’une entreprise.

Toutefois, les rôles ne fonctionnent pas très bien lorsqu’une décision d’accès à la sécurité repose sur les caractéristiques d’un élément de données particulier. Par exemple, il serait difficile d’utiliser des rôles pour refléter des relations de données utilisateur complexes, telles que les suivantes :

-   « Un gestionnaire particulier peut accéder aux données du personnel pour ses rapports uniquement ».

-   « Joe Consumer peut rechercher le solde de son compte ».

Dans ce cas, la vérification de la sécurité doit souvent être effectuée au niveau de la base de données, où il est plus facile de prendre en compte les caractéristiques innées des données faisant l’objet d’un accès. Cela signifie que vous devez utiliser l' *emprunt d’identité* pour transmettre l’identité du client à la base de données et laisser la base de données valider la demande. Cela peut affecter les performances et peut affecter la conception de l’application, par exemple, le regroupement de connexions peut ne pas fonctionner quand une connexion est ouverte sous une identité d’utilisateur spécifique. Pour plus d’informations sur les problèmes liés à, consultez sécurité et [emprunt d’identité des clients et délégation](client-impersonation-and-delegation.md)de l' [application multiniveau](multi-tier-application-security.md) .

## <a name="complexity-and-scalability-of-a-role-based-authorization-policy"></a>Complexité et extensibilité d’une stratégie d’autorisation Role-Based

Quelle que soit la stratégie de sécurité que vous mettez en place, elle est aussi efficace que celle des administrateurs système qui déploient votre application. Si les administrateurs font des erreurs lors de l’attribution d’utilisateurs aux rôles appropriés conformément à votre stratégie de sécurité, votre stratégie ne fonctionnera pas comme prévu. Des problèmes sont susceptibles de se produire dans les circonstances suivantes :

-   Vous avez effectué une stratégie basée sur les rôles très complexe, avec de nombreux rôles et utilisateurs mappés à de nombreux rôles.
-   Vous créez des rôles avec des critères ambigus pour ceux qui doivent leur appartenir.
-   Il y a de nombreux utilisateurs sur le site sur lequel l’application est installée, et les utilisateurs se déplacent souvent au sein de l’organisation, en modifiant par rapport aux rôles que vous avez créés.
-   Il existe de nombreux administrateurs sur le site sur lequel l’application est installée, avec la répartition des responsabilités, afin qu’un administrateur connaissant les exigences de sécurité de votre application ne soit pas familier avec les grands groupes d’utilisateurs qui doivent l’utiliser. Cela pose un problème particulier lorsque les utilisateurs se déplacent au sein de l’organisation. ces informations doivent être communiquées correctement.

En outre, à mesure que le nombre de rôles affectés à une application augmente, le temps que COM+ doit consacrer à la recherche de l’appartenance de l’appelant à ces rôles, avec une dégradation probable des performances.

Pour gérer la complexité et atténuer ces préoccupations, vous pouvez suivre les instructions suivantes :

-   Choisissez des noms de rôle qui sont explicites. Rendez le plus évident possible les utilisateurs qui doivent appartenir aux rôles.
-   Rendez votre stratégie basée sur les rôles aussi simple que possible (et pas plus simple). Choisissez le moins de rôles possible, tout en conservant une stratégie efficace.
-   Documentez clairement la stratégie basée sur les rôles que vous construisez pour les administrateurs, que l’appartenance aux rôles soit évidente (pour vous). En particulier, utilisez le champ Description disponible pour chaque rôle pour décrire l’intention du rôle. Si vous ne pouvez pas décrire en général qui doit appartenir au rôle dans quelques phrases, cela est probablement trop compliqué.
-   Suggérez fortement aux administrateurs de votre application de remplir des rôles avec des groupes d’utilisateurs plutôt qu’avec des utilisateurs individuels. Il s’agit d’une solution bien plus évolutive. Elle facilite la réaffectation ou la suppression d’utilisateurs lorsqu’ils se déplacent au sein de l’organisation et isole les administrateurs d’un certain nombre de problèmes de surveillance et de problèmes de communication.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Limites de sécurité](security-boundaries.md)
</dt> <dt>

[Informations de contexte de l’appel de sécurité](security-call-context-information.md)
</dt> <dt>

[Propriété de contexte de sécurité](security-context-property.md)
</dt> <dt>

[Utilisation de rôles pour l’autorisation du client](using-roles-for-client-authorization.md)
</dt> </dl>

 

 



