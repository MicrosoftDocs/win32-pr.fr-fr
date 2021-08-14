---
description: Commence une recherche pour une chaîne de recherche spécifiée.
ms.assetid: 6ecad03c-e8e0-45ba-8def-b55a029992f2
title: 'IShellFolderSearchable :: FindString, méthode (MMC. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchable.FindString
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 947cda4094491702fa0f847e6a8abd4fed7bcbe9bd3504c5f8aec2097b0d6b8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118220935"
---
# <a name="ishellfoldersearchablefindstring-method"></a>IShellFolderSearchable :: FindString, méthode

Commence une recherche pour une chaîne de recherche spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT FindString(
  [in]  LPCWSTR      pwszTarget,
  [in]  DWORD        *pdwFlags,
  [in]  IUnknown     *punkOnAsyncSearch,
  [out] LPITEMIDLIST ppidlOut
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pwszTarget* \[ dans\]
</dt> <dd>

Type : **LPCWSTR**

Pointeur vers une chaîne qui spécifie le mot clé de recherche.

</dd> <dt>

*pdwFlags* \[ dans\]
</dt> <dd>

Type : **DWORD \***

Aucun indicateur n’est actuellement défini. Affectez la valeur **null**.

</dd> <dt>

*punkOnAsyncSearch* \[ dans\]
</dt> <dd>

Type : **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***

Pointeur vers un objet de type [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown). Cet objet doit prendre en charge l’interface [**IShellFolderSearchableCallback**](ishellfoldersearchablecallback.md) . Affectez la valeur **null** si aucun rappel n’est nécessaire.

</dd> <dt>

*ppidlOut* \[ à\]
</dt> <dd>

Type : **LPITEMIDLIST**

Pointeur vers une structure [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) pour le dossier de recherche.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                             |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>MMC. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 
