---
description: Charge une texture à partir d’une texture.
ms.assetid: 126e71e1-a3b2-418b-be35-434a2e9472ca
title: D3DX10LoadTextureFromTexture, fonction (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10LoadTextureFromTexture
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: bfc36423154bfd56f0695a3a8178b89aefce6e4dfc5a67f3866fa13a99c5e6d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990499"
---
# <a name="d3dx10loadtexturefromtexture-function"></a>D3DX10LoadTextureFromTexture fonction)

Charge une texture à partir d’une texture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DX10LoadTextureFromTexture(
   ID3D10Resource           *pSrcTexture,
   D3DX10_TEXTURE_LOAD_INFO *pLoadInfo,
   ID3D10Resource           *pDstTexture
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSrcTexture* 
</dt> <dd>

Type : **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***

Pointeur vers la texture source. Consultez [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).

</dd> <dt>

*pLoadInfo* 
</dt> <dd>

Type : **[ **d3dx10 \_ texture \_ load \_ info**](d3dx10-texture-load-info.md)\***

Pointeur vers les paramètres de chargement de texture. Consultez [**d3dx10 \_ texture \_ load \_ info**](d3dx10-texture-load-info.md).

</dd> <dt>

*pDstTexture* 
</dt> <dd>

Type : **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***

Pointeur vers la texture de destination. Voir [**interface ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3DX10Tex. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de texture dans D3DX 10](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 




