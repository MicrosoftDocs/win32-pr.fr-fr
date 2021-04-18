---
description: L’évolutivité est la capacité d’une application à traiter une charge supplémentaire avec une augmentation linéaire de l’utilisation des ressources.
ms.assetid: 8249f1af-9c96-4545-ad6a-3736c6e63c6d
title: Conception pour l’évolutivité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54ab0aa9d67afaac14c6d8f59df34183bde36113
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543070"
---
# <a name="designing-for-scalability"></a>Conception pour l’évolutivité

L’évolutivité est la capacité d’une application à traiter une charge supplémentaire avec une augmentation linéaire de l’utilisation des ressources. L’évolutivité est importante dans toutes les applications distribuées. Les limites de l’évolutivité sont généralement centrées autour de l’utilisation des ressources et des dépendances créées par inadvertance dans la conception de l’application.

La liste suivante décrit les problèmes d’extensibilité et suggère des solutions :

-   Ressources intra-ordinateur. Le nombre de threads et de mémoire disponibles peut limiter l’extensibilité. Utilisez un modèle de thread plus efficace pour votre application.
-   Ressources inter-ordinateurs. Le nombre d’ordinateurs disponibles pour distribuer la charge de travail d’application peut affecter l’évolutivité.
-   Affinité du client. Deux situations d’affinité peuvent être créées par inadvertance par une application : une situation dans laquelle l’application dépend de l’état des données envoyées par le client avec sa demande ; et une situation dans laquelle l’application requiert un état spécifique au client. Évitez de concevoir la dépendance d’État entre le client et l’application.
-   Affinité de serveur. Une application COM+ peut limiter son extensibilité en créant une affinité de serveur, où l’application dépend de l’option accéder à un ordinateur serveur particulier pour obtenir des informations. Cette affinité peut se produire avec de nombreuses applications orientées base de données. Pour éviter un goulot d’étranglement au niveau du serveur, la meilleure méthode consiste à partitionner les données sur différents ordinateurs serveurs. Par exemple, vous pouvez diviser les données client entre les serveurs à l’aide de la clé la plus fréquemment utilisée, ou étendre une base de données client sur plusieurs serveurs à l’aide du nom de famille du client (par exemple, server1 : a-f, Server2 : g-m, Server3 : n-z).
    > [!Note]  
    > Le partitionnement des données peut ajouter une grande complexité à la logique de programmation et ne doit être effectué qu’une fois que d’autres options pour augmenter l’évolutivité ont été essayées.

     

-   Durée de vie des objets. Pour être évolutive, une application COM+ doit prêter une attention particulière à la durée de vie des objets. Bien qu’un objet existe, il consomme des ressources. Il est important de s’assurer que les durées de vie des objets qui détiennent des ressources coûteuses sont gérées avec soin. Pour les objets à forte demande qui ne consomment pas de ressources coûteuses, le [regroupement d’objets com+](com--object-pooling.md) peut augmenter l’évolutivité, car vous pouvez modifier administrativement les valeurs de regroupement pour tirer parti de tout le matériel que vous pourriez avoir. Et c’est un moyen naturel de régir les connexions : par exemple, si vous disposez d’une licence pour 20 connexions SQL, vous pouvez dicter cela avec le paramètre de pool max.
-   Regroupement des composants d’application. Pour améliorer l’évolutivité d’une application COM+, les composants de niveau intermédiaire doivent être divisés en services qui dépendent du temps et du temps. Cela vous permet de vous concentrer sur l’utilisation éventuelle d’un service Microsoft Windows pour implémenter une action de composant requise. Par exemple, vous pouvez choisir d’utiliser un service comme [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) ou des [composants en file d’attente com+](com--queued-components.md) pour gérer des tâches asynchrones indépendantes du temps.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Conception pour la disponibilité](designing-for-availability.md)
</dt> <dt>

[Conception pour le déploiement](designing-for-deployment.md)
</dt> <dt>

[Conception pour la sécurité](designing-for-security.md)
</dt> </dl>

 

 



