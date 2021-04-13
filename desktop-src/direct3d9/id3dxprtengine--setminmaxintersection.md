---
description: Définit les distances minimale et maximale de l’intersection entre les objets 3D.
ms.assetid: da825c70-0c55-4303-b78a-a761ba037182
title: 'ID3DXPRTEngine :: SetMinMaxIntersection, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetMinMaxIntersection
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 68845f713289c524afc844037ca305909e5b89b0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323037"
---
# <a name="id3dxprtenginesetminmaxintersection-method"></a>ID3DXPRTEngine :: SetMinMaxIntersection, méthode

Définit les distances minimale et maximale de l’intersection entre les objets 3D. Ces valeurs de distance peuvent être utilisées pour contrôler la distance minimale ou maximale que les objets peuvent ombrer ou pour refléter la lumière. Par exemple, la méthode peut être utilisée pour limiter l’occultation des fonctionnalités avoisinantes d’un modèle 3D.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetMinMaxIntersection(
  [in] FLOAT fMin ,
  [in] FLOAT fMax
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*fmin,* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Distance d’intersection minimale. Doit être positif et inférieur à fMax.

</dd> <dt>

*Fmax* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Distance d’intersection maximale. Si 0.0 f, la valeur précédente est utilisée ; Sinon, doit être supérieur à fmin,.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Notes

Cette méthode ne peut pas être utilisée dans les simulations de transfert luminance (PRT) précalculées qui s’exécutent dans le GPU. Consultez [**ID3DXPRTEngine :: ComputeDirectLightingSHGPU**](id3dxprtengine--computedirectlightingshgpu.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
