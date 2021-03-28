---
title: Énumération D3DX11_FILTER_FLAG (D3DX11tex. h)
description: 'Remarque : la bibliothèque de l’utilitaire D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store. Indicateurs de filtrage de texture.'
ms.assetid: 083a6a19-1933-4831-9501-36d4867f3dce
keywords:
- Énumération D3DX11_FILTER_FLAG Direct3D 11
- Pointeur d’énumération LPD3DX11_FILTER_FLAG Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_FILTER_FLAG
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f2105970efb7f2ec07464d8a902df49d8f75bc2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982575"
---
# <a name="d3dx11_filter_flag-enumeration"></a>\_Énumération de l’indicateur de filtre D3DX11 \_

> [!Note]  
> La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.

 

Indicateurs de filtrage de texture.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum D3DX11_FILTER_FLAG { 
  D3DX11_FILTER_NONE              = (1 << 0),
  D3DX11_FILTER_POINT             = (2 << 0),
  D3DX11_FILTER_LINEAR            = (3 << 0),
  D3DX11_FILTER_TRIANGLE          = (4 << 0),
  D3DX11_FILTER_BOX               = (5 << 0),
  D3DX11_FILTER_MIRROR_U          = (1 << 16),
  D3DX11_FILTER_MIRROR_V          = (2 << 16),
  D3DX11_FILTER_MIRROR_W          = (4 << 16),
  D3DX11_FILTER_MIRROR            = (7 << 16),
  D3DX11_FILTER_DITHER            = (1 << 19),
  D3DX11_FILTER_DITHER_DIFFUSION  = (2 << 19),
  D3DX11_FILTER_SRGB_IN           = (1 << 21),
  D3DX11_FILTER_SRGB_OUT          = (2 << 21),
  D3DX11_FILTER_SRGB              = (3 << 21)
} D3DX11_FILTER_FLAG, *LPD3DX11_FILTER_FLAG;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DX11_FILTER_NONE"></span><span id="d3dx11_filter_none"></span>**\_Filtre D3DX11 \_ aucun**
</dt> <dd>

Aucune mise à l’échelle ou aucun filtrage n’aura lieu. Les pixels en dehors des limites de l’image source sont supposés être en noir transparent.

</dd> <dt>

<span id="D3DX11_FILTER_POINT"></span><span id="d3dx11_filter_point"></span>**\_Point de filtre D3DX11 \_**
</dt> <dd>

Chaque pixel de destination est calculé en échantillonnant le pixel le plus proche de l’image source.

</dd> <dt>

<span id="D3DX11_FILTER_LINEAR"></span><span id="d3dx11_filter_linear"></span>**\_Filtre \_ linéaire D3DX11**
</dt> <dd>

Chaque pixel de destination est calculé en échantillonnant les quatre pixels les plus proches de l’image source. Ce filtre fonctionne mieux lorsque la mise à l’échelle sur les deux axes est inférieure à deux.

</dd> <dt>

<span id="D3DX11_FILTER_TRIANGLE"></span><span id="d3dx11_filter_triangle"></span>**\_Triangle de filtre D3DX11 \_**
</dt> <dd>

Chaque pixel de l’image source contribue de manière égale à l’image de destination. Il s’agit de la plus lente des filtres.

</dd> <dt>

<span id="D3DX11_FILTER_BOX"></span><span id="d3dx11_filter_box"></span>**\_Zone de filtre D3DX11 \_**
</dt> <dd>

Chaque pixel est calculé en calculant la moyenne d’une zone de pixels 2x2 (x2) à partir de l’image source. Ce filtre fonctionne uniquement lorsque les dimensions de la destination sont la moitié de la source, comme c’est le cas avec des mipmaps.

</dd> <dt>

<span id="D3DX11_FILTER_MIRROR_U"></span><span id="d3dx11_filter_mirror_u"></span>**\_Miroir de filtre D3DX11 \_ \_ U**
</dt> <dd>

Les pixels du bord de la texture sur l’axe u doivent être mis en miroir, et non encapsulés.

</dd> <dt>

<span id="D3DX11_FILTER_MIRROR_V"></span><span id="d3dx11_filter_mirror_v"></span>**\_Miroir de filtre D3DX11 \_ \_ V**
</dt> <dd>

Les pixels du bord de la texture sur l’axe v doivent être mis en miroir, et non encapsulés.

</dd> <dt>

<span id="D3DX11_FILTER_MIRROR_W"></span><span id="d3dx11_filter_mirror_w"></span>**\_Miroir de filtre D3DX11 \_ \_ W**
</dt> <dd>

Les pixels du bord de la texture sur l’axe des w doivent être mis en miroir, et non encapsulés.

</dd> <dt>

<span id="D3DX11_FILTER_MIRROR"></span><span id="d3dx11_filter_mirror"></span>**\_Miroir de filtre D3DX11 \_**
</dt> <dd>

La spécification de cet indicateur revient à spécifier les \_ indicateurs de filtre D3DX en miroir \_ \_ U, D3DX \_ Filter \_ miroir \_ V et D3DX \_ Filter- \_ MIRROR \_ W.

</dd> <dt>

<span id="D3DX11_FILTER_DITHER"></span><span id="d3dx11_filter_dither"></span>**\_Filtre D3DX11 \_ tramé**
</dt> <dd>

L’image résultante doit être tramée à l’aide d’un algorithme de trame trié 4x4. Cela se produit lors de la conversion d’un format vers un autre.

</dd> <dt>

<span id="D3DX11_FILTER_DITHER_DIFFUSION"></span><span id="d3dx11_filter_dither_diffusion"></span>**D3DX11 \_ filtre de \_ diffusion en trame \_**
</dt> <dd>

Effectuez un tramage diffus sur l’image lors du passage d’un format à un autre.

</dd> <dt>

<span id="D3DX11_FILTER_SRGB_IN"></span><span id="d3dx11_filter_srgb_in"></span>**D3DX11 \_ filtre \_ sRVB \_ dans**
</dt> <dd>

Les données d’entrée se trouvent dans l’espace de couleurs RVB standard (sRVB). Consultez la section Remarques.

</dd> <dt>

<span id="D3DX11_FILTER_SRGB_OUT"></span><span id="d3dx11_filter_srgb_out"></span>**D3DX11 \_ filtre \_ en \_ grisé**
</dt> <dd>

Les données de sortie sont dans l’espace de couleurs RVB standard (sRVB). Consultez la section Remarques.

</dd> <dt>

<span id="D3DX11_FILTER_SRGB"></span><span id="d3dx11_filter_srgb"></span>**D3DX11 \_ filtre \_ sRVB**
</dt> <dd>

Identique à la spécification \_ de la fonction de filtre D3DX \_ sRVB \_ dans le \| \_ filtre D3DX \_ \_ out. Consultez la section Remarques.

</dd> </dl>

## <a name="remarks"></a>Notes

D3DX11 effectue automatiquement une correction gamma (pour convertir les données de couleur de l’espace RVB en espace RVB standard) lors du chargement des données de texture. Cette opération est effectuée automatiquement par exemple lorsque les données RVB sont chargées à partir d’un fichier. png dans une texture sRVB. Utilisez les indicateurs de filtre sRVB pour indiquer si les données n’ont pas besoin d’être converties en espace sRVB.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3DX11tex. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations D3DX](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 





