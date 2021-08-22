---
description: Une ressource est une zone de mémoire accessible au pipeline Direct3D.
ms.assetid: 24859fbc-b5e1-4963-baf8-4f083f41f39a
title: Ressources (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93448fadd14d1a0849c9b730d34030b70d42a8cbc0926743e7059e222a6ea9c8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119567049"
---
# <a name="resources-direct3d-10"></a>Ressources (Direct3D 10)

Une ressource est une zone de mémoire accessible au pipeline Direct3D. Pour que le pipeline puisse accéder efficacement à la mémoire, les données fournies au pipeline (telles que la géométrie d’entrée, les ressources du nuanceur, les textures, etc.) doivent être stockées dans une ressource. Il existe deux types de ressource dont dérivent l’ensemble des ressources Direct3D : la mémoire tampon et la texture. Jusqu’à 128 ressources peuvent être actives à chaque phase du pipeline.

Chaque application crée généralement de nombreuses ressources. Exemples de ressources : mémoires tampons de vertex, tampon d’index, mémoire tampon constante, textures et ressources de nuanceur. Il existe plusieurs options qui déterminent la façon dont les ressources peuvent être utilisées. Vous pouvez créer des ressources fortement typées ou de type inférieur ; vous pouvez contrôler si les ressources ont un accès en lecture et en écriture. vous pouvez rendre les ressources accessibles uniquement au processeur, au GPU ou aux deux. Naturellement, il y aura un compromis entre vitesse et fonctionnalité : plus le nombre de fonctionnalités que vous autorisez à disposer d’une ressource est faible, plus les performances attendues sont élevées.

Étant donné qu’une application utilise souvent de nombreuses textures, Direct3D introduit également le concept d’un tableau de texture pour simplifier la gestion des textures. Un tableau de texture contient une ou plusieurs textures (toutes des mêmes types et dimensions) qui peuvent être indexées à partir d’une application ou par des nuanceurs. Les tableaux de texture vous permettent d’utiliser une seule interface avec plusieurs index pour accéder à de nombreuses textures. Vous pouvez créer autant de tableaux de textures que nécessaire pour gérer différents types de texture.

Une fois que vous avez créé les ressources que votre application utilisera, vous connectez ou liez chaque ressource aux étapes de pipeline qui vont les utiliser. Pour ce faire, vous devez appeler une API de liaison, qui prend un pointeur vers la ressource. Étant donné que plusieurs étapes de pipeline peuvent avoir besoin d’accéder à la même ressource, Direct3D 10 introduit le concept d’affichage des ressources. Une vue identifie la partie d’une ressource qui est accessible. Vous pouvez créer des vues m ou une ressource et les lier à n étapes de canalisation, en supposant que vous suivez les règles de liaison pour les ressources partagées (le runtime génère des erreurs au moment de la compilation, si ce n’est pas le cas).

Un affichage des ressources fournit un modèle général pour l’accès à une ressource (textures, mémoires tampons, etc.). Étant donné que vous pouvez utiliser une vue pour indiquer à l’exécution les données auxquelles accéder et comment y accéder, les vues de ressources vous permettent de créer moins de ressources. Autrement dit, vous pouvez créer des ressources pour une taille donnée au moment de la compilation, puis déclarer le type de données dans la ressource lorsque la ressource est liée au pipeline. Les vues présentent de nombreuses nouvelles fonctionnalités permettant d’utiliser des ressources, telles que la capacité à lire des surfaces de stencil/profondeur dans le nuanceur, de générer des cubemaps dynamiques en une seule passe et de les afficher simultanément sur plusieurs secteurs d’un volume.

Pour en savoir plus sur les types de ressources de base, les tableaux de texture et la création et l’utilisation des ressources, consultez les rubriques suivantes :

-   [Types de ressources](d3d10-graphics-programming-guide-resources-types.md)
-   [Choix d’une ressource](d3d10-graphics-programming-guide-resources-choosing-basic.md)
-   [Création de ressources de mémoire tampon](d3d10-graphics-programming-guide-resources-creating.md)
-   [Création de ressources de texture](d3d10-graphics-programming-guide-resources-creating-textures.md)
-   [Copie et accès aux données de ressources](d3d10-graphics-programming-guide-resources-mapping.md)
-   [Structure et vues de la mémoire](d3d10-graphics-programming-guide-resources-access-views.md)
-   [Compression de bloc](d3d10-graphics-programming-guide-resources-block-compression.md)
-   [Tableau des limites de ressources](d3d10-graphics-programming-guide-resources-limits.md)
-   [Systèmes de coordonnées](d3d10-graphics-programming-guide-resources-coordinates.md)
-   [Règles à virgule flottante](d3d10-graphics-programming-guide-resources-float-rules.md)
-   [Règles de conversion des types de données](d3d10-graphics-programming-guide-resources-data-conversion.md)
-   [Mappage des formats hérités](d3d10-graphics-programming-guide-resources-legacy-formats.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de programmation pour Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 



