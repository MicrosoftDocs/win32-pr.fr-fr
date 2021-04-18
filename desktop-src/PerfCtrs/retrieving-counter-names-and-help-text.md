---
description: Les données de performances contiennent des valeurs d’index que vous utilisez pour localiser les noms et le texte d’aide pour chaque objet et compteur inscrits.
ms.assetid: 9ddd1672-61cf-41c2-bec0-0d2b775bf970
title: Récupération des noms de compteur et du texte d’aide
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5b49f852e6af22dc2ec31d341ee6176913f98e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533893"
---
# <a name="retrieving-counter-names-and-help-text"></a><span data-ttu-id="573fb-103">Récupération des noms de compteur et du texte d’aide</span><span class="sxs-lookup"><span data-stu-id="573fb-103">Retrieving Counter Names and Help Text</span></span>

<span data-ttu-id="573fb-104">Les données de performances contiennent des valeurs d’index que vous utilisez pour localiser les noms et le texte d’aide pour chaque objet et compteur inscrits.</span><span class="sxs-lookup"><span data-stu-id="573fb-104">The performance data contains index values that you use to locate the names and help text for each registered object and counter.</span></span> <span data-ttu-id="573fb-105">Les membres **ObjectNameTitleIndex** et **ObjectHelpTitleIndex** de la structure de [**\_ \_ type d’objet perf**](/windows/desktop/api/Winperf/ns-winperf-perf_object_type) contiennent les valeurs d’index du nom d’objet et du texte d’aide, respectivement, et les membres **CounterNameTitleIndex** et **CounterHelpTitleIndex** de la structure de [**\_ \_ définition de compteur de performances**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_definition) contiennent les valeurs d’index du nom de compteur et du texte d’aide, respectivement.</span><span class="sxs-lookup"><span data-stu-id="573fb-105">The **ObjectNameTitleIndex** and **ObjectHelpTitleIndex** members of the [**PERF\_OBJECT\_TYPE**](/windows/desktop/api/Winperf/ns-winperf-perf_object_type) structure contain the index values to the object name and help text, respectively, and the **CounterNameTitleIndex** and **CounterHelpTitleIndex** members of the [**PERF\_COUNTER\_DEFINITION**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_definition) structure contain the index values to the counter name and help text, respectively.</span></span>

<span data-ttu-id="573fb-106">Pour récupérer le nom ou le texte d’aide, appelez la fonction [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) .</span><span class="sxs-lookup"><span data-stu-id="573fb-106">To retrieve the names or help text, call the [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) function.</span></span> <span data-ttu-id="573fb-107">Définissez le paramètre *HKEY* sur l’une des clés prédéfinies suivantes.</span><span class="sxs-lookup"><span data-stu-id="573fb-107">Set the *hKey* parameter to one of the following predefined keys.</span></span> <span data-ttu-id="573fb-108">En règle générale, vous utilisez la clé **HKEY \_ performance \_ NLSTEXT** , de sorte que vous n’avez pas à déterminer l’identificateur de langue de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="573fb-108">Typically, you would use the **HKEY\_PERFORMANCE\_NLSTEXT** key, so you do not have to determine the user's language identifier.</span></span>



| <span data-ttu-id="573fb-109">Clé</span><span class="sxs-lookup"><span data-stu-id="573fb-109">Key</span></span>                            | <span data-ttu-id="573fb-110">Description</span><span class="sxs-lookup"><span data-stu-id="573fb-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="573fb-111">**\_données de performances HKEY \_**</span><span class="sxs-lookup"><span data-stu-id="573fb-111">**HKEY\_PERFORMANCE\_DATA**</span></span>    | <span data-ttu-id="573fb-112">Interrogez les chaînes en fonction de la valeur de l’identificateur de langue que vous spécifiez dans le paramètre *lpValueName* .</span><span class="sxs-lookup"><span data-stu-id="573fb-112">Query strings based on the language identifier value that you specify in the *lpValueName* parameter.</span></span> <span data-ttu-id="573fb-113">Affectez au paramètre *lpValueName* la valeur « Counter &lt; LangID &gt; » ou « Help &lt; LangID &gt; » pour récupérer les noms ou le texte d’aide, respectivement, où « &lt; LangID &gt; » est l’identificateur de langue système au format **hexadécimal à 3 chiffres**.</span><span class="sxs-lookup"><span data-stu-id="573fb-113">Set *lpValueName* parameter to either "Counter &lt;langid&gt;" or "Help &lt;langid&gt;" to retrieve the names or help text, respectively, where "&lt;langid&gt;" is the system language identifier formatted as **zero-padded 3-digit hex number**.</span></span> <span data-ttu-id="573fb-114">L’identificateur de langue est facultatif.</span><span class="sxs-lookup"><span data-stu-id="573fb-114">The language identifier is optional.</span></span> <span data-ttu-id="573fb-115">Si vous ne spécifiez pas d’identificateur de langue, la fonction retourne des chaînes en anglais.</span><span class="sxs-lookup"><span data-stu-id="573fb-115">If you do not specify a language identifier, the function returns English strings.</span></span> <span data-ttu-id="573fb-116">Vérifiez la `HKEY_LOCAL_MACHINE\Software\Microsoft\Windows NT\CurrentVersion\Perflib` clé de Registre pour obtenir la liste des langues disponibles sur votre système.</span><span class="sxs-lookup"><span data-stu-id="573fb-116">Check the `HKEY_LOCAL_MACHINE\Software\Microsoft\Windows NT\CurrentVersion\Perflib` registry key for the list of languages available on your system.</span></span><br/><span data-ttu-id="573fb-117">Pour récupérer du texte dans la plupart des langues, spécifiez uniquement l’identificateur de langue primaire.</span><span class="sxs-lookup"><span data-stu-id="573fb-117">To retrieve text in most languages, specify the primary language identifier only.</span></span> <span data-ttu-id="573fb-118">Par exemple, pour récupérer des chaînes en anglais, spécifiez l’identificateur de langue 009, et non 1033 pour anglais-États-Unis.</span><span class="sxs-lookup"><span data-stu-id="573fb-118">For example, to retrieve English strings, specify the language identifier as 009, not 1033 for English-US.</span></span><br/><span data-ttu-id="573fb-119">Pour récupérer du texte chinois et portugais, spécifiez les identificateurs primaire et de sous-langue.</span><span class="sxs-lookup"><span data-stu-id="573fb-119">To retrieve Chinese and Portuguese text, specify both the primary and sublanguage identifiers.</span></span><br/><span data-ttu-id="573fb-120">**Windows Server 2003 et Windows XP :** Spécifiez uniquement l’identificateur de langue principale pour le portugais.</span><span class="sxs-lookup"><span data-stu-id="573fb-120">**Windows Server 2003 and Windows XP:** Specify only the primary language identifier for Portuguese.</span></span><br/><span data-ttu-id="573fb-121">**Windows 10**: le texte « Help &lt; LangID &gt; » avec l’identificateur de langue personnalisé retourne toujours les chaînes en anglais, bien que la valeur localisée puisse toujours être récupérée à partir du Registre à l’aide de la clé susmentionnée.</span><span class="sxs-lookup"><span data-stu-id="573fb-121">**Windows 10**: "Help &lt;langid&gt;" text with custom language identifier always returns strings in English, although localized value can still be retrieved from the registry using the aforementioned key.</span></span><br/><br/> |
| <span data-ttu-id="573fb-122">**HKEY \_ performance \_ NLSTEXT**</span><span class="sxs-lookup"><span data-stu-id="573fb-122">**HKEY\_PERFORMANCE\_NLSTEXT**</span></span> | <span data-ttu-id="573fb-123">Des chaînes de requête basées sur la langue d’interface utilisateur par défaut de l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="573fb-123">Query strings based on the default UI language of the current user.</span></span> <span data-ttu-id="573fb-124">Définissez le paramètre *lpValueName* sur « Counter » ou « Help » pour récupérer les noms ou le texte d’aide, respectivement.</span><span class="sxs-lookup"><span data-stu-id="573fb-124">Set the *lpValueName* parameter to either "Counter" or "Help" to retrieve the names or help text, respectively.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="573fb-125">**HKEY \_ performance \_ Text**</span><span class="sxs-lookup"><span data-stu-id="573fb-125">**HKEY\_PERFORMANCE\_TEXT**</span></span>    | <span data-ttu-id="573fb-126">Interroger les chaînes anglaises.</span><span class="sxs-lookup"><span data-stu-id="573fb-126">Query English strings.</span></span> <span data-ttu-id="573fb-127">Définissez le paramètre *lpValueName* sur « Counter » ou « Help » pour récupérer les noms ou le texte d’aide, respectivement.</span><span class="sxs-lookup"><span data-stu-id="573fb-127">Set the *lpValueName* parameter to either "Counter" or "Help" to retrieve the names or help text, respectively.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |





<span data-ttu-id="573fb-128">La fonction retourne les données sous la forme d’une liste de chaînes.</span><span class="sxs-lookup"><span data-stu-id="573fb-128">The function returns the data as a list of strings.</span></span> <span data-ttu-id="573fb-129">Chaque chaîne se termine par un caractère null.</span><span class="sxs-lookup"><span data-stu-id="573fb-129">Each string is null-terminated.</span></span> <span data-ttu-id="573fb-130">La dernière chaîne est suivie d’une marque de fin null supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="573fb-130">The last string is followed by an additional null terminator.</span></span> <span data-ttu-id="573fb-131">Les chaînes sont répertoriées par paires.</span><span class="sxs-lookup"><span data-stu-id="573fb-131">The strings are listed in pairs.</span></span> <span data-ttu-id="573fb-132">La première chaîne de chaque paire est l’index et la deuxième chaîne est le texte associé à l’index.</span><span class="sxs-lookup"><span data-stu-id="573fb-132">The first string of each pair is the index, and the second string is the text associated with the index.</span></span> <span data-ttu-id="573fb-133">Les données de compteur utilisent uniquement des index pairs, tandis que les données d’aide utilisent des index non numérotés.</span><span class="sxs-lookup"><span data-stu-id="573fb-133">The counter data uses only even-numbered indexes, while the help data uses odd-numbered indexes.</span></span> <span data-ttu-id="573fb-134">Les paires sont retournées dans l’ordre d’index de plus en plus important.</span><span class="sxs-lookup"><span data-stu-id="573fb-134">The pairs are returned in increasing index order.</span></span>

<span data-ttu-id="573fb-135">Les listes suivantes présentent des exemples de données de compteur et d’aide.</span><span class="sxs-lookup"><span data-stu-id="573fb-135">The following lists show examples of counter and help data.</span></span> <span data-ttu-id="573fb-136">L’incrémentation d’une valeur d’index de compteur donnée vous donne l’index du texte d’aide du compteur.</span><span class="sxs-lookup"><span data-stu-id="573fb-136">Incrementing a given counter's index value by one gives you the index to the counter's help text.</span></span> <span data-ttu-id="573fb-137">Par exemple, 7 est l’index d’aide associé à l’index de compteur 6.</span><span class="sxs-lookup"><span data-stu-id="573fb-137">For example, 7 is the help index associated with counter index 6.</span></span>

<span data-ttu-id="573fb-138">Paires de données de compteur.</span><span class="sxs-lookup"><span data-stu-id="573fb-138">Counter data pairs.</span></span>

<dl> <span data-ttu-id="573fb-139">2 mémoire système 4 6% de temps processeur</span><span class="sxs-lookup"><span data-stu-id="573fb-139">2 System 4 Memory 6 % Processor Time</span></span>
</dl>

<span data-ttu-id="573fb-140">Les paires de données d’aide.</span><span class="sxs-lookup"><span data-stu-id="573fb-140">Help data pairs.</span></span>

<dl> <span data-ttu-id="573fb-141">3 le type d’objet système comprend ces compteurs... 5 le type d’objet mémoire comprend ces compteurs... 7 le temps processeur est exprimé sous la forme d’un pourcentage de...</span><span class="sxs-lookup"><span data-stu-id="573fb-141">3 The System object type includes those counters that ... 5 The Memory object type includes those counters that ... 7 Processor Time is expressed as a percentage of the ...</span></span>
</dl>

<span data-ttu-id="573fb-142">Notez que la première paire de chaînes dans les données de compteur n’identifie pas un nom de compteur et peut être ignorée.</span><span class="sxs-lookup"><span data-stu-id="573fb-142">Note that the first pair of strings in the counter data do not identify a counter name and can be ignored.</span></span> <span data-ttu-id="573fb-143">Le numéro d’index de la première paire est 1 et la chaîne est une chaîne numérique qui représente la valeur d’index maximale pour les compteurs système.</span><span class="sxs-lookup"><span data-stu-id="573fb-143">The index number of the first pair is 1 and the string is a numeric string that represents the maximum index value for system counters.</span></span>

<span data-ttu-id="573fb-144">Pour plus d’informations sur la façon dont un fournisseur charge le nom et le texte d’aide, consultez [Ajout de noms de compteur et de descriptions au registre](adding-counter-names-and-descriptions-to-the-registry.md).</span><span class="sxs-lookup"><span data-stu-id="573fb-144">For information on how a provider loads the name and help text, see [Adding Counter Names and Descriptions to the Registry](adding-counter-names-and-descriptions-to-the-registry.md).</span></span>

<span data-ttu-id="573fb-145">Il n’y a aucune information dans le texte qui indique si le texte identifie un compteur ou un objet de performance.</span><span class="sxs-lookup"><span data-stu-id="573fb-145">There is no information in the text that indicates if the text identifies a counter or performance object.</span></span> <span data-ttu-id="573fb-146">La seule façon de déterminer cela, ou la relation entre les compteurs et les objets, est d’interroger les données de performance elles-mêmes.</span><span class="sxs-lookup"><span data-stu-id="573fb-146">The only way to determine this, or the relationship between counters and objects, is to query the performance data itself.</span></span> <span data-ttu-id="573fb-147">Par exemple, si vous souhaitez afficher une liste d’objets et leurs compteurs dans une interface utilisateur, vous devez récupérer les données de performances, puis utiliser les valeurs d’index pour analyser les données texte des chaînes.</span><span class="sxs-lookup"><span data-stu-id="573fb-147">For example, if you want to display a list of objects and their counters in a user interface, you must retrieve the performance data, and then use the index values to parse the text data for the strings.</span></span> <span data-ttu-id="573fb-148">Pour obtenir un exemple qui fait cela, consultez [affichage des noms d’objet, d’instance et de compteur](displaying-object-instance-and-counter-names.md).</span><span class="sxs-lookup"><span data-stu-id="573fb-148">For an example that does this, see [Displaying Object, Instance, and Counter Names](displaying-object-instance-and-counter-names.md).</span></span>

<span data-ttu-id="573fb-149">L’exemple suivant montre comment utiliser **HKEY \_ performance \_ NLSTEXT** pour récupérer le compteur et le texte d’aide et créer une table pour un accès ultérieur.</span><span class="sxs-lookup"><span data-stu-id="573fb-149">The following example shows how to use **HKEY\_PERFORMANCE\_NLSTEXT** to retrieve the counter and help text and build a table for subsequent access.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

#pragma comment(lib, "advapi32.lib")

LPWSTR GetText(LPWSTR pwszSource);
BOOL BuildTextTable(LPWSTR pCounterHead, LPWSTR pHelpHead, LPDWORD* pOffsetsHead, LPDWORD pNumberOfOffsets);
DWORD GetNumberOfTextEntries(LPWSTR pwszSource);
void PrintCounterAndHelpText(LPWSTR pCounterTextHead, LPWSTR pHelpTextHead, LPDWORD pTextOffsets, DWORD dwNumberOfOffsets);

void wmain(void)
{
    LPWSTR pCounterTextHead = NULL; // Head of the MULTI_SZ buffer that contains the Counter text.
    LPWSTR pHelpTextHead = NULL;    // Head of the MULTI_SZ buffer that contains the Help text.
    LPDWORD pTextOffsets = NULL;    // Array of DWORDS that contain the offsets to the text in
                                    // pCounterTextHead and pHelpTextHead. The text index
                                    // values mirror the array index.
    DWORD dwNumberOfOffsets = 0;    // Number of elements in the pTextOffsets array.


    pCounterTextHead = GetText(L"Counter");
    if (NULL == pCounterTextHead)
    {
        wprintf(L"GetText(L\"Counter\") failed.\n");
        goto cleanup;
    }

    pHelpTextHead = GetText(L"Help");
    if (NULL == pHelpTextHead)
    {
        wprintf(L"GetText(L\"Help\") failed.\n");
        goto cleanup;
    }

    if (BuildTextTable(pCounterTextHead, pHelpTextHead, &pTextOffsets, &dwNumberOfOffsets))
    {
        PrintCounterAndHelpText(pCounterTextHead, pHelpTextHead, pTextOffsets, dwNumberOfOffsets);
    }
    else
    {
        wprintf(L"BuildTextTable failed.\n");
    }

cleanup:

    if (pCounterTextHead)
        free(pCounterTextHead);

    if (pHelpTextHead)
        free(pHelpTextHead);

    if (pTextOffsets)
        free(pTextOffsets);

    // You do not need to call RegCloseKey if you are only
    // retrieving names and help text.
}


// Get the text based on the source value. This function uses the
// HKEY_PERFORMANCE_NLSTEXT key to get the strings.
LPWSTR GetText(LPWSTR pwszSource)
{
    LPWSTR pBuffer = NULL;
    DWORD dwBufferSize = 0;
    LONG status = ERROR_SUCCESS;

    // Query the size of the text data so you can allocate the buffer.
    status = RegQueryValueEx(HKEY_PERFORMANCE_NLSTEXT, pwszSource, NULL, NULL, NULL, &dwBufferSize);
    if (ERROR_SUCCESS != status)
    {
        wprintf(L"RegQueryValueEx failed getting required buffer size. Error is 0x%x.\n", status);
        goto cleanup;
    }

    // Allocate the text buffer and query the text.
    pBuffer = (LPWSTR)malloc(dwBufferSize);
    if (pBuffer)
    {
        status = RegQueryValueEx(HKEY_PERFORMANCE_NLSTEXT, pwszSource, NULL, NULL, (LPBYTE)pBuffer, &dwBufferSize);
        if (ERROR_SUCCESS != status)
        {
            wprintf(L"RegQueryValueEx failed with 0x%x.\n", status);
            free(pBuffer);
            pBuffer = NULL;
            goto cleanup;
        }
    }
    else
    {
        wprintf(L"malloc failed to allocate memory.\n");
    }

cleanup:

    return pBuffer;
}


// Build a table of offsets into the counter and help text buffers. Use the index
// values from the performance data queries to access the offsets.
BOOL BuildTextTable(LPWSTR pCounterHead, LPWSTR pHelpHead, LPDWORD* pOffsetsHead, LPDWORD pNumberOfOffsets)
{
    BOOL fSuccess = FALSE;
    LPWSTR pwszCounterText = NULL;  // Used to cycle through the Counter text
    LPWSTR pwszHelpText = NULL;     // Used to cycle through the Help text
    LPDWORD pOffsets = NULL;
    DWORD dwCounterIndex = 0;       // Index value of the Counter text
    DWORD dwHelpIndex = 0;          // Index value of the Help text
    DWORD dwSize = 0;               // Size of the block of memory that holds the offset array


    pwszCounterText = pCounterHead;
    pwszHelpText = pHelpHead;

    *pNumberOfOffsets = GetNumberOfTextEntries(L"Last Help");
    if (0 == *pNumberOfOffsets)
    {
        wprintf(L"GetNumberOfTextEntries failed; returned 0 for number of entries.\n");
        goto cleanup;
    }

    dwSize = sizeof(DWORD) * (*pNumberOfOffsets + 1);  // Add one to make the array one-based

    pOffsets = (LPDWORD)malloc(dwSize);
    if (pOffsets)
    {
        ZeroMemory(pOffsets, dwSize);
        *pOffsetsHead = pOffsets;

        // Bypass first record (pair) of the counter data - contains upper bounds of system counter index.
        pwszCounterText += (wcslen(pwszCounterText)+1);
        pwszCounterText += (wcslen(pwszCounterText)+1);

        for (; *pwszCounterText; pwszCounterText += (wcslen(pwszCounterText)+1))
        {
            dwCounterIndex = _wtoi(pwszCounterText);
            dwHelpIndex = _wtoi(pwszHelpText);

            // Use the counter's index value as an indexer into the pOffsets array.
            // Store the offset to the counter text in the array element.
            pwszCounterText += (wcslen(pwszCounterText)+1);  //Skip past index value
            pOffsets[dwCounterIndex] = (DWORD)(pwszCounterText - pCounterHead);

            // Some help indexes for system counters do not have a matching counter, so loop
            // until you find the matching help index or the index is greater than the corresponding
            // counter index. For example, if the indexes were as follows, you would loop
            // until the help index was 11.
            //
            // Counter index       Help Index
            //   2                    3
            //   4                    5
            //   6                    7
            //                        9   (skip because there is no matching Counter index)
            //   10                   11
            while (*pwszHelpText && dwHelpIndex < dwCounterIndex)
            {
                pwszHelpText += (wcslen(pwszHelpText)+1);  // Skip past index value
                pwszHelpText += (wcslen(pwszHelpText)+1);  // Skip past help text to the next index value
                dwHelpIndex = _wtoi(pwszHelpText);
            }

            // Use the Help index value as an indexer into the pOffsets array.
            // Store the offset to the help text in the array element.
            if (dwHelpIndex == (dwCounterIndex + 1))
            {
                pwszHelpText += (wcslen(pwszHelpText)+1);  //Skip past index value
                pOffsets[dwHelpIndex] = (DWORD)(pwszHelpText - pHelpHead);
                pwszHelpText += (wcslen(pwszHelpText)+1);  //Skip past help text to next index value
            }
        }

        fSuccess = TRUE;
    }

cleanup:

    return fSuccess;
}


// Retrieve the last help index used from the registry. Use this number
// to allocate an array of DWORDs. Note that index values are not contiguous.
DWORD GetNumberOfTextEntries(LPWSTR pwszSource)
{
    DWORD dwEntries = 0;
    LONG status = ERROR_SUCCESS;
    HKEY hkey = NULL;
    DWORD dwSize = sizeof(DWORD);
    LPWSTR pwszMessage = NULL;

    status = RegOpenKeyEx(HKEY_LOCAL_MACHINE,
        L"SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Perflib",
        0,
        KEY_READ,
        &hkey);

    if (ERROR_SUCCESS != status)
    {
        wprintf(L"RegOpenKeyEx failed with 0x%x.\n", status);
        goto cleanup;
    }

    status = RegQueryValueEx(hkey, pwszSource, NULL, 0, (LPBYTE)&dwEntries, &dwSize);

    if (ERROR_SUCCESS != status)
    {
        wprintf(L"RegQueryValueEx failed with 0x%x.\n", status);
    }

cleanup:

    if (hkey)
        RegCloseKey(hkey);

    return dwEntries;
}


// Print the pairs of counter and help text.
void PrintCounterAndHelpText(LPWSTR pCounterTextHead, LPWSTR pHelpTextHead, LPDWORD pTextOffsets, DWORD dwNumberOfOffsets)
{    UNREFERENCED_PARAMETER(dwNumberOfOffsets);
    // Counter index values are even numbers that start at 2 so begin with
    // the second element of the array of offsets. Many array elements will
    // not contain offset values (index values are not contiguous).

    // There is typically a large number of counters, so this example prints
    // the first 10 counters and help text.
    //for (DWORD i = 2; i < (dwNumberOfOffsets+1); i++)

    for (DWORD i = 2; i < 22; i++)
    {
        if (pTextOffsets[i]) // If index offset is not zero
        {
            if (0 == (i % 2)) // Counter text index (even number)
                wprintf(L"%d %s\n", i, pCounterTextHead+pTextOffsets[i]);
            else
                wprintf(L"%d %s\n\n", i, pHelpTextHead+pTextOffsets[i]);
        }
    }
}
```



<span data-ttu-id="573fb-150">L’exemple suivant montre comment utiliser les **\_ \_ données de performance HKEY** pour récupérer le texte de compteur.</span><span class="sxs-lookup"><span data-stu-id="573fb-150">The following example shows how to use **HKEY\_PERFORMANCE\_DATA** to retrieve the counter text.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <strsafe.h>

#pragma comment(lib, "advapi32.lib")

LPWSTR GetText(LPWSTR pwszSource);
BOOL BuildTextTable(LPWSTR pCounterHead, LPWSTR pHelpHead, LPDWORD* pOffsetsHead, LPDWORD pNumberOfOffsets);
DWORD GetNumberOfTextEntries(LPWSTR pwszSource);
void PrintCounterAndHelpText(LPWSTR pCounterTextHead, LPWSTR pHelpTextHead, LPDWORD pTextOffsets, DWORD dwNumberOfOffsets);
LANGID GetLanguageId();

void wmain(void)
{
    LPWSTR pCounterTextHead = NULL; // Head of the MULTI_SZ buffer that contains the Counter text.
    LPWSTR pHelpTextHead = NULL;    // Head of the MULTI_SZ buffer that contains the Help text.
    LPDWORD pTextOffsets = NULL;    // Array of DWORDS that contain the offsets to the text in
                                    // pCounterTextHead and pHelpTextHead. The text index
                                    // values mirror the array index.
    DWORD dwNumberOfOffsets = 0;    // Number of elements in the pTextOffsets array.

    pCounterTextHead = GetText(L"Counter");
    if (NULL == pCounterTextHead)
    {
        wprintf(L"GetText(L\"Counter\") failed.\n");
        goto cleanup;
    }

    pHelpTextHead = GetText(L"Help");
    if (NULL == pHelpTextHead)
    {
        wprintf(L"GetText(L\"Help\") failed.\n");
        goto cleanup;
    }

    if (BuildTextTable(pCounterTextHead, pHelpTextHead, &pTextOffsets, &dwNumberOfOffsets))
    {
        PrintCounterAndHelpText(pCounterTextHead, pHelpTextHead, pTextOffsets, dwNumberOfOffsets);
    }
    else
    {
        wprintf(L"BuildTextTable failed.\n");
    }

cleanup:

    if (pCounterTextHead)
        free(pCounterTextHead);

    if (pHelpTextHead)
        free(pHelpTextHead);

    if (pTextOffsets)
        free(pTextOffsets);

    // You do not need to call RegCloseKey if you are only
    // retrieving names and help text.
}


// Get the text based on the source value. This function uses the
// HKEY_PERFORMANCE_DATA key to get the strings.
LPWSTR GetText(LPWSTR pwszSource)
{
    LPWSTR pBuffer = NULL;
    DWORD dwBufferSize = 0;
    LONG status = ERROR_SUCCESS;
    LANGID langid = 0;
    WCHAR wszSourceAndLangId[15];   // Identifies the source of the text; either
                                    // "Counter <langid>" or "Help <langid>"


    // Create the lpValueName string for the registry query.
    langid = GetLanguageId();
    if (0 == langid)
    {
        wprintf(L"GetLanguageId failed to get the default language identifier.\n");
        goto cleanup;
    }

    StringCchPrintf(wszSourceAndLangId, 15, L"%s %03x", pwszSource, langid);

    // Query the size of the text data so you can allocate the buffer.
    status = RegQueryValueEx(HKEY_PERFORMANCE_DATA, wszSourceAndLangId, NULL, NULL, NULL, &dwBufferSize);
    if (ERROR_SUCCESS != status)
    {
        wprintf(L"RegQueryValueEx failed getting required buffer size. Error is 0x%x.\n", status);
        goto cleanup;
    }

    // Allocate the text buffer and query the text.
    pBuffer = (LPWSTR)malloc(dwBufferSize);
    if (pBuffer)
    {
        status = RegQueryValueEx(HKEY_PERFORMANCE_DATA, wszSourceAndLangId, NULL, NULL, (LPBYTE)pBuffer, &dwBufferSize);
        if (ERROR_SUCCESS != status)
        {
            wprintf(L"RegQueryValueEx failed with 0x%x.\n", status);
            free(pBuffer);
            pBuffer = NULL;
            goto cleanup;
        }
    }
    else
    {
        wprintf(L"malloc failed to allocate memory.\n");
    }

cleanup:

    return pBuffer;
}


// Retrieve the default language identifier of the current user. For most languages,
// you use the primary language identifier only to retrieve the text. In Windows XP and
// Windows Server 2003, you use the complete language identifier to retrieve Chinese
// text. In Windows Vista, you use the complete language identifier to retrieve Portuguese
// text.
LANGID GetLanguageId()
{
    LANGID langid = 0;  // Complete language identifier.
    WORD primary = 0;   // Primary language identifier.
    OSVERSIONINFO osvi;

    ZeroMemory(&osvi, sizeof(OSVERSIONINFO));
    osvi.dwOSVersionInfoSize = sizeof(OSVERSIONINFO);

    if (GetVersionEx(&osvi))
    {
        langid = GetUserDefaultUILanguage();
        primary = PRIMARYLANGID(langid);

        if ( (LANG_PORTUGUESE == primary && osvi.dwBuildNumber > 5) || // Windows Vista and later
             (LANG_CHINESE == primary && (osvi.dwMajorVersion == 5 && osvi.dwMinorVersion >= 1)) ) // XP and Windows Server 2003
        {
            ; //Use the complete language identifier.
        }
        else
        {
            langid = primary;
        }
    }
    else
    {
        wprintf(L"GetVersionEx failed with 0x%x.\n", GetLastError());
    }

    return langid;
}


// Build a table of offsets into the counter and help text buffers. Use the index
// values from the performance data queries to access the offsets.
BOOL BuildTextTable(LPWSTR pCounterHead, LPWSTR pHelpHead, LPDWORD* pOffsetsHead, LPDWORD pNumberOfOffsets)
{
    BOOL fSuccess = FALSE;
    LPWSTR pwszCounterText = NULL;  // Used to cycle through the Counter text
    LPWSTR pwszHelpText = NULL;     // Used to cycle through the Help text
    LPDWORD pOffsets = NULL;
    DWORD dwCounterIndex = 0;       // Index value of the Counter text
    DWORD dwHelpIndex = 0;          // Index value of the Help text
    DWORD dwSize = 0;               // Size of the block of memory that holds the offset array

    pwszCounterText = pCounterHead;
    pwszHelpText = pHelpHead;

    *pNumberOfOffsets = GetNumberOfTextEntries(L"Last Help");
    if (0 == *pNumberOfOffsets)
    {
        wprintf(L"GetNumberOfTextEntries failed; returned 0 for number of entries.\n");
        goto cleanup;
    }

    dwSize = sizeof(DWORD) * (*pNumberOfOffsets + 1);  // Add one to make the array one-based

    pOffsets = (LPDWORD)malloc(dwSize);
    if (pOffsets)
    {
        ZeroMemory(pOffsets, dwSize);
        *pOffsetsHead = pOffsets;

        // Bypass first record (pair) of the counter data - contains upper bounds of system counter index.
        pwszCounterText += (wcslen(pwszCounterText)+1);
        pwszCounterText += (wcslen(pwszCounterText)+1);

        for (; *pwszCounterText; pwszCounterText += (wcslen(pwszCounterText)+1))
        {
            dwCounterIndex = _wtoi(pwszCounterText);
            dwHelpIndex = _wtoi(pwszHelpText);

            // Use the counter's index value as an indexer into the pOffsets array.
            // Store the offset to the counter text in the array element.
            pwszCounterText += (wcslen(pwszCounterText)+1);  //Skip past index value
            pOffsets[dwCounterIndex] = (DWORD)(pwszCounterText - pCounterHead);

            // Some help indexes for system counters do not have a matching counter, so loop
            // until you find the matching help index or the index is greater than the corresponding
            // counter index. For example, if the indexes were as follows, you would loop
            // until the help index was 11.
            //
            // Counter index       Help Index
            //   2                    3
            //   4                    5
            //   6                    7
            //                        9   (skip because there is no matching Counter index)
            //   10                   11
            while (*pwszHelpText && dwHelpIndex < dwCounterIndex)
            {
                pwszHelpText += (wcslen(pwszHelpText)+1);  // Skip past index value
                pwszHelpText += (wcslen(pwszHelpText)+1);  // Skip past help text to the next index value
                dwHelpIndex = _wtoi(pwszHelpText);
            }

            // Use the Help index value as an indexer into the pOffsets array.
            // Store the offset to the help text in the array element.
            if (dwHelpIndex == (dwCounterIndex + 1))
            {
                pwszHelpText += (wcslen(pwszHelpText)+1);  //Skip past index value
                pOffsets[dwHelpIndex] = (DWORD)(pwszHelpText - pHelpHead);
                pwszHelpText += (wcslen(pwszHelpText)+1);  //Skip past help text to next index value
            }
        }

        fSuccess = TRUE;
    }

cleanup:

    return fSuccess;
}


// Retrieve the last help index used from the registry. Use this number
// to allocate an array of DWORDs. Note that index values are not contiguous.
DWORD GetNumberOfTextEntries(LPWSTR pwszSource)
{
    DWORD dwEntries = 0;
    LONG status = ERROR_SUCCESS;
    HKEY hkey = NULL;
    DWORD dwSize = sizeof(DWORD);
    LPWSTR pwszMessage = NULL;

    status = RegOpenKeyEx(HKEY_LOCAL_MACHINE,
        L"SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Perflib",
        0,
        KEY_READ,
        &hkey);

    if (ERROR_SUCCESS != status)
    {
        wprintf(L"RegOpenKeyEx failed with 0x%x.\n", status);
        goto cleanup;
    }

    status = RegQueryValueEx(hkey, pwszSource, NULL, 0, (LPBYTE)&dwEntries, &dwSize);

    if (ERROR_SUCCESS != status)
    {
        wprintf(L"RegQueryValueEx failed with 0x%x.\n", status);
    }

cleanup:

    if (hkey)
        RegCloseKey(hkey);

    return dwEntries;
}


// Print the pairs of counter and help text.
void PrintCounterAndHelpText(LPWSTR pCounterTextHead, LPWSTR pHelpTextHead, LPDWORD pTextOffsets, DWORD dwNumberOfOffsets)
{   UNREFERENCED_PARAMETER(dwNumberOfOffsets);
    // Counter index values are even numbers that start at 2 so begin with
    // the second element of the array of offsets. Many array elements will
    // not contain offset values (index values are not contiguous).

    // There is typically a large number of counters, so this example prints
    // the first 10 counters and help text.
    //for (DWORD i = 2; i < (dwNumberOfOffsets+1); i++)

    for (DWORD i = 2; i < 22; i++)
    {
        if (pTextOffsets[i]) // If index offset is not zero
        {
            if (0 == (i % 2)) // Counter text index (even number)
                wprintf(L"%d %s\n", i, pCounterTextHead+pTextOffsets[i]);
            else
                wprintf(L"%d %s\n\n", i, pHelpTextHead+pTextOffsets[i]);
        }
    }
}
```
