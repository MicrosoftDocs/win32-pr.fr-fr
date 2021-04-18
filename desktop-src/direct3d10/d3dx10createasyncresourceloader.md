---
description: Créez un chargeur de ressources asynchrones.
ms.assetid: 1b3eb21c-4ba6-4910-b2f0-2ffa4ae50e47
title: D3DX10CreateAsyncResourceLoader, fonction (D3DX10Async. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncResourceLoader
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 0539817ffff75c28af41289fc5197f6440a915bd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522944"
---
# <a name="d3dx10createasyncresourceloader-function"></a>D3DX10CreateAsyncResourceLoader fonction)

Créez un chargeur de ressources asynchrones.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DX10CreateAsyncResourceLoader(
  _In_  HMODULE           hSrcModule,
  _In_  LPCTSTR           pSrcResource,
  _Out_ ID3DX10DataLoader **ppDataLoader
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hSrcModule* \[ dans\]
</dt> <dd>

Type : **[ **HMODULE**](../winprog/windows-data-types.md)**

Handle du module de ressources. Utilisez la [fonction GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) pour récupérer le descripteur.

</dd> <dt>

*pSrcResource* \[ dans\]
</dt> <dd>

Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Nom de la ressource dans hSrcModule. Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR. Dans le cas contraire, le type de données est résolu en LPCSTR.

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

 

 
