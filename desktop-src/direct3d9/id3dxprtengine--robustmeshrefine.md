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
ms.openlocfilehash: 280e4552af6de13995ed81afab4d743232485e92446c72b61fd10ae17fea7b07
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790559"
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

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Configuration requise



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

 

 
