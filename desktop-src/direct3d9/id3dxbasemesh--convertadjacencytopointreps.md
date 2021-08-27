---
description: Convertit les informations d’adjacence de maillage en un tableau de représentants de point.
ms.assetid: b8914f9c-8550-498d-813d-bb1afe0fb5b2
title: 'ID3DXBaseMesh :: ConvertAdjacencyToPointReps, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.ConvertAdjacencyToPointReps
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 729e6b67c68f5a9560cbf0aeab5d8f28b72854be49ebc00fb0f0924a5afa4b38
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096029"
---
# <a name="id3dxbasemeshconvertadjacencytopointreps-method"></a>ID3DXBaseMesh :: ConvertAdjacencyToPointReps, méthode

Convertit les informations d’adjacence de maillage en un tableau de représentants de point.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ConvertAdjacencyToPointReps(
  [in]      const DWORD *pAdjacency,
  [in, out]       DWORD *pPRep
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pAdjacency* \[ dans\]
</dt> <dd>

Type : **const [**DWORD**](../winprog/windows-data-types.md) \***

Pointeur vers un tableau de trois DWORD par visage qui spécifient les trois voisins pour chaque face de la maille. Le nombre d’octets dans ce tableau doit être au moins égal à 3 \* [**ID3DXBaseMesh :: GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof (DWORD).

</dd> <dt>

*pPRep* \[ in, out\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)\***

Pointeur vers un tableau d’une valeur DWORD par vertex de la maille qui sera remplie avec des données représentatives de point.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 
