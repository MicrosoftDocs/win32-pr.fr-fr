---
title: Étape de Stream-Output
description: L’objectif de l’étape de flux de sortie est de générer continuellement des données de vertex (ou de diffuser) à partir de l’étape Geometry-Shader (ou de l’étape de nuanceur de vertex si l’étape Geometry-Shader est inactive) vers une ou plusieurs mémoires tampons en mémoire (voir Prise en main avec l’étape Stream-Output).
ms.assetid: f902dc93-9612-481b-a6bd-073e924a4c79
keywords:
- étape de sortie de flux (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0879cde2ba2f1bb3ed9cc6121aaf378cd4af312
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104463951"
---
# <a name="stream-output-stage"></a>Étape de Stream-Output

L’objectif de l’étape de flux de sortie est de générer continuellement des données de vertex (ou de diffuser) à partir de l’étape Geometry-Shader (ou de l’étape de nuanceur de vertex si l’étape Geometry-Shader est inactive) vers une ou plusieurs mémoires tampons en mémoire (voir [prise en main avec l’étape Stream-Output](d3d10-graphics-programming-guide-output-stream-stage-getting-started.md)).

L’étape flux-sortie (SO) se trouve dans le pipeline juste après l’étape Geometry-Shader et juste avant l’étape de pixellisation, comme indiqué dans le diagramme suivant.

![diagramme de l’emplacement de l’étape de sortie de flux dans le pipeline](images/d3d10-pipeline-stages-so.png)

Les données transmises en mémoire vers la mémoire peuvent être lues dans le pipeline dans une passe de rendu ultérieure, ou peuvent être copiées dans une ressource intermédiaire (afin qu’elles puissent être lues par l’UC). La quantité de données transmises en continu peut varier. l’API [**ID3D11DeviceContext ::D rawauto**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawauto) est conçue pour gérer les données sans qu’il soit nécessaire d’interroger (le GPU) sur la quantité de données écrites.

Lorsqu’un triangle ou une frange est lié à l’étape assembleur d’entrée, chaque bande est convertie en liste avant d’être diffusée en continu. Les vertex sont toujours écrits comme des primitives complètes (par exemple, 3 sommets à la fois pour les triangles); les primitives incomplètes ne sont jamais transmises en continu. Les types primitifs avec contiguïté ignorent les données d’adjacence avant la diffusion des données en continu.

Il existe deux façons d’alimenter les données de sortie de flux dans le pipeline :

-   Les données de sortie de flux peuvent être réintégrées à l’étape assembleur d’entrée.
-   Les données de sortie de flux peuvent être lues par des nuanceurs programmables à l’aide de fonctions de chargement (telles que [Load](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-load)).

Pour utiliser une mémoire tampon en tant que ressource de flux de sortie, créez la mémoire tampon avec l’indicateur de [**\_ sortie de \_ flux \_ de liaison d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) . L’étape flux-sortie prend en charge jusqu’à 4 mémoires tampons simultanément.

-   Si vous diffusez des données dans plusieurs mémoires tampons, chaque mémoire tampon peut uniquement capturer un seul élément (jusqu’à 4 composants) de données par vertex, avec une Stride de données implicite égale à la largeur d’élément dans chaque mémoire tampon (compatible avec la manière dont les mémoires tampons d’élément unique peuvent être liées à l’entrée dans des étapes de nuanceur). En outre, si les mémoires tampons ont des tailles différentes, l’écriture s’arrête dès que l’une des mémoires tampons est pleine.
-   Si vous diffusez des données dans une seule mémoire tampon, la mémoire tampon peut capturer jusqu’à 64 composants scalaires de données par vertex (256 octets ou moins) ou le nombre de vertex peut atteindre jusqu’à 2048 octets.


## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                                                               | Description                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [Prise en main avec l’étape de Stream-Output](d3d10-graphics-programming-guide-output-stream-stage-getting-started.md)<br/> | Cette section décrit comment utiliser un nuanceur Geometry avec l’étape de sortie de flux.<br/> |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Pipeline graphique](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Étapes de pipeline (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

