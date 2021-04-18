---
description: Charge une version spécifiée d’une DLL de bibliothèque .NET Framework.
ms.assetid: f001774d-ea9a-4820-aec0-99ce958b1e1d
title: LoadLibraryShim, fonction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadLibraryShim
api_type:
- DllExport
api_location:
- Mscoree.dll
ms.openlocfilehash: 3a2fd8ab6aef8d0309748cbbf37d56ccd032b050
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532919"
---
# <a name="loadlibraryshim-function"></a>LoadLibraryShim, fonction

Charge une version spécifiée d’une DLL de bibliothèque .NET Framework.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT LoadLibraryShim(
  _In_  LPCWSTR szDllName,
  _In_  LPCWSTR szVersion,
        LPVOID  pvReserved,
  _Out_ HMODULE *phModDll
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*szDllName* \[ dans\]
</dt> <dd>

Nom de la DLL à charger à partir du .NET Framework.

</dd> <dt>

*szVersion* \[ dans\]
</dt> <dd>

Version de la DLL à charger. Si *szVersion* a la **valeur null**, la version la plus récente de la DLL spécifiée est chargée.

</dd> <dt>

*pvReserved* 
</dt> <dd>

Réservé.

</dd> <dt>

*phModDll* \[ à\]
</dt> <dd>

Handle du module.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Cette fonction est utilisée pour charger les dll de bibliothèque qui sont incluses dans le package redistribuable .NET Framework, et non des dll générées par l’utilisateur.

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Mscoree.dll</dt> </dl> |



 

 
