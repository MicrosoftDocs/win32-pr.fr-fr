---
description: Convertissez le sous-ensemble de maillage spécifié en une série de bandes.
ms.assetid: 4f005383-6a5a-4393-ac88-202e45946d3d
title: D3DXConvertMeshSubsetToStrips, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXConvertMeshSubsetToStrips
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 345c80305f42df410f42cf255f1b9e0d8f353b448134779b416d686db4b40c05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118526787"
---
# <a name="d3dxconvertmeshsubsettostrips-function"></a>D3DXConvertMeshSubsetToStrips fonction)

Convertissez le sous-ensemble de maillage spécifié en une série de bandes.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXConvertMeshSubsetToStrips(
  _In_  LPD3DXBASEMESH         MeshIn,
  _In_  DWORD                  AttribId,
  _In_  DWORD                  IBOptions,
  _Out_ LPDIRECT3DINDEXBUFFER9 *ppIndexBuffer,
  _Out_ DWORD                  *pNumIndices,
  _Out_ LPD3DXBUFFER           *ppStripLengths,
  _Out_ DWORD                  *pNumStrips
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Mailler* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**

Pointeur vers une interface [**ID3DXBaseMesh**](id3dxbasemesh.md) représentant le maillage à convertir en bande.

</dd> <dt>

*AttribId* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

ID d’attribut du sous-ensemble de maillage à convertir en bandes.

</dd> <dt>

*IBOptions* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Combinaison d’un ou plusieurs indicateurs de l’énumération [**D3DXMESH**](./d3dxmesh.md) , en spécifiant des options pour la création de la mémoire tampon d’index. Ne peut pas être D3DXMESH \_ 32 bits. Le tampon d’index sera créé avec des index 32 bits ou 16 bits selon le format de la mémoire tampon d’index de la maille spécifiée par le paramètre *meshy* .

</dd> <dt>

*ppIndexBuffer* \[ à\]
</dt> <dd>

Type : **[ **LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***

Pointeur vers une interface [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) , représentant la mémoire tampon d’index contenant la bande.

</dd> <dt>

*pNumIndices* \[ à\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)\***

Nombre d’index dans la mémoire tampon retournée dans le paramètre *ppIndexBuffer* .

</dd> <dt>

*ppStripLengths* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Mémoire tampon contenant un tableau d’un DWORD par bande, qui spécifie le nombre de triangles dans cette frange.

</dd> <dt>

*pNumStrips* \[ à\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)\***

Nombre de bandes individuelles dans le tampon d’index et le tableau de longueur de bande correspondant.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des valeurs suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarques

Avant d’exécuter cette fonction, appelez [**optimize**](id3dxmesh--optimize.md) ou [**D3DXOptimizeFaces**](d3dxoptimizefaces.md), avec l' \_ indicateur D3DXMESHOPT ATTRSORT défini.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de maillage](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
