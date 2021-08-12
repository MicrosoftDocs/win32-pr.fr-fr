---
description: Décrit une surface.
ms.assetid: fad8ffdb-36e5-4695-b343-e1315357c31a
title: Structure D3DSURFACE_DESC (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSURFACE_DESC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: b18c9cd3428463f82a6e243a57ade3fffd650bb35f2c73234b725fa5bf0607eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118300231"
---
# <a name="d3dsurface_desc-structure"></a>D3DSURFACE \_ desc, structure

Décrit une surface.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DSURFACE_DESC {
  D3DFORMAT           Format;
  D3DRESOURCETYPE     Type;
  DWORD               Usage;
  D3DPOOL             Pool;
  D3DMULTISAMPLE_TYPE MultiSampleType;
  DWORD               MultiSampleQuality;
  UINT                Width;
  UINT                Height;
} D3DSURFACE_DESC, *LPD3DSURFACE_DESC;
```



## <a name="members"></a>Membres

<dl> <dt>

**Format**
</dt> <dd>

Type : **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Membre du type énuméré [D3DFORMAT](d3dformat.md) , décrivant le format de surface.

</dd> <dt>

**Type**
</dt> <dd>

Type : **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**

</dd> <dd>

Membre du type énuméré [**D3DRESOURCETYPE**](./d3dresourcetype.md) , identifiant cette ressource comme une surface.

</dd> <dt>

**Utilisation**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

\_Valeurs D3DUSAGE DEPTHSTENCIL ou D3DUSAGE \_ RENDERTARGET. Pour plus d’informations, consultez [**D3DUSAGE**](d3dusage.md).

</dd> <dt>

**Pool**
</dt> <dd>

Type : **[ **D3DPOOL**](./d3dpool.md)**

</dd> <dd>

Membre du type énuméré [**D3DPOOL**](./d3dpool.md) , spécifiant la classe de mémoire allouée pour cette surface.

</dd> <dt>

**MultiSampleType**
</dt> <dd>

Type : **[ **D3DMULTISAMPLE \_**](./d3dmultisample-type.md)**

</dd> <dd>

Membre du type [**énuméré \_ D3DMULTISAMPLE**](./d3dmultisample-type.md) , en spécifiant les niveaux d’échantillonnage multiple de la scène intégrale pris en charge par l’aire.

</dd> <dt>

**MultiSampleQuality**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Niveau de qualité. La plage valide est comprise entre zéro et un de moins que le niveau retourné par pQualityLevels utilisé par [**CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype). La transmission d’une valeur supérieure retourne l’erreur D3DERR \_ INVALIDCALL. Les valeurs MultisampleQuality des cibles de rendu jumelées, des surfaces du stencil de profondeur et du type d’échantillonnage multigraphique doivent toutes correspondre.

</dd> <dt>

**Width**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Largeur de la surface, en pixels.

</dd> <dt>

**Height**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Hauteur de la surface, en pixels.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetLevelDesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getleveldesc)
</dt> <dt>

[**GetDesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-getdesc)
</dt> <dt>

[**GetLevelDesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getleveldesc)
</dt> </dl>

 

 
