---
description: Calcule les vecteurs de tangente pour les coordonnées de texture données dans l’étape de texture. Fourni pour prendre en charge les applications héritées. Utilisez D3DXComputeTangentFrameEx pour obtenir de meilleurs résultats.
ms.assetid: 39748459-3f9b-4b48-ae13-7143eb29c292
title: D3DXComputeTangent, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeTangent
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5cdb6a9dae3bdbad0f239fa61ba066d7b1bffb14
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106527733"
---
# <a name="d3dxcomputetangent-function"></a>D3DXComputeTangent fonction)

Calcule les vecteurs de tangente pour les coordonnées de texture données dans l’étape de texture. Fourni pour prendre en charge les applications héritées. Utilisez [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) pour obtenir de meilleurs résultats.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXComputeTangent(
  _In_       LPD3DXMESH Mesh,
  _In_       DWORD      TexStageIndex,
  _In_       DWORD      TangentIndex,
  _In_       DWORD      BinormIndex,
  _In_       DWORD      Wrap,
  _In_ const DWORD      *pAdjacency
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Maille* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXMESH**](id3dxmesh.md)**

Pointeur vers une interface [**ID3DXMesh**](id3dxmesh.md) qui représente le maillage d’entrée.

</dd> <dt>

*TexStageIndex* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Index qui représente l’étape de la texture.

</dd> <dt>

*TangentIndex* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Index qui fournit l’index d’utilisation pour les données de tangente. La déclaration de vertex implique l’utilisation ; Cet index modifie l’utilisation avec l’index d’utilisation. Pour plus d’informations sur une déclaration de vertex, consultez la rubrique [déclaration de vertex (Direct3D 9)](vertex-declaration.md).

</dd> <dt>

*BinormIndex* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Index qui fournit l’index d’utilisation pour les données binormales. La déclaration de vertex implique l’utilisation ; Cet index modifie l’utilisation avec l’index d’utilisation. Pour plus d’informations sur une déclaration de vertex, consultez la rubrique [déclaration de vertex (Direct3D 9)](vertex-declaration.md).

</dd> <dt>

*Retour à la ligne* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Définissez cette valeur sur 0 pour aucun habillage, ou sur 1 pour l’habillage dans les directions vous et V.

</dd> <dt>

*pAdjacency* \[ dans\]
</dt> <dd>

Type : **const [**DWORD**](../winprog/windows-data-types.md) \***

Pointeur vers un tableau de trois DWORDs par visage à remplir avec des indices de face adjacente. Le nombre d’octets dans ce tableau doit être au moins égal à ((3 \* [**GetNumFaces**](id3dxbasemesh--getnumfaces.md)) \* sizeof (DWORD)).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est S \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Notes

Si la déclaration de vertex de maillage spécifie des champs tangente ou binormal, **D3DXComputeTangent** met à jour les données de tangente ou binormal fournies par l’utilisateur. Vous pouvez également définir TangentIndex sur [D3DX \_ default](other-d3dx-constants.md) pour ne pas mettre à jour les données tangentes fournies par l’utilisateur, ou définir BinormIndex sur D3DX \_ Default pour ne pas mettre à jour les données binormales fournies par l’utilisateur. TexStageIndex ne peut pas être défini sur D3DX \_ default.

**D3DXComputeTangent** dépend de la déclaration de vertex de maillage contenant soit le champ binormal (BinormIndex), le champ tangente (TangentIndex), ou les deux. Si les deux sont absents, cette fonction échoue.

Cette fonction appelle simplement [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) avec les paramètres d’entrée suivants :


```
D3DXComputeTangentFrameEx( Mesh,
                           D3DDECLUSAGE_TEXCOORD,
                           TexStageIndex,
                           ( BinormIndex == D3DX_DEFAULT ) ?
                               D3DX_DEFAULT : D3DDECLUSAGE_BINORMAL,
                               // provides backward function compatibility
                           BinormIndex,
                           ( TangentIndex == D3DX_DEFAULT ) ?
                               D3DX_DEFAULT : D3DDECLUSAGE_TANGENT,
                           TangentIndex,
                           D3DX_DEFAULT, // do not store normals
                           0,
                           ( Wrap ? D3DXTANGENT_WRAP_UV : 0 )
                               | D3DXTANGENT_GENERATE_IN_PLACE
                               | D3DXTANGENT_ORTHOGONALIZE_FROM_U,
                           pAdjacency,
                           -1.01f,
                           -0.01f,
                           -1.01f,
                           NULL,
                           NULL);
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

 

 
