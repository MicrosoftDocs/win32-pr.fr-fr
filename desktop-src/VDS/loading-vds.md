---
description: Chargement de VDS
ms.assetid: 6b75fdb2-3d4c-4419-96e8-8677439e366b
title: Chargement de VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01c66685668641f3036739c57bd7353f72052c6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526149"
---
# <a name="loading-vds"></a><span data-ttu-id="608fd-103">Chargement de VDS</span><span class="sxs-lookup"><span data-stu-id="608fd-103">Loading VDS</span></span>

<span data-ttu-id="608fd-104">\[À compter de Windows 8 et de Windows Server 2012, l’interface com du [service de disque virtuel](virtual-disk-service-portal.md) est remplacée par l' [API de gestion de stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="608fd-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="608fd-105">**Pour charger et initialiser VDS**</span><span class="sxs-lookup"><span data-stu-id="608fd-105">**To load and initialize VDS**</span></span>

1.  <span data-ttu-id="608fd-106">Libère les interfaces non null.</span><span class="sxs-lookup"><span data-stu-id="608fd-106">Release non-null interfaces.</span></span>
2.  <span data-ttu-id="608fd-107">Appelez la fonction [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), [**CoCreateInstanceEx**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstanceex)ou [**CoGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-cogetclassobject) pour obtenir un pointeur vers l’objet service Loader.</span><span class="sxs-lookup"><span data-stu-id="608fd-107">Call the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), [**CoCreateInstanceEx**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstanceex), or [**CoGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-cogetclassobject) function to obtain a pointer to the service loader object.</span></span>

    <span data-ttu-id="608fd-108">**CLSCTX \_ Impossible \_** de spécifier AAA dans cet appel.</span><span class="sxs-lookup"><span data-stu-id="608fd-108">**CLSCTX\_DISABLE\_AAA** cannot be specified in this call.</span></span> <span data-ttu-id="608fd-109">Si la méthode [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) est appelée, **EOAC \_ Disable \_ AAA** ne peut pas être spécifié dans le paramètre *dwCapabilities* .</span><span class="sxs-lookup"><span data-stu-id="608fd-109">If [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) is called, **EOAC\_DISABLE\_AAA** cannot be specified in the *dwCapabilities* parameter.</span></span>

3.  <span data-ttu-id="608fd-110">Appelez la méthode [**IVdsServiceLoader :: LoadService**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice) pour charger VDS.</span><span class="sxs-lookup"><span data-stu-id="608fd-110">Call the [**IVdsServiceLoader::LoadService**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice) method to load VDS.</span></span>

    <span data-ttu-id="608fd-111">Le passage de la **valeur null** en tant que premier paramètre charge et initialise VDS sur l’hôte local.</span><span class="sxs-lookup"><span data-stu-id="608fd-111">Passing **NULL** as the first parameter loads and initializes VDS on the local host.</span></span>

4.  <span data-ttu-id="608fd-112">Appelez la méthode [**IVdsService :: WaitForServiceReady**](/windows/desktop/api/Vds/nf-vds-ivdsservice-waitforserviceready) pour attendre la fin de l’initialisation de VDS.</span><span class="sxs-lookup"><span data-stu-id="608fd-112">Call the [**IVdsService::WaitForServiceReady**](/windows/desktop/api/Vds/nf-vds-ivdsservice-waitforserviceready) method to wait for VDS initialization to complete.</span></span>

<span data-ttu-id="608fd-113">L’exemple de code suivant initialise le service qui retourne un pointeur vers l’objet de service.</span><span class="sxs-lookup"><span data-stu-id="608fd-113">The following code example initializes the service that returns a pointer to the service object.</span></span>


```C++
#include "initguid.h"
#include "vds.h"
#include <stdio.h>

#pragma comment( lib, "ole32.lib" )

//
// Simple macro to release non-null interfaces.
//
#define _SafeRelease(x) {if (NULL != x) { x->Release(); x = NULL; } }

void __cdecl main(void) 
{
    HRESULT hResult;
    IVdsService *pService = NULL;
    IVdsServiceLoader *pLoader = NULL;

    // For this, you first get a pointer to the VDS Loader
    // Launch the VDS service. 
    //

    hResult = CoInitialize(NULL);

    if (SUCCEEDED(hResult)) 
    {
    
        hResult = CoCreateInstance(CLSID_VdsLoader,
            NULL,
            CLSCTX_LOCAL_SERVER,
            IID_IVdsServiceLoader,
            (void **) &pLoader);

        // 
        // And then load VDS on the local computer.
        //
        if (SUCCEEDED(hResult)) 
        {
            hResult = pLoader->LoadService(NULL, &pService);
        }

        //
        // You're done with the Loader interface at this point.
        //
        _SafeRelease(pLoader); 
        
        if (SUCCEEDED(hResult)) 
        {
            hResult = pService->WaitForServiceReady();
            if (SUCCEEDED(hResult)) 
            {
                //
                // You obtained an interface to the service: pService.
                // This interface can now be used to query for providers 
                // and perform other operations. 
                //
                printf("VDS Service Loaded");
            }

        } 
        else 
        {
            printf("VDS Service failed hr=%x\n",hResult);
        }
    }
}

```



## <a name="related-topics"></a><span data-ttu-id="608fd-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="608fd-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="608fd-115">Utilisation de VDS</span><span class="sxs-lookup"><span data-stu-id="608fd-115">Using VDS</span></span>](using-vds.md)
</dt> <dt>

[<span data-ttu-id="608fd-116">**IVdsService::WaitForServiceReady**</span><span class="sxs-lookup"><span data-stu-id="608fd-116">**IVdsService::WaitForServiceReady**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsservice-waitforserviceready)
</dt> <dt>

[<span data-ttu-id="608fd-117">**IVdsServiceLoader::LoadService**</span><span class="sxs-lookup"><span data-stu-id="608fd-117">**IVdsServiceLoader::LoadService**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice)
</dt> <dt>

[<span data-ttu-id="608fd-118">Objets d’installation et de service</span><span class="sxs-lookup"><span data-stu-id="608fd-118">Setup and Service Objects</span></span>](startup-and-service-objects.md)
</dt> </dl>

 

 
