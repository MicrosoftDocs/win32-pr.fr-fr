---
title: Exemples fonctionnels
description: Des exemples fonctionnels sont disponibles au téléchargement, qui illustrent l’utilisation d’un certain nombre de fonctionnalités de Direct3D 12.
ms.assetid: 4C4475D4-534F-484F-8D60-9ACEA09AC109
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb1b61ec374e21c9173797121ee90ec72e789de8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104632"
---
# <a name="working-samples"></a>Exemples fonctionnels

Des exemples fonctionnels sont disponibles au téléchargement, qui illustrent l’utilisation d’un certain nombre de fonctionnalités de Direct3D 12.

## <a name="working-samples"></a>Exemples fonctionnels

Des exemples fonctionnels (sous la forme de projets Visual Studio 2015) peuvent être téléchargés à partir de [GitHub/Microsoft/DirectX-Graphics-Samples](https://github.com/Microsoft/DirectX-Graphics-Samples).

> [!Note]  
> La liste exacte des exemples disponibles à cet emplacement variera en fonction de l’ajout et de la mise à jour des exemples.

 



<table>
<thead>
<tr class="header">
<th>Exemple de titre</th>
<th>Description</th>
<th>Bureau</th>
<th>UWP</th>
<th>Procédure pas à pas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>HelloWorld<dl> HelloWindow<br />
HelloTriangle<br />
HelloBundles<br />
HelloConstBuffers<br />
HelloTexture<br />
</dl></td>
<td>L’exemple de jeu HelloWorld contient les projets simples suivants pour vous aider à commencer à utiliser Direct3D 12.<dl> Crée une fenêtre en préparation du rendu du contenu Direct3D 12.<br />
Restitue un triangle simple à l’aide de Direct3D 12.<br />
Montre l’utilisation d’un bundle pour le rendu à l’aide de Direct3D 12.<br />
Montre comment utiliser des mémoires tampons constantes pour transmettre des données au GPU utilisé pour le rendu dans Direct3D 12.<br />
Montre comment appliquer une texture à un triangle à l’aide de Direct3D 12.<br />
</dl></td>
<td>O</td>
<td>O</td>
<td><a href="creating-a-basic-direct3d-12-component.md">Création d’un composant Direct3D 12 de base</a></td>
</tr>
<tr class="even">
<td>D3D12Bundles</td>
<td>Montre les pratiques recommandées pour la mise en mémoire tampon des frames et la synchronisation, ainsi que le rendu d’un maillage simple utilisant des tresses.</td>
<td>O</td>
<td>O</td>

</tr>
<tr class="odd">
<td>D3D12Multithreading</td>
<td>Exemple de création d’une application multithread.</td>
<td>O</td>
<td>N</td>

</tr>
<tr class="even">
<td>D3D12nBodyGravity</td>
<td>Montre comment plusieurs moteurs peuvent être utilisés pour effectuer des tâches de calcul asynchrones, en même temps que du travail 3D sur le même GPU.</td>
<td>O</td>
<td>O</td>
<td><a href="multi-engine-n-body-gravity-simulation.md">Simulation de gravité n-corps multi-moteur</a></td>
</tr>
<tr class="odd">
<td>D3D12PredicationQueries</td>
<td>Illustre l’élimination d’occlusion à l’aide de segments et de prédicats de requête.</td>
<td>O</td>
<td>O</td>
<td><a href="predication-queries.md">Requêtes de prédicat</a></td>
</tr>
<tr class="even">
<td>D3D12DynamicIndexing</td>
<td>Illustre les fonctionnalités d’indexation dynamique de DirectX 12 et HLSL.</td>
<td>O</td>
<td>O</td>
<td><a href="dynamic-indexing-using-hlsl-5-1.md">Indexation dynamique à l’aide de HLSL 5.1</a></td>
</tr>
<tr class="odd">
<td>D3D1211on12</td>
<td>Illustre l’utilisation de base de la couche 11on12. Cet exemple restitue le texte à l’aide de D2D à l’aide de l’API Direct3D 11 sur un appareil Direct3D 12 11on12.</td>
<td>O</td>
<td>O</td>
<td><a href="d2d-using-d3d11on12.md">D2D à l’aide de D3D11on12</a></td>
</tr>
<tr class="even">
<td>D3D12ExecuteIndirect</td>
<td>Illustre le Culling du moteur de calcul conjointement avec la fonctionnalité d’exécution indirecte pour afficher uniquement les objets qui réussissent le test d’élimination.</td>
<td>O</td>
<td>O</td>
<td><a href="indirect-drawing-and-gpu-culling-.md">Dessin indirect et élimination du GPU</a></td>
</tr>
<tr class="odd">
<td>D3D12PipelineStateCache</td>
<td>Illustre la mise en cache d’un objet d’état de pipeline.</td>
<td>O</td>
<td>O</td>

</tr>
<tr class="even">
<td>D3D12Fullscreen</td>
<td>Montre comment gérer fullscreen pour les transitions avec fenêtres et le redimensionnement de fenêtre dans DirectX 12.</td>
<td>O</td>
<td>O</td>

</tr>
<tr class="odd">
<td>D3D12HeterogeneousMultiadapter</td>
<td>Montre comment partager des charges de travail entre plusieurs GPU hétérogènes à l’aide de tas partagés.</td>
<td>O</td>
<td>O</td>

</tr>
<tr class="even">
<td>D3D12ReservedResources</td>
<td>Illustre l’utilisation de ressources réservées (en mosaïque). Dans cet exemple, un quadruple est texturé avec une ressource réservée contenant une chaîne MIP complète.</td>
<td>O</td>
<td>O</td>

</tr>
<tr class="odd">
<td>D3D12Residency</td>
<td>Il s’agit d’une solution à faible coût d’intégration qui permet de gérer vos tas Direct3D 12 et les ressources validées, à l’aide de techniques de gestion de la mémoire de Direct3D 11.</td>
<td>O</td>
<td>O</td>

</tr>
<tr class="even">
<td>D3D12SmallResources</td>
<td>Illustre l’utilisation de ressources placées de petite taille, montrant les économies potentielles de mémoire obtenues à l’aide de ressources passées (avec un alignement de 4 Ko) sur les ressources validées et réservées (avec un alignement de 64 Ko).</td>
<td>O</td>
<td>O</td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de programmation Direct3D 12](directx-12-programming-guide.md)
</dt> <dt>

[Guide pas à pas du code D3D12](d3d12-code-walk-throughs.md)
</dt> </dl>

 

 




