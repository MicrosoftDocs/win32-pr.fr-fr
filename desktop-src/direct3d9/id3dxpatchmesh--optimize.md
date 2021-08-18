---
description: Optimise le maillage des correctifs pour une polygonalisation efficace.
ms.assetid: 0049e649-5fe5-45b4-9b09-14b7f99b4988
title: 'ID3DXPatchMesh :: Optimize, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.Optimize
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 245f3ddb2c85f5de6ae2acc040f929387d522c12d65eeb4d4307f162b8532af8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120723"
---
# <a name="id3dxpatchmeshoptimize-method"></a>ID3DXPatchMesh :: Optimize, méthode

Optimise le maillage des correctifs pour une polygonalisation efficace.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Optimize(
  [in] DWORD Flags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Indicateurs* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Actuellement inutilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ CANNOTATTRSORT.

## <a name="remarks"></a>Remarques

Une fois qu’une application a généré des informations d’adjacence pour une maille, les données de maillage peuvent être optimisées (réorganisées) pour améliorer les performances de dessin. Cette méthode détermine les correctifs adjacents (dans la tolérance fournie).

Les informations d’contiguïté sont également utilisées pour optimiser la pavage. Générez des informations d’adjacence une fois et paver à plusieurs reprises en appelant [**ID3DXPatchMesh :: paver**](id3dxpatchmesh--tessellate.md). L’optimisation effectuée est indépendante du niveau de pavage réel utilisé. Toutefois, si les vertex de maillage sont modifiés, vous devez régénérer les informations d’adjacence.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> <dt>

[**ID3DXPatchMesh::GenerateAdjacency**](id3dxpatchmesh--generateadjacency.md)
</dt> </dl>

 

 
