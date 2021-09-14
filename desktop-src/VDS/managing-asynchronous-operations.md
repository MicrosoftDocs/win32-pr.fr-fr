---
description: Gestion des opérations asynchrones
ms.assetid: e5136e15-3ae1-4e0a-ae97-fcf16203b21d
title: Gestion des opérations asynchrones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d220c5633f9ee044dbf9cdb6a63b563747620afd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126853048"
---
# <a name="managing-asynchronous-operations"></a>Gestion des opérations asynchrones

\[à partir de Windows 8 et Windows Server 2012, le [Service de disque virtuel](virtual-disk-service-portal.md) est remplacé par l’API de gestion de l' [Stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

L’exemple de code suivant montre comment un appelant travaille avec un objet Async. Ici, la fonction **SynchronousCreateLun** appelle la méthode asynchrone [**IVdsSubSystem :: CreateLun**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-createlun) à l’aide des paramètres donnés. La fonction attend que l’appel de la méthode **CreateLun** asynchrone se termine sur l’objet Async. Quand la méthode [**IVdsAsync :: wait**](/windows/desktop/api/Vds/nf-vds-ivdsasync-wait) retourne, **SynchronousCreateLun** obtient l’interface [**IVdsLun**](/windows/desktop/api/Vds/nn-vds-ivdslun) pour le LUN nouvellement créé et le retourne comme argument out.


```C++
//
// Simple macro to release non-null interfaces.
//
#include <windows.h>
#include "vds.h"
#include <stdio.h>

#define _SafeRelease(x) {if (NULL != x) { x->Release(); x = NULL; } }

HRESULT SynchronousCreateLun(
    IVdsSubSystem *pSubsystem,
    VDS_LUN_TYPE  type,
    ULONGLONG     ullSize,
    VDS_OBJECT_ID *pDriveIdArray,
    LONG          lNumberOfDrives,
    LPWSTR        pwszUnmaskingList,
    VDS_HINTS     *pHints,
    IVdsLun       **ppLun)
{
    HRESULT hResult = S_OK;
    HRESULT hResult2 = S_OK;
    IVdsAsync *pAsync = NULL;
    VDS_ASYNC_OUTPUT AsyncOut;
    IUnknown* pUnknown = NULL;

    ZeroMemory( &AsyncOut, sizeof(VDS_ASYNC_OUTPUT));

    hResult = pSubsystem->CreateLun(
        type,
        ullSize,
        pDriveIdArray,
        lNumberOfDrives,
        pwszUnmaskingList,
        pHints,
        &pAsync);

    if (SUCCEEDED(hResult) && (!pAsync)) {
        hResult = E_UNEXPECTED; // Errant provider, returned S_OK 
                                // with a NULL pointer.
    }

    if (SUCCEEDED(hResult)) {
        // Wait until the Async is done.
        hResult2 = pAsync->Wait( &hResult, &AsyncOut);
        if (SUCCEEDED(hResult) && FAILED(hResult2)) {
            hResult = hResult2;
        }
    }

    if (SUCCEEDED(hResult) && (VDS_ASYNCOUT_CREATELUN != AsyncOut.type)) {
        hResult = E_UNEXPECTED; // Errant provider, returned S_OK  
                                // with an unexpected type.
    }

    if (SUCCEEDED(hResult)) {
        pUnknown = AsyncOut.cl.pLunUnk;
        if (!pUnknown) {
            hResult = E_UNEXPECTED; // Errant provider, returned 
                                    // S_OK with a NULL pointer.
        }
    }

    if (SUCCEEDED(hResult)) {
        hResult = pUnknown->QueryInterface(IID_IVdsLun, (void **)ppLun);
    }

    _SafeRelease(pAsync);
    _SafeRelease(pUnknown);

    return hResult;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de VDS](using-vds.md)
</dt> <dt>

[Objets d’assistance](helper-objects.md)
</dt> <dt>

[**IVdsSubSystem::CreateLun**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-createlun)
</dt> <dt>

[**IVdsAsync :: wait**](/windows/desktop/api/Vds/nf-vds-ivdsasync-wait)
</dt> <dt>

[**IVdsLun**](/windows/desktop/api/Vds/nn-vds-ivdslun)
</dt> </dl>

 

 
