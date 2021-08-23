---
description: Générez une liste de bords de maillage et les correctifs qui partagent chaque périphérie.
ms.assetid: 024528c0-2c0d-4448-9b38-05cf8d6ffc63
title: 'ID3DXPatchMesh :: GenerateAdjacency, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GenerateAdjacency
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 41e821d853a8a8f981f1174d654f17475c0363cdcc97bb537e308ccd72e38190
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987199"
---
# <a name="id3dxpatchmeshgenerateadjacency-method"></a>ID3DXPatchMesh :: GenerateAdjacency, méthode

Générez une liste de bords de maillage et les correctifs qui partagent chaque périphérie.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GenerateAdjacency(
  [in] FLOAT fTolerance
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*fTolerance* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Spécifie que les vertex qui diffèrent d’une position inférieure à la tolérance doivent être traités comme coïncidents.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarques

Une fois qu’une application a généré des informations d’adjacence pour une maille, les données de maillage peuvent être optimisées pour améliorer les performances de dessin. Cette méthode détermine les correctifs adjacents (dans la tolérance fournie). Ces informations sont utilisées en interne pour optimiser le pavage.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> <dt>

[**ID3DXPatchMesh :: Optimize**](id3dxpatchmesh--optimize.md)
</dt> </dl>

 

 
