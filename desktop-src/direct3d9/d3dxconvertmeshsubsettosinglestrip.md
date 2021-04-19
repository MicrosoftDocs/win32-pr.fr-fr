---
description: Convertit le sous-ensemble de maillage spécifié en une seule bande triangulaire.
ms.assetid: 618c7bee-dd09-4379-bb8b-30505e809df9
title: D3DXConvertMeshSubsetToSingleStrip, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXConvertMeshSubsetToSingleStrip
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c76aa52b08a21faf9bc2a6ef35745513063cc3b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539163"
---
# <a name="d3dxconvertmeshsubsettosinglestrip-function"></a>D3DXConvertMeshSubsetToSingleStrip fonction)

Convertit le sous-ensemble de maillage spécifié en une seule bande triangulaire.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXConvertMeshSubsetToSingleStrip(
  _In_  LPD3DXBASEMESH         MeshIn,
  _In_  DWORD                  AttribId,
  _In_  DWORD                  IBOptions,
  _Out_ LPDIRECT3DINDEXBUFFER9 *ppIndexBuffer,
  _Out_ DWORD                  *pNumIndices
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

Combinaison d’un ou plusieurs indicateurs de l’énumération [**D3DXMESH**](./d3dxmesh.md) , en spécifiant des options pour la création de la mémoire tampon d’index. Ne peut pas être D3DXMESH \_ 32 bits. Le tampon d’index sera créé avec des index 32 bits ou 16 bits, selon le format de la mémoire tampon d’index de la maille spécifiée par le paramètre *meshy* .

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

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des valeurs suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Notes

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

 

 
