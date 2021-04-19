---
description: Énumération et libération de services
ms.assetid: 526e51c7-9ff2-4590-b092-172f4942ce8e
title: Énumération et libération de services
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 859abe590ccaf2f71df676d5989778d5b391be57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541955"
---
# <a name="enumerating-and-freeing-services"></a><span data-ttu-id="ea498-103">Énumération et libération de services</span><span class="sxs-lookup"><span data-stu-id="ea498-103">Enumerating and Freeing Services</span></span>

<span data-ttu-id="ea498-104">L’application ELS appelle la fonction [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) pour déterminer les services disponibles sur le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="ea498-104">The ELS application calls the [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) function to determine the services that are available on the operating system.</span></span> <span data-ttu-id="ea498-105">La fonction peut être utilisée pour énumérer tous les services ELS disponibles ou pour filtrer les services en fonction des critères de recherche fournis par l’application.</span><span class="sxs-lookup"><span data-stu-id="ea498-105">The function can be used either to enumerate all available ELS services, or to filter the services based on application-provided search criteria.</span></span> <span data-ttu-id="ea498-106">Lorsque les services ne sont plus nécessaires, l’application appelle [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices).</span><span class="sxs-lookup"><span data-stu-id="ea498-106">When services are no longer needed, the application calls [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices).</span></span>

## <a name="get-all-supported-services"></a><span data-ttu-id="ea498-107">Récupération de tous les services pris en charge</span><span class="sxs-lookup"><span data-stu-id="ea498-107">Get All Supported Services</span></span>

<span data-ttu-id="ea498-108">Cet exemple de code illustre l’utilisation de [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) et [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) pour énumérer, puis libérer tous les services disponibles sur le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="ea498-108">This code example illustrates the use of [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) and [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) to enumerate and then free all available services on the operating system.</span></span> <span data-ttu-id="ea498-109">Pour ce faire, l’application passe la **valeur null** pour le paramètre *pOptions* de **MappingGetServices**.</span><span class="sxs-lookup"><span data-stu-id="ea498-109">To do this, the application passes **NULL** for the *pOptions* parameter of **MappingGetServices**.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <elscore.h>

int __cdecl main()
{
    PMAPPING_SERVICE_INFO   prgServices = NULL;
    DWORD                   dwServicesCount = 0;
    HRESULT                 Result;
    DWORD                   i;

    // Get all installed ELS services.
    Result = MappingGetServices(NULL, &prgServices, &dwServicesCount);

    if (SUCCEEDED(Result))
    {
        for (i = 0; i < dwServicesCount; ++i)
        {
            // Do something with each service.
            // ... prgServices[i] ...
            printf_s("Service: %ws, category: %ws\n",
                prgServices[i].pszDescription, prgServices[i].pszCategory);
        }
        MappingFreeServices(prgServices);
    }
    return 0;
}
```



## <a name="get-specific-services"></a><span data-ttu-id="ea498-110">Accéder à des services spécifiques</span><span class="sxs-lookup"><span data-stu-id="ea498-110">Get Specific Services</span></span>

<span data-ttu-id="ea498-111">L’exemple suivant illustre l’utilisation de [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) et [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) pour énumérer, puis libérer tous les services de la catégorie « détection de langue ».</span><span class="sxs-lookup"><span data-stu-id="ea498-111">The next example illustrates the use of [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) and [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) to enumerate and then free all services of category "Language Detection".</span></span> <span data-ttu-id="ea498-112">Pour plus d’informations sur cette catégorie de service, consultez [**Microsoft détection de langue**](microsoft-language-detection.md).</span><span class="sxs-lookup"><span data-stu-id="ea498-112">For more information about this service category, see [**Microsoft Language Detection**](microsoft-language-detection.md).</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <elscore.h>

int __cdecl main()
{
    MAPPING_ENUM_OPTIONS    EnumOptions;
    PMAPPING_SERVICE_INFO   prgServices = NULL;
    DWORD                   dwServicesCount = 0;
    HRESULT                 Result;
    DWORD                   i;

    ZeroMemory(&EnumOptions, sizeof (MAPPING_ENUM_OPTIONS));
    EnumOptions.Size = sizeof (MAPPING_ENUM_OPTIONS);

    // Use the Language Auto-Detection category to enumerate
    // all language detection services.
    EnumOptions.pszCategory = L"Language Detection";

    // Execute the enumeration:
    Result = MappingGetServices(&EnumOptions, &prgServices, &dwServicesCount);

    if (SUCCEEDED(Result))
    {
        for (i = 0; i < dwServicesCount; ++i)
        {
            // Do something with each service.
            // ... prgServices[i] ...
            printf_s("Service: %ws, category: %ws\n",
                prgServices[i].pszDescription, prgServices[i].pszCategory);
        }
        MappingFreeServices(prgServices);
    }
    return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="ea498-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ea498-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea498-114">Utilisation des services linguistiques étendus</span><span class="sxs-lookup"><span data-stu-id="ea498-114">Using Extended Linguistic Services</span></span>](using-extended-linguistic-services.md)
</dt> <dt>

[<span data-ttu-id="ea498-115">**MappingFreeServices**</span><span class="sxs-lookup"><span data-stu-id="ea498-115">**MappingFreeServices**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices)
</dt> <dt>

[<span data-ttu-id="ea498-116">**MappingGetServices**</span><span class="sxs-lookup"><span data-stu-id="ea498-116">**MappingGetServices**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices)
</dt> </dl>

 

 



