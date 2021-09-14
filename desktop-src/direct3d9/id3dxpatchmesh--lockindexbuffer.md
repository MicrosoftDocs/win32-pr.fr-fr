---
description: Verrouillez le tampon d’index.
ms.assetid: b68aff75-9ba6-4088-b35f-f56d700d1aff
title: 'ID3DXPatchMesh :: LockIndexBuffer, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.LockIndexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 81dc410262ff21ea972d4c501ac3b5d26a361642
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126998521"
---
# <a name="id3dxpatchmeshlockindexbuffer-method"></a>ID3DXPatchMesh :: LockIndexBuffer, méthode

Verrouillez le tampon d’index.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT LockIndexBuffer(
  [in]          DWORD  flags,
  [out, retval] LPVOID *ppData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*indicateurs* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Combinaison de zéro ou plusieurs indicateurs de verrouillage qui décrivent le type de verrou à effectuer. Pour cette méthode, les indicateurs valides sont les suivants :

-   D3DLOCK \_ Ignorer
-   D3DLOCK \_ aucune \_ \_ mise à jour incorrecte
-   D3DLOCK \_ NOSYSLOCK
-   D3DLOCK en \_ lecture seule

Pour obtenir une description des indicateurs, consultez [D3DLOCK](d3dlock.md).

</dd> <dt>

*ppData* \[ out, retval\]
</dt> <dd>

Type : **[ **LPVOID**](../winprog/windows-data-types.md)\***

\*Pointeur void vers une mémoire tampon contenant les données d’index retournées.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Notes

La mémoire tampon d’index est généralement verrouillée, écrite dans, puis déverrouillée pour la lecture. Les tampons d’index de maillage de correctifs sont des mémoires tampons de 16 bits.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> <dt>

[**D3DXCreatePatchMesh**](d3dxcreatepatchmesh.md)
</dt> </dl>

 

 
