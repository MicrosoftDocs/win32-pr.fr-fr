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
ms.openlocfilehash: cb5c6e324e657962a4a0bbbfa64cb45fefa7d37a3ca5ce21cd25e072fc1a6594
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119223369"
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

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Retourne S \_ OK en cas d’annulation, ou \_ a la valeur false si la recherche n’est pas en cours d’exécution.

## <a name="remarks"></a>Remarques

Lorsque la recherche est effectivement annulée, [**RunEnd**](ishellfoldersearchablecallback-runend.md) est appelé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                             |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




