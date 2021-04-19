---
description: Calcule les IMT par triangle à partir des données par vertex. Cette fonction vous permet de calculer le IMT en fonction de la valeur d’une maille (couleur, normal, etc.).
ms.assetid: a417a8ad-77b1-49ae-aea0-6a32a154499f
title: D3DXComputeIMTFromPerVertexSignal, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeIMTFromPerVertexSignal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7b12ea3f15f1a185125da46f575d37ad97dd5622
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538061"
---
# <a name="d3dxcomputeimtfrompervertexsignal-function"></a>D3DXComputeIMTFromPerVertexSignal fonction)

Calcule les IMT par triangle à partir des données par vertex. Cette fonction vous permet de calculer le IMT en fonction de la valeur d’une maille (couleur, normal, etc.).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXComputeIMTFromPerVertexSignal(
  _In_        LPD3DXMESH      pMesh,
  _In_  const FLOAT           *pfVertexSignal,
  _In_        UINT            uSignalDimension,
  _In_        UINT            uSignalStride,
  _In_        DWORD           dwOptions,
              LPD3DXUVATLASCB pStatusCallback,
              LPVOID          pUserContext,
  _Out_       LPD3DXBUFFER    *ppIMTData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pMesh* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXMESH**](id3dxmesh.md)**

Pointeur vers un maillage d’entrée (voir [**ID3DXMesh**](id3dxmesh.md)) qui contient la géométrie d’objet pour le calcul du IMT.

</dd> <dt>

*pfVertexSignal* \[ dans\]
</dt> <dd>

Type : **const [**float**](../winprog/windows-data-types.md) \***

Pointeur vers un tableau de données par vertex à partir duquel IMT sera calculé. La taille du tableau est uSignalStride \* v, où v est le nombre de vertex dans le maillage.

</dd> <dt>

*uSignalDimension* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre de valeurs float par vertex.

</dd> <dt>

*uSignalStride* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre d’octets par vertex dans le tableau. Il doit s’agir d’un multiple de sizeof (float)

</dd> <dt>

*dwOptions* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Options de retour à la ligne. Il s’agit d’une combinaison d’un ou plusieurs [**indicateurs D3DXIMT**](./d3dximt-flags.md).

</dd> <dt>

*pStatusCallback* 
</dt> <dd>

Type : **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**

Pointeur vers une fonction de rappel pour surveiller la progression du calcul IMT.

</dd> <dt>

*pUserContext* 
</dt> <dd>

Type : **[ **LPVOID**](../winprog/windows-data-types.md)**

Pointeur vers une variable définie par l’utilisateur qui est passée à la fonction de rappel d’État. Généralement utilisé par une application pour passer un pointeur vers une structure de données qui fournit des informations de contexte pour la fonction de rappel.

</dd> <dt>

*ppIMTData* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Pointeur vers la mémoire tampon (consultez [**ID3DXBuffer**](id3dxbuffer.md)) contenant le tableau IMT retourné. Ce tableau peut être fourni comme entrée aux fonctions D3DX [UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md) pour classer par ordre de priorité l’allocation d’espace de texture dans le paramétrage de la texture.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK ; sinon, la valeur est D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[UVAtlas, fonctions](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

[Utilisation de UVAtlas (Direct3D 9)](using-uvatlas.md)
</dt> </dl>

 

 
