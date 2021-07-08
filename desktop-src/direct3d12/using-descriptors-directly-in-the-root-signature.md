---
title: Utilisation directe des descripteurs dans la signature racine
description: Pour éviter d’avoir à passer par un tas de descripteur, vous pouvez placer un descripteur directement dans la signature racine.
ms.assetid: 033E3D8F-3003-42F7-BF77-68A7D62802E5
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff9d459f3195a4cf722ea210edbe63e5c1bf3cc8
ms.sourcegitcommit: 170bc12e9724d00cecbb96d57c7226c51e135dee
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/07/2021
ms.locfileid: "113489166"
---
# <a name="using-descriptors-directly-in-the-root-signature"></a>Utilisation directe des descripteurs dans la signature racine

Pour éviter d’avoir à passer par un tas de descripteur, vous pouvez placer un descripteur directement dans la signature racine. Ces descripteurs occupent beaucoup d’espace dans la signature racine (voir [limites de signature racine](/windows/win32/direct3d12/root-signature-limits)). nous vous recommandons donc de les utiliser avec modération.

Un exemple d’utilisation serait de placer dans la disposition racine une vue de mémoire tampon constante (CBV) qui est modifiée par dessin. C’est pour cela que l’espace du tas du descripteur ne doit pas être alloué par l’application par dessin (et enregistre le pointage d’une table de descripteur au nouvel emplacement dans le tas du descripteur). En plaçant un texte dans la signature racine, l’application confie simplement la responsabilité du contrôle de version au pilote ; mais c’est l’infrastructure que les pilotes possèdent déjà.

Dans le cas d’un rendu qui utilise très peu de ressources, l’utilisation des tables ou des tas de descripteurs peut ne pas être nécessaire du tout si tous les descripteurs nécessaires peuvent être placés directement dans la signature racine.

Ce sont les seuls types de descripteurs pris en charge dans la signature racine.

- Vue de la mémoire tampon constante (CBVs).
- Vues des ressources de nuanceur (SRVs)/vues d’accès non ordonnées (UAVs) des ressources de mémoire tampon où la conversion de format n’est pas requise (mémoires tampons non typées). Voici quelques exemples de mémoires tampons non typées qui peuvent être liées à des descripteurs racine : `StructuredBuffer<type>` , `RWStructuredBuffer<type>` `ByteAddressBuffer` et `RWByteAddressBuffer` . Les mémoires tampons typées telles que `Buffer<uint>` et `Buffer<float2>` ne peuvent pas.
- SRVs de structures d’accélération Raytracing, dans les signatures racines locales ou globales. 

Un UAV dans la racine ne peut pas être associé à des compteurs. Les descripteurs dans la signature racine apparaissent chacun sous forme de descripteurs distincts, &mdash; mais ils ne peuvent pas être indexés de manière dynamique.

``` syntax
struct SceneData
{
   uint foo;
   float bar[2];
   int moo;
};
ConstantBuffer<SceneData> mySceneData : register(b6);
```

Dans l’exemple ci-dessus, `mySceneData` ne peut pas être déclaré en tant que tableau, comme dans `cbuffer mySceneData[2]` s’il va être mappé sur un descripteur dans la signature racine. Cela est dû au fait que l’indexation entre les descripteurs n’est pas prise en charge dans la signature racine. Si vous le souhaitez, vous pouvez définir des mémoires tampons de constante individuelles distinctes et les définir comme une entrée distincte dans la signature racine. Notez que, dans le `mySceneData` cas ci-dessus, il existe un tableau `bar[2]` . L’indexation dynamique au sein de la mémoire tampon constante est valide &mdash; un descripteur dans la signature racine se comporte de la même façon que le même descripteur se comporterait s’il était accessible via un tas de descripteur. Cela est contraire aux constantes d’incorporation directement dans la signature racine, qui apparaît également comme une mémoire tampon constante, sauf si la contrainte stipule que l’indexation dynamique au sein des constantes inline n’est pas autorisée `bar[2]` .

Ces API (à partir de l’interface [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) ) servent à définir des descripteurs directement sur la signature racine.

-   [**SetComputeRootConstantBufferView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootconstantbufferview)
-   [**SetGraphicsRootConstantBufferView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootconstantbufferview)
-   [**SetComputeRootShaderResourceView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootshaderresourceview)
-   [**SetGraphicsRootShaderResourceView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootshaderresourceview)
-   [**SetComputeRootUnorderedAccessView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootunorderedaccessview)
-   [**SetGraphicsRootUnorderedAccessView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootunorderedaccessview)

> [!NOTE]  
> Il n’existe aucun concept de *tableau de descripteurs racine* dans Direct3D 12. Les tableaux de descripteurs sont pris en charge uniquement dans les tas de descripteurs.

## <a name="related-topics"></a>Rubriques connexes

* [Signatures racines](root-signatures.md)
