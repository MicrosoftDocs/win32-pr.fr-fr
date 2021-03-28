---
title: Présentation des mémoires tampons dans Direct3D 11
description: Une ressource de mémoire tampon est une collection de données entièrement typées regroupées en éléments.
ms.assetid: e33ca01e-f13c-4f91-b0db-2b2bc6b4fd8f
keywords:
- mémoire tampon constante, présentation
- mémoire tampon de vertex, présentation
- mémoire tampon d’index, présentation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 241ade0721ae87b1371586bc901ee18f8975b53f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315450"
---
# <a name="introduction-to-buffers-in-direct3d-11"></a>Présentation des mémoires tampons dans Direct3D 11

Une ressource de mémoire tampon est une collection de données entièrement typées regroupées en éléments. Vous pouvez utiliser des mémoires tampons pour stocker un large éventail de données, notamment des vecteurs de position, des vecteurs normaux, des coordonnées de texture dans une mémoire tampon de vertex, des index dans une mémoire tampon d’index ou un état de périphérique. Un élément buffer est constitué de 1 à 4 composants. Les éléments de mémoire tampon peuvent inclure des valeurs de données compressées (telles que des valeurs de surface R8G8B8A8), des entiers 8 bits uniques ou des valeurs à virgule flottante 4 32 bits.

Une mémoire tampon est créée en tant que ressource non structurée. Étant donné qu’elle n’est pas structurée, une mémoire tampon ne peut pas contenir de niveaux de mipmap, elle ne peut pas être filtrée lors de la lecture et elle ne peut pas être multiéchantillonnée.

## <a name="buffer-types"></a>Types de mémoires tampons

Voici les types de ressources de mémoire tampon pris en charge par Direct3D 11. Tous les types de mémoires tampons sont encapsulés par l’interface [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) .

-   [Mémoire tampon de vertex](#vertex-buffer)
-   [Mémoire tampon d’index](#index-buffer)
-   [Mémoire tampon constante](#constant-buffer)

### <a name="vertex-buffer"></a>Mémoire tampon de vertex

Une mémoire tampon de vertex contient les données de vertex utilisées pour définir votre géométrie. Les données de vertex incluent les coordonnées de position, les données de couleur, les données de coordonnées de texture, les données normales, etc.

L’exemple le plus simple d’une mémoire tampon de vertex est celui qui contient uniquement des données de position. Il peut être visualisé comme dans l’illustration suivante.

![illustration d’une mémoire tampon de vertex qui contient des données de position](images/d3d10-resources-single-element-vb2.png)

Plus souvent, une mémoire tampon de vertex contient toutes les données nécessaires pour spécifier entièrement les sommets 3D. Par exemple, il peut s’agir d’une mémoire tampon de vertex qui contient la position par vertex, les coordonnées normales et de texture. Ces données sont généralement organisées sous la forme d’ensembles d’éléments par vertex, comme indiqué dans l’illustration suivante.

![illustration d’une mémoire tampon de vertex qui contient la position, la normale et les données de texture](images/d3d10-vertex-buffer-element.png)

Cette mémoire tampon de vertex contient des données par vertex ; chaque vertex stocke trois éléments (coordonnées de position, normale et de texture). La position et la normale sont généralement spécifiées à l’aide des valeurs float 3 32 bits (DXGI \_ format \_ R32G32B32 \_ float) et des coordonnées de texture utilisant des valeurs float 2 32 bits (dxgi \_ format \_ R32G32 \_ float).

Pour accéder aux données à partir d’une mémoire tampon de vertex, vous devez connaître le vertex auquel accéder, ainsi que les paramètres de mémoire tampon supplémentaires suivants :

-   Offset : nombre d’octets à partir du début de la mémoire tampon vers les données du premier vertex. Vous pouvez spécifier le décalage à l’aide de la méthode [**ID3D11DeviceContext :: IASetVertexBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetvertexbuffers) .
-   BaseVertexLocation-nombre d’octets entre le décalage et le premier vertex utilisé par l’appel de dessin approprié.

Avant de créer une mémoire tampon de vertex, vous devez définir sa disposition en créant une interface [**ID3D11InputLayout**](/windows/win32/api/d3d11/nn-d3d11-id3d11inputlayout) ; pour ce faire, appelez la méthode [**ID3D11Device :: CreateInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createinputlayout) . Une fois l’objet de disposition d’entrée créé, vous pouvez le lier à l’étape assembleur d’entrée en appelant [**ID3D11DeviceContext :: IASetInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetinputlayout).

Pour créer une mémoire tampon de vertex, appelez [**ID3D11Device :: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer).

### <a name="index-buffer"></a>Mémoire tampon d’index

Les tampons d’index contiennent des décalages d’entiers dans les mémoires tampons de vertex et sont utilisés pour restituer les primitives plus efficacement. Une mémoire tampon d’index contient un ensemble séquentiel d’index 16 bits ou 32 bits ; chaque index est utilisé pour identifier un vertex dans une mémoire tampon de vertex. Un tampon d’index peut être visualisé comme dans l’illustration suivante.

![illustration d’un tampon d’index](images/d3d10-index-buffer.png)

Les index séquentiels stockés dans une mémoire tampon d’index se trouvent avec les paramètres suivants :

-   Offset-nombre d’octets à partir de l’adresse de base de la mémoire tampon d’index. Le décalage est fourni à la méthode [**ID3D11DeviceContext :: IASetIndexBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetindexbuffer) .
-   StartIndexLocation : spécifie le premier élément de mémoire tampon d’index à partir de l’adresse de base et l’offset fourni dans [**IASetIndexBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetindexbuffer). L’emplacement de départ est fourni à la méthode [**ID3D11DeviceContext ::D rawindexed**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexed) ou [**ID3D11DeviceContext ::D rawindexedinstanced**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexedinstanced) et représente le premier index à restituer.
-   IndexCount-nombre d’index à afficher. Le nombre est fourni à la méthode [**DrawIndexed**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexed)

Début de la mémoire tampon d’index = adresse de base du tampon d’index + décalage (octets) + StartIndexLocation \* (octets);

Dans ce calcul, la valeur d’élément est la taille de chaque élément de mémoire tampon d’index, soit deux ou quatre octets.

Pour créer un tampon d’index, appelez [**ID3D11Device :: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer).

### <a name="constant-buffer"></a>Mémoire tampon constante

Une mémoire tampon constante vous permet de fournir efficacement des données de constantes de nuanceur au pipeline. Vous pouvez utiliser une mémoire tampon constante pour stocker les résultats de l’étape de flux de sortie. Conceptuellement, une mémoire tampon constante ressemble à une mémoire tampon de vertex à un seul élément, comme indiqué dans l’illustration suivante.

![illustration d’une mémoire tampon de nuanceur constante](images/d3d10-shader-resource-buffer.png)

Chaque élément stocke une constante composant de 1 à 4, déterminée par le format des données stockées. Pour créer une mémoire tampon de nuanceur constante, appelez [**ID3D11Device :: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) et spécifiez le membre de la **\_ \_ \_ mémoire tampon constante de liaison d3d11** du type énuméré de l' [**\_ \_ indicateur de liaison d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) .

Une mémoire tampon constante ne peut utiliser qu’un seul indicateur de liaison (d3d11 de la **\_ \_ \_ mémoire tampon constante**), qui ne peut pas être combiné avec un autre indicateur de liaison. Pour lier une mémoire tampon de nuanceur constante au pipeline, appelez l’une des méthodes suivantes : [**ID3D11DeviceContext :: GSSetConstantBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-gssetconstantbuffers), [**ID3D11DeviceContext ::P ssetconstantbuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetconstantbuffers)ou [**ID3D11DeviceContext :: VSSetConstantBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-vssetconstantbuffers).

Pour lire une mémoire tampon de nuanceur constante à partir d’un nuanceur, utilisez une fonction de chargement HLSL (par exemple, [**Load**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-load)). Chaque étape de nuanceur autorise jusqu’à 15 mémoires tampons constantes de nuanceur ; chaque mémoire tampon peut contenir jusqu’à 4096 constantes.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mémoires tampons](overviews-direct3d-11-resources-buffers.md)
</dt> </dl>

 

 