---
description: Utilise l’efficacité du traçage de rayon dans les simulations de transfert luminance (PRT) précalculées pour déterminer si un rayon croise une maille. Généralement utilisé pour déterminer si un point donné se trouve dans une ombre.
ms.assetid: fcd53a0f-80e8-4013-8efd-125e38f4ccd0
title: 'ID3DXPRTEngine :: ShadowRayIntersects, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ShadowRayIntersects
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 701aa4c89ee6a9d657721d872565c9b2056bb435
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104043125"
---
# <a name="id3dxprtengineshadowrayintersects-method"></a>ID3DXPRTEngine :: ShadowRayIntersects, méthode

Utilise l’efficacité du traçage de rayon dans les simulations de transfert luminance (PRT) précalculées pour déterminer si un rayon croise une maille. Généralement utilisé pour déterminer si un point donné se trouve dans une ombre.

## <a name="syntax"></a>Syntaxe


```C++
BOOL ShadowRayIntersects(
  [in] const D3DXVECTOR3 *pRayPos,
  [in] const D3DXVECTOR3 *pRayDir
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pRayPos* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) , en spécifiant le point de départ du rayon.

</dd> <dt>

*pRayDir* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) , en spécifiant la direction normalisée du rayon.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **bool**](../winprog/windows-data-types.md)**

Retourne la **valeur true** si le rayon croise le maillage actuel ; Sinon, retourne **false**.

## <a name="remarks"></a>Notes

Utilisez [**ID3DXPRTEngine :: SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md) pour définir les distances minimale et maximale de l’intersection avec le rayon.

Cette méthode s’exécute plus rapidement que [**ID3DXPRTEngine :: ClosestRayIntersects**](id3dxprtengine--closestrayintersects.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::ClosestRayIntersects**](id3dxprtengine--closestrayintersects.md)
</dt> <dt>

[**ID3DXPRTEngine::SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md)
</dt> </dl>

 

 
