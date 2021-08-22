---
description: Le pipeline graphique Direct3D 10 représente une modification d’architecture fondamentale, reconstruite à partir de la base du matériel et des logiciels pour alimenter la prochaine génération de jeux et d’applications multimédias 3D.
ms.assetid: 2e24de6c-4f73-4844-b87f-3487ef069db6
title: Fonctionnalités de l’API (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 416018fcddf2643ba9fbc8e633ec2f636b8158ff329780a55205034e5dbbe240
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858659"
---
# <a name="api-features-direct3d-10"></a>Fonctionnalités de l’API (Direct3D 10)

Le pipeline graphique Direct3D 10 représente une modification d’architecture fondamentale, reconstruite à partir de la base du matériel et des logiciels pour alimenter la prochaine génération de jeux et d’applications multimédias 3D. il utilise le modèle WDDM (Windows Display Driver Model), qui permet des améliorations des performances et du comportement, telles que la mémoire du GPU virtuel.

Les développeurs familiarisés avec Direct3D 9 découvriront une série d’améliorations fonctionnelles et des améliorations des performances dans Direct3D 10, notamment :

-   Capacité de traiter des primitives entières dans la nouvelle [étape Geometry-Shader](/previous-versions//bb205146(v=vs.85)).
-   Possibilité de produire des données de vertex générées par le pipeline dans la mémoire à l’aide de l' [étape de flux de sortie](../direct3d11/d3d10-graphics-programming-guide-output-stream-stage.md).
-   Organisation de l’état du pipeline en 5 [objets d’État](d3d10-graphics-programming-guide-api-features-state-objects.md)immuables, permettant une configuration rapide du pipeline.
-   Organisation des constantes de nuanceur dans des [mémoires tampons constantes](d3d10-graphics-programming-guide-resources-types.md), minimisant la surcharge de bande passante pour fournir des données de nuanceur constantes.
-   La possibilité d’effectuer un échange de matériel par primitive et une configuration à l’aide d’un nuanceur Geometry.
-   Nouveaux [types de ressources](d3d10-graphics-programming-guide-resources-types.md) (y compris des tableaux de textures qui peuvent être indexés à partir de nuanceurs) et des formats de ressources.
-   Plus grande généralisation de l’accès aux ressources à l’aide d’une [vue](d3d10-graphics-programming-guide-resources-access-views.md).
-   Les bits des fonctionnalités matérielles héritées ont été supprimés en faveur d’un ensemble complet de fonctionnalités garanties, qui ciblent le matériel de classe Direct3D 10 (minimum).
-   [Runtime à couches](d3d10-graphics-programming-guide-api-features-layers.md) : l’API Direct3D 10 est construite avec des couches, en commençant par les fonctionnalités de base au cœur et en créant des fonctionnalités facultatives et d’assistance aux développeurs (débogage, etc.) dans les couches externes.
-   Intégration HLSL complète : tous les nuanceurs Direct3D 10 sont écrits en HLSL et implémentés avec le [Common-Shader Core](../direct3dhlsl/dx-graphics-hlsl-common-core.md).
-   Augmentation du nombre de cibles de rendu, de textures et d’échantillonneurs. Il n’existe pas non plus de limite de longueur de nuanceur.
-   Opérations sur les entiers et les nuanceurs au niveau du bit.
-   Readback d’une surface de profondeur/stencil ou d’une ressource à échantillonnage unique, une fois qu’elle n’est plus liée en tant que cible de rendu.
-   Prise en charge de l’alpha-à-couverture à l’échantillonnage.

Des différences de comportement supplémentaires doivent également être prises en charge par les développeurs Direct3D 9 (voir [considérations relatives à Direct3D 9 vers Direct3D 10](d3d10-graphics-programming-guide-d3d9-to-d3d10-considerations.md)).

Voici une liste de fonctionnalités Direct3D 9 qui ne sont plus prises en charge ou qui ont été révisées dans Direct3D 10 (voir [fonctionnalités déconseillées](d3d10-graphics-programming-guide-api-features-deprecated.md)).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de programmation pour Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
