---
description: Demande de reconnaissance de texte
ms.assetid: 9db9045d-b289-4c6c-9b17-ddbc2c1d3089
title: Demande de reconnaissance de texte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db2442cfa1e26185c4c8d882fe71bb178911f4d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517258"
---
# <a name="requesting-text-recognition"></a><span data-ttu-id="76c60-103">Demande de reconnaissance de texte</span><span class="sxs-lookup"><span data-stu-id="76c60-103">Requesting Text Recognition</span></span>

<span data-ttu-id="76c60-104">L’application appelle la fonction [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) pour demander la reconnaissance de texte à partir d’un service Els spécifique.</span><span class="sxs-lookup"><span data-stu-id="76c60-104">The application calls the [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) function to request text recognition from a specific ELS service.</span></span> <span data-ttu-id="76c60-105">Le service doit avoir été découvert dans un appel précédent à [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices), comme décrit dans [**énumération et libération de services**](enumerating-and-freeing-services.md).</span><span class="sxs-lookup"><span data-stu-id="76c60-105">The service must have been discovered in a previous call to [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices), as described in [**Enumerating and Freeing Services**](enumerating-and-freeing-services.md).</span></span>

> [!Note]  
> <span data-ttu-id="76c60-106">La plateforme peut traiter les appels [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) de façon synchrone ou asynchrone.</span><span class="sxs-lookup"><span data-stu-id="76c60-106">The platform can process [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) calls either synchronously or asynchronously.</span></span>

 

<span data-ttu-id="76c60-107">[**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) gère les types de texte suivants :</span><span class="sxs-lookup"><span data-stu-id="76c60-107">[**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) handles the following types of text:</span></span>

-   <span data-ttu-id="76c60-108">Détection de la langue Microsoft.</span><span class="sxs-lookup"><span data-stu-id="76c60-108">Microsoft language detection.</span></span> <span data-ttu-id="76c60-109">UTF-16, formulaire de normalisation C, texte pour lequel déterminer la langue.</span><span class="sxs-lookup"><span data-stu-id="76c60-109">UTF-16, normalization form C, text for which to determine the language.</span></span>
-   <span data-ttu-id="76c60-110">Détection de scripts Microsoft.</span><span class="sxs-lookup"><span data-stu-id="76c60-110">Microsoft script detection.</span></span> <span data-ttu-id="76c60-111">Texte UTF-16 pour lequel déterminer les plages de scripts.</span><span class="sxs-lookup"><span data-stu-id="76c60-111">UTF-16 text for which to determine script ranges.</span></span>
-   <span data-ttu-id="76c60-112">Services de translittération.</span><span class="sxs-lookup"><span data-stu-id="76c60-112">Transliteration services.</span></span> <span data-ttu-id="76c60-113">Texte UTF-16 écrit dans le script source (système d’écriture).</span><span class="sxs-lookup"><span data-stu-id="76c60-113">UTF-16 text written in source script (writing system).</span></span>

## <a name="use-synchronous-text-recognition"></a><span data-ttu-id="76c60-114">Utiliser la reconnaissance de texte synchrone</span><span class="sxs-lookup"><span data-stu-id="76c60-114">Use Synchronous Text Recognition</span></span>

<span data-ttu-id="76c60-115">Cette section fournit des instructions pour effectuer une reconnaissance de texte synchrone de plusieurs façons.</span><span class="sxs-lookup"><span data-stu-id="76c60-115">This section provides instructions for several ways to perform synchronous text recognition.</span></span>

<span data-ttu-id="76c60-116">**Reconnaissance de texte synchrone avec Microsoft Détection de langue service**</span><span class="sxs-lookup"><span data-stu-id="76c60-116">**Synchronous Text Recognition with Microsoft Language Detection Service**</span></span>

<span data-ttu-id="76c60-117">L’exemple suivant illustre l’utilisation de [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) avec le service Microsoft détection de langue, et imprime tous les résultats extraits par le service.</span><span class="sxs-lookup"><span data-stu-id="76c60-117">The following example illustrates the use of [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) with the Microsoft Language Detection service, and prints all the results retrieved by the service.</span></span> <span data-ttu-id="76c60-118">Le format de sortie de ce service est une structure de [**\_ \_ plage de données de mappage**](/windows/desktop/api/Elscore/ns-elscore-mapping_data_range) unique avec son membre **pData** qui pointe vers un tableau de chaînes au format de Registre et se terminant par deux caractères Unicode.</span><span class="sxs-lookup"><span data-stu-id="76c60-118">The output format of this service is a single [**MAPPING\_DATA\_RANGE**](/windows/desktop/api/Elscore/ns-elscore-mapping_data_range) structure with its **pData** member pointing to a Unicode double-null-terminated, registry-formatted array of strings.</span></span> <span data-ttu-id="76c60-119">Chaque chaîne du tableau se termine par un caractère null et une chaîne vide est utilisée pour spécifier la fin du tableau.</span><span class="sxs-lookup"><span data-stu-id="76c60-119">Every string of the array is null-terminated and an empty string is used to specify the end of the array.</span></span> <span data-ttu-id="76c60-120">Le contenu du tableau est un nom de langue trié par confiance.</span><span class="sxs-lookup"><span data-stu-id="76c60-120">The contents of the array are language names sorted by confidence.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <elscore.h>
#include <elssrvc.h>

#define USER_TEXT ( \
    L"Skip This is a simple sentence. " \
    L"\x0422\x0445\x0438\x0441 \x0438\x0441 \x0415\x043d\x0433\x043b\x0438\x0441\x0445.")
#define USER_TEXT_SKIP (5)

int __cdecl main();
HRESULT CallMappingRecognizeText(PMAPPING_SERVICE_INFO pService);
void PrintAllResults(PMAPPING_PROPERTY_BAG pBag);

int __cdecl main()
{
    MAPPING_ENUM_OPTIONS    EnumOptions;
    PMAPPING_SERVICE_INFO   prgServices = NULL;
    DWORD                   dwServicesCount = 0;
    HRESULT                 hResult;

    ZeroMemory(&EnumOptions, sizeof (MAPPING_ENUM_OPTIONS));
    EnumOptions.Size = sizeof (MAPPING_ENUM_OPTIONS);
    // Using the Language Auto-Detection GUID to enumerate LAD only:
    EnumOptions.pGuid = (GUID *)&ELS_GUID_LANGUAGE_DETECTION;
    hResult = MappingGetServices(&EnumOptions, &prgServices, &dwServicesCount);

    if (SUCCEEDED(hResult))
    {
        hResult = CallMappingRecognizeText(&prgServices[0]);
        if (SUCCEEDED(hResult))
        {
            printf("Calling the service %ws has succeeded!\n",
                prgServices[0].pszDescription);
        }
        else
        {
            printf("Calling the service %ws has failed, failure = 0x%x!\n",
                prgServices[0].pszDescription, hResult);
        }
        MappingFreeServices(prgServices);
    }

    return 0;
}

HRESULT CallMappingRecognizeText(PMAPPING_SERVICE_INFO pService)
{
    MAPPING_PROPERTY_BAG bag;
    HRESULT hResult;

    ZeroMemory(&bag, sizeof (MAPPING_PROPERTY_BAG));
    bag.Size = sizeof (MAPPING_PROPERTY_BAG);

    // MappingRecognizeText's dwIndex parameter specifies the first
    // index inside the text from where the recognition should start.
    // We pass USER_TEXT_SKIP, thus skipping the "Skip " part
    // of the input string.
    // Calling without MAPPING_OPTIONS:
    hResult = MappingRecognizeText(pService, USER_TEXT, wcslen(USER_TEXT), USER_TEXT_SKIP, NULL, &bag);
    if (SUCCEEDED(hResult))
    {
        printf("Results from service: %ws\n", pService->pszDescription);
        PrintAllResults(&bag);
        hResult = MappingFreePropertyBag(&bag);
    }
    return hResult;
}

void PrintAllResults(PMAPPING_PROPERTY_BAG pBag)
{
    WCHAR * p;

    // The return format of the Language Auto-Detection is a
    // double null-terminated registry-formatted array of strings.
    // Every string of the array is null-terminated and there's an
    // empty string specifying the end of the array.
    for (p = (WCHAR *)pBag->prgResultRanges[0].pData; *p; p += wcslen(p) + 1)
    {
        printf("%ws\n", p);
    }
}
```



<span data-ttu-id="76c60-121">**Reconnaissance de texte synchrone avec Microsoft Script Detection service**</span><span class="sxs-lookup"><span data-stu-id="76c60-121">**Synchronous Text Recognition with Microsoft Script Detection Service**</span></span>

<span data-ttu-id="76c60-122">L’exemple suivant illustre l’utilisation de [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) avec le service de détection de script Microsoft et imprime tous les résultats extraits.</span><span class="sxs-lookup"><span data-stu-id="76c60-122">The next example illustrates the use of [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) with the Microsoft Script Detection service, and prints all the retrieved results.</span></span> <span data-ttu-id="76c60-123">Le format de sortie de ce service est un tableau de structures de [**\_ \_ plage de données de mappage**](/windows/desktop/api/Elscore/ns-elscore-mapping_data_range) , chacune spécifiant le texte écrit dans le même script.</span><span class="sxs-lookup"><span data-stu-id="76c60-123">The output format of this service is an array of [**MAPPING\_DATA\_RANGE**](/windows/desktop/api/Elscore/ns-elscore-mapping_data_range) structures, each specifying text written in the same script.</span></span> <span data-ttu-id="76c60-124">Les caractères communs (ZYYY) sont ajoutés à la plage précédente ou à la plage suivante si la plage précédente n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="76c60-124">Common (Zyyy) characters are added to the previous range, or to the next range if the previous range does not exist.</span></span> <span data-ttu-id="76c60-125">Le membre **pData** de chaque structure pointe vers une chaîne Unicode terminée par le caractère null qui contient le nom Unicode standard du script pour la plage particulière.</span><span class="sxs-lookup"><span data-stu-id="76c60-125">The **pData** member of each structure points to a Unicode null-terminated string containing the standard Unicode name of the script for the particular range.</span></span>

> [!Note]  
> <span data-ttu-id="76c60-126">À compter de Windows 7, le service de détection de script Microsoft est conforme à la norme Unicode 5,1.</span><span class="sxs-lookup"><span data-stu-id="76c60-126">As of Windows 7, the Microsoft Script Detection service complies with Unicode 5.1.</span></span>

 


```C++
#include <windows.h>
#include <stdio.h>
#include <elscore.h>
#include <elssrvc.h>

#define USER_TEXT ( \
    L"Skip This is a simple sentence. " \
    L"\x0422\x0445\x0438\x0441 \x0438\x0441 \x0415\x043d\x0433\x043b\x0438\x0441\x0445.")
#define USER_TEXT_SKIP (5)

int __cdecl main();
HRESULT CallMappingRecognizeText(PMAPPING_SERVICE_INFO pService);
void PrintAllResults(PMAPPING_PROPERTY_BAG pBag);

int __cdecl main()
{
    MAPPING_ENUM_OPTIONS    EnumOptions;
    PMAPPING_SERVICE_INFO   prgServices = NULL;
    DWORD                   dwServicesCount = 0;
    HRESULT                 hResult;

    ZeroMemory(&EnumOptions, sizeof (MAPPING_ENUM_OPTIONS));
    EnumOptions.Size = sizeof (MAPPING_ENUM_OPTIONS);
    // Using the Script Detection GUID to enumerate SD only:
    EnumOptions.pGuid = (GUID *)&ELS_GUID_SCRIPT_DETECTION;
    hResult = MappingGetServices(&EnumOptions, &prgServices, &dwServicesCount);

    if (SUCCEEDED(hResult))
    {
        hResult = CallMappingRecognizeText(&prgServices[0]);
        if (SUCCEEDED(hResult))
        {
            printf("Calling the service %ws has succeeded!\n",
                prgServices[0].pszDescription);
        }
        else
        {
            printf("Calling the service %ws has failed, failure = 0x%x!\n",
                prgServices[0].pszDescription, hResult);
        }
        MappingFreeServices(prgServices);
    }

    return 0;
}

HRESULT CallMappingRecognizeText(PMAPPING_SERVICE_INFO pService)
{
    MAPPING_PROPERTY_BAG bag;
    HRESULT hResult;

    ZeroMemory(&bag, sizeof (MAPPING_PROPERTY_BAG));
    bag.Size = sizeof (MAPPING_PROPERTY_BAG);

    // MappingRecognizeText's dwIndex parameter specifies the first
    // index inside the text from where the recognition should start.
    // We pass USER_TEXT_SKIP, thus skipping the "Skip " part
    // of the input string.
    // Calling without MAPPING_OPTIONS:
    hResult = MappingRecognizeText(pService, USER_TEXT, wcslen(USER_TEXT), USER_TEXT_SKIP, NULL, &bag);
    if (SUCCEEDED(hResult))
    {
        printf("Results from service: %ws\n", pService->pszDescription);
        PrintAllResults(&bag);
        hResult = MappingFreePropertyBag(&bag);
    }
    return hResult;
}

void PrintAllResults(PMAPPING_PROPERTY_BAG pBag)
{
    DWORD dwRangeIndex;

    for (dwRangeIndex = 0; dwRangeIndex < pBag->dwRangesCount; ++dwRangeIndex)
    {
        if (dwRangeIndex > 0)
        {
            printf("   ----\n");
        }
        printf("Range from %u to %u\n",
            (unsigned)pBag->prgResultRanges[dwRangeIndex].dwStartIndex,
            (unsigned)pBag->prgResultRanges[dwRangeIndex].dwEndIndex);
        printf("Data size in WCHARs: %u\n",
            (unsigned)pBag->prgResultRanges[dwRangeIndex].dwDataSize / 2);
        printf("\"%ws\"\n", (WCHAR *)pBag->prgResultRanges[dwRangeIndex].pData);
    }
}
```



<span data-ttu-id="76c60-127">**Reconnaissance de texte synchrone avec le service de translittération Microsoft cyrillique vers latin**</span><span class="sxs-lookup"><span data-stu-id="76c60-127">**Synchronous Text Recognition with Microsoft Cyrillic to Latin Transliteration Service**</span></span>

<span data-ttu-id="76c60-128">L’exemple suivant illustre l’utilisation de [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) avec le service de translittération Microsoft cyrillique vers latin, et imprime les résultats récupérés.</span><span class="sxs-lookup"><span data-stu-id="76c60-128">The following example illustrates the use of [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) with the Microsoft Cyrillic to Latin transliteration service, and prints the retrieved results.</span></span> <span data-ttu-id="76c60-129">Notez les deux façons différentes d’énumérer ce service, soit par GUID, soit par catégorie et par script d’entrée.</span><span class="sxs-lookup"><span data-stu-id="76c60-129">Note the two different ways to enumerate this service, either by GUID or by category and input script.</span></span>

<span data-ttu-id="76c60-130">Le format de sortie est le même pour tous les services de translittération disponibles.</span><span class="sxs-lookup"><span data-stu-id="76c60-130">The output format is the same for all available transliteration services.</span></span> <span data-ttu-id="76c60-131">Il s’agit d’une structure de [**\_ \_ plage de données de mappage**](/windows/desktop/api/Elscore/ns-elscore-mapping_data_range) unique avec son membre **pData** pointant vers un tableau de caractères Unicode représentant le texte d’origine de la transcription dans le script de sortie en appliquant uniquement les règles du service de translittération spécifique.</span><span class="sxs-lookup"><span data-stu-id="76c60-131">It is a single [**MAPPING\_DATA\_RANGE**](/windows/desktop/api/Elscore/ns-elscore-mapping_data_range) structure with its **pData** member pointing to an array of Unicode characters representing the original text transliterated into the output script by applying only the rules of the specific transliteration service.</span></span> <span data-ttu-id="76c60-132">Ce service ne termine pas sa sortie si l’entrée ne contient pas le caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="76c60-132">This service does not null-terminate its output if the input does not contain the terminating null character.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <elscore.h>
#include <elssrvc.h>

#define USER_TEXT (L"Skip The russian word for 'yes' is transliterated to Latin as '\x0434\x0430'.")
#define USER_TEXT_SKIP (5)

int __cdecl main();
HRESULT CallMappingRecognizeText(PMAPPING_SERVICE_INFO pService);
void PrintAllResults(PMAPPING_PROPERTY_BAG pBag);

int __cdecl main()
{
    MAPPING_ENUM_OPTIONS    EnumOptions;
    PMAPPING_SERVICE_INFO   prgServices;
    DWORD                   dwServicesCount;
    HRESULT                 hResult;

    // 1. Enumerate by GUID:
    prgServices = NULL;
    dwServicesCount = 0;
    ZeroMemory(&EnumOptions, sizeof (MAPPING_ENUM_OPTIONS));
    EnumOptions.Size = sizeof (MAPPING_ENUM_OPTIONS);
    // Use the Cyrl->Latn Transliteration GUID to enumerate only this service:
    EnumOptions.pGuid = (GUID *)&ELS_GUID_TRANSLITERATION_CYRILLIC_TO_LATIN;
    hResult = MappingGetServices(&EnumOptions, &prgServices, &dwServicesCount);

    if (SUCCEEDED(hResult))
    {
        hResult = CallMappingRecognizeText(&prgServices[0]);
        if (SUCCEEDED(hResult))
        {
            printf("Calling the service %ws has succeeded!\n",
                prgServices[0].pszDescription);
        }
        else
        {
            printf("Calling the service %ws has failed, failure = 0x%x!\n",
                prgServices[0].pszDescription, hResult);
        }
        MappingFreeServices(prgServices);
    }

    printf("--\n");

    // 2. Enumerate by input script and category:
    prgServices = NULL;
    dwServicesCount = 0;
    ZeroMemory(&EnumOptions, sizeof (MAPPING_ENUM_OPTIONS));
    EnumOptions.Size = sizeof (MAPPING_ENUM_OPTIONS);
    EnumOptions.pszCategory = L"Transliteration";
    EnumOptions.pszInputScript = L"Cyrl";
    hResult = MappingGetServices(&EnumOptions, &prgServices, &dwServicesCount);

    if (SUCCEEDED(hResult))
    {
        hResult = CallMappingRecognizeText(&prgServices[0]);
        if (SUCCEEDED(hResult))
        {
            printf("Calling the service %ws has succeeded!\n",
                prgServices[0].pszDescription);
        }
        else
        {
            printf("Calling the service %ws has failed, failure = 0x%x!\n",
                prgServices[0].pszDescription, hResult);
        }
        MappingFreeServices(prgServices);
    }

    return 0;
}

HRESULT CallMappingRecognizeText(PMAPPING_SERVICE_INFO pService)
{
    MAPPING_PROPERTY_BAG bag;
    HRESULT hResult;

    ZeroMemory(&bag, sizeof (MAPPING_PROPERTY_BAG));
    bag.Size = sizeof (MAPPING_PROPERTY_BAG);

    // MappingRecognizeText's dwIndex parameter specifies the first
    // index inside the text from where the recognition should start.
    // We pass USER_TEXT_SKIP, thus skipping the "Skip " part
    // of the input string.
    // Calling without MAPPING_OPTIONS:
    // We want the result to be null-terminated for display.
    // That's why we will also pass the input null terminator:
    hResult = MappingRecognizeText(pService, USER_TEXT, wcslen(USER_TEXT) + 1, USER_TEXT_SKIP, NULL, &bag);
    if (SUCCEEDED(hResult))
    {
        printf("Results from service: %ws\n", pService->pszDescription);
        PrintAllResults(&bag);
        hResult = MappingFreePropertyBag(&bag);
    }
    return hResult;
}

void PrintAllResults(PMAPPING_PROPERTY_BAG pBag)
{
    printf("\"%ws\"\n", (WCHAR *)pBag->prgResultRanges[0].pData);
}
```



<span data-ttu-id="76c60-133">**Reconnaissance de texte synchrone avec un appel à tous les services disponibles**</span><span class="sxs-lookup"><span data-stu-id="76c60-133">**Synchronous Text Recognition with a Call to All Available Services**</span></span>

<span data-ttu-id="76c60-134">L’exemple suivant illustre l’utilisation de [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) avec tous les services disponibles et imprime les résultats récupérés pour tous les services.</span><span class="sxs-lookup"><span data-stu-id="76c60-134">The following example shows the use of [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) with all available services, and prints the retrieved results for all the services.</span></span> <span data-ttu-id="76c60-135">Cet exemple fournit une bonne illustration du fonctionnement de chaque service.</span><span class="sxs-lookup"><span data-stu-id="76c60-135">This example provides a good illustration of the operation of each service.</span></span> <span data-ttu-id="76c60-136">En examinant la sortie de l’exemple d’application, il est facile de savoir ce qui se passe en interne avec les services.</span><span class="sxs-lookup"><span data-stu-id="76c60-136">By looking at the output of the example application, it is easy to find out what is happening internally with the services.</span></span> <span data-ttu-id="76c60-137">Cet exemple montre également que presque tout le code utilisé pour appeler l’un des services ELS est le même.</span><span class="sxs-lookup"><span data-stu-id="76c60-137">This example also shows that almost all code used to call any of the ELS services is the same.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <elscore.h>

#define USER_TEXT ( \
    L"Skip This is a simple sentence. " \
    L"\x0422\x0445\x0438\x0441 \x0438\x0441 \x0415\x043d\x0433\x043b\x0438\x0441\x0445.")
#define USER_TEXT_SKIP (5)

int __cdecl main();
HRESULT CallMappingRecognizeText(PMAPPING_SERVICE_INFO pService);
void PrintAllResults(PMAPPING_PROPERTY_BAG pBag);

int __cdecl main()
{
    PMAPPING_SERVICE_INFO   prgServices = NULL;
    DWORD                   dwServicesCount = 0;
    HRESULT                 hResult;

    DWORD i;

    // Get all installed ELS services:
    hResult = MappingGetServices(NULL, &prgServices, &dwServicesCount);

    if (SUCCEEDED(hResult))
    {
        for (i = 0; i < dwServicesCount; ++i)
        {
            // Do something with each service:
            // ... prgServices[i] ...
            if (i > 0)
            {
                printf("--\n");
            }
            hResult = CallMappingRecognizeText(&prgServices[i]);
            if (SUCCEEDED(hResult))
            {
                printf("Calling the service %ws has succeeded!\n",
                    prgServices[i].pszDescription);
            }
            else
            {
                printf("Calling the service %ws has failed, failure = 0x%x!\n",
                    prgServices[i].pszDescription, hResult);
            }
        }
        MappingFreeServices(prgServices);
    }

    return 0;
}

HRESULT CallMappingRecognizeText(PMAPPING_SERVICE_INFO pService)
{
    MAPPING_PROPERTY_BAG bag;
    HRESULT hResult;

    ZeroMemory(&bag, sizeof (MAPPING_PROPERTY_BAG));
    bag.Size = sizeof (MAPPING_PROPERTY_BAG);

    // MappingRecognizeText's dwIndex parameter specifies the first
    // index inside the text from where the recognition should start.
    // We pass USER_TEXT_SKIP, thus skipping the "Skip " part
    // of the input string.
    // Calling without MAPPING_OPTIONS:
    hResult = MappingRecognizeText(pService, USER_TEXT, wcslen(USER_TEXT), USER_TEXT_SKIP, NULL, &bag);
    if (SUCCEEDED(hResult))
    {
        printf("Results from service: %ws\n", pService->pszDescription);
        PrintAllResults(&bag);
        hResult = MappingFreePropertyBag(&bag);
    }
    return hResult;
}

void PrintAllResults(PMAPPING_PROPERTY_BAG pBag)
{
    DWORD dwRangeIndex;
    DWORD dwDataIndex;
    WCHAR c;

    for (dwRangeIndex = 0; dwRangeIndex < pBag->dwRangesCount; ++dwRangeIndex)
    {
        if (dwRangeIndex > 0)
        {
            printf("   ----\n");
        }
        printf("Range from %u to %u\n",
            (unsigned)pBag->prgResultRanges[dwRangeIndex].dwStartIndex,
            (unsigned)pBag->prgResultRanges[dwRangeIndex].dwEndIndex);
        // Currently, we can treat all results as arrays of unicode WCHAR
        // characters, but there can be services in the future
        // that use different formatting, i.e. XML, HTML, etc.
        printf("Data size in WCHARs: %u\n",
            (unsigned)pBag->prgResultRanges[dwRangeIndex].dwDataSize / 2);
        printf("\"");
        for (dwDataIndex = 0; dwDataIndex < pBag->prgResultRanges[dwRangeIndex].dwDataSize / 2; ++dwDataIndex)
        {
            c = ((WCHAR *)pBag->prgResultRanges[dwRangeIndex].pData)[dwDataIndex];
            if (c >= 32 && c < 128 && c != '"') printf("%wc", c);
            else printf("#%x", (unsigned)c);
        }
        printf("\"\n");
    }
}

void CallRecognizeText(LPCWSTR Category, LPCWSTR Text)
{
    HRESULT               Result;
    PMAPPING_SERVICE_INFO rgServices;
    DWORD                 ServicesCount;
    MAPPING_ENUM_OPTIONS  options = {sizeof(MAPPING_ENUM_OPTIONS), (LPWSTR) Category, 0};

    Result = MappingGetServices(&options, &rgServices, &ServicesCount);
    if (Result == S_OK && ServicesCount > 0)
    {
        MAPPING_PROPERTY_BAG bag = { sizeof(MAPPING_PROPERTY_BAG), 0};
        Result = MappingRecognizeText(&rgServices[0], Text, wcslen(Text), 0, NULL, &bag);
        if (Result == S_OK)
        {
            MappingFreePropertyBag(&bag);
        }

        MappingFreeServices(rgServices);
    }
}
int _tmain(int argc, _TCHAR* argv[])
{
    CallRecognizeText(L"Language Detection", L"Text to be recognized");
  
    UNREFERENCED_PARAMETER(argc);
    UNREFERENCED_PARAMETER(argv);
    return 0;
}
```



## <a name="use-asynchronous-text-recognition"></a><span data-ttu-id="76c60-138">Utiliser la reconnaissance de texte asynchrone</span><span class="sxs-lookup"><span data-stu-id="76c60-138">Use Asynchronous Text Recognition</span></span>

<span data-ttu-id="76c60-139">L’exemple suivant illustre l’utilisation de [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) pour la reconnaissance de texte asynchrone.</span><span class="sxs-lookup"><span data-stu-id="76c60-139">The following example shows the use of [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) for asynchronous text recognition.</span></span> <span data-ttu-id="76c60-140">Lorsque le rappel est utilisé, l’application doit s’assurer que le conteneur de propriétés, le texte d’entrée, les options et le service sont tous valides jusqu’à la fin de l’exécution du rappel.</span><span class="sxs-lookup"><span data-stu-id="76c60-140">When the callback is used, the application must make sure that the property bag, the input text, the options, and the service are all valid until after the callback has finished executing.</span></span>

<span data-ttu-id="76c60-141">L’application doit appeler [**MappingFreePropertyBag**](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag) immédiatement après que le conteneur a été consommé par la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="76c60-141">The application must call [**MappingFreePropertyBag**](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag) immediately after the bag is consumed by the callback function.</span></span> <span data-ttu-id="76c60-142">Pour plus d’informations, consultez [fourniture de rappels pour les services Els](providing-callbacks-for-els-services.md).</span><span class="sxs-lookup"><span data-stu-id="76c60-142">For more information, see [Providing Callbacks for ELS Services](providing-callbacks-for-els-services.md).</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <elscore.h>
#include <elssrvc.h>

#define USER_TEXT ( \
    L"Skip This is a simple sentence. " \
    L"\x0422\x0445\x0438\x0441 \x0438\x0441 \x0415\x043d\x0433\x043b\x0438\x0441\x0445.")
#define USER_TEXT_SKIP (5)

int __cdecl main();
HRESULT CallMappingRecognizeText(PMAPPING_SERVICE_INFO pService);
void RecognizeCallback(PMAPPING_PROPERTY_BAG pBag, LPVOID data, DWORD dwDataSize, HRESULT Result);

int __cdecl main()
{
    MAPPING_ENUM_OPTIONS    EnumOptions;
    PMAPPING_SERVICE_INFO   prgServices = NULL;
    DWORD                   dwServicesCount = 0;
    HRESULT                 hResult;

    ZeroMemory(&EnumOptions, sizeof (MAPPING_ENUM_OPTIONS));
    EnumOptions.Size = sizeof (MAPPING_ENUM_OPTIONS);
    // Using the Language Auto-Detection GUID to enumerate LAD only:
    EnumOptions.pGuid = (GUID *)&ELS_GUID_LANGUAGE_DETECTION;
    hResult = MappingGetServices(&EnumOptions, &prgServices, &dwServicesCount);

    if (SUCCEEDED(hResult))
    {
        hResult = CallMappingRecognizeText(&prgServices[0]);
        if (SUCCEEDED(hResult))
        {
            printf("Calling the service %ws has succeeded!\n",
                prgServices[0].pszDescription);
        }
        else
        {
            printf("Calling the service %ws has failed, failure = 0x%x!\n",
                prgServices[0].pszDescription, hResult);
        }
        MappingFreeServices(prgServices);
    }

    return 0;
}

HRESULT CallMappingRecognizeText(PMAPPING_SERVICE_INFO pService)
{
    MAPPING_PROPERTY_BAG    bag;
    MAPPING_OPTIONS         Options;
    HRESULT                 hResult;
    HANDLE                  SyncEvent;
    DWORD                   dwWaitResult;

    SyncEvent = CreateEvent(NULL, FALSE, FALSE, NULL);

    if (SyncEvent == NULL)
    {
        hResult = E_FAIL;
    }
    else
    {
        ZeroMemory(&bag, sizeof (MAPPING_PROPERTY_BAG));
        bag.Size = sizeof (MAPPING_PROPERTY_BAG);

        ZeroMemory(&Options, sizeof (MAPPING_OPTIONS));
        Options.Size = sizeof (MAPPING_OPTIONS);
        Options.pfnRecognizeCallback = (PFN_MAPPINGCALLBACKPROC)RecognizeCallback;
        Options.pRecognizeCallerData = &SyncEvent;
        Options.dwRecognizeCallerDataSize = sizeof (HANDLE);

        // MappingRecognizeText's dwIndex parameter specifies the first
        // index inside the text from where the recognition should start.
        // We pass USER_TEXT_SKIP, thus skipping the "Skip " part
        // of the input string.
        hResult = MappingRecognizeText(pService, USER_TEXT, wcslen(USER_TEXT), USER_TEXT_SKIP, &Options, &bag);
        if (SUCCEEDED(hResult))
        {
            // We are using an event to synchronize our waiting for the call to end,
            // because some objects have to be valid till the end of the callback call:
            // - the input text
            // - the property bag
            // - the options
            // - the service
            dwWaitResult = WaitForSingleObject(SyncEvent, INFINITE);
            if (dwWaitResult != WAIT_OBJECT_0)
            {
                hResult = E_FAIL;
            }
        }
        CloseHandle(SyncEvent);
    }
    return hResult;
}

void RecognizeCallback(PMAPPING_PROPERTY_BAG pBag, LPVOID data, DWORD dwDataSize, HRESULT Result)
{
    HANDLE SyncEvent;
    WCHAR * p;

    UNREFERENCED_PARAMETER(dwDataSize);

    if (SUCCEEDED(Result))
    {
        for (p = (WCHAR *)pBag->prgResultRanges[0].pData; *p; p += wcslen(p) + 1)
        {
            printf("%ws\n", p);
        }
        MappingFreePropertyBag(pBag);
    }

    SyncEvent = *((HANDLE *)data);
    SetEvent(SyncEvent);
}
```



## <a name="related-topics"></a><span data-ttu-id="76c60-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="76c60-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76c60-144">Utilisation des services linguistiques étendus</span><span class="sxs-lookup"><span data-stu-id="76c60-144">Using Extended Linguistic Services</span></span>](using-extended-linguistic-services.md)
</dt> <dt>

[<span data-ttu-id="76c60-145">Fourniture de rappels pour les services ELS</span><span class="sxs-lookup"><span data-stu-id="76c60-145">Providing Callbacks for ELS Services</span></span>](providing-callbacks-for-els-services.md)
</dt> <dt>

[<span data-ttu-id="76c60-146">**MappingFreePropertyBag**</span><span class="sxs-lookup"><span data-stu-id="76c60-146">**MappingFreePropertyBag**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag)
</dt> <dt>

[<span data-ttu-id="76c60-147">**MappingGetServices**</span><span class="sxs-lookup"><span data-stu-id="76c60-147">**MappingGetServices**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices)
</dt> <dt>

[<span data-ttu-id="76c60-148">**MappingRecognizeText**</span><span class="sxs-lookup"><span data-stu-id="76c60-148">**MappingRecognizeText**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext)
</dt> </dl>

 

 



