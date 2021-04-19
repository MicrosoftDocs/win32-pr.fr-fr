---
description: Calcule une projection d’éclairage distant dans des vecteurs d’harmoniques sphériques (SH) qui représentent des luminance d’incident aux emplacements spécifiés.
ms.assetid: 4d07b288-aec1-48eb-8d27-f3d7d8cfb69e
title: 'ID3DXPRTEngine :: ComputeVolumeSamplesDirectSH, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeVolumeSamplesDirectSH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 757e227907eab73848f43b2b8e2f40f9b4b1071b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106529631"
---
# <a name="id3dxprtenginecomputevolumesamplesdirectsh-method"></a>ID3DXPRTEngine :: ComputeVolumeSamplesDirectSH, méthode

Calcule une projection d’éclairage distant dans des vecteurs d’harmoniques sphériques (SH) qui représentent des luminance d’incident aux emplacements spécifiés.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ComputeVolumeSamplesDirectSH(
  [in]            UINT            OrderIn,
  [in]            UINT            OrderOut,
  [in]            UINT            NumVolSamples.xml,
  [in]      const D3DXVECTOR3     *pSampleLocs,
  [in, out]       LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Ordre de tri* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Ordre de la représentation SH de l’éclairage distant. La valeur doit être comprise entre [D3DXSH \_ MINORDER](other-d3dx-constants.md) et D3DXSH \_ MAXORDER, inclus. Le degré de l’évaluation est Order in-1.

</dd> <dt>

*OrderOut* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Ordre de la représentation SH de l’éclairage local. La valeur doit être comprise entre [D3DXSH \_ MINORDER](other-d3dx-constants.md) et D3DXSH \_ MAXORDER, inclus. Le degré de l’évaluation est OrderOut-1.

</dd> <dt>

*NumVolSamples.xml* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre d’emplacements d’échantillonnage.

</dd> <dt>

*pSampleLocs* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Position pour chaque exemple.

</dd> <dt>

*pDataOut* \[ in, out\]
</dt> <dd>

Type : **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Pointeur vers un objet [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de sortie qui projette l’éclairage distant dans les vecteurs de base sh. Cette mémoire tampon doit avoir le nombre approprié de canaux de couleur alloués pour la simulation. Cette méthode génère l’ordre des \* OrderOut ² «² scalaires par canal à chaque emplacement d’échantillonnage.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Notes

Cette méthode calcule la lumière d’une source distante arrivant à chaque point dans l’espace spécifié par pSampleLocs. Les coefficients SH représentent le mappage, à chaque point de pSampleLocs, du luminance source au luminance de l’incident transféré.

Pour utiliser cette méthode avec succès, vous devez définir l’échantillonnage sur une sphère avec UseSphere = **true** et UseCosine = **false** dans [**ID3DXPRTEngine :: SetSamplingInfo**](id3dxprtengine--setsamplinginfo.md); Sinon, cette méthode retourne une erreur avec D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::ComputeVolumeSamples**](id3dxprtengine--computevolumesamples.md)
</dt> </dl>

 

 
