---
description: Calcule les coefficients de transfert de luminance précalculés (LDPRT) déformables localement par rapport aux vecteurs normaux par échantillon pour réduire l’erreur des moindres carrés en ce qui concerne les données d’entrée ID3DXPRTBuffer.
ms.assetid: 302c20cd-d495-4a23-9692-7456355471eb
title: 'ID3DXPRTEngine :: ComputeLDPRTCoeffs, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeLDPRTCoeffs
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 351ecb8022e06b1a5a24abad8fa8541798d13ba0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106537288"
---
# <a name="id3dxprtenginecomputeldprtcoeffs-method"></a>ID3DXPRTEngine :: ComputeLDPRTCoeffs, méthode

Calcule les coefficients de transfert de luminance précalculés (LDPRT) déformables localement par rapport aux vecteurs normaux par échantillon pour réduire l’erreur des moindres carrés en ce qui concerne les données d’entrée [**ID3DXPRTBuffer**](id3dxprtbuffer.md) . Ces coefficients peuvent être utilisés avec des vecteurs normaux dépouillés ou transformés pour modéliser les effets globaux sur les objets dynamiques.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ComputeLDPRTCoeffs(
  [in]      LPD3DXPRTBUFFER pDataIn,
  [in]      UINT            Order,
  [in, out] D3DXVECTOR3     *pNormOut,
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDataIn* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Pointeur vers un objet de données d’entrée [**ID3DXPRTBuffer**](id3dxprtbuffer.md) (SH) de transfert d’harmonique sphérique (SH) précalculé (PRT).

</dd> <dt>

*Commande* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Ordre de l’évaluation SH. La valeur doit être comprise entre [D3DXSH \_ MINORDER](other-d3dx-constants.md) et D3DXSH \_ MAXORDER, inclus. L’évaluation génère des coefficients de commande ². Le degré de l’évaluation est Order-1.

</dd> <dt>

*pNormOut* \[ in, out\]
</dt> <dd>

Type : **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Tableau de vecteurs facultatif à remplir avec les vecteurs normaux optimaux pour lesquels les coefficients LDPRT sont optimisés. Ce tableau doit avoir la même taille que le nombre d’exemples dans pDataIn. Si la **valeur est null**, les vecteurs normaux de surface sont utilisés.

</dd> <dt>

*pDataOut* \[ in, out\]
</dt> <dd>

Type : **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Pointeur vers un objet [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de sortie qui contient les coefficients d’harmoniques Zona ordonnés par canal de couleur par échantillon.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Notes

Les solutions pour les vecteurs normaux d’ombrage peuvent éventuellement être obtenues avec cette méthode. Ces vecteurs normaux, ainsi que les coefficients LDPRT, peuvent représenter plus précisément le signal PRT. Dans ce cas, les coefficients représentent les harmoniques zonales orientées dans la direction normale.

Cette méthode ne peut pas être utilisée avec les résultats de [**ID3DXPRTEngine :: ComputeSurfSamplesBounce**](id3dxprtengine--computesurfsamplesbounce.md) ou [**ID3DXPRTEngine :: ComputeSurfSamplesDirectSH**](id3dxprtengine--computesurfsamplesdirectsh.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
