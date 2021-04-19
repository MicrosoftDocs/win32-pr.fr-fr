---
description: Obtient un jeu d’animations en fonction de son nom.
ms.assetid: 4c3f3002-45f6-49b2-8a42-18d5824fb36f
title: 'ID3DXAnimationController :: GetAnimationSetByName, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetAnimationSetByName
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d520625e457a50fe962ae74d6e25fc17e2beb729
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531560"
---
# <a name="id3dxanimationcontrollergetanimationsetbyname-method"></a>ID3DXAnimationController :: GetAnimationSetByName, méthode

Obtient un jeu d’animations en fonction de son nom.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetAnimationSetByName(
  [in]  LPCSTR             pName,
  [out] LPD3DXANIMATIONSET *ppAnimSet
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pname* \[ dans\]
</dt> <dd>

Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**

Chaîne contenant le nom de l’ensemble d’animations.

</dd> <dt>

*ppAnimSet* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)\***

Pointeur vers le jeu d’animations [**ID3DXAnimationSet**](id3dxanimationset.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur suivante est retournée : D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Notes

Le contrôleur d’animation contient un tableau d’ensembles d’animations. Cette méthode retourne un jeu d’animations qui porte le nom donné.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
