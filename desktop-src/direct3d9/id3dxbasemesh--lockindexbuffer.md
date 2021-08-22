---
description: Verrouille un tampon d’index et obtient un pointeur vers la mémoire tampon d’index.
ms.assetid: c8941164-1f2a-4aed-b0bd-8130aac61da4
title: 'ID3DXBaseMesh :: LockIndexBuffer, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.LockIndexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c2eab2806775572cb4e4c4a50899d48263c6ddf0d55138c37bcaff8367225c3f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118819"
---
# <a name="id3dxbasemeshlockindexbuffer-method"></a>ID3DXBaseMesh :: LockIndexBuffer, méthode

Verrouille un tampon d’index et obtient un pointeur vers la mémoire tampon d’index.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT LockIndexBuffer(
  [in]          DWORD  Flags,
  [out, retval] LPVOID *ppData
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

*ppData* \[ out, retval\]
</dt> <dd>

Type : **[ **LPVOID**](../winprog/windows-data-types.md)\***

\*Pointeur void vers une mémoire tampon contenant les données d’index. Le nombre d’index dans cette mémoire tampon est égal à [**ID3DXBaseMesh :: GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* 3.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Remarques

Lorsque vous utilisez des mémoires tampons d’index, vous êtes autorisé à effectuer plusieurs appels de verrouillage. Toutefois, vous devez vous assurer que le nombre d’appels de verrous correspond au nombre d’appels de déverrouillage. Les appels DrawPrimitive échouent avec un nombre de verrous en attente sur un tampon d’index actuellement défini.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 
