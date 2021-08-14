---
description: Expose des méthodes qui permettent à une extension de Shell de fournir un espace de noms pouvant faire l’objet d’une recherche.
title: Interface IShellFolderSearchable
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchable
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 359def5c-d7ad-46bd-bdda-30a7b3eea56c
ms.openlocfilehash: 249ec6e6f1d4cbe471a89b19138a5b7a235536e595c62bc6d4a655bf55eee8d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118220392"
---
# <a name="ishellfoldersearchable-interface"></a>Interface IShellFolderSearchable

Expose des méthodes qui permettent à une extension de Shell de fournir un espace de noms pouvant faire l’objet d’une recherche.

## <a name="members"></a>Membres

L’interface **IShellFolderSearchable** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IShellFolderSearchable** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IShellFolderSearchable** possède ces méthodes.



| Méthode                                                                | Description                                                               |
|:----------------------------------------------------------------------|:--------------------------------------------------------------------------|
| [**CancelAsyncSearch**](ishellfoldersearchable-cancelasyncsearch.md) | Commence le processus d’annulation d’une recherche asynchrone en attente.<br/> |
| [**FindString**](ishellfoldersearchable-findstring.md)               | Commence une recherche pour une chaîne de recherche spécifiée.<br/>                 |
| [**InvalidateSearch**](ishellfoldersearchable-invalidatesearch.md)   | Rend ce PIDL une partie non valide du dossier shell.<br/>        |



 

## <a name="remarks"></a>Remarques

Cette interface n’est définie dans aucun fichier d’en-tête public. Si vous choisissez d’implémenter cette interface, vous pouvez utiliser le code C/C++ suivant pour déclarer ses méthodes.


```
#undef  INTERFACE
#define INTERFACE IShellFolderSearchable
DECLARE_INTERFACE_IID_(IShellFolderSearchable, IUnknown, "4E1AE66C-204B-11d2-8DB3-0000F87A556C")
{
    // *** IUnknown methods ***
    STDMETHOD(QueryInterface) (THIS_ REFIID riid, __out void **ppv) PURE;
    STDMETHOD_(ULONG,AddRef)  (THIS) PURE;
    STDMETHOD_(ULONG,Release) (THIS) PURE;

    // *** IShellFolderSearchable methods ***

    // FindString -
    //  The returned Shell folder's enumerator will have any
    //   search hits for the given search string.
    //  punkOnAsyncSearch will be QI'd for IShellFolderSearchableCallback
    STDMETHOD(FindString)(THIS_ LPCWSTR pwszTarget, __inout_opt DWORD *pdwFlags,
                          __in_opt IUnknown *punkOnAsyncSearch, __out LPITEMIDLIST *ppidlOut)   PURE;
    // CancelAsyncSearch -
    //   Begins the process of canceling any pending
    //    asynchronous search from this pidl.
    //    When the search is actually canceled, RunEnd will be called
    //   Returns: S_OK => cancelling, S_FALSE => not running
    STDMETHOD(CancelAsyncSearch) (THIS_ LPCITEMIDLIST pidlSearch, __inout_opt DWORD *pdwFlags) PURE;

    // InvalidateSearch -
    //   Makes this pidl no longer a valid portion of the Shell folder
    //    Also does some cleanup of any databases used in the search and
    //    will cause the eventual release of the callback
    //   May cause async search to be canceled
    STDMETHOD(InvalidateSearch)  (THIS_ LPCITEMIDLIST pidlSearch, __inout_opt DWORD *pdwFlags) PURE;
};
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                             |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 
