---
description: Verrouille la mémoire tampon de maillage qui contient les données d’attribut de maillage et retourne un pointeur vers celle-ci.
ms.assetid: 17a321b8-bfb4-4018-869f-6b09e0a811eb
title: 'ID3DXMesh :: LockAttributeBuffer, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh.LockAttributeBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8ca767c6bc223c40d6013b93162de057aac9f4fb1b71303990f9128e4eca1ee6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118802152"
---
# <a name="id3dxmeshlockattributebuffer-method"></a>ID3DXMesh :: LockAttributeBuffer, méthode

Verrouille la mémoire tampon de maillage qui contient les données d’attribut de maillage et retourne un pointeur vers celle-ci.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT LockAttributeBuffer(
  [in]  DWORD Flags,
  [out] DWORD **ppData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Indicateurs* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Combinaison de zéro ou plusieurs indicateurs de verrouillage qui décrivent le type de verrou à effectuer. Pour cette méthode, les indicateurs valides sont les suivants :

-   D3DLOCK \_ Ignorer
-   D3DLOCK \_ aucune \_ \_ mise à jour incorrecte
-   D3DLOCK \_ NOSYSLOCK
-   D3DLOCK en \_ lecture seule

Pour obtenir une description des indicateurs, consultez [D3DLOCK](d3dlock.md).

</dd> <dt>

*ppData* \[ à\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)\*\***

Adresse d’un pointeur vers une mémoire tampon contenant un DWORD pour chaque face de la maille.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Remarques

Si [**ID3DXMesh :: Optimize**](id3dxmesh--optimize.md) a été appelé, la maille aura également une table d’attributs accessible à l’aide de la méthode [**ID3DXBaseMesh :: GetAttributeTable**](id3dxbasemesh--getattributetable.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXMesh](id3dxmesh.md)
</dt> <dt>

[**ID3DXMesh::UnlockAttributeBuffer**](id3dxmesh--unlockattributebuffer.md)
</dt> <dt>

[**ID3DXBaseMesh::GetAttributeTable**](id3dxbasemesh--getattributetable.md)
</dt> <dt>

[**ID3DXMesh::SetAttributeTable**](id3dxmesh--setattributetable.md)
</dt> </dl>

 

 
