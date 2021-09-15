---
description: Expose des routines de rappel pour surveiller le processus de recherche.
title: Interface IShellFolderSearchableCallback
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchableCallback
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 3412a01b-d5ea-44e1-819c-f10f81fac391
ms.openlocfilehash: cf1a3b03eed2a15e82e1313875a4ab8584243190
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127530401"
---
# <a name="ishellfoldersearchablecallback-interface"></a>Interface IShellFolderSearchableCallback

Expose des routines de rappel pour surveiller le processus de recherche.

## <a name="members"></a>Membres

L’interface **IShellFolderSearchableCallback** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IShellFolderSearchableCallback** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IShellFolderSearchableCallback** possède ces méthodes.



| Méthode                                                      | Description                                      |
|:------------------------------------------------------------|:-------------------------------------------------|
| [**RunBegin**](ishellfoldersearchablecallback-runbegin.md) | Indique qu’une recherche a été démarrée.<br/>  |
| [**RunEnd**](ishellfoldersearchablecallback-runend.md)     | Indique qu’une recherche est terminée.<br/> |



 

## <a name="remarks"></a>Notes

Cette interface n’est définie dans aucun fichier d’en-tête public. Si vous choisissez d’implémenter cette interface, vous pouvez utiliser le code C/C++ suivant pour déclarer ses méthodes.


```
#undef  INTERFACE
#define INTERFACE IShellFolderSearchableCallback
DECLARE_INTERFACE_IID_(IShellFolderSearchableCallback, IUnknown, "F98D8294-2BBC-11d2-8DBD-0000F87A556C")
{
    // *** IUnknown methods ***
    STDMETHOD(QueryInterface) (THIS_ REFIID riid, __out void **ppv) PURE;
    STDMETHOD_(ULONG,AddRef)  (THIS) PURE;
    STDMETHOD_(ULONG,Release) (THIS) PURE;

    // *** IShellFolderSearchableCallback Methods ***

    STDMETHOD(RunBegin)(THIS_ DWORD dwReserved) PURE;
    STDMETHOD(RunEnd)(THIS_ DWORD dwReserved) PURE;
};
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                             |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 
