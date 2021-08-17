---
title: D3DX11ComputeNormalMap, fonction (D3DX11tex. h)
description: 'remarque : la bibliothèque de l’utilitaire d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store. Notez qu’au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser la bibliothèque DirectXTex, ComputeNormalMap.'
ms.assetid: 3ccdbd9a-669e-48ff-97d5-e5a6c7d2fb26
keywords:
- Fonction D3DX11ComputeNormalMap Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11ComputeNormalMap
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 747b8b01834126beb12e42d2fa26e15ea99c7471935af8ad74d078d15e9233ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124914"
---
# <a name="d3dx11computenormalmap-function"></a>D3DX11ComputeNormalMap fonction)

> [!Note]  
> la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store.

 

> [!Note]  
> Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser la bibliothèque [DirectXTex](https://github.com/Microsoft/DirectXTex) , **ComputeNormalMap**.

 

Convertit une carte de hauteur en une carte normale. Les composants (x, y, z) de chaque normal sont mappés aux canaux (r, g, b) de la texture de sortie.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DX11ComputeNormalMap(
  _In_ ID3D11DeviceContext *pContext,
  _In_ ID3D11Texture2D     *pSrcTexture,
  _In_ UINT                Flags,
  _In_ UINT                Channel,
  _In_ FLOAT               Amplitude,
  _In_ ID3D11Texture2D     *pDestTexture
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pContext* \[ dans\]
</dt> <dd>

Type : **[ **ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***

Pointeur vers une interface [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) représentant la texture de la carte de hauteur source.

</dd> <dt>

*pSrcTexture* \[ dans\]
</dt> <dd>

Type : **[ **ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***

Pointeur vers une interface [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) représentant la texture de la carte de hauteur source.

</dd> <dt>

*Indicateurs* \[ dans\]
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Un ou plusieurs \_ indicateurs D3DX NORMALMAP qui contrôlent la génération de mappages normaux.

</dd> <dt>

*Chaîne* \[ dans\]
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Un \_ indicateur de canal D3DX spécifiant la source des informations de hauteur.

</dd> <dt>

*Amplitude* \[ dans\]
</dt> <dd>

Type : **[ **float**](/windows/desktop/WinProg/windows-data-types)**

Multiplicateur de valeur constante qui augmente (ou diminue) les valeurs dans la carte normale. Les valeurs plus élevées rendent généralement les bosses plus visibles, les valeurs basses rendent généralement les rugosités moins visibles.

</dd> <dt>

*pDestTexture* \[ dans\]
</dt> <dd>

Type : **[ **ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***

Pointeur vers une interface [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) représentant la texture de destination.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être la valeur suivante : D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Remarques

Cette méthode calcule le normal à l’aide de la différence centrale avec une taille de noyau de 3 x 3. Les canaux RVB dans la destination contiennent des composants (x, y, z) biaisés de la normale. Le dénominateur de différenciation central est codé en dur sur 2,0.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX11tex. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3DX11. lib</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[D3DX, fonctions](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

