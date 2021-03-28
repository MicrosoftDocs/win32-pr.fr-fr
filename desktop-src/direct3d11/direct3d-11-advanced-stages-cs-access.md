---
title: Accès aux ressources
description: Il existe plusieurs façons d’accéder aux ressources.
ms.assetid: 83950c4d-5df2-4ed1-9d8f-222a62791c18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e69ab7bffd22b2271c4d648c3a95ec8d98656973
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104990972"
---
# <a name="accessing-resources"></a>Accès aux ressources

Il existe plusieurs façons d’accéder aux [ressources](overviews-direct3d-11-resources-types.md). Indépendamment, Direct3D garantit de retourner zéro pour toute ressource qui est accessible à partir de limites.

-   [Accès par décalage d’octet](#access-by-byte-offset)
-   [Accès par index](#access-by-index)
-   [Accès par méthode mips](#access-by-mips-method)
-   [Rubriques connexes](#related-topics)

## <a name="access-by-byte-offset"></a>Accès par décalage d’octet

Il est possible d’accéder à deux nouveaux types de tampons à l’aide d’un décalage d’octet :

-   [**ByteAddressBuffer**](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer) est un tampon en lecture seule.
-   [**RWByteAddressBuffer**](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer) est un tampon de lecture ou d’écriture.

## <a name="access-by-index"></a>Accès par index

Les types de ressources peuvent utiliser un index pour faire référence à un emplacement spécifique dans la ressource. Prenons l’exemple suivant :


```
uint2 pos;
Texture2D<float4> myTexture;
float4 myVar = myTexture[pos];
```



Cet exemple affecte les 4 valeurs float qui sont stockées au Texel situé à la position *pos* dans la ressource de texture 2D *myTexture* à la variable *MyVar* .

> [!Note]  
> La valeur par défaut pour accéder à une texture de cette façon est le niveau mipmap zéro (le niveau le plus détaillé).

 

> [!Note]  
> La ligne « float4 myVar = myTexture \[ pos \] ; » équivaut à « float4 MyVar = MyTexture. Load (uint3 (POS, 0)); ». L’accès par index est une nouvelle amélioration de la syntaxe HLSL.

 

> [!Note]  
> Le compilateur dans la version de juin 2010 du kit de développement logiciel (SDK) DirectX et ultérieur vous permet d’indexer tous les types de ressources, à l’exception des [mémoires tampons d’adresse d’octets](direct3d-11-advanced-stages-cs-resources.md).

 

> [!Note]  
> Le compilateur 2010 de juin et les versions ultérieures vous permettent de déclarer des variables de ressource locales. Vous pouvez assigner des ressources globalement définies (comme *myTexture*) à ces variables et les utiliser de la même façon que leurs équivalents globaux.

 

## <a name="access-by-mips-method"></a>Accès par méthode mips

Les objets texture ont une méthode **mips** (par exemple, [**Texture2D. mips**](/previous-versions/windows/desktop/legacy/ff471560(v=vs.85))), que vous pouvez utiliser pour spécifier le niveau de mipmap. Cet exemple lit la couleur stockée sur (7, 16) sur le mipmap niveau 2 dans une texture 2D :


```
uint x = 7;
uint y = 16;
float4 myColor = myTexture.mips[2][uint2(x,y)];
```



Il s’agit d’une amélioration du compilateur 2010 de juin et versions ultérieures. L’expression « myTexture. mips \[ 2 \] \[ uint2 (x, y) \] » est équivalente à « myTexture. Load (uint3 (x, y, 2)) ».

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vue d’ensemble du nuanceur de calcul](direct3d-11-advanced-stages-compute-shader.md)
</dt> </dl>

 

 