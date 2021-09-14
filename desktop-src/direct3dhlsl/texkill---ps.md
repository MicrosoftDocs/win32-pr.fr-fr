---
title: texkill-PS
description: Annule le rendu du pixel actuel si l’un des trois premiers composants (UVW) des coordonnées de texture est inférieur à zéro.
ms.assetid: 7641aef8-8931-4a19-827a-75ab17e901ac
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4da9c6b59a3c16eeecb8755f2f19542df6ee8a7b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126921227"
---
# <a name="texkill---ps"></a>texkill-PS

Annule le rendu du pixel actuel si l’un des trois premiers composants (UVW) des coordonnées de texture est inférieur à zéro.

## <a name="syntax"></a>Syntaxe



| texkill DST |
|-------------|



 

where

-   l’heure d’été est un registre de destination

## <a name="remarks"></a>Notes



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texkill               | x    | x    | x    | x    | x    | x    | x     | x    | x     |



 

Cette instruction correspond à la fonction de [**découpage**](dx-graphics-hlsl-clip.md) du langage HLSL.

texkill n’échantillonne aucune texture. Il opère sur les trois premiers composants des coordonnées de texture fournies par le numéro de registre de destination. Pour PS \_ 1 \_ 4, texkill fonctionne sur les données dans les trois premiers composants du registre de destination.

Vous pouvez utiliser cette instruction pour implémenter des plans de clips arbitraires dans le rastériseur.

Lorsque vous utilisez des nuanceurs vertex, l’application est responsable de l’application de la transformation de perspective. Cela peut entraîner des problèmes pour les plans de découpage arbitraires, car s’ils contiennent des facteurs d’échelle anisomorphic, les plans de clip doivent également être transformés. Par conséquent, il est préférable de fournir une position de vertex non projetée à utiliser dans le Clipper arbitraire, qui est le jeu de coordonnées de texture identifié par l’opérateur texkill.

Cette instruction est utilisée comme suit :

<dl> texkill TN  
Le masquage des pixels s’effectue comme suit :  
if (les composants x, y, z de TextureCoordinates (stage n)<sub>UVWQ</sub>< 0)  
annuler le rendu de pixel
</dl>

Pour le nuanceur de pixels 1 \_ 1, 1 \_ 2 et 1 \_ 3, texkill opère sur le jeu de coordonnées de texture donné par le numéro de registre de destination. Dans la version 1 \_ 4, toutefois, texkill fonctionne sur les données contenues dans le [Registre de coordonnées de texture](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (TN) ou dans le registre temporaire (RN) qui a été spécifié comme destination.

Lorsque l’échantillonnage multiple est activé, tout effet d’anticrénelage atteint sur les arêtes de polygones en raison de l’échantillonnage multiple n’est pas effectué sur un bord qui a été généré par texkill. Le nuanceur de pixels s’exécute une fois par pixel.

Cet exemple n'est donné qu'à titre indicatif.

Cet exemple masque les pixels qui ont des coordonnées de texture négatives. Les couleurs de pixel sont interpolées à partir des couleurs de vertex fournies dans les données de vertex.


```
ps_1_1       // Version instruction
texkill t0   // Mask out pixel using texture coordinates from stage 0
mov r0, v0   // Move the diffuse color in v0 to r0

// The rendered output from the pixel shader is shown below
```



Les coordonnées de texture sont comprises entre-0,5 et 0,5 dans u, et 0,0 à 1,0 dans v. Cette instruction entraîne le masquage des valeurs d’u négatives. La première illustration ci-dessous montre la couleur de vertex appliquée au Quad sans l’instruction texkill appliquée. La deuxième illustration suivante montre le résultat de l’instruction texkill. Les couleurs de pixel des coordonnées de texture inférieures à 0 (où x passe de-0,5 à 0,0) sont masquées. La couleur d’arrière-plan (blanc) est utilisée pour masquer la couleur de pixel.

![illustration de la sortie avec la couleur de vertex appliquée au Quad sans l’instruction texkill](images/pstexkill-in.jpg)![illustration de la sortie avec l’instruction texkill appliquée](images/pstexkill-out.jpg)

Les données de coordonnée de texture sont déclarées dans la déclaration de données de vertex dans cet exemple.


```
   
struct CUSTOMVERTEX
{
    FLOAT x, y, z;
    DWORD color;
    FLOAT tu1, tv1;
};

#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZ|D3DFVF_DIFFUSE|D3DFVF_TEX1|D3DTEXCOORD2(0))

static CUSTOMVERTEX g_Vertices[]=
{
    //  x      y     z    color         u1,    v1  
    { -1.0f, -1.0f, 0.0f, 0xffff0000, -0.5f,  1.0f, },
    {  1.0f, -1.0f, 0.0f, 0xff00ff00,  0.5f,  1.0f, },
    {  1.0f,  1.0f, 0.0f, 0xff0000ff,  0.5f,  0.0f, },
    { -1.0f,  1.0f, 0.0f, 0xffffffff, -0.5f,  0.0f, },

};
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




