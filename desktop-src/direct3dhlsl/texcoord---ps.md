---
title: texcoord-PS
description: Interprète les données de coordonnée de texture (UVW1) en tant que données de couleur (RVBA).
ms.assetid: 0f79a62c-1142-4dcd-aa2f-a5bd1c369ffc
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9e871d1f91d89d0eb0ddadee34b5ac215916d0af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728060"
---
# <a name="texcoord---ps"></a>texcoord-PS

Interprète les données de coordonnée de texture (UVW1) en tant que données de couleur (RVBA).

## <a name="syntax"></a>Syntaxe



| texcoord DST |
|--------------|



 

where

-   l’heure d’été est le registre de destination.

## <a name="remarks"></a>Notes



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texcoord              | x    | x    | x    |      |      |      |       |      |       |



 

Cette instruction interprète le jeu de coordonnées de texture (UVW1) correspondant au numéro de registre de destination en tant que données de couleur (RVBA). Si le jeu de coordonnées de texture contient moins de trois composants, les composants manquants ont la valeur 0. Le quatrième composant est toujours défini sur 1. Toutes les valeurs sont ancrées entre 0 et 1.

L’avantage de texcoord est qu’il fournit un moyen de passer des données de vertex interpolées à haute précision directement dans le nuanceur de pixels. Toutefois, lorsque les données sont écrites dans le registre de destination, une certaine précision est perdue, en fonction du nombre de bits utilisés par le matériel pour les registres.

Aucune texture n’est échantillonnée par cette instruction. Seules les coordonnées de texture définies pour cette étape de texture sont pertinentes.

Toutes les données de texture (telles que la position, la normale et la direction de la source de lumière) peuvent être mappées par un nuanceur de sommets à une coordonnée de texture. Pour ce faire, associez une texture à un registre de texture à l’aide de [**SetTexture**](/windows/desktop/direct3d9/id3dxbaseeffect--settexture) et spécifiez comment l’échantillonnage de texture est effectué à l’aide de [**SetTextureStageState**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate). Si le pipeline de fonction fixe est utilisé, veillez à fournir l' \_ indicateur TSS TEXCOORDINDEX.

Cette instruction est utilisée comme suit :


```
texcoord tn
```



Un [Registre de coordonnées de texture](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (TN) contient quatre valeurs de couleur (RVBA). Les données peuvent également être considérées comme des données vectorielles (XYZW). texcoord récupère trois de ces valeurs (XYZ) à partir du jeu de coordonnées de texture x et le quatrième composant (w) a la valeur 1. L’adresse de texture est copiée à partir du jeu de coordonnées de texture n. Le résultat est bloqué entre 0 et 1.

Cet exemple n'est donné qu'à titre indicatif. Le code C qui accompagne le nuanceur n’a pas été optimisé pour les performances.

Voici un exemple de nuanceur utilisant texcoord.


```
ps_1_1        ; version instruction
texcoord t0   ; declare t0 hold texture coordinates, 
              ; which represent rgba values in this example
mov r0, t0    ; move the color in t0 to output register r0
```



La sortie rendue par le nuanceur de pixels est présentée dans l’illustration suivante. Les valeurs de coordonnée (u, v, w, 1) sont mappées aux canaux (RVB). Le canal alpha est défini sur 1. Aux angles de l’illustration, la coordonnée (0, 0, 0, 1) est interprétée comme noir ; (1, 0, 0, 1) est rouge ; (0, 1, 0, 1) est vert ; et (1, 1, 0, 1) contient le vert et le rouge, ce qui produit le jaune.

![illustration de la sortie rendue de l’exemple de nuanceur de pixels](images/pstexcoord.jpg)

Du code supplémentaire est nécessaire pour utiliser ce nuanceur et un exemple de scénario est illustré ci-dessous.


```
// This code creates the shader from a file. The contents of  
// the shader file can also be supplied as a text string.
LPD3DXBUFFER        pCode;

// Assemble the vertex shader from the file
D3DXAssembleShaderFromFile(strPShaderPath, 0, NULL, &pCode, NULL);
m_pd3dDevice->CreatePixelShader((DWORD*)pCode->GetBufferPointer(),
                   &m_hPixelShader);
pCode->Release();

// This code defines the object vertex data
struct CUSTOMVERTEX
{
    FLOAT x, y, z;
    FLOAT tu1, tv1;
};

#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZ|D3DFVF_TEX1|TEXCOORD2(0))

static CUSTOMVERTEX g_Vertices[]=
{
    //  x      y     z     u1    v1   
    { -1.0f, -1.0f, 0.0f, 0.0f, 0.0f, },
    { +1.0f, -1.0f, 0.0f, 1.0f, 0.0f, },
    { +1.0f, +1.0f, 0.0f, 1.0f, 1.0f, },
    { -1.0f, +1.0f, 0.0f, 0.0f, 1.0f, },
};
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 