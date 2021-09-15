---
description: Les États de l’échantillonneur définissent des opérations d’échantillonnage de texture, telles que l’adressage et le filtrage de texture.
ms.assetid: 03a6a5f1-5e4f-4ba8-be4a-74d78fbc85d0
title: Énumération D3DSAMPLERSTATETYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSAMPLERSTATETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3e12764db306e61422f8c06ef514f6fad59b3ed8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127516980"
---
# <a name="d3dsamplerstatetype-enumeration"></a>Énumération D3DSAMPLERSTATETYPE

Les États de l’échantillonneur définissent des opérations d’échantillonnage de texture, telles que l’adressage et le filtrage de texture. Certains États de l’échantillonneur configurent le traitement des vertex et un traitement des pixels configurés. Les États de l’échantillonneur peuvent être enregistrés et restaurés à l’aide de stateblocks (consultez États d' [enregistrement et de restauration des blocs d’État (Direct3D 9)](state-blocks-save-and-restore-state.md)).

## <a name="syntax"></a>Syntaxe


```C++
typedef enum D3DSAMPLERSTATETYPE { 
  D3DSAMP_ADDRESSU       = 1,
  D3DSAMP_ADDRESSV       = 2,
  D3DSAMP_ADDRESSW       = 3,
  D3DSAMP_BORDERCOLOR    = 4,
  D3DSAMP_MAGFILTER      = 5,
  D3DSAMP_MINFILTER      = 6,
  D3DSAMP_MIPFILTER      = 7,
  D3DSAMP_MIPMAPLODBIAS  = 8,
  D3DSAMP_MAXMIPLEVEL    = 9,
  D3DSAMP_MAXANISOTROPY  = 10,
  D3DSAMP_SRGBTEXTURE    = 11,
  D3DSAMP_ELEMENTINDEX   = 12,
  D3DSAMP_DMAPOFFSET     = 13,
  D3DSAMP_FORCE_DWORD    = 0x7fffffff
} D3DSAMPLERSTATETYPE, *LPD3DSAMPLERSTATETYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DSAMP_ADDRESSU"></span><span id="d3dsamp_addressu"></span>**\_Adresse D3DSAMP**
</dt> <dd>

Texture-mode d’adresse pour la coordonnée u. La valeur par défaut est D3DTADDRESS \_ Wrap. Pour plus d’informations, consultez [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).

</dd> <dt>

<span id="D3DSAMP_ADDRESSV"></span><span id="d3dsamp_addressv"></span>**D3DSAMP \_ ADDRESSV**
</dt> <dd>

Texture-mode d’adresse pour la coordonnée v. La valeur par défaut est D3DTADDRESS \_ Wrap. Pour plus d’informations, consultez [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).

</dd> <dt>

<span id="D3DSAMP_ADDRESSW"></span><span id="d3dsamp_addressw"></span>**D3DSAMP \_ ADDRESSW**
</dt> <dd>

Texture-mode d’adresse pour la coordonnée w. La valeur par défaut est D3DTADDRESS \_ Wrap. Pour plus d’informations, consultez [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).

</dd> <dt>

<span id="D3DSAMP_BORDERCOLOR"></span><span id="d3dsamp_bordercolor"></span>**D3DSAMP \_ BORDERCOLOR**
</dt> <dd>

Couleur de la bordure ou [**D3DCOLOR**](d3dcolor.md)de type. La couleur par défaut est 0x00000000.

</dd> <dt>

<span id="D3DSAMP_MAGFILTER"></span><span id="d3dsamp_magfilter"></span>**D3DSAMP \_ MAGFILTER**
</dt> <dd>

Filtre d’agrandissement de type [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md). La valeur par défaut est D3DTEXF \_ point.

</dd> <dt>

<span id="D3DSAMP_MINFILTER"></span><span id="d3dsamp_minfilter"></span>**D3DSAMP \_ MINFILTER**
</dt> <dd>

Filtre de minimisation de type [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md). La valeur par défaut est D3DTEXF \_ point.

</dd> <dt>

<span id="D3DSAMP_MIPFILTER"></span><span id="d3dsamp_mipfilter"></span>**D3DSAMP \_ MIPFILTER**
</dt> <dd>

Filtre mipmap à utiliser pendant la minimisation. Consultez [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md). La valeur par défaut est D3DTEXF \_ None.

</dd> <dt>

<span id="D3DSAMP_MIPMAPLODBIAS"></span><span id="d3dsamp_mipmaplodbias"></span>**D3DSAMP \_ MIPMAPLODBIAS**
</dt> <dd>

Biais du niveau de détail mipmap. La valeur par défaut est zéro.

</dd> <dt>

<span id="D3DSAMP_MAXMIPLEVEL"></span><span id="d3dsamp_maxmiplevel"></span>**D3DSAMP \_ MAXMIPLEVEL**
</dt> <dd>

index de niveau de détail du mappage le plus grand à utiliser. Les valeurs sont comprises entre 0 et (n-1), 0 étant le plus grand. La valeur par défaut est zéro.

</dd> <dt>

<span id="D3DSAMP_MAXANISOTROPY"></span><span id="d3dsamp_maxanisotropy"></span>**D3DSAMP \_ MAXANISOTROPY**
</dt> <dd>

Anisotropie maximale DWORD. Les valeurs sont comprises entre 1 et la valeur spécifiée dans le membre **MaxAnisotropy** de la structure [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) . La valeur par défaut est 1.

</dd> <dt>

<span id="D3DSAMP_SRGBTEXTURE"></span><span id="d3dsamp_srgbtexture"></span>**D3DSAMP \_ SRGBTEXTURE**
</dt> <dd>

Valeur de correction gamma. La valeur par défaut est 0, ce qui signifie que gamma est 1,0 et qu’aucune correction n’est requise. Dans le cas contraire, cette valeur signifie que l’échantillonneur doit supposer la valeur gamma de 2,2 sur le contenu et le convertir en linéaire (gamma 1,0) avant de le présenter au nuanceur de pixels.

</dd> <dt>

<span id="D3DSAMP_ELEMENTINDEX"></span><span id="d3dsamp_elementindex"></span>**D3DSAMP \_ ELEMENTINDEX**
</dt> <dd>

Quand une texture multiélément est assignée à l’échantillonneur, cela indique l’index d’élément à utiliser. La valeur par défaut est 0.

</dd> <dt>

<span id="D3DSAMP_DMAPOFFSET"></span><span id="d3dsamp_dmapoffset"></span>**D3DSAMP \_ DMAPOFFSET**
</dt> <dd>

Décalage du vertex dans le mappage de déplacement prééchantillonné. Il s’agit d’une constante utilisée par du paveur, sa valeur par défaut est 0.

</dd> <dt>

<span id="D3DSAMP_FORCE_DWORD"></span><span id="d3dsamp_force_dword"></span>**D3DSAMP \_ forcer \_ DWORD**
</dt> <dd>

Force cette énumération à se compiler à 32 bits de taille. Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits. Cette valeur n'est pas utilisée.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 
