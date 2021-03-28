---
description: Commence le processus d’annulation d’une recherche asynchrone en attente.
title: 'IShellFolderSearchable :: CancelAsyncSearch, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchable.CancelAsyncSearch
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 5c920dca-fbca-48e1-9dce-38713cf1fcef
ms.openlocfilehash: e9e3231e8cc602a4e00b6ee79a25392717b6e68b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972350"
---
# <a name="ishellfoldersearchablecancelasyncsearch-method"></a>IShellFolderSearchable :: CancelAsyncSearch, méthode

Commence le processus d’annulation d’une recherche asynchrone en attente.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CancelAsyncSearch(
  [in] LPCITEMIDLIST pidlSearch,
  [in] DWORD         *pdwFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pidlSearch* \[ dans\]
</dt> <dd>

Type : **LPCITEMIDLIST**

Pointeur vers un [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) pour la recherche.

</dd> <dt>

*pdwFlags* \[ dans\]
</dt> <dd>

Type : **DWORD \** _

Aucun indicateur n’est actuellement défini. définissez sur _ * NULL * *.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Retourne S \_ OK en cas d’annulation, ou \_ a la valeur false si la recherche n’est pas en cours d’exécution.

## <a name="remarks"></a>Notes

Lorsque la recherche est effectivement annulée, [**RunEnd**](ishellfoldersearchablecallback-runend.md) est appelé.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                             |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




