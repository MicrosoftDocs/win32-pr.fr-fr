---
description: Sous-divise les visages sur une maille, ce qui permet un échantillonnage adaptatif prudent qui n’élimine pas les caractéristiques de la maille.
ms.assetid: 0d74a01a-de67-4607-99eb-ed98e239f199
title: 'ID3DXPRTEngine :: RobustMeshRefine, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.RobustMeshRefine
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 65d49fcec3072956365ce1ed8dc5d7a11ce6c826
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918348"
---
# <a name="id3dxprtenginerobustmeshrefine-method"></a>ID3DXPRTEngine :: RobustMeshRefine, méthode

Sous-divise les visages sur une maille, ce qui permet un échantillonnage adaptatif prudent qui n’élimine pas les caractéristiques de la maille.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT RobustMeshRefine(
  [in] FLOAT MinEdgeLength,
  [in] UINT  MaxSubdiv
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*MinEdgeLength* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Longueur minimale du bord de face qui sera générée dans l’échantillonnage adaptatif. Si la valeur est zéro, une valeur par défaut raisonnable est remplacée.

</dd> <dt>

*MaxSubdiv* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Niveau maximal de subdivision d’un visage qui sera utilisé dans l’échantillonnage adaptatif. Si la valeur est zéro, la valeur par défaut 5 est remplacée.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::ComputeBounceAdaptive**](id3dxprtengine--computebounceadaptive.md)
</dt> <dt>

[**ID3DXPRTEngine::ComputeDirectLightingSHAdaptive**](id3dxprtengine--computedirectlightingshadaptive.md)
</dt> </dl>

 

 
