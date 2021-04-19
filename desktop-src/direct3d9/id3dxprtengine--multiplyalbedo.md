---
description: Multiplie chaque vecteur de transfert luminance (PRT) précalculé par le Albedo par vertex.
ms.assetid: 2b3e4b19-7778-4240-ac79-3237fda2ed96
title: 'ID3DXPRTEngine :: MultiplyAlbedo, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.MultiplyAlbedo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a282605789644382f39fd8fff9ce8bb47d6dfc7d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106524876"
---
# <a name="id3dxprtenginemultiplyalbedo-method"></a>ID3DXPRTEngine :: MultiplyAlbedo, méthode

Multiplie chaque vecteur de transfert luminance (PRT) précalculé par le Albedo par vertex.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT MultiplyAlbedo(
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDataOut* \[ in, out\]
</dt> <dd>

Type : **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Pointeur vers un objet [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de sortie qui contiendra les VECTEURs PRT multipliés par le Albedo par vertex. Si cette mémoire tampon de sortie est un objet de texture, vous devez veiller à stocker le albedo de la texture à la même résolution que la mémoire tampon de simulation. Vous pouvez définir la résolution appropriée sur le Albedo avec [**D3DXLoadSurfaceFromSurface**](d3dxloadsurfacefromsurface.md), en appliquant les zones de marge de texture, le cas échéant.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Notes

Les méthodes ID3DXPRTEngine :: Computexxx calculent les mémoires tampons de sortie dans lesquelles le signal lumineux n’a pas été multiplié par Albedo. En ne multipliant pas Albedo, vous pouvez modéliser la variation Albedo à une échelle plus fine que le luminance source, ce qui donne des résultats plus précis de la compression.

Pour inclure Albedo dans le modèle de lumière rendue, appelez cette méthode après l’une des méthodes Computexxx.

[**ID3DXPRTEngine :: SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md) doit être appelé avant d’appeler cette méthode.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::ComputeDirectLightingSH**](id3dxprtengine--computedirectlightingsh.md)
</dt> </dl>

 

 




