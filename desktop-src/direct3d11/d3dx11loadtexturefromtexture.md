---
title: D3DX11LoadTextureFromTexture, fonction (D3DX11tex. h)
description: 'Remarque : la bibliothèque de l’utilitaire D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store. Notez que, au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser la bibliothèque DirectXTex, redimensionner, convertir, compresser, décompresser et/ou CopyRectangle. Charge une texture à partir d’une texture.'
ms.assetid: 4e673f73-531d-4df8-8542-798e4e70c481
keywords:
- Fonction D3DX11LoadTextureFromTexture Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11LoadTextureFromTexture
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 246429433dea11fddfd4396f3e59677877081592
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974591"
---
# <a name="d3dx11loadtexturefromtexture-function"></a>D3DX11LoadTextureFromTexture fonction)

> [!Note]  
> La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.

 

> [!Note]  
> Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser la bibliothèque [DirectXTex](https://github.com/Microsoft/DirectXTex) , **Redimensionner**, **convertir**, **compresser**, **décompresser** et/ou **CopyRectangle**.

 

Charge une texture à partir d’une texture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DX11LoadTextureFromTexture(
   ID3D11DeviceContext      *pContext,
   ID3D11Resource           *pSrcTexture,
   D3DX11_TEXTURE_LOAD_INFO *pLoadInfo,
   ID3D11Resource           *pDstTexture
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pContext* 
</dt> <dd>

Type : **[ **ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***

Pointeur vers un objet [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .

</dd> <dt>

*pSrcTexture* 
</dt> <dd>

Type : **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***

Pointeur vers la texture source. Consultez [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).

</dd> <dt>

*pLoadInfo* 
</dt> <dd>

Type : **[ **D3DX11 \_ texture \_ load \_ info**](d3dx11-texture-load-info.md)\***

Pointeur vers les paramètres de chargement de texture. Consultez [**D3DX11 \_ texture \_ load \_ info**](d3dx11-texture-load-info.md).

</dd> <dt>

*pDstTexture* 
</dt> <dd>

Type : **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***

Pointeur vers la texture de destination. Consultez [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX11tex. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3DX11. lib</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[D3DX, fonctions](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

 





