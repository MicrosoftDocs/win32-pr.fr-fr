---
title: Liste des commandes
description: Une liste de commandes est une séquence de commandes GPU qui peut être enregistrée et lue. Une liste de commandes peut améliorer les performances en réduisant la quantité de surcharge générée par le Runtime.
ms.assetid: 4f581bc7-6c5e-4e56-b768-7f3cc5dbcb3e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27f8821645588ac7a9b48a4f6ce562c8c48cf96
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673894"
---
# <a name="command-list"></a>Liste des commandes

Une liste de commandes est une séquence de commandes GPU qui peut être enregistrée et lue. Une liste de commandes peut améliorer les performances en réduisant la quantité de surcharge générée par le Runtime.

Utilisez une liste de commandes dans les scénarios suivants :

-   Dans un frame unique, affichez une partie de la scène sur un thread tout en enregistrant une autre partie de la scène sur un deuxième thread. À la fin du frame, lisez la liste de commandes enregistrée sur le premier thread. Utilisez cette approche pour mettre à l’échelle des tâches de rendu complexes sur plusieurs threads ou cœurs.
-   Pré-enregistre une liste de commandes avant de devoir la restituer (par exemple, pendant le chargement d’un niveau) et la relire efficacement plus tard dans votre scène. Cette optimisation fonctionne bien lorsque vous devez effectuer un rendu fréquent.

Une liste de commandes est immuable et conçue pour être enregistrée et lue lors d’une seule exécution d’une application. Une liste de commandes n’est pas conçue pour être préenregistrée avant l’exécution du jeu et chargée à partir de votre média, car il n’existe aucun moyen de conserver la liste.

Une liste de commandes doit être enregistrée par un contexte différé, mais elle ne peut être lue que dans un contexte immédiat. Les contextes différés peuvent générer simultanément des listes de commandes.

-   Pour enregistrer une liste de commandes, consultez [Comment : enregistrer une liste de commandes](overviews-direct3d-11-render-multi-thread-command-list-record.md).
-   Pour lire une liste de commandes, consultez [Comment : lire une liste de commandes](overviews-direct3d-11-render-multi-thread-command-list-play.md).
-   Lorsque vous utilisez une liste de commandes, les performances dépendent de la quantité de prise en charge implémentée dans un pilote. Pour vérifier la prise en charge des pilotes, consultez [procédure : vérifier la prise en charge des pilotes](overviews-direct3d-11-render-multi-thread-support.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Rendu immédiat et différé](overviews-direct3d-11-render-multi-thread-render.md)
</dt> <dt>

[MultiThreading](overviews-direct3d-11-render-multi-thread.md)
</dt> </dl>

 

 




