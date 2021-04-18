---
description: Créez un chargeur de mémoire asynchrone.
ms.assetid: 92177390-cb09-445e-9828-806a23ef91b5
title: D3DX10CreateAsyncMemoryLoader, fonction (D3DX10Async. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncMemoryLoader
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 0219026eabfcff6dfcec0df4721716302f09f5e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522761"
---
# <a name="d3dx10createasyncmemoryloader-function"></a>D3DX10CreateAsyncMemoryLoader fonction)

Créez un chargeur de mémoire asynchrone.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DX10CreateAsyncMemoryLoader(
  _In_  LPCVOID           pData,
  _In_  SIZE_T            cbData,
  _Out_ ID3DX10DataLoader **ppDataLoader
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pData* \[ dans\]
</dt> <dd>

Type : **[ **LPCVOID**](../winprog/windows-data-types.md)**

Pointeur vers les données.

</dd> <dt>

*cbData* \[ dans\]
</dt> <dd>

Type : **[ **taille \_ T**](../winprog/windows-data-types.md)**

Taille des données.

</dd> <dt>

*ppDataLoader* \[ à\]
</dt> <dd>

Type : **[ **ID3DX10DataLoader**](id3dx10dataloader.md)\*\***

Adresse d’un pointeur vers le processeur de données asynchrones (voir [**interface ID3DX10DataProcessor**](id3dx10dataprocessor.md)).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3DX10Async. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions usage général](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
