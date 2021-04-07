---
description: Gestion des opérations asynchrones
ms.assetid: e5136e15-3ae1-4e0a-ae97-fcf16203b21d
title: Gestion des opérations asynchrones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d220c5633f9ee044dbf9cdb6a63b563747620afd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952351"
---
# <a name="managing-asynchronous-operations"></a><span data-ttu-id="2ef1c-103">Gestion des opérations asynchrones</span><span class="sxs-lookup"><span data-stu-id="2ef1c-103">Managing Asynchronous Operations</span></span>

<span data-ttu-id="2ef1c-104">\[À compter de Windows 8 et de Windows Server 2012, le [service de disque virtuel](virtual-disk-service-portal.md) est remplacé par l' [API de gestion de stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2ef1c-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="2ef1c-105">L’exemple de code suivant montre comment un appelant travaille avec un objet Async.</span><span class="sxs-lookup"><span data-stu-id="2ef1c-105">The code example that follows demonstrates how a caller works with an async object.</span></span> <span data-ttu-id="2ef1c-106">Ici, la fonction **SynchronousCreateLun** appelle la méthode asynchrone [**IVdsSubSystem :: CreateLun**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-createlun) à l’aide des paramètres donnés.</span><span class="sxs-lookup"><span data-stu-id="2ef1c-106">Here, the **SynchronousCreateLun** function calls the asynchronous [**IVdsSubSystem::CreateLun**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-createlun) method using the given parameters.</span></span> <span data-ttu-id="2ef1c-107">La fonction attend que l’appel de la méthode **CreateLun** asynchrone se termine sur l’objet Async.</span><span class="sxs-lookup"><span data-stu-id="2ef1c-107">The function will wait on the async object for the asynchronous **CreateLun** method call to finish.</span></span> <span data-ttu-id="2ef1c-108">Quand la méthode [**IVdsAsync :: wait**](/windows/desktop/api/Vds/nf-vds-ivdsasync-wait) retourne, **SynchronousCreateLun** obtient l’interface [**IVdsLun**](/windows/desktop/api/Vds/nn-vds-ivdslun) pour le LUN nouvellement créé et le retourne comme argument out.</span><span class="sxs-lookup"><span data-stu-id="2ef1c-108">When the [**IVdsAsync::Wait**](/windows/desktop/api/Vds/nf-vds-ivdsasync-wait) method returns, **SynchronousCreateLun** gets the [**IVdsLun**](/windows/desktop/api/Vds/nn-vds-ivdslun) interface for the newly created LUN and returns it as an out argument.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="2ef1c-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2ef1c-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ef1c-110">Utilisation de VDS</span><span class="sxs-lookup"><span data-stu-id="2ef1c-110">Using VDS</span></span>](using-vds.md)
</dt> <dt>

[<span data-ttu-id="2ef1c-111">Objets d’assistance</span><span class="sxs-lookup"><span data-stu-id="2ef1c-111">Helper Objects</span></span>](helper-objects.md)
</dt> <dt>

[<span data-ttu-id="2ef1c-112">**IVdsSubSystem::CreateLun**</span><span class="sxs-lookup"><span data-stu-id="2ef1c-112">**IVdsSubSystem::CreateLun**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-createlun)
</dt> <dt>

[<span data-ttu-id="2ef1c-113">**IVdsAsync :: wait**</span><span class="sxs-lookup"><span data-stu-id="2ef1c-113">**IVdsAsync::Wait**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsasync-wait)
</dt> <dt>

[<span data-ttu-id="2ef1c-114">**IVdsLun**</span><span class="sxs-lookup"><span data-stu-id="2ef1c-114">**IVdsLun**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdslun)
</dt> </dl>

 

 
