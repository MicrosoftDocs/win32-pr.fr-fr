---
description: Divise un maillage en maillages plus petits que la taille spécifiée.
ms.assetid: 55cdd82f-91fa-4805-969f-8fbe53cbde58
title: D3DXSplitMesh, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSplitMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d1f01cdb4ddd009f5cdf0b7f0310a492840955f1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535809"
---
# <a name="d3dxsplitmesh-function"></a>D3DXSplitMesh fonction)

Divise un maillage en maillages plus petits que la taille spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
void D3DXSplitMesh(
  _In_        LPD3DXMESH   pMeshIn,
  _In_  const DWORD        *pAdjacencyIn,
  _In_  const DWORD        MaxSize,
  _In_  const DWORD        Options,
  _Out_       DWORD        *pMeshesOut,
  _Out_       LPD3DXBUFFER *ppMeshArrayOut,
  _Out_       LPD3DXBUFFER *ppAdjacencyArrayOut,
  _Out_       LPD3DXBUFFER *ppFaceRemapArrayOut,
  _Out_       LPD3DXBUFFER *ppVertRemapArrayOut
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pMeshIn* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXMESH**](id3dxmesh.md)**

Pointeur vers une interface [**ID3DXMesh**](id3dxmesh.md) représentant la maille source.

</dd> <dt>

*pAdjacencyIn* \[ dans\]
</dt> <dd>

Type : **const [**DWORD**](../winprog/windows-data-types.md) \***

Pointeur vers un tableau de trois DWORD par visage qui spécifient les trois voisins pour chaque visage de la maille à simplifier.

</dd> <dt>

*MaxSize* \[ dans\]
</dt> <dd>

Type : **const [**DWORD**](../winprog/windows-data-types.md)**

Nombre maximal de vertex dans le maillage résultant.

</dd> <dt>

*Options* \[ dans\]
</dt> <dd>

Type : **const [**DWORD**](../winprog/windows-data-types.md)**

Indicateurs d’option pour les nouveaux maillages.

</dd> <dt>

*pMeshesOut* \[ à\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)\***

Nombre de maillages retournés.

</dd> <dt>

*ppMeshArrayOut* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Mémoire tampon contenant un tableau d’interfaces [**ID3DXMesh**](id3dxmesh.md) pour les nouveaux maillages. Pour un maillage source divisé en n maillages, *ppMeshArrayOut* est un tableau de n pointeurs **ID3DXMesh** .

</dd> <dt>

*ppAdjacencyArrayOut* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Mémoire tampon contenant un tableau de tableaux d’adjacence (DWORDs) pour les nouveaux maillages. Consultez [**ID3DXBuffer**](id3dxbuffer.md). Ce paramètre est facultatif.

</dd> <dt>

*ppFaceRemapArrayOut* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Mémoire tampon contenant un tableau de tableaux de remappages de visages (DWORDs) pour les nouveaux maillages. Consultez [**ID3DXBuffer**](id3dxbuffer.md). Ce paramètre est facultatif.

</dd> <dt>

*ppVertRemapArrayOut* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Mémoire tampon contenant un tableau de tableaux de remappage de vertex pour les nouveaux maillages. Consultez [**ID3DXBuffer**](id3dxbuffer.md). Ce paramètre est facultatif.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des valeurs suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Notes

Cette fonction est couramment utilisée pour fractionner un maillage avec des index 32 bits (plus de 65535 sommets) en plusieurs maillages, chacun ayant des index 16 bits.

Les tableaux d’adjacence, de remappage de sommets et de remappage de face sont des tableaux de type DWORD, où chaque tableau contient n pointeurs DWORD, suivis des données DWORD référencées par les pointeurs. Par exemple, pour obtenir les informations de remappage de visage pour la face 3 de la maille 2, vous pouvez utiliser le code suivant, en supposant que les données de remappage de face ont été retournées dans une variable nommée *ppFaceRemapArrayOut*.


```
   
const DWORD **face_remaps = 
    static_cast<DWORD **>(ppFaceRemapArrayOut->GetBufferPointer());
const DWORD remap = face_remaps[2][3];
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de maillage](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
