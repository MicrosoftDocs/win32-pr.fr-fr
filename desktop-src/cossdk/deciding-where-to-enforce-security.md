---
description: Les compromis sont inhérents à l’application de la sécurité.
ms.assetid: f01573f3-aae6-400e-bdd9-6f34f4e262f6
title: Choix de l’emplacement de l’application de la sécurité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ac994fb98d50a7e26f1b8142e77dc9ff771f6b2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523260"
---
# <a name="deciding-where-to-enforce-security"></a>Choix de l’emplacement de l’application de la sécurité

Les compromis sont inhérents à l’application de la sécurité. Une base de données peut être un emplacement naturel pour mettre en place une logique de sécurité, étant donné que les données sont la chose la plus importante à protéger. Toutefois, cela a des implications significatives sur les performances. L’application de la sécurité au niveau de la base de données peut s’avérer très coûteuse, s’adapte médiocrement et n’est pas flexible.

## <a name="enforcing-security-in-the-middle-tier"></a>Application de la sécurité dans la couche intermédiaire

La règle générale à suivre avec les applications multiniveaux évolutives à l’aide de COM+ est que, chaque fois que cela est possible, vous devez appliquer une sécurité détaillée dans l’application COM+ au niveau intermédiaire. Cela vous permet de tirer pleinement parti des services évolutifs fournis par COM+. Appliquez l’authentification au niveau de la base de données uniquement lorsque vous en avez absolument besoin et évaluez entièrement les implications en matière de performances.

La situation optimale est de pouvoir sécuriser les tables de base de données afin que l’application COM+ puisse y accéder sous sa propre identité. La base de données doit simplement authentifier l’application COM+ et l’approuver pour authentifier et autoriser correctement les clients qui accèdent aux données. Les avantages de cette approche sont les suivants :

-   Il permet le regroupement de connexions entre tous les clients, car les connexions sont entièrement génériques.
-   Il optimise généralement l’accès aux données, souvent un point d’amaigrissement problématique lors de la mise à l’échelle des applications.
-   Cela peut réduire la surcharge logique pour l’application de la sécurité, en particulier si la sécurité déclarative basée sur les rôles peut être utilisée.
-   Il peut fournir une grande flexibilité dans une stratégie de sécurité. Vous pouvez le configurer et le reconfigurer facilement, comme décrit dans administration de la [sécurité basée sur les rôles](role-based-security-administration.md).

Toutefois, comme nous l’avons vu dans [conception de rôles de manière efficace](designing-roles-effectively.md), bien que les rôles puissent être appliqués facilement et efficacement à certaines relations utilisateur-données, ils ne constituent pas une solution universelle pour prendre des décisions d’accès à la sécurité.

## <a name="enforcing-security-at-the-database"></a>Application de la sécurité au niveau de la base de données

Malgré l’application de la sécurité au niveau intermédiaire, il existe plusieurs raisons pour mettre en œuvre la sécurité dans la base de données, notamment les suivantes :

-   Vous n’avez pas de choix, peut-être pour des raisons d’héritage ou peut-être parce que la décision n’est tout simplement pas dans vos mains.
-   La base de données est accessible par un large éventail d’applications et sa sécurité ne peut pas être configurée sur la base d’une seule application.
-   Une base de données peut être rendue protégée de manière prévisible. Si vous conservez les données critiques de l’entreprise dans une base de données, vous pouvez dessiner un petit wagon et aider à contrôler qui le voit.
-   L’authentification des clients d’origine dans la base de données permet une journalisation détaillée des personnes qui ont fait quoi dans la base de données.
-   Certaines données sont liées à des utilisateurs particuliers, et la logique de prise de décisions d’accès extrêmement affinées peut être plus efficace dans la base de données elle-même, à proximité des données.

Lorsque vous avez le luxe de concevoir la sécurité de la base de données et de l’application COM+ en tandem, la plupart de ces problèmes se rapportent aux caractéristiques des données elles-mêmes et à leur relation avec les utilisateurs qui y accèdent. Avec les données accessibles par des catégories d’utilisateurs prévisibles, il est efficace de contrôler l’accès au niveau intermédiaire à l’aide de rôles. Avec les données qui sont liées de manière complexe aux très petites catégories d’utilisateurs, ces relations doivent souvent être exprimées avec les données elles-mêmes et, par conséquent, vous devez appliquer une sécurité à la base de données.

### <a name="performance-implications-of-enforcing-security-at-the-database"></a>Implications sur les performances de l’application de la sécurité au niveau de la base de données

Si vous authentifiez ou autorisez des utilisateurs au niveau de la base de données, l’identité de l’utilisateur doit être propagée à la base de données pour prendre en charge cela. Si la base de données approuve l’application de couche intermédiaire pour ce faire, il est possible de transmettre les informations de sécurité utilisateur dans les paramètres. Dans le cas contraire, l’appel à la base de données doit être effectué sous l’identité de l’utilisateur, ce qui signifie que l’application serveur doit emprunter l’identité du client. Cela peut avoir des répercussions sur les performances, notamment les suivantes :

-   L’emprunt d’identité du client peut être beaucoup plus lent que l’appel direct sous l’identité de l’application. Pour plus d’informations, consultez [emprunt d’identité et délégation du client](client-impersonation-and-delegation.md).
-   Une connexion de base de données effectuée sous une identité d’utilisateur spécifique ne peut pas être regroupée.
-   L’ajout de logique dans la base de données elle-même exécute le risque de créer un goulot d’étranglement de mise à l’échelle.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Scénarios de base pour la sécurisation des données dans les applications multiniveau](basic-scenarios-for-securing-data-in-multi-tier-applications.md)
</dt> <dt>

[Sécurité des applications multiniveau](multi-tier-application-security.md)
</dt> </dl>

 

 



