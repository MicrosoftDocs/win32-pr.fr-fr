---
description: Une ressource est une collection de données qui est utilisée par le pipeline 3D.
ms.assetid: 802400fa-a606-4d3d-a61d-1cdb5a9f0437
title: Choix d’une ressource (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3de635e9ad5ece322de9c34438be45db991e6700dc6192509f70b6b0f53e351b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119380319"
---
# <a name="choosing-a-resource-direct3d-10"></a>Choix d’une ressource (Direct3D 10)

Une ressource est une collection de données qui est utilisée par le pipeline 3D. La création de ressources et la définition de leur comportement constituent la première étape de la programmation de votre application. Ce guide couvre les rubriques de base pour le choix des ressources requises par votre application.

-   [Identifier les étapes de pipeline nécessitant des ressources](#identify-pipeline-stages-that-need-resources)
-   [Identifier la manière dont chaque ressource sera utilisée](#identify-how-each-resource-will-be-used)
-   [Liaison de ressources à des étapes de pipeline](#binding-resources-to-pipeline-stages)
-   [Rubriques connexes](#related-topics)

## <a name="identify-pipeline-stages-that-need-resources"></a>Identifier les étapes de pipeline nécessitant des ressources

La première étape consiste à choisir l’étape (ou les étapes) de [pipeline](d3d10-graphics-programming-guide-pipeline-stages.md) qui utilisera une ressource. Autrement dit, Identifiez chaque étape qui lira des données à partir d’une ressource, ainsi que les étapes permettant d’écrire des données dans une ressource. Connaître les étapes de pipeline dans lesquelles les ressources seront utilisées détermine les API qui seront appelées pour lier la ressource à l’étape.

Ce tableau répertorie les types de ressources qui peuvent être liées à chaque étape du pipeline. Elle indique si la ressource peut être liée en tant qu’entrée ou en sortie, ainsi que l’API de liaison.



| Étape de pipeline  | Entrée/Sortie | Ressource               | Type de ressource                           | API de liaison                                                                                                                                                                                                |
|-----------------|--------|------------------------|-----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Assembleur d'entrée | Dans     | Mémoire tampon de vertex          | Buffer                                  | [**IASetVertexBuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-iasetvertexbuffers)                                                                                                                                           |
| Assembleur d'entrée | Dans     | Mémoire tampon d’index           | Buffer                                  | [**IASetIndexBuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-iasetindexbuffer)                                                                                                                                               |
| Étapes du nuanceur   | Dans     | Shader-ResourceView    | Buffer, Texture1D, Texture2D, Texture3D | [**VSSetShaderResources**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetshaderresources), [**GSSetShaderResources**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-gssetshaderresources), [**PSSetShaderResources**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-pssetshaderresources) |
| Étapes du nuanceur   | Dans     | Mémoire tampon de Shader-Constant | Buffer                                  | [**VSSetConstantBuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetconstantbuffers), [**GSSetConstantBuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-gssetconstantbuffers), [**PSSetConstantBuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-pssetconstantbuffers) |
| Sortie de flux   | Sortie    | Buffer                 | Buffer                                  | [**SOSetTargets**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-sosettargets)                                                                                                                                                       |
| Fusion de sortie   | Sortie    | Affichage de la cible de rendu     | Buffer, Texture1D, Texture2D, Texture3D | [**OMSetRenderTargets**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetrendertargets)                                                                                                                                           |
| Fusion de sortie   | Sortie    | Affichage de la profondeur/du gabarit     | Texture1D, Texture2D                    | [**OMSetRenderTargets**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetrendertargets)                                                                                                                                           |



 

## <a name="identify-how-each-resource-will-be-used"></a>Identifier la manière dont chaque ressource sera utilisée

Une fois que vous avez choisi les étapes de pipeline que votre application utilisera (et par conséquent les ressources requises par chaque étape), l’étape suivante consiste à déterminer la manière dont chaque ressource sera utilisée, c’est-à-dire, si une ressource est accessible par le processeur ou le GPU.

Le matériel sur lequel votre application s’exécute aura au minimum au moins un processeur et un GPU. Pour choisir une valeur d’utilisation, déterminez le type de processeur qui doit lire ou écrire dans la ressource à partir des options suivantes (consultez [**\_ utilisation de D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)).



| Utilisation des ressources | Peut être mis à jour par                    | Fréquence des mises à jour |
|----------------|--------------------------------------|---------------------|
| Default        | GPU                                  | rarement        |
| Dynamique        | Processeur                                  | fréquemment          |
| Staging        | GPU                                  | n/a                 |
| Non modifiable      | UC (uniquement au moment de la création de la ressource) | n/a                 |



 

L’utilisation par défaut doit être utilisée pour une ressource qui est censée être mise à jour par l’UC rarement (moins d’une fois par frame). Dans l’idéal, l’UC n’écrira jamais directement dans une ressource avec une utilisation par défaut afin d’éviter des pénalités de performances potentielles.

L’utilisation dynamique doit être utilisée pour une ressource que l’UC met à jour relativement souvent (une ou plusieurs fois par trame). Un scénario classique pour une ressource dynamique consiste à créer des tampons de vertex et d’index dynamiques qui seraient remplis au moment de l’exécution avec des données relatives à la géométrie visible du point de vue de l’utilisateur pour chaque image. Ces mémoires tampons sont utilisées pour afficher uniquement la géométrie visible par l’utilisateur pour ce frame.

L’utilisation intermédiaire doit être utilisée pour copier des données vers et à partir d’autres ressources. Un scénario classique consiste à copier des données dans une ressource avec l’utilisation par défaut (à laquelle l’UC ne peut pas accéder) à une ressource avec une utilisation intermédiaire (à laquelle l’UC peut accéder).

Les ressources immuables doivent être utilisées lorsque les données de la ressource ne seront jamais modifiées.

Une autre façon de regarder la même idée est de réfléchir à ce que fait une application avec une ressource.



| Comment l’application utilise la ressource     | Utilisation des ressources       |
|---------------------------------------|----------------------|
| Charger une seule fois et ne jamais la mettre à jour            | Immuable ou par défaut |
| L’application remplit les ressources à plusieurs reprises | Dynamique              |
| Restituer à la texture                     | Default              |
| Accès de l’UC des données GPU                | Staging              |



 

Si vous n’êtes pas sûr de l’utilisation à choisir, commencez par utiliser l’utilisation par défaut, car il est supposé être le cas le plus courant. Une mémoire tampon de Shader-Constant est le type de ressource qui doit toujours avoir une utilisation par défaut.

## <a name="binding-resources-to-pipeline-stages"></a>Liaison de ressources à des étapes de pipeline

Une ressource peut être liée à plusieurs étapes de pipeline en même temps, à condition que les restrictions spécifiées lors de la création de la ressource ([**indicateurs d’utilisation**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage), [**indicateurs de liaison**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag), [**indicateurs d’accès au processeur**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cpu_access_flag)) soient remplies. Plus précisément, une ressource peut être liée en tant qu’entrée et en sortie simultanément, à condition que la lecture et l’écriture d’une partie d’une ressource ne puissent pas se produire en même temps.

Lors de la liaison d’une ressource, réfléchissez à la façon dont le GPU et l’UC accèdent à la ressource. Les ressources qui sont conçues pour un seul but (n’utilisez pas plusieurs indicateurs d’accès d’utilisation, de liaison et d’UC) peuvent avoir une meilleure performance.

Par exemple, considérez le cas d’une cible de rendu utilisée comme texture plusieurs fois. Il peut être plus rapide d’avoir deux ressources : une cible de rendu et une texture utilisées comme ressource de nuanceur. Chaque ressource n’utilise qu’un seul indicateur de liaison ([**D3D10 \_ lier la \_ \_ cible de rendu**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag) ou la **\_ \_ \_ ressource de nuanceur de liaison D3D10**). Les données sont copiées de la texture de cible de rendu vers la texture de nuanceur à l’aide de [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) ou [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion). Cela peut améliorer les performances en isolant l’écriture de la cible de rendu de la lecture de la texture du nuanceur. Bien entendu, le seul moyen de s’assurer consiste à implémenter les deux approches et à mesurer la différence de performances dans votre application.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Ressources (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 



