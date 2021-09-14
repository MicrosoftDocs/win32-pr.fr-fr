---
title: Walk-Throughs de code D3D12
description: Cette section fournit du code pour les exemples de scénarios. La plupart des procédures pas à pas fournissent des détails sur le codage requis pour être ajouté à un exemple de base, afin d’éviter de répéter le code de base du composant pour chaque scénario.
ms.assetid: 1F37FD3A-385C-4DD5-B04C-980F078D90D0
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fdea9b519e2a0adac9dc346d6bee455af0018da
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127293658"
---
# <a name="d3d12-code-walk-throughs"></a>Walk-Throughs de code D3D12

Cette section fournit du code pour les exemples de scénarios. La plupart des procédures pas à pas fournissent des détails sur le codage requis pour être ajouté à un exemple de base, afin d’éviter de répéter le code de base du composant pour chaque scénario.

Pour obtenir le composant le plus basique, reportez-vous à la section [création d’un composant Direct3D 12 de base](creating-a-basic-direct3d-12-component.md) . Les procédures pas à pas suivantes décrivent des scénarios plus avancés.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                           | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [D2D à l’aide de D3D11on12](d2d-using-d3d11on12.md)<br/>                                       | L’exemple **D3D1211on12** montre comment restituer du contenu D2D sur du contenu D3D12 en partageant des ressources entre un appareil 11 et un appareil 12. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [Simulation de gravité n-corps multi-moteur](multi-engine-n-body-gravity-simulation.md)<br/> | L’exemple **D3D12nBodyGravity** montre comment effectuer un travail de calcul de manière asynchrone. L’exemple fait tourner un certain nombre de threads, chacun avec une file d’attente de commandes Compute, et planifie le travail de calcul sur le GPU qui effectue une simulation de gravité en n corps. Chaque thread opère sur deux mémoires tampons complètes de données de position et de vélocité. À chaque itération, le nuanceur de calcul lit les données de position et de vélocité actuelles d’une mémoire tampon et écrit l’itération suivante dans l’autre mémoire tampon. Lorsque l’itération est terminée, le nuanceur de calcul permute la mémoire tampon qui sert à lire les données de position/vélocité et qui est le UAV pour l’écriture des mises à jour de position/vélocité en modifiant l’état de la ressource sur chaque mémoire tampon.<br/> |
| [Requêtes de prédicat](predication-queries.md)<br/>                                       | L’exemple **D3D12PredicationQueries** illustre l’élimination d’occlusion à l’aide de tas et de prédicats de requête DirectX 12. La procédure pas à pas décrit le code supplémentaire nécessaire pour étendre l’exemple **HelloConstBuffer** afin de gérer les requêtes de prédicat. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [Indexation dynamique à l’aide de HLSL 5.1](dynamic-indexing-using-hlsl-5-1.md)<br/>               | L’exemple **D3D12DynamicIndexing** illustre certaines des nouvelles fonctionnalités HLSL disponibles dans le modèle de nuanceur 5,1, en particulier l’indexation dynamique et les tableaux non liés, pour restituer le même maillage plusieurs fois, chaque fois que vous le rendez avec un matériau sélectionné dynamiquement. Avec l’indexation dynamique, les nuanceurs peuvent désormais indexer dans un tableau sans connaître la valeur de l’index au moment de la compilation. En cas de combinaison avec des tableaux non liés, cela ajoute un autre niveau d’indirection et de flexibilité aux auteurs de nuanceur et aux pipelines d’art.<br/>                                                                                                                                                                                  |
| [Dessin indirect et élimination du GPU](indirect-drawing-and-gpu-culling-.md)<br/>            | L’exemple D3D12ExecuteIndirect montre comment utiliser des commandes indirectes pour dessiner du contenu. Il montre également comment ces commandes peuvent être manipulées sur le GPU dans un nuanceur de calcul avant leur émission. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de programmation de Direct3D 12](directx-12-programming-guide.md)
</dt> <dt>

[Didacticiels vidéo sur DirectX Advanced Learning](https://www.youtube.com/channel/UCiaX2B8XiXR70jaN7NK-FpA)
</dt> <dt>

[Exemple de code dans la référence D3D12](notes-on-example-code.md)
</dt> <dt>

[Exemples fonctionnels](working-samples.md)
</dt> </dl>

 

 





