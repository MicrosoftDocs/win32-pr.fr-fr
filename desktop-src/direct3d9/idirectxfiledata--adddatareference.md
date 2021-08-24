---
description: Crée et ajoute un objet de référence de données en tant qu’objet enfant. Action déconseillée.
ms.assetid: 71a770a2-1502-4b93-b368-990c3318bd33
title: 'IDirectXFileData :: AddDataReference, méthode (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.AddDataReference
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 4c291e4f5754975f7e564c8c579b3651b29f0e6b684ad474f2f8436875dbf078
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747259"
---
# <a name="idirectxfiledataadddatareference-method"></a>IDirectXFileData :: AddDataReference, méthode

Crée et ajoute un objet de référence de données en tant qu’objet enfant. Action déconseillée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT AddDataReference(
  [in]       LPCSTR szRef,
  [in] const GUID   *pguidRef
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*szRef* \[ dans\]
</dt> <dd>

Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**

Pointeur vers le nom de l’objet de données référencé. Ce paramètre peut avoir la **valeur null** si pguidRef fournit une référence au GUID.

</dd> <dt>

*pguidRef* \[ dans\]
</dt> <dd>

Type : **const [**GUID**](guid.md) \***

Pointeur vers le GUID représentant les données. Ce paramètre peut avoir la **valeur null** si szRef fournit une référence au nom.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est DXFILE \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des valeurs suivantes. DXFILEERR \_ BADALLOC DXFILEERR \_ BADVALUE

## <a name="remarks"></a>Remarques

Pour que cette méthode aboutisse, le paramètre szRef ou pguidRef doit être non **null**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[IDirectXFileData](idirectxfiledata.md)
</dt> </dl>

 

 
