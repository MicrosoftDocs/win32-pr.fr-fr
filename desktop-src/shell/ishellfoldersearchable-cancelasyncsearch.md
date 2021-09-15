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
ms.openlocfilehash: 3146fea4f6c8d8547c8c86096b434cbaea5b5926
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412444"
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

Type : **DWORD \***

Aucun indicateur n’est actuellement défini. Affectez la valeur **null**.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

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



 

 




