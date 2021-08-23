---
description: Ajoute une sortie d’animation au contrôleur d’animation et enregistre les pointeurs pour les transformations de mise à l’échelle, de rotation et de translation (SRT).
ms.assetid: 8c3197bc-9d03-40ba-869b-151f9c8e96ba
title: 'ID3DXAnimationController :: RegisterAnimationOutput, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.RegisterAnimationOutput
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: dc48eb9f2fd6ee5fee6c04936801997145a5ea21542b9b5ff8ec6d257eee80e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987819"
---
# <a name="id3dxanimationcontrollerregisteranimationoutput-method"></a>ID3DXAnimationController :: RegisterAnimationOutput, méthode

Ajoute une sortie d’animation au contrôleur d’animation et enregistre les pointeurs pour les transformations de mise à l’échelle, de rotation et de translation (SRT).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT RegisterAnimationOutput(
  [in] LPCSTR         Name,
  [in] D3DXMATRIX     *pMatrix,
  [in] D3DXVECTOR3    *pScale,
  [in] D3DXQUATERNION *pRotation,
  [in] D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Nom* \[ dans\]
</dt> <dd>

Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**

Nom de la sortie de l’animation.

</dd> <dt>

*pMatrix* \[ dans\]
</dt> <dd>

Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Pointeur vers une structure [**D3DXMATRIX**](d3dxmatrix.md) contenant les données de transformation SRT. Peut avoir la **valeur null**.

</dd> <dt>

*pScale* \[ dans\]
</dt> <dd>

Type : **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Pointeur vers un vecteur [**D3DXVECTOR3**](d3dxvector3.md) qui décrit l’échelle de l’ensemble d’animations. Peut avoir la **valeur null**.

</dd> <dt>

*protique* \[ dans\]
</dt> <dd>

Type : **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Pointeur vers un Quaternion [**D3DXQUATERNION**](d3dxquaternion.md) qui décrit la rotation de l’ensemble d’animations. Peut avoir la **valeur null**.

</dd> <dt>

*pTranslation* \[ dans\]
</dt> <dd>

Type : **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Pointeur vers un vecteur [**D3DXVECTOR3**](d3dxvector3.md) qui décrit la traduction de l’ensemble d’animations. Peut avoir la **valeur null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des valeurs suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarques

Si la sortie de l’animation est déjà inscrite, pMatrix est rempli avec les données de transformation d’entrée.

Les jeux d’animations créés avec [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) inscrivent automatiquement tous les jeux d’animations chargés.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
