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
# <a name="enumerating-and-freeing-services"></a>Énumération et libération de services

L’application ELS appelle la fonction [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) pour déterminer les services disponibles sur le système d’exploitation. La fonction peut être utilisée pour énumérer tous les services ELS disponibles ou pour filtrer les services en fonction des critères de recherche fournis par l’application. Lorsque les services ne sont plus nécessaires, l’application appelle [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices).

## <a name="get-all-supported-services"></a>Récupération de tous les services pris en charge

Cet exemple de code illustre l’utilisation de [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) et [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) pour énumérer, puis libérer tous les services disponibles sur le système d’exploitation. Pour ce faire, l’application passe la **valeur null** pour le paramètre *pOptions* de **MappingGetServices**.


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



## <a name="get-specific-services"></a>Accéder à des services spécifiques

L’exemple suivant illustre l’utilisation de [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) et [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) pour énumérer, puis libérer tous les services de la catégorie « détection de langue ». Pour plus d’informations sur cette catégorie de service, consultez [**Microsoft détection de langue**](microsoft-language-detection.md).


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des services linguistiques étendus](using-extended-linguistic-services.md)
</dt> <dt>

[**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices)
</dt> <dt>

[**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices)
</dt> </dl>

 

 



