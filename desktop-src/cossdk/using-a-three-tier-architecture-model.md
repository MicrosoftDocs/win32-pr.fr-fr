---
description: Le modèle d’architecture à trois niveaux, qui est l’infrastructure fondamentale pour le modèle de conception logique, segmente les composants d’une application en trois niveaux de services.
ms.assetid: a03327c1-e427-4c07-b3d4-808ce81c2c96
title: Utilisation d’un modèle d’architecture Three-Tier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e20b765a6d103f3c349ffd9a44853f495c64a070
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393188"
---
# <a name="using-a-three-tier-architecture-model"></a>Utilisation d’un modèle d’architecture Three-Tier

Le modèle d’architecture à trois niveaux, qui est l’infrastructure fondamentale pour le [modèle de conception logique](the-logical-model--application-definition-and-planning.md), segmente les composants d’une application en trois niveaux de services. Ces niveaux ne correspondent pas nécessairement à des emplacements physiques sur différents ordinateurs sur un réseau, mais plutôt à des couches logiques de l’application. La façon dont les éléments d’une application sont distribués dans une topologie physique peut changer en fonction de la configuration requise.

Voici une brève description des services alloués à chaque niveau :

-   **La couche présentation, ou couche services utilisateur, permet à un utilisateur d’accéder à l’application.** Cette couche présente les données à l’utilisateur et permet éventuellement la manipulation de données et l’entrée de données. Les deux principaux types d’interface utilisateur pour cette couche sont l’application traditionnelle et l’application Web. Les applications basées sur le Web contiennent désormais souvent la plupart des fonctionnalités de manipulation de données utilisées par les applications traditionnelles. Cela s’effectue grâce à l’utilisation de sources de données et de curseurs de données côté client et DHTML dynamiques.

    > [!Note]  
    > Dans une application à trois niveaux, l’application côté client est skinniere qu’une application client-serveur, car elle ne contient pas les composants de service situés à présent dans la couche intermédiaire. Cela réduit le temps de traitement de l’utilisateur, mais davantage de trafic réseau pour le système, car les composants sont répartis entre les différents ordinateurs.

     

-   **La couche intermédiaire, ou couche de services d’entreprise, se compose de règles métier et de données.** Également connu sous le terme de *niveau de logique métier*, la couche intermédiaire est l’endroit où les développeurs com+ peuvent résoudre des problèmes métier stratégiques et obtenir des avantages de productivité majeurs. Les composants qui composent cette couche peuvent exister sur un serveur, pour faciliter le partage des ressources. Ces composants peuvent être utilisés pour appliquer des règles d’entreprise, telles que les algorithmes métier et les réglementations juridiques ou gouvernementales, et les règles de données, qui sont conçues pour maintenir la cohérence des structures de données dans des bases de données spécifiques ou multiples. Étant donné que ces composants de couche intermédiaire ne sont pas liés à un client spécifique, ils peuvent être utilisés par toutes les applications et peuvent être déplacés vers des emplacements différents, car le temps de réponse et les autres règles requièrent. Par exemple, les modifications simples peuvent être placées côté client pour réduire les allers-retours sur le réseau, ou les règles de données peuvent être placées dans des procédures stockées.

-   **La couche de données, ou couche de services de données, interagit avec les données persistantes généralement stockées dans une base de données ou dans un stockage permanent.** Il s’agit de la couche d’accès SGBD réelle. Elle est accessible par le biais de la couche des services d’entreprise et, à l’occasion, par la couche des services de l’utilisateur. Cette couche se compose de composants d’accès aux données (plutôt que de connexions SGBD brutes) pour faciliter le partage des ressources et permettre la configuration des clients sans installer les bibliothèques SGBD et les pilotes ODBC sur chaque client.

Pendant le cycle de vie d’une application, l’approche à trois niveaux offre des avantages tels que la réutilisabilité, la flexibilité, la facilité de gestion, la facilité de maintenance et l’évolutivité. Vous pouvez partager et réutiliser les composants et les services que vous créez, et vous pouvez les distribuer sur un réseau d’ordinateurs en fonction des besoins. Vous pouvez diviser des projets de grande taille et complexes en projets plus simples et les assigner à différents programmeurs ou équipes de programmation. Vous pouvez également déployer des composants et des services sur un serveur pour vous aider à suivre les modifications, et vous pouvez les redéployer au fur et à mesure que la croissance de la base d’utilisateurs, des données et du volume de transactions augmente.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Modèle logique : définition et planification de l’application](the-logical-model--application-definition-and-planning.md)
</dt> </dl>

 

 



