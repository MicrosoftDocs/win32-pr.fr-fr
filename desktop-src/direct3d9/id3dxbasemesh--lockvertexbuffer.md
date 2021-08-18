---
description: Verrouille une mémoire tampon de vertex et obtient un pointeur vers la mémoire tampon de vertex.
ms.assetid: afcd479c-b268-4720-b26c-88b82f1aab08
title: 'ID3DXBaseMesh :: LockVertexBuffer, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.LockVertexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5bb0cd8539a996b66ccf9f413e57ebf1d213fe6372e56b50b35abc5e210595f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987609"
---
# <a name="id3dxbasemeshlockvertexbuffer-method"></a>ID3DXBaseMesh :: LockVertexBuffer, méthode

Verrouille une mémoire tampon de vertex et obtient un pointeur vers la mémoire tampon de vertex.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT LockVertexBuffer(
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
-   D3DLOCK \_ NOOVERWRITE

Pour obtenir une description des indicateurs, consultez [D3DLOCK](d3dlock.md).

</dd> <dt>

*ppData* \[ out, retval\]
</dt> <dd>

Type : **[ **LPVOID**](../winprog/windows-data-types.md)\***

\*Pointeur void vers une mémoire tampon contenant les données de vertex.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Remarques

Lorsque vous utilisez des mémoires tampons de vertex, vous êtes autorisé à effectuer plusieurs appels de verrouillage. Toutefois, vous devez vous assurer que le nombre d’appels de verrous correspond au nombre d’appels de déverrouillage. Les appels DrawPrimitive échouent avec un nombre de verrous en attente sur une mémoire tampon de vertex actuellement définie.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 
