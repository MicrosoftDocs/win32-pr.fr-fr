---
description: Le modèle de programmation distribuée de Microsoft est constitué de plusieurs technologies, notamment MSMQ, IIS, DCOM et COM+. Tous ces services ont été conçus pour être utilisés par des applications distribuées.
ms.assetid: c72bbd47-0219-40ba-a7d5-2a6b725972d0
title: Hypothèses et principes de conception de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7dea86c404896a3d6095d39ebd6031767f6ccdd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126922964"
---
# <a name="com-design-assumptions-and-principles"></a>Hypothèses et principes de conception de COM+

Le modèle de programmation distribuée de Microsoft est constitué de plusieurs technologies, notamment MSMQ, IIS, DCOM et COM+. Tous ces services ont été conçus pour être utilisés par des applications distribuées.

COM+ a été développé pour faciliter la création d’applications distribuées. L’architecture globale est basée sur un ensemble d’hypothèses et de principes.

## <a name="assumptions"></a>Hypothèses

Les hypothèses sont les suivantes :

-   **L’application COM+ prend en charge plusieurs utilisateurs sur plusieurs serveurs.** En d’autres termes, vous créez une application distribuée, et ces utilisateurs seront sur différents ordinateurs hôtes à partir desquels le code s’exécute. Les utilisateurs vont accéder au code via Internet ou via un réseau privé. l’interface utilisateur va être présentée via un navigateur ou une application personnalisée, telle qu’une application basée sur des formulaires écrite avec Microsoft Visual Basic ou MFC. Cette interface utilisateur va se trouver sur l’ordinateur client.
-   **L’application COM+ peut être mise à l’échelle et offrir une plus grande disponibilité et fiabilité en déployant l’application sur plusieurs serveurs.** en procédant ainsi, vous pouvez équilibrer la charge de travail de l’application et fournir une tolérance de panne à l’aide du clustering de Windows.
-   **En cas de problème, l’état des données persistantes, stockées dans une base de données, à partir d’une application COM+ sera conservé si vous utilisez des transactions.** L’état de l’application doit survivre à des accidents qui peuvent se produire, tels que des erreurs d’application, des pannes du système ou des défaillances du réseau.

## <a name="principles"></a>Principes

Outre ces trois hypothèses, les principes suivants affectent le modèle de programmation COM+ :

-   **La logique d’application réside sur les ordinateurs serveurs, et non sur les ordinateurs clients.** Il existe trois raisons principales à cela :
    -   L’ordinateur client ne dispose peut-être pas de la puissance de traitement ou des fonctionnalités nécessaires pour exécuter la logique d’application. En outre, la conservation de la logique d’application sur le serveur simplifie le déploiement.
    -   Les ordinateurs serveurs sont souvent plus proches des données, et ces données sont le plus souvent dans une base de données. Étant donné que votre application accède aux bases de données, vous devez être très sensible au coût des connexions de base de données. En plaçant la plus grande partie de la logique sur les ordinateurs serveurs, vous pouvez partager des connexions de base de données et obtenir une amélioration significative des performances. D’autres ressources sur les ordinateurs serveurs peuvent également être partagées, avec un avantage en matière de performances.
    -   La logique d’application résidant sur les serveurs garde le contrôle du contexte de sécurité avec l’application. Vous bénéficiez d’un contrôle accru sur la sécurité si vous conservez cette sécurité sur des composants d’application exécutés sur des serveurs plutôt que sur des ordinateurs clients.
-   **Les transactions sont le noyau.** Par défaut, les transactions permettent d’obtenir le modèle de programmation COM+ qui est très important pour que vous les compreniez. Bien que vous puissiez utiliser un grand nombre des services de COM+ sans utiliser de transactions, si vous choisissez de ne pas les utiliser, vous ne pouvez pas tirer pleinement parti des services COM+ mis à votre disposition. Voici quelques-uns des principaux avantages de l’utilisation des transactions :
    -   Les transactions constituent une solution raisonnable pour le problème de la gestion de la concurrence. En outre, les transactions aident à vous protéger contre les pannes et ont un bon modèle de récupération d’erreur. En outre, les transactions sont un excellent moyen de gérer des tâches sur plusieurs systèmes.
    -   Vous pouvez concevoir une application COM+ basée sur des transactions pour qu’elle fonctionne avec un gestionnaire de ressources et une base de données, ce qui permet de protéger la plupart des informations d’État. En conservant l’État à l’intérieur d’une base de données ou d’un autre stockage géré par un gestionnaire de ressources, vous n’avez pas besoin de conserver un grand État dans les objets réels créés par votre application. Bien qu’il s’agit d’un départ d’un modèle purement orienté objet, il fonctionne bien pour la création d’applications distribuées avec récupération d’erreur.
-   **Les fonctionnalités d’application sont générées en tant qu’objets COM, encapsulant les protocoles utilisés pour communiquer avec d’autres systèmes ou technologies.** Étant donné que vous créez probablement des composants qui vont réunir plusieurs technologies ou systèmes hérités, envisagez d’utiliser un large éventail de protocoles de communication. Utilisez le protocole HTTP pour la communication client/serveur ou la communication entre applications via Internet. Utilisez DCOM pour la communication entre les applications et les composants sur le serveur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions de base pour la conception d’applications COM+](basic-guidelines-for-designing-com--applications.md)
</dt> <dt>

[Conception de l’application COM+ à l’aide d’UML](designing-the-com--application-using-uml.md)
</dt> <dt>

[Astuces de conception générale pour l’utilisation de COM+](general-design-tips-for-using-com-.md)
</dt> <dt>

[Optimisation des interactions avec le niveau de logique métier COM+](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> <dt>

[Autres outils Microsoft pour la création d’applications distribuées](other-microsoft-tools-for-building-distributed-applications.md)
</dt> </dl>

 

 



