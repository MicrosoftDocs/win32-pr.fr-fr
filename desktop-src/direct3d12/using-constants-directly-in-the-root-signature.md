---
title: Utilisation des constantes directement dans la signature racine
description: Les applications peuvent définir des constantes racine dans la signature racine, chacune sous la forme d’un ensemble de valeurs 32 bits. Elles s’affichent en langage HLSL (High Level Shading Language) en tant que mémoire tampon constante. Notez que les mémoires tampons constantes pour des raisons historiques sont affichées sous forme d’ensembles de valeurs 4x32 bits.
ms.assetid: F9A2640F-D1FA-481C-BDF1-B15372E3C512
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a3cd3980bede72d6e2f4b163abe11b249970eb7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103390"
---
# <a name="using-constants-directly-in-the-root-signature"></a>Utilisation des constantes directement dans la signature racine

Les applications peuvent définir des constantes racine dans la signature racine, chacune sous la forme d’un ensemble de valeurs 32 bits. Elles s’affichent en langage HLSL (High Level Shading Language) en tant que mémoire tampon constante. Notez que les mémoires tampons constantes pour des raisons historiques sont affichées sous forme d’ensembles de valeurs 4x32 bits.

Chaque ensemble de constantes utilisateur est traité comme un tableau scalaire de valeurs 32 bits, indexable dynamiquement et en lecture seule à partir du nuanceur. En dehors des limites, l’indexation d’un ensemble donné de constantes racine génère des résultats indéfinis. En langage HLSL, les définitions de structure de données peuvent être fournies pour que les constantes utilisateur leur fournissent des types. Par exemple, si la signature racine définit un ensemble de 4 constantes racine, le langage HLSL peut superposer la structure suivante.

``` syntax
struct DrawConstants
{
    uint foo;
    float2 bar;
    int moo;
};
ConstantBuffer<DrawConstants> myDrawConstants : register(b1, space0);
```

Les tableaux ne sont pas autorisés dans les mémoires tampons constantes qui sont mappées sur les constantes racine puisque l’indexation dynamique dans l’espace de signature racine n’est pas prise en charge. Par exemple, il n’est pas valide d’avoir une entrée dans la mémoire tampon constante telle que `float myArray[2];` . Une mémoire tampon constante mappée aux constantes racine ne peut pas être un tableau ; par conséquent, il n’est pas valide de mapper à des `cbuffer myCBArray[2]` constantes racine.

Les constantes peuvent être partiellement définies. Par exemple, si la signature racine définit des valeurs 4 32 bits à *RootTableBindSlot* 2, tout sous-ensemble des quatre constantes peut être défini à la fois (les autres restent inchangées). Cela peut être utile dans les regroupements qui héritent de l’état de signature racine et peuvent être modifiés partiellement.

Lors de la définition de constantes, faites attention à la disposition de mémoire tampon constante attendue par le nuanceur. Il est possible que les constantes soient remplies dans `vec4` les limites, par exemple. Pour vérifier la disposition attendue, vérifiez les informations de réflexion du nuanceur HLSL.

Les API suivantes (à partir de l’interface [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist) ) concernent la définition de constantes directement sur la signature racine :

-   [**SetGraphicsRoot32BitConstant**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsroot32bitconstant)
-   [**SetGraphicsRoot32BitConstants**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsroot32bitconstants)
-   [**SetComputeRoot32BitConstant**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstant)
-   [**SetComputeRoot32BitConstants**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstants)

Reportez-vous également à la structure des [**\_ \_ constantes racine D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Signatures racines](root-signatures.md)
</dt> </dl>

 

 




