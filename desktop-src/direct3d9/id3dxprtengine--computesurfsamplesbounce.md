---
description: Calcule les exemples de transfert luminance (PRT) précalculés pour un point arbitraire (et vecteur normal).
ms.assetid: 862a9067-5c5e-4428-86f4-ebef653411b9
title: 'ID3DXPRTEngine :: ComputeSurfSamplesBounce, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeSurfSamplesBounce
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 55cea3e87850273b6ea8d190422bd77afeb831f4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127520749"
---
# <a name="id3dxprtenginecomputesurfsamplesbounce-method"></a>ID3DXPRTEngine :: ComputeSurfSamplesBounce, méthode

Calcule les exemples de transfert luminance (PRT) précalculés pour un point arbitraire (et vecteur normal).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ComputeSurfSamplesBounce(
  [in]            LPD3DXPRTBUFFER pSurfDataIn,
  [in]            UINT            NumSamples,
  [in]      const D3DXVECTOR3     *pSampleLocs,
  [in]      const D3DXVECTOR3     *pSampleNorms,
  [in, out]       LPD3DXPRTBUFFER pDataOut,
  [in, out]       LPD3DXPRTBUFFER pDataTotal
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSurfDataIn* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Pointeur vers un objet [**ID3DXPRTBuffer**](id3dxprtbuffer.md) d’entrée qui représente le luminance source de l’objet 3D. Cette mémoire tampon d’entrée doit avoir le nombre approprié de canaux de couleur alloués pour la simulation.

</dd> <dt>

*Échantillons* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre d’emplacements d’échantillonnage.

</dd> <dt>

*pSampleLocs* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Position pour chaque exemple.

</dd> <dt>

*pSampleNorms* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Vecteur normal pour chaque exemple d’emplacement.

</dd> <dt>

*pDataOut* \[ in, out\]
</dt> <dd>

Type : **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Pointeur vers un objet [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de sortie qui modélise la contribution de l’éclairage direct au point, à l’aide de la approximation de l’harmonique sphérique (SH).

</dd> <dt>

*pDataTotal* \[ in, out\]
</dt> <dd>

Type : **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Pointeur vers un objet [**ID3DXPRTBuffer**](id3dxprtbuffer.md) facultatif qui est la somme cumulée de toutes les sorties pDataOut précédentes. Peut avoir la **valeur null**.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::ComputeSurfSamplesDirectSH**](id3dxprtengine--computesurfsamplesdirectsh.md)
</dt> </dl>

 

 
