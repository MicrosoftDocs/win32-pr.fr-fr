---
title: Différences dans le modèle de liaison de Direct3D 11
description: L’une des principales décisions de conception derrière la liaison DirectX12 est de la séparer des autres tâches de gestion. Cela impose des exigences sur l’application pour gérer certains dangers potentiels.
ms.assetid: 3EE7E9AE-203D-40D4-9F12-4313ED179035
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43b2785da6497fd4e775d9f88847928e7c4c08e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104224"
---
# <a name="differences-in-the-binding-model-from-direct3d-11"></a>Différences dans le modèle de liaison de Direct3D 11

L’une des principales décisions de conception derrière la liaison DirectX12 est de la séparer des autres tâches de gestion. Cela impose des exigences sur l’application pour gérer certains dangers potentiels.

Le principal avantage du modèle de liaison D3D12 est qu’il permet aux applications de modifier fréquemment les liaisons de texture, sans coût énorme de performances de l’UC. D’autres avantages sont que les nuanceurs ont accès à un très grand nombre de ressources, que les nuanceurs n’ont pas besoin de savoir à l’avance le nombre de ressources qui seront liées et qu’un modèle de liaison de ressources unifiées peut être utilisé indépendamment du matériel ou du contenu du contenu des applications.

Pour améliorer les performances, le modèle de liaison ne requiert pas que le système effectue le suivi des liaisons qu’une application a demandées pour l’utilisation du GPU et qu’il existe une propre intégration entre la liaison et les listes de commandes multithread.

Les sections suivantes répertorient certaines des modifications apportées au modèle de liaison de ressources depuis D3D11.

-   [Gestion de la résidence de la mémoire séparée de la liaison](#memory-residency-management-separated-from-binding)
-   [Gestion de la durée de vie des objets séparée de la liaison](#object-lifetime-management-separated-from-binding)
-   [Suivi de l’état des ressources du pilote séparé de la liaison](#driver-resource-state-tracking-separated-from-binding)
-   [Synchronisation de la mémoire mappée du GPU de l’UC séparée de la liaison](#cpu-gpu-mapped-memory-synchronization-separated-from-binding)
-   [Rubriques connexes](#related-topics)

## <a name="memory-residency-management-separated-from-binding"></a>Gestion de la résidence de la mémoire séparée de la liaison

Les applications ont un contrôle explicite sur les surfaces qu’elles doivent être disponibles pour que le GPU soit directement utilisé (appelé « résident »). Inversement, ils peuvent appliquer d’autres États sur les ressources, par exemple les rendre explicitement inrésidents ou laisser le système d’exploitation choisir pour certaines classes d’applications qui nécessitent un encombrement minimal de la mémoire. Le point important ici est que la gestion de l’application de ce qui est résident est entièrement dissociée de la façon dont elle donne accès aux ressources aux nuanceurs.

Le découplage de la gestion de la résidence à partir du mécanisme permettant aux nuanceurs d’accéder aux ressources réduit le coût du système/matériel pour le rendu, car le système d’exploitation n’a pas besoin d’inspecter constamment l’état de la liaison locale pour savoir ce qu’il faut faire résident. En outre, les nuanceurs n’ont plus à connaître les surfaces exactes qu’ils devront peut-être référencer, à condition que l’ensemble des ressources éventuellement accessibles ait été mis en attente à l’avance.

## <a name="object-lifetime-management-separated-from-binding"></a>Gestion de la durée de vie des objets séparée de la liaison

Contrairement aux API précédentes, le système n’effectue plus le suivi des liaisons des ressources avec le pipeline. Utilisé pour permettre au système de conserver les ressources actives que l’application a publiées parce qu’elles sont toujours référencées par un travail GPU en suspens.

Avant de libérer une ressource, telle qu’une texture, les applications doivent maintenant s’assurer que le GPU a terminé de la référencer. Cela signifie qu’avant qu’une application puisse libérer en toute sécurité une ressource, le GPU doit avoir terminé l’exécution de la liste de commandes référençant la ressource.

## <a name="driver-resource-state-tracking-separated-from-binding"></a>Suivi de l’état des ressources du pilote séparé de la liaison

Le système n’inspecte plus les liaisons de ressources pour comprendre le moment où des transitions de ressources ont eu lieu, ce qui nécessite un fonctionnement supplémentaire du pilote ou du GPU. Un exemple courant d’un grand nombre de processeurs graphiques et de pilotes doit savoir quand une surface passe d’être utilisée en tant que vue de la cible de rendu (RTV) sur le Affichage des ressources de nuanceur (SRV). Les applications elles-mêmes doivent maintenant déterminer à quel moment les transitions de ressources auxquelles le système peut s’intéresser se produisent via des API dédiées.

## <a name="cpu-gpu-mapped-memory-synchronization-separated-from-binding"></a>Synchronisation de la mémoire mappée du GPU de l’UC séparée de la liaison

Le système n’inspecte plus les liaisons de ressources pour comprendre si le rendu doit être retardé, car il dépend d’une ressource qui a été mappée pour l’accès de l’UC mais qui n’a pas encore été annulée. Les applications ont maintenant la responsabilité de synchroniser les accès à la mémoire de l’UC et du GPU. Pour faciliter cette opération, le système fournit des mécanismes permettant à l’application de demander le sommeil d’un thread d’UC jusqu’à ce que le travail soit terminé. L’interrogation peut également être effectuée, mais elle peut être moins efficace.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Liaison de ressource](resource-binding.md)
</dt> </dl>

 

 




