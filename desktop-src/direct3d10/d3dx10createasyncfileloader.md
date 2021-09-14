---
description: Créez un chargeur de fichiers asynchrones.
ms.assetid: 1b79fba5-e7f0-4160-9cec-ffea94f84fde
title: D3DX10CreateAsyncFileLoader, fonction (D3DX10Async. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncFileLoader
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: e98bccf709fa4a6d921e266148b94fd8623429ef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126922720"
---
# <a name="d3dx10createasyncfileloader-function"></a>D3DX10CreateAsyncFileLoader fonction)

Créez un chargeur de fichiers asynchrones.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DX10CreateAsyncFileLoader(
  _In_  LPCTSTR           pFileName,
  _Out_ ID3DX10DataLoader **ppDataLoader
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pFileName* \[ dans\]
</dt> <dd>

Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Nom du fichier à charger. Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR. Dans le cas contraire, le type de données est résolu en LPCSTR.

</dd> <dt>

*ppDataLoader* \[ à\]
</dt> <dd>

Type : **[ **ID3DX10DataLoader**](id3dx10dataloader.md)\*\***

Adresse d’un pointeur vers le chargeur de données asynchrones (voir [**interface ID3DX10DataLoader**](id3dx10dataloader.md)).

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3DX10Async. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions usage général](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
