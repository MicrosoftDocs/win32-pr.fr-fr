---
description: Le mappage d’environnement est une technique qui simule des surfaces fortement réfléchissantes sans utiliser le traçage de rayon.
ms.assetid: vs|directx_sdk|~\environment_mapping.htm
title: Mappage d’environnement (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 686f15b2f097550206f9c02cfc4104e7c9f6c030
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745949"
---
# <a name="environment-mapping-direct3d-9"></a>Mappage d’environnement (Direct3D 9)

Le mappage d’environnement est une technique qui simule des surfaces fortement réfléchissantes sans utiliser le traçage de rayon. Dans la pratique, le mappage d’environnement applique une carte de texture spéciale qui contient une image de la scène entourant un objet à l’objet lui-même. Le résultat est proche de l’apparence d’une surface réfléchissante, presque suffisamment pour tromper l’oeil, sans impliquer les calculs complexes impliqués dans le traçage de rayon.

L’illustration suivante montre un type de mappage d’environnement appelé « mappage d’environnement sphérique ». Pour plus d’informations, consultez [mappage d’environnement sphérique](spherical-environment-mapping.md).

![illustration d’un théière avec une texture appliquée qui reflète l’environnement](images/spheremapped-teapot.png)

Le théière de cette image semble refléter son environnement ; Il s’agit en fait d’une texture appliquée à l’objet. Étant donné que le mappage d’environnement utilise une texture combinée à des coordonnées de texture calculées, il peut être exécuté en temps réel.

Cette section fournit des informations sur l’exécution de deux types courants de mappage d’environnement avec Direct3D. De nombreux types de mappage d’environnement sont utilisés dans l’ensemble de l’industrie graphique, mais les rubriques suivantes ciblent les deux formes les plus courantes : le mappage d’environnement cubique et le mappage d’environnement sphérique.

-   [Mappage d’environnement cubique](cubic-environment-mapping.md)
-   [Mappage d’environnement sphérique](spherical-environment-mapping.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Pipeline de pixels](pixel-pipeline.md)
</dt> </dl>

 

 



