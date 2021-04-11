---
description: Une fois les modèles conceptuels et logiques terminés, vous pouvez prendre des décisions sur l’implémentation physique de l’application.
ms.assetid: 18c440f0-88c8-4738-9f29-c82772439b51
title: 'Modèle physique : architecture de l’application'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f0fab87d76e445a365958ab330f572f657d1505
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111426"
---
# <a name="the-physical-model-application-architecture"></a>Modèle physique : architecture de l’application

Une fois les modèles conceptuels et logiques terminés, vous pouvez prendre des décisions sur l’implémentation physique de l’application. Pour créer le modèle physique, vous devez comprendre où se trouvent les différents services de l’application et comment ils doivent être implémentés. Il est recommandé de déterminer l’emplacement des différents services avant d’implémenter les services.

Une règle de base pour déterminer l’emplacement des différents services est la suivante : placer le composant dans lequel il est utilisé. Si, par exemple, un composant affiche des informations pour le client de base, il doit se trouver sur l’ordinateur de l’utilisateur. Si un composant valide des informations à partir du client de base, il doit également résider sur l’ordinateur du client de base. Si un composant met à jour des informations dans une base de données, il doit résider sur le serveur de base de données.

Il existe, bien sûr, des considérations supplémentaires qui rendent des exceptions à cette règle. Les problèmes de performances et de sécurité peuvent également dicter l’emplacement d’un composant. Tenez compte des éléments suivants :

-   Un composant va-t-il changer fréquemment, ce qui complique la distribution des mises à jour ?
-   Le composant sera-t-il utilisé par d’autres applications, par exemple un composant de vérification de sécurité courant ?
-   Le composant effectue-t-il des calculs longs ou exécute des fonctions, telles que l’impression, qui peuvent être déchargées sur un serveur ?
-   La sécurité d’un composant peut-elle être améliorée en la plaçant sur un serveur ?

Localiser correctement les composants d’une application peut également isoler l’équipe de développement du recodage coûteux si le système ou l’emplacement des données change. Par exemple, en plaçant les règles d’accès aux données dans une couche de données plutôt que dans des procédures stockées, il est plus facile d’isoler l’application de la dépendance sur un SGBD spécifique. Non seulement les modifications sont confinées et les tests sont compartimentés, mais les sources de données peuvent être modifiées et les données peuvent être distribuées sans modification radicale de l’application.

Enfin, la localisation des composants doit tirer parti de l’efficacité du système. Il est temps et économique de placer des objets métier dans des emplacements centralisés sur le réseau. Les objets peuvent être partagés entre les applications, et les tests unitaires peuvent être effectués avant le déploiement des composants. Les coûts de maintenance peuvent également être réduits, car les modifications de règles ne se produisent qu’à un seul point.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Modèle conceptuel : exigences de l’application](the-conceptual-model--application-requirements.md)
</dt> <dt>

[Modèle logique : définition et planification de l’application](the-logical-model--application-definition-and-planning.md)
</dt> </dl>

 

 



