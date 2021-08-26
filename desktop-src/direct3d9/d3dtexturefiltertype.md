---
description: Définit les modes de filtrage de texture pour une étape de texture.
ms.assetid: 4e0420fa-ac76-4be4-90d7-944d8d5a5de1
title: Énumération D3DTEXTUREFILTERTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTUREFILTERTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: a9a55632ee1f1b8f2e40b1be1272411c7c24b3b18c576563ff9c0de7c79bc413
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069369"
---
# <a name="d3dtexturefiltertype-enumeration"></a>Énumération D3DTEXTUREFILTERTYPE

Définit les modes de filtrage de texture pour une étape de texture.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum D3DTEXTUREFILTERTYPE { 
  D3DTEXF_NONE             = 0,
  D3DTEXF_POINT            = 1,
  D3DTEXF_LINEAR           = 2,
  D3DTEXF_ANISOTROPIC      = 3,
  D3DTEXF_PYRAMIDALQUAD    = 6,
  D3DTEXF_GAUSSIANQUAD     = 7,
  D3DTEXF_CONVOLUTIONMONO  = 8,
  D3DTEXF_FORCE_DWORD      = 0x7fffffff
} D3DTEXTUREFILTERTYPE, *LPD3DTEXTUREFILTERTYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DTEXF_NONE"></span><span id="d3dtexf_none"></span>**D3DTEXF \_ aucun**
</dt> <dd>

En cas d’utilisation avec [**D3DSAMP \_ MIPFILTER**](./d3dsamplerstatetype.md), désactive mappage MIP.

</dd> <dt>

<span id="D3DTEXF_POINT"></span><span id="d3dtexf_point"></span>**\_Point D3DTEXF**
</dt> <dd>

Lorsqu’il est utilisé avec [**D3DSAMP \_ MAGFILTER**](./d3dsamplerstatetype.md) ou [**D3DSAMP \_ MINFILTER**](./d3dsamplerstatetype.md), spécifie que le filtrage de point doit être utilisé comme facteur d’agrandissement ou de réduction de la texture, respectivement. En cas d’utilisation avec **D3DSAMP \_ MIPFILTER**, active mappage MIP et spécifie que le rastériseur choisit la couleur à partir de la texture du niveau MIP le plus proche.

</dd> <dt>

<span id="D3DTEXF_LINEAR"></span><span id="d3dtexf_linear"></span>**D3DTEXF \_ linéaire**
</dt> <dd>

Lorsqu’il est utilisé avec [**D3DSAMP \_ MAGFILTER**](./d3dsamplerstatetype.md) ou [**D3DSAMP \_ MINFILTER**](./d3dsamplerstatetype.md), spécifie que le filtrage linéaire doit être utilisé en tant que facteur d’agrandissement de texture ou de filtre de réduction, respectivement. En cas d’utilisation avec **D3DSAMP \_ MIPFILTER**, active le filtrage mappage MIP et trilinéaire ; il spécifie que le rastériseur interpole entre les deux niveaux les plus proches.

</dd> <dt>

<span id="D3DTEXF_ANISOTROPIC"></span><span id="d3dtexf_anisotropic"></span>**D3DTEXF \_ anisotrope**
</dt> <dd>

Lorsqu’il est utilisé avec [**D3DSAMP \_ MAGFILTER**](./d3dsamplerstatetype.md) ou [**D3DSAMP \_ MINFILTER**](./d3dsamplerstatetype.md), spécifie que le filtrage de texture anisotrope est utilisé respectivement comme un facteur d’agrandissement de texture ou de réduction. Compense la distorsion causée par la différence d’angle entre le polygone de texture et le plan de l’écran. L’utilisation de avec **D3DSAMP \_ MIPFILTER** n’est pas définie.

</dd> <dt>

<span id="D3DTEXF_PYRAMIDALQUAD"></span><span id="d3dtexf_pyramidalquad"></span>**D3DTEXF \_ PYRAMIDALQUAD**
</dt> <dd>

Filtre chevalet à 4 échantillons utilisé comme un zoom de texture ou un filtre de réduction. L’utilisation de avec [**D3DSAMP \_ MIPFILTER**](./d3dsamplerstatetype.md) n’est pas définie.

</dd> <dt>

<span id="D3DTEXF_GAUSSIANQUAD"></span><span id="d3dtexf_gaussianquad"></span>**D3DTEXF \_ GAUSSIANQUAD**
</dt> <dd>

Filtre gaussien à 4 échantillons utilisé comme un agrandissement de texture ou un filtre de réduction. L’utilisation de avec [**D3DSAMP \_ MIPFILTER**](./d3dsamplerstatetype.md) n’est pas définie.

</dd> <dt>

<span id="D3DTEXF_CONVOLUTIONMONO"></span><span id="d3dtexf_convolutionmono"></span>**D3DTEXF \_ CONVOLUTIONMONO**
</dt> <dd>

Filtre de convolution pour les textures monochromes. Consultez [D3DFMT \_ a1](d3dformat.md).

Différences entre Direct3D 9 et Direct3D 9Ex :

- Cet indicateur est disponible uniquement dans Direct3D 9Ex.



 

L’utilisation de avec [**D3DSAMP \_ MIPFILTER**](./d3dsamplerstatetype.md) n’est pas définie.

</dd> <dt>

<span id="D3DTEXF_FORCE_DWORD"></span><span id="d3dtexf_force_dword"></span>**D3DTEXF \_ forcer \_ DWORD**
</dt> <dd>

Force cette énumération à se compiler à 32 bits de taille. Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits. Cette valeur n'est pas utilisée.

</dd> </dl>

## <a name="remarks"></a>Remarques

D3DTEXTUREFILTERTYPE est utilisé par [**IDirect3DDevice9 :: SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) avec [**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md) pour définir les modes de filtrage de texture pour une étape de texture.

Pour vérifier si un format prend en charge d’autres types de filtre de texture que \_ le point de D3DTEXF (qui est toujours pris en charge), appelez [**IDirect3D9 :: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) avec le \_ filtre de requête D3DUSAGE \_ .

Définissez le filtre d’agrandissement d’une étape de texture en appelant [**IDirect3DDevice9 :: SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) avec la \_ valeur MAGFILTER D3DSAMP comme deuxième paramètre et un membre de cette énumération comme troisième paramètre.

Définissez le filtre de réduction d’une étape de texture en appelant [**IDirect3DDevice9 :: SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) avec la \_ valeur MINFILTER D3DSAMP comme deuxième paramètre et un membre de cette énumération comme troisième paramètre.

Définissez le filtre de texture à utiliser entre les niveaux de mipmap en appelant [**IDirect3DDevice9 :: SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) avec la \_ valeur MIPFILTER D3DSAMP comme deuxième paramètre et un membre de cette énumération comme troisième paramètre.

Tous les modes de filtrage valides pour un appareil ne s’appliquent pas aux mappages de volume. En général, \_ \_ les filtres d’agrandissement linéaire D3DTEXF point et D3DTEXF sont pris en charge pour les mappages de volume. Si D3DPTEXTURECAPS \_ MIPVOLUMEMAP est défini, le \_ filtre MIPMAP point D3DTEXF et le \_ point D3DTEXF et les \_ filtres de minimisation linéaire D3DTEXF sont pris en charge pour les mappages de volume. L’appareil peut ou non prendre en charge le \_ filtre mipmap linéaire D3DTEXF pour les mappages de volume. Les appareils qui prennent en charge le filtrage anisotrope pour les mappages 2D ne prennent pas nécessairement en charge le filtrage anisotrope pour les mappages de volume. Toutefois, les applications qui activent le filtrage anisotrope recevront le meilleur filtrage disponible (probablement linéaire) si le filtrage anisotrope n’est pas pris en charge.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**ID3DXPatchMesh::GetDisplaceParam**](id3dxpatchmesh--getdisplaceparam.md)
</dt> <dt>

[**ID3DXPatchMesh::SetDisplaceParam**](id3dxpatchmesh--setdisplaceparam.md)
</dt> <dt>

[**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md)
</dt> <dt>

[**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate)
</dt> </dl>

 

 
