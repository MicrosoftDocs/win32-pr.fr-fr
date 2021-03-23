---
title: Utilisation des descripteurs directement dans la signature racine
description: Les applications peuvent placer des descripteurs directement dans la signature racine pour éviter d’avoir à passer par un tas de descripteur.
ms.assetid: 033E3D8F-3003-42F7-BF77-68A7D62802E5
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd97a7d68f5c9b51b6d15d3b71c6e30d04bb36e5
ms.sourcegitcommit: 83afb2f3e9e5d37f3f5a11e975515e9ed8b044ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2020
ms.locfileid: "104548598"
---
# <a name="using-descriptors-directly-in-the-root-signature"></a>Utilisation des descripteurs directement dans la signature racine

Les applications peuvent placer des descripteurs directement dans la signature racine pour éviter d’avoir à passer par un tas de descripteur. Ces descripteurs occupent beaucoup d’espace dans la signature racine (voir la section limites de signature racine), de sorte que les applications doivent les utiliser avec modération.

Un exemple d’utilisation consiste à placer des vues de mémoire tampon constante (CBV) qui changent par dessin dans la disposition racine afin que l’espace du tas de descripteurs ne doit pas être alloué par l’application par dessin (et qu’il ne soit pas possible de l’enregistrer en pointant sur une table de descripteur au nouvel emplacement dans le tas du descripteur). En plaçant un texte dans la signature racine, l’application confie simplement la responsabilité du contrôle de version au pilote, mais il s’agit d’une infrastructure dont ils disposent déjà.

Dans le cas d’un rendu qui utilise très peu de ressources, l’utilisation des tables ou des tas de descripteurs peut ne pas être nécessaire du tout si tous les descripteurs nécessaires peuvent être placés directement dans la signature racine.

Les seuls types de descripteurs pris en charge dans la signature racine sont les suivants :
- CBVs.
- Les vues des ressources de nuanceur (SRVs)/unordered Access views (UAVs) des ressources de mémoire tampon où le format SRV/UAV contient uniquement des composants 32 bits FLOAT/UINT/Saint (il n’y a pas de conversion de format).
- SRVs de structures d’accélération Raytracing, dans les signatures racines locales ou globales. 

Les UAVs dans la racine ne peuvent pas être associés à des compteurs. Les descripteurs dans la signature racine apparaissent chacun sous forme de descripteurs distincts, &mdash; mais ils ne peuvent pas être indexés de manière dynamique.

``` syntax
struct SceneData
{
   uint foo;
   float bar[2];
   int moo;
};
ConstantBuffer<SceneData> mySceneData : register(b6);
```

Dans l’exemple ci-dessus, `mySceneData` ne peut pas être déclaré en tant que tableau, comme dans `cbuffer mySceneData[2]` s’il va être mappé à un descripteur dans la signature racine, puisque l’indexation entre les descripteurs n’est pas prise en charge dans la signature racine. L’application peut définir des tampons de constante individuels distincts et les définir comme une entrée distincte dans la signature racine, si vous le souhaitez. Notez que, dans le `mySceneData` cas ci-dessus, il existe un tableau `bar[2]` . L’indexation dynamique dans la mémoire tampon constante est valide : un descripteur dans la signature racine se comporte de la même manière que le même descripteur, s’il est accessible via un tas de descripteur. Cela est différent avec les constantes d’incorporation directement dans la signature racine, qui apparaît également comme une mémoire tampon constante, sauf si la contrainte stipule que l’indexation dynamique dans les constantes inline n’est pas autorisée, ce qui n’est `bar[2]` pas autorisé ici.

Les API suivantes (à partir de l’interface [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) ) servent à définir des descripteurs directement sur la signature racine :

-   [**SetComputeRootConstantBufferView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootconstantbufferview)
-   [**SetGraphicsRootConstantBufferView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootconstantbufferview)
-   [**SetComputeRootShaderResourceView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootshaderresourceview)
-   [**SetGraphicsRootShaderResourceView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootshaderresourceview)
-   [**SetComputeRootUnorderedAccessView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootunorderedaccessview)
-   [**SetGraphicsRootUnorderedAccessView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootunorderedaccessview)

> [!Note]  
> Il n’existe aucun concept de « tableau de descripteur racine » dans Direct3D 12. Les tableaux de descripteurs sont pris en charge uniquement dans les tas de descripteurs.

## <a name="related-topics"></a>Rubriques connexes

[Signatures racines](root-signatures.md)
