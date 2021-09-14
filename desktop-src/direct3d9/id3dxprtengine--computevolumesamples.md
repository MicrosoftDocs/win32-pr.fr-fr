---
description: Calcule une projection de l’éclairage direct de la lumière précédente dans les vecteurs de base d’harmoniques sphériques (SH) qui représentent des luminance d’incident aux emplacements spécifiés.
ms.assetid: ccde7c59-cb82-4d61-822a-e1e9ecea0a28
title: 'ID3DXPRTEngine :: ComputeVolumeSamples, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeVolumeSamples
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bd77fff723f0cf7e3dc2a52be6a40ff6f0d71fe1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127292683"
---
# <a name="id3dxprtenginecomputevolumesamples-method"></a>ID3DXPRTEngine :: ComputeVolumeSamples, méthode

Calcule une projection de l’éclairage direct de la lumière précédente dans les vecteurs de base d’harmoniques sphériques (SH) qui représentent des luminance d’incident aux emplacements spécifiés.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ComputeVolumeSamples(
  [in]            LPD3DXPRTBUFFER pSurfDataIn,
  [in]            UINT            Order,
  [in]            UINT            NumVolSamples.xml,
  [in]      const D3DXVECTOR3     *pSampleLocs,
  [in, out]       LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSurfDataIn* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Pointeur vers un objet [**ID3DXPRTBuffer**](id3dxprtbuffer.md) d’entrée qui représente l’objet 3D du retour de lumière précédent.

</dd> <dt>

*Commande* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Ordre de l’évaluation SH. La valeur doit être comprise entre [D3DXSH \_ MINORDER](other-d3dx-constants.md) et D3DXSH \_ MAXORDER, inclus. L’évaluation génère des coefficients de commande ². Le degré de l’évaluation est Order-1.

</dd> <dt>

*NumVolSamples.xml* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre d’emplacements d’échantillonnage.

</dd> <dt>

*pSampleLocs* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Position pour chaque exemple. Si pSampleLocs a la **valeur null**, ComputeVolumeSamples calcule les matrices de transfert à chaque vertex de maillage. Toutefois, si pSampleLocs n’a pas la **valeur null**, vous devez échantillonner une sphère (Set UseSphere = **true** et UseCosine = **false** dans [**ID3DXPRTEngine :: SetSamplingInfo**](id3dxprtengine--setsamplinginfo.md)); Sinon, ComputeVolumeSamples retourne D3DERR \_ INVALIDCALL.

</dd> <dt>

*pDataOut* \[ in, out\]
</dt> <dd>

Type : **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Pointeur vers un objet [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de sortie qui projette l’éclairage direct de la lumière précédente Bounce dans les vecteurs de base sh. Cette mémoire tampon doit avoir le nombre approprié de canaux de couleur alloués pour la simulation.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Notes

Cette méthode calcule la façon dont la lumière de la fonction luminance source est réfléchie à partir de la surface qui représente la scène (pSurfDataIn) et arrive à chaque point dans l’espace spécifié par pSampleLocs. Les coefficients SH représentent le mappage, à chaque point de pSampleLocs, du luminance source au luminance de l’incident transféré.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::ComputeVolumeSamplesDirectSH**](id3dxprtengine--computevolumesamplesdirectsh.md)
</dt> </dl>

 

 
