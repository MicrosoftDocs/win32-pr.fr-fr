---
description: Nettoie un maillage, en le préparant à des fins de simplification.
ms.assetid: 2b586ecc-db87-4b20-a4fc-c8b547bebf65
title: D3DXCleanMesh, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCleanMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: adc5d60b66dc9eaa06314e18ead26412b8572e9dbc649070c37891a62fb9ecbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119495909"
---
# <a name="d3dxcleanmesh-function"></a>D3DXCleanMesh fonction)

Nettoie un maillage, en le préparant à des fins de simplification.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXCleanMesh(
  _In_        D3DXCLEANTYPE CleanType,
  _In_        LPD3DXMESH    pMeshIn,
  _In_  const DWORD         *pAdjacencyIn,
  _Out_       LPD3DXMESH    *ppMeshOut,
  _Out_       DWORD         *pAdjacencyOut,
  _Out_       LPD3DXBUFFER  *ppErrorsAndWarnings
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*CleanType* \[ dans\]
</dt> <dd>

Type : **[ **D3DXCLEANTYPE**](./d3dxcleantype.md)**

Opérations de vertex à effectuer en préparation du nettoyage de maillage. Consultez [**D3DXCLEANTYPE**](./d3dxcleantype.md).

</dd> <dt>

*pMeshIn* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXMESH**](id3dxmesh.md)**

Pointeur vers une interface [**ID3DXMesh**](id3dxmesh.md) représentant le maillage à nettoyer.

</dd> <dt>

*pAdjacencyIn* \[ dans\]
</dt> <dd>

Type : **const [**DWORD**](../winprog/windows-data-types.md) \***

Pointeur vers un tableau de trois DWORD par visage qui spécifient les trois voisins pour chaque face de la maille à nettoyer.

</dd> <dt>

*ppMeshOut* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXMESH**](id3dxmesh.md)\***

Adresse d’un pointeur vers une interface [**ID3DXMesh**](id3dxmesh.md) représentant le maillage nettoyé retourné. Le même maillage est retourné qui a été transmis si aucun nettoyage n’était nécessaire.

</dd> <dt>

*pAdjacencyOut* \[ à\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)\***

Pointeur vers un tableau de trois DWORD par visage qui spécifient les trois voisins pour chaque visage dans le maillage de sortie.

</dd> <dt>

*ppErrorsAndWarnings* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Retourne une mémoire tampon contenant une chaîne d’erreurs et d’avertissements, qui expliquent les problèmes détectés dans la maille.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarques

Cette fonction nettoie un maillage à l’aide de la méthode de nettoyage et des options spécifiées dans le paramètre CleanType. Pour obtenir une description des options disponibles, consultez l’énumération [**D3DXCLEANTYPE**](./d3dxcleantype.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de maillage](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
