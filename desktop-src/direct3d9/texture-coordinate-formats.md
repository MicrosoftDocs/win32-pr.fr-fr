---
description: Les coordonnées de texture dans Direct3D peuvent inclure un, deux, trois ou quatre éléments à virgule flottante pour adresser des textures avec différents niveaux de dimension.
ms.assetid: d841af62-41b0-4b80-960b-4630b9a7210c
title: Formats de coordonnée de texture (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c48ec28b9c99357fe8825f5ff79da3c8869719389c4a4bc4874c5740fc71f42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118519882"
---
# <a name="texture-coordinate-formats-direct3d-9"></a>Formats de coordonnée de texture (Direct3D 9)

Les coordonnées de texture dans Direct3D peuvent inclure un, deux, trois ou quatre éléments à virgule flottante pour adresser des textures avec différents niveaux de dimension. Une texture 1D-une surface de texture avec des dimensions de texels 1-par-n, est traitée par une coordonnée de texture. Le cas le plus courant, les textures 2D, sont traités avec deux coordonnées de texture couramment appelées « vous » et « v ». Direct3D prend en charge deux types de textures 3D, de cartes d’environnement cubique et de textures de volume. Les cartes d’environnement cubiques ne sont pas véritablement en 3D, mais elles sont traitées par un vecteur à 3 éléments. Pour plus d’informations, consultez [mappage d’environnement cubique (Direct3D 9)](cubic-environment-mapping.md).

Comme décrit dans les [codes de fonction fixe (Direct3D 9)](fixed-function-fvf-codes.md), les applications encodent des coordonnées de texture au format vertex. Le format vertex peut inclure plusieurs jeux de coordonnées de texture. Utilisez la D3DFVF \_ TEX0 à D3DFVF \_ TEX8 [D3DFVF](d3dfvf.md) pour décrire un format de vertex qui n’a pas de coordonnées de texture, ou jusqu’à huit jeux.

Chaque jeu de coordonnées de texture peut avoir entre un et quatre éléments. Les \_ indicateurs D3DFVF TEXTUREFORMAT1 à D3DFVF \_ TEXTUREFORMAT4 décrivent le nombre d’éléments dans une coordonnée de texture dans un jeu, mais ces indicateurs ne sont pas utilisés eux-mêmes. Au lieu de cela, le jeu de macros [**\_ TEXCOORDSIZEN D3DFVF**](d3dfvf-texcoordsizen.md) utilise ces indicateurs pour créer des modèles binaires qui décrivent le nombre d’éléments utilisés par un jeu de coordonnées de texture particulier au format de vertex. Ces macros acceptent un paramètre unique qui identifie l’index du jeu de coordonnées dont le nombre d’éléments est défini. L’exemple suivant illustre l’utilisation de ces macros.


```
// This vertex format contains two sets of texture coordinates.
// The first set (index 0) has 2 elements, and the second set 
// has 1 element. The description for this vertex format would be: 
//     dwFVF = D3DFVF_XYZ  | D3DFVF_NORMAL | D3DFVF_DIFFUSE | D3DFVF_TEX2 |
//             D3DFVF_TEXCOORDSIZE2(0) | D3DFVF_TEXCOORDSIZE1(1); 
//
typedef struct CVF
{
    D3DVECTOR position;
    D3DVECTOR normal;
    D3DCOLOR  diffuse;
    float     u, v;   // 1st set, 2D
    float     t;      // 2nd set, 1D
} CustomVertexFormat;
```



> [!Note]  
> À l’exception des cartes de l’environnement cubique et des textures de volume, les rastériseurs ne peuvent pas traiter les textures à l’aide de plus de deux éléments. Les applications peuvent fournir jusqu’à trois éléments pour une coordonnée de texture, mais uniquement si la texture est un mappage de cube, une texture de volume ou l' \_ indicateur de transformation de texture projeté D3DTTFF est utilisé. L' \_ indicateur D3DTTFF projeté amène le rastériseur à diviser les deux premiers éléments par le troisième (ou n) élément. Pour plus d’informations, consultez [transformations de coordonnées de texture (Direct3D 9)](texture-coordinate-transformations.md).

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Coordonnées de texture](texture-coordinates.md)
</dt> </dl>

 

 



