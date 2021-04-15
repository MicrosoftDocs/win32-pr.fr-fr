---
description: Définit les types de texture de l’échantillonneur pour les nuanceurs de vertex.
ms.assetid: 8e9923f9-6f30-45e5-a557-f26d441a534d
title: Énumération D3DSAMPLER_TEXTURE_TYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSAMPLER_TEXTURE_TYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 337e8b25a8ec8389a6252fb48582128c601730ca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394063"
---
# <a name="d3dsampler_texture_type-enumeration"></a>\_Énumération de type de texture D3DSAMPLER \_

Définit les types de texture de l’échantillonneur pour les nuanceurs de vertex.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum D3DSAMPLER_TEXTURE_TYPE { 
  D3DSTT_UNKNOWN,
  D3DSTT_2D,
  D3DSTT_CUBE,
  D3DSTT_VOLUME,
  D3DSTT_FORCE_DWORD
} D3DSAMPLER_TEXTURE_TYPE, *LPD3DSAMPLER_TEXTURE_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DSTT_UNKNOWN"></span><span id="d3dstt_unknown"></span>**D3DSTT \_ inconnu**
</dt> <dd>

Valeur non initialisée. La valeur de cet élément est 0 &lt; &lt; D3DSP \_ TEXTURETYPE \_ Shift.

</dd> <dt>

<span id="D3DSTT_2D"></span><span id="d3dstt_2d"></span>**D3DSTT \_ 2D**
</dt> <dd>

Déclaration d’une texture 2D. La valeur de cet élément est 2 &lt; &lt; D3DSP \_ TEXTURETYPE \_ Shift.

</dd> <dt>

<span id="D3DSTT_CUBE"></span><span id="d3dstt_cube"></span>**\_Cube D3DSTT**
</dt> <dd>

Déclaration d’une texture de cube. La valeur de cet élément est 3 &lt; &lt; D3DSP \_ TEXTURETYPE \_ Shift.

</dd> <dt>

<span id="D3DSTT_VOLUME"></span><span id="d3dstt_volume"></span>**\_Volume D3DSTT**
</dt> <dd>

Déclaration d’une texture de volume. La valeur de cet élément est 4 &lt; &lt; D3DSP \_ TEXTURETYPE \_ Shift.

</dd> <dt>

<span id="D3DSTT_FORCE_DWORD"></span><span id="d3dstt_force_dword"></span>**D3DSTT \_ forcer \_ DWORD**
</dt> <dd>

Force cette énumération à se compiler à 32 bits de taille. Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits. Cette valeur n'est pas utilisée.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




