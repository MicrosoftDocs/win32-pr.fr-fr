---
description: 'Fonction D3DXSHPRTCompSuperCluster : utilisée avec les résultats compressés de la version vertex du simulateur de transfert luminance (PRT) précalculé.'
ms.assetid: 0ec28b8c-5010-48a4-8e45-d7f9aa08185f
title: D3DXSHPRTCompSuperCluster, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHPRTCompSuperCluster
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 55556046c7fa8e0a8e7666a9d2dd0a20d81b5f3cf59253f499cbd7d0fba41fbc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749828"
---
# <a name="d3dxshprtcompsupercluster-function"></a>D3DXSHPRTCompSuperCluster fonction)

Utilisé avec les résultats compressés de la version vertex du simulateur de transfert luminance (PRT) précalculé. Génère des « superclusters », qui sont des groupes de clusters qui peuvent être dessinés dans le même appel de dessin. Un algorithme gourmand qui minimise le surdessin est utilisé pour regrouper les clusters.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXSHPRTCompSuperCluster(
  _In_    UINT       *pClusterIDs,
  _In_    LPD3DXMESH pScene,
  _In_    UINT       MaxNumClusters,
  _In_    UINT       NumClusters,
  _Inout_ UINT       *pSClusterIDs,
  _Inout_ UINT       *pNumSCs
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pClusterIDs* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)\***

Pointeur vers un ID de cluster NumVerts (extrait d’une mémoire tampon compressée.)

</dd> <dt>

*pScene* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXMESH**](id3dxmesh.md)**

Pointeur vers un maillage qui représente la scène composite transmise au simulateur. Consultez [**ID3DXMesh**](id3dxmesh.md).

</dd> <dt>

*MaxNumClusters* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre maximal de clusters alloués par Super cluster.

</dd> <dt>

*NumClusters* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre de clusters calculés dans le simulateur.

</dd> <dt>

*pSClusterIDs* \[ in, out\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)\***

Pointeur vers un tableau de longueur *NumClusters*. Contient l’index du Super cluster auquel le cluster correspondant a été affecté.

</dd> <dt>

*pNumSCs* \[ in, out\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)\***

Nombre de Super clusters alloués.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de transfert luminance précalculées](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
