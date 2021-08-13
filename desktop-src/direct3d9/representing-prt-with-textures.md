---
description: L’exemple PRTDemo et le simulateur PRTCmdLine inclus dans le kit de développement logiciel (SDK) DirectX représentent des vecteurs de transfert aux sommets d’une maille.
ms.assetid: cee049e8-3245-4fce-ab2f-ba251eacc72a
title: Représentation de PRT avec des textures (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e827e24258d75a91aa75c9eb51ed6563d476ab16f75fedc31a7071bca28a4a78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118797921"
---
# <a name="representing-prt-with-textures-direct3d-9"></a>Représentation de PRT avec des textures (Direct3D 9)

L’exemple PRTDemo et le simulateur PRTCmdLine inclus dans le kit de développement logiciel (SDK) DirectX représentent des vecteurs de transfert aux sommets d’une maille. Pour représenter le signal PRT avec précision, cela peut nécessiter des pavages qui ne sont pas pratiques pour les jeux actuels. La représentation des vecteurs de transfert dans les cartes de texture est une approche alternative qui a le même coût des données indépendamment de la complexité du maillage. Il existe plusieurs façons de générer des mappages de texture vecteur de transfert à l’aide de la bibliothèque D3DX PRT.

## <a name="precomputing-transfer-vectors"></a>Vecteurs de transfert de précalcul

Une approche consisterait à modifier les exemples PRTDemo et PRTCmdLine pour calculer un vecteur de transfert à chaque Texel dans un paramétrage d’une surface. Pour ce faire :

1.  Modifiez l’appel à [**D3DXCreatePRTEngine**](d3dxcreateprtengine.md) pour extraire les coordonnées de texture de la maille (ExtractUVs doit avoir la **valeur true**)
2.  Remplacez les appels [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md) par [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md) à l’aide de la même taille de texture.

Toutes les méthodes ID3DXPRTEngine fonctionnent avec les simulations par Texel, à l’exception de : ComputeBounceAdaptive, ComputeSSAdaptive, compartss et ComputeDirectLightingSHAdaptive. Bien que la simulation d’espace de texture produise le résultat correct, elle peut souvent être assez lente, car il s’agit probablement de vecteurs de transfert de calcul à haute densité.

Une autre approche consiste à calculer une simulation adaptative par vertex PRT (avec des coordonnées de texture qui seront utilisées pour les données par Texel), puis à appeler [**ID3DXPRTEngine :: ResampleBuffer**](id3dxprtengine--resamplebuffer.md) (à l’aide d’une mémoire tampon de sortie créée à l’aide de [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md) à la résolution appropriée). Cela fonctionne avec toutes les fonctionnalités de D3DX PRT dans le kit de développement logiciel (SDK) et peut souvent être bien plus efficace que le calcul direct d’une mémoire tampon de transfert par texture.

## <a name="runtime-calculations"></a>Calculs du Runtime

Si un seul cluster est utilisé, les résultats peuvent être filtrés et MIP-mappé comme n’importe quelle autre texture et le nuanceur de pixels est identique au code du nuanceur de sommets fourni avec PRTDemo.

Si la compression génère plusieurs clusters, vous ne pouvez pas filtrer ou démipmapr les données, car les index de clustering ne sont pas continus. Voici quelques alternatives pour la gestion des données à plusieurs clusters :

-   Procédez à la totalité du filtrage dans le nuanceur de pixels. Malheureusement, cela n’est généralement pas pratique pour des raisons de performances.
-   Si les textures sont des textures non mappées à faible résolution (IE : cartes de lumière), il est probablement plus efficace de calculer l’éclairage directement dans l’espace de texture, où aucun filtrage n’est effectué et de restituer l’objet avec une texture ombrée. Il s’agit essentiellement d’une carte d’éclairage dynamique créée entièrement sur le GPU.
-   Si un Atlas de textures est utilisé (voir [utilisation de UVAtlas (Direct3D 9)](using-uvatlas.md)), vous pouvez mettre manuellement en cluster la scène en faisant en sorte que tous les vecteurs de transfert d’un composant connecté dans l’espace de texture soient dans le même cluster. De cette façon, vous pouvez filtrer la texture, car tous les texels accédés sont dans le même cluster par construction. L’ID de cluster d’une face donnée peut être propagé à partir du nuanceur de sommets.

Les nuanceurs de pixels ont beaucoup moins de registres constants qui ne peuvent pas être indexés, le nuanceur de pixels est donc légèrement différent du nuanceur de sommets. Le stockage du travail par cluster dans une texture dynamique à faible résolution et l’utilisation de charges de texture est le moyen le plus efficace pour le rendu lors de l’utilisation de plusieurs clusters.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Transfert de luminance précalculé](precomputed-radiance-transfer.md)
</dt> <dt>

[PRT, exemple de démonstration](https://msdn.microsoft.com/library/Ee418763(v=VS.85).aspx)
</dt> <dt>

[Simulateur PRT (prtcmdline.exe)](https://msdn.microsoft.com/library/Ee418766(v=VS.85).aspx)
</dt> </dl>

 

 



