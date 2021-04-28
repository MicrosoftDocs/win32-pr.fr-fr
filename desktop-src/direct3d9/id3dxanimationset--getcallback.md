---
description: 'ID3DXAnimationSet :: GetCallback, méthode-obtient des informations sur un rappel spécifique dans l’ensemble d’animations.'
ms.assetid: e8388bfc-5438-4216-a98f-dd0dbca12c87
title: 'ID3DXAnimationSet :: GetCallback, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetCallback
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 563c1007cc471ab10a9609e776da69b7c5ed493b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097537"
---
# <a name="id3dxanimationsetgetcallback-method"></a>ID3DXAnimationSet :: GetCallback, méthode

Obtient des informations sur un rappel spécifique dans l’ensemble d’animations.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetCallback(
  [in]  DOUBLE Position,
  [in]  DWORD  Flags,
  [out] DOUBLE *pCallbackPosition,
  [out] LPVOID *ppCallbackData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Position* \[ dans\]
</dt> <dd>

Type : **[ **double**](../winprog/windows-data-types.md)**

Position à partir de laquelle rechercher les rappels.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Indicateurs de recherche de rappel. Ce paramètre peut être défini sur une combinaison d’un ou plusieurs indicateurs d' [**\_ \_ indicateurs de recherche D3DXCALLBACK**](./d3dxcallback-search-flags.md).

</dd> <dt>

*pCallbackPosition* \[ à\]
</dt> <dd>

Type : **[ **double**](../winprog/windows-data-types.md)\***

Pointeur vers la position du rappel.

</dd> <dt>

*ppCallbackData* \[ à\]
</dt> <dd>

Type : **[ **LPVOID**](../winprog/windows-data-types.md)\***

Adresse du pointeur de données de rappel.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Les valeurs de retour de cette méthode sont implémentées par un programmeur d’applications. En général, si aucune erreur ne se produit, programmez la méthode pour retourner D3D \_ OK. Sinon, programmez la méthode pour retourner un message d’erreur approprié à partir de [D3DERR](d3derr.md) ou [**D3DXERR**](./d3dxerr.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXAnimationSet](id3dxanimationset.md)
</dt> </dl>

 

 
