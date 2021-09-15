---
description: Les interfaces de rendu pour Direct3D consistent en des méthodes qui restituent des primitives à partir des données de vertex stockées dans une ou plusieurs mémoires tampons de données.
ms.assetid: e89eae14-f480-470c-b301-f7ff316ad339
title: Flux de données de Vertex (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efd45fc3f645de49060cd201a6a6e9e238712338
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127530957"
---
# <a name="vertex-data-streams-direct3d-9"></a>Flux de données de Vertex (Direct3D 9)

Les interfaces de rendu pour Direct3D consistent en des méthodes qui restituent des primitives à partir des données de vertex stockées dans une ou plusieurs mémoires tampons de données. Les données de vertex se composent d’éléments vertex combinés pour former des composants vertex. Les éléments vertex, la plus petite unité d’un vertex, représentent des entités telles que la position, la normale ou la couleur.

Les composants vertex sont un ou plusieurs éléments de vertex stockés en continu (entrelacés par vertex) dans une mémoire tampon unique. Un vertex complet se compose d’un ou de plusieurs composants, où chaque composant se trouve dans une mémoire tampon distincte. Pour restituer une primitive, plusieurs composants vertex sont lus et assemblés afin que les vertex complets soient disponibles pour le traitement des vertex. Le diagramme suivant illustre le processus de rendu des primitives à l’aide de composants de vertex.

![diagramme du processus de rendu des primitives à l’aide de composants vertex](images/vertexdata.png)

Le rendu des primitives se compose de deux étapes. Tout d’abord, configurez un ou plusieurs flux de composants de vertex. Ensuite, appelez une méthode [**IDirect3DDevice9 ::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) pour effectuer le rendu à partir de ces flux. L’identification des éléments de vertex dans ces flux de composants est spécifiée par le nuanceur de sommets.

Les méthodes [**IDirect3DDevice9 ::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) spécifient un décalage dans les flux de données de vertex afin qu’un sous-ensemble contigu arbitraire des primitives dans un ensemble de données de vertex puisse être rendu avec chaque appel de dessin. Cela vous permet de modifier l’état de rendu de l’appareil entre des groupes de primitives qui sont restituées à partir des mêmes mémoires tampons de vertex.

Les méthodes de dessin indexées et non indexées sont prises en charge. Pour plus d’informations, consultez [rendu à partir des mémoires tampons de vertex et d’index (Direct3D 9)](rendering-from-vertex-and-index-buffers.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Rendu des primitives](rendering-primitives.md)
</dt> </dl>

 

 
