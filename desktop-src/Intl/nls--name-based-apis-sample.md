---
description: L’exemple d’application décrit dans cette rubrique présente quelques-uns des &NLS \# 0034 ; nom des paramètres régionaux&\# 0034 ; fonctions. Dans la mesure du possible, vos applications doivent utiliser des noms de paramètres régionaux plutôt que des identificateurs de paramètres régionaux.
ms.assetid: 0502dba0-a26f-4238-b68e-bb41ef17ff08
title: 'NLS : exemple d’API basées sur un nom'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fd5acab078f06e345184769b5a472e6d2f307c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538189"
---
# <a name="nls-name-based-apis-sample"></a><span data-ttu-id="27712-104">NLS : exemple d’API basées sur un nom</span><span class="sxs-lookup"><span data-stu-id="27712-104">NLS: Name-based APIs Sample</span></span>

<span data-ttu-id="27712-105">L’exemple d’application décrit dans cette rubrique présente certaines fonctions NLS [« nom des paramètres régionaux »](calling-the--locale-name--functions.md).</span><span class="sxs-lookup"><span data-stu-id="27712-105">The sample application described in this topic demonstrates some of the NLS ["locale name" functions](calling-the--locale-name--functions.md).</span></span> <span data-ttu-id="27712-106">Dans la mesure du possible, vos applications doivent utiliser des [noms de paramètres régionaux](locale-names.md) plutôt que des [identificateurs de paramètres régionaux](locale-identifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="27712-106">Your applications should use [locale names](locale-names.md) instead of [locale identifiers](locale-identifiers.md) when possible.</span></span>

<span data-ttu-id="27712-107">L’exemple d’application utilise [**EnumSystemLocalesEx**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex) pour énumérer tous les paramètres régionaux du système d’exploitation, y compris les [paramètres régionaux supplémentaires](custom-locales.md).</span><span class="sxs-lookup"><span data-stu-id="27712-107">The sample application uses [**EnumSystemLocalesEx**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex) to enumerate all locales on the operating system, including [supplemental locales](custom-locales.md).</span></span>

<span data-ttu-id="27712-108">La fonction de rappel d’énumération prise en charge par l’application peut prendre un ou plusieurs noms de paramètres régionaux en tant que paramètres.</span><span class="sxs-lookup"><span data-stu-id="27712-108">The enumeration callback function supported by the application can take one or more locale names as parameters.</span></span> <span data-ttu-id="27712-109">[**EnumSystemLocalesEx**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex) transmet ces noms à la fonction de rappel dans la valeur *lParam* facultative.</span><span class="sxs-lookup"><span data-stu-id="27712-109">[**EnumSystemLocalesEx**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex) passes these names to the callback function in the optional *lparam* value.</span></span> <span data-ttu-id="27712-110">Si l’utilisateur entre les paramètres régionaux sur la ligne de commande, la fonction de rappel affiche uniquement les paramètres régionaux spécifiés au lieu d’afficher tous les paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="27712-110">If the user enters the locales on the command line, the callback function only displays the specified locales instead of displaying all locales.</span></span>

<span data-ttu-id="27712-111">Pour chaque paramètre régional affiché, la fonction de rappel indique s’il s’agit des paramètres régionaux système, imprime la date actuelle à l’aide des formats par défaut des paramètres régionaux et affiche toutes les données des paramètres régionaux dans chaque [constante d’informations de paramètres régionaux](locale-information-constants.md) introduite dans Windows Vista, par exemple, [paramètres régionaux \_ SSCRIPTS](locale-sscripts.md).</span><span class="sxs-lookup"><span data-stu-id="27712-111">For each displayed locale, the callback function reports whether it is the system locale, prints the current date using the default formats of the locale, and displays all data for the locale in each [locale information constant](locale-information-constants.md) introduced in Windows Vista, for example, [LOCALE\_SSCRIPTS](locale-sscripts.md).</span></span>

<span data-ttu-id="27712-112">L’exemple d’application analyse tous les paramètres régionaux d’entrée pour voir s’ils sont valides à l’aide de [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename).</span><span class="sxs-lookup"><span data-stu-id="27712-112">The sample application parses any input locales to see if they are valid by using [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename).</span></span>

<span data-ttu-id="27712-113">Cet exemple illustre les fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="27712-113">This sample demonstrates the following functions:</span></span>

-   [<span data-ttu-id="27712-114">CompareStringEx</span><span class="sxs-lookup"><span data-stu-id="27712-114">CompareStringEx</span></span>](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex)
-   [<span data-ttu-id="27712-115">**EnumSystemLocalesEx**</span><span class="sxs-lookup"><span data-stu-id="27712-115">**EnumSystemLocalesEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex)
-   [<span data-ttu-id="27712-116">**GetDateFormatEx**</span><span class="sxs-lookup"><span data-stu-id="27712-116">**GetDateFormatEx**</span></span>](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex)
-   [<span data-ttu-id="27712-117">**GetLocaleInfoEx**</span><span class="sxs-lookup"><span data-stu-id="27712-117">**GetLocaleInfoEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex)
-   [<span data-ttu-id="27712-118">**GetSystemDefaultLocaleName**</span><span class="sxs-lookup"><span data-stu-id="27712-118">**GetSystemDefaultLocaleName**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultlocalename)
-   [<span data-ttu-id="27712-119">**IsValidLocaleName**</span><span class="sxs-lookup"><span data-stu-id="27712-119">**IsValidLocaleName**</span></span>](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename)
-   [<span data-ttu-id="27712-120">**LocaleNameToLCID**</span><span class="sxs-lookup"><span data-stu-id="27712-120">**LocaleNameToLCID**</span></span>](/windows/desktop/api/Winnls/nf-winnls-localenametolcid)


```C++
// THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF 
// ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO 
// THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A 
// PARTICULAR PURPOSE. 
// 
// Copyright (c) Microsoft Corporation. All rights reserved. 
// 
// ======================================================================== 
//   CONSOLE APPLICATION : NamedNlsFunctions Project Overview 

#include "stdafx.h"
#include "windows.h"
#include "stdio.h"

// All of the LCTYPES new to Windows Vista 
LCTYPE NewTypes[] =
{
    LOCALE_SNAME,
    LOCALE_SDURATION,
    LOCALE_SKEYBOARDSTOINSTALL,
    LOCALE_SSHORTESTDAYNAME1,
    LOCALE_SSHORTESTDAYNAME2,
    LOCALE_SSHORTESTDAYNAME3,
    LOCALE_SSHORTESTDAYNAME4,
    LOCALE_SSHORTESTDAYNAME5,
    LOCALE_SSHORTESTDAYNAME6,
    LOCALE_SSHORTESTDAYNAME7,
    LOCALE_SISO639LANGNAME2,
    LOCALE_SISO3166CTRYNAME2,
    LOCALE_SNAN,
    LOCALE_SPOSINFINITY,
    LOCALE_SNEGINFINITY,
    LOCALE_SSCRIPTS
};

// Strings so we can print out the LCTYPES 
LPCWSTR NewTypeNames[] =
{
    L"LOCALE_SNAME",
    L"LOCALE_SDURATION",
    L"LOCALE_SKEYBOARDSTOINSTALL",
    L"LOCALE_SSHORTESTDAYNAME1",
    L"LOCALE_SSHORTESTDAYNAME2",
    L"LOCALE_SSHORTESTDAYNAME3",
    L"LOCALE_SSHORTESTDAYNAME4",
    L"LOCALE_SSHORTESTDAYNAME5",
    L"LOCALE_SSHORTESTDAYNAME6",
    L"LOCALE_SSHORTESTDAYNAME7",
    L"LOCALE_SISO639LANGNAME2",
    L"LOCALE_SISO3166CTRYNAME2",
    L"LOCALE_SNAN",
    L"LOCALE_SPOSINFINITY",
    L"LOCALE_SNEGINFINITY",
    L"LOCALE_SSCRIPTS"
};

// Callback for EnumSystemLocalesEx() 
#define BUFFER_SIZE 512
BOOL CALLBACK MyFuncLocaleEx(LPWSTR pStr, DWORD dwFlags, LPARAM lparam)
{
    UNREFERENCED_PARAMETER(dwFlags);
    WCHAR** argv = (WCHAR**)lparam;
    WCHAR wcBuffer[BUFFER_SIZE];
    int iResult;
    int i;

    // If specific locales were specified on the command line check for a match 
    if (*argv && argv[1])
    {
        // Check each argument to see if our locale matches 
        for (i = 1; argv[i] != 0; i++)
        {
            // Using invariant, check if the name matches the input.  CompareStringEx 
            // is probably overkill, but we want to demonstrate that named API. 
            if (CompareStringEx(LOCALE_NAME_INVARIANT,
                                LINGUISTIC_IGNORECASE,
                                argv[i],
                                -1,
                                pStr,
                                -1,
                                NULL,
                                NULL,
                                0) == CSTR_EQUAL)
            {
                break;
            }
        }

        // If no match then stop and don't output this one 
        if (argv[i] == 0)
            return TRUE;
    }

    // Print out the locale name we found 
    iResult = GetLocaleInfoEx(pStr, LOCALE_SENGLANGUAGE, wcBuffer, BUFFER_SIZE);

    // If it succeeds, print it out 
    if (iResult > 0)
        wprintf(L"Locale %s (%s)\n", pStr, wcBuffer);
    else
        wprintf(L"Locale %s had error %d\n", pStr, GetLastError());
 
    // If this is the system locale, let us know.  CompareStringEx 
    // is probably overkill, but we want to demonstrate that named API. 
    iResult = GetSystemDefaultLocaleName(wcBuffer, BUFFER_SIZE);
    if (iResult > 0)
    {
        if (CompareStringEx(LOCALE_NAME_INVARIANT,
                            LINGUISTIC_IGNORECASE,
                            wcBuffer,
                            -1,
                            pStr,
                            -1,
                            NULL,
                            NULL,
                            0) == CSTR_EQUAL)
        {
            wprintf(L"Locale %s is the system locale!\n", wcBuffer);
        }
    }
    else
    {
        wprintf(L"Error %d getting system locale\n", GetLastError());
    }
    
    // Get its LCID 
    LCID lcid = LocaleNameToLCID(pStr, NULL);
    if (lcid != 0)
        wprintf(L"LCID for %s is %x\n", pStr, lcid);
    else
        wprintf(L"Error %d getting LCID\n", GetLastError());

    // Get today's date 
    iResult = GetDateFormatEx(pStr, DATE_LONGDATE, NULL, NULL, wcBuffer, BUFFER_SIZE, NULL);

    if (iResult > 0)
        wprintf(L"Date: %s\n", wcBuffer);
    else
        wprintf(L"Error %d getting today's date for %s\n", GetLastError(), pStr);

    // Loop through all of the new LCTYPES and do GetLocaleInfoEx on them 
    for (i = 0; i < sizeof(NewTypes) / sizeof(NewTypes[0]); i++)
    {
        // Get this LCTYPE result for this locale 
        iResult = GetLocaleInfoEx(pStr, NewTypes[i], wcBuffer, BUFFER_SIZE);

        // If it succeeds, print it out 
        if (iResult > 0)
        {
            wprintf(L"  %s has value %s\n", NewTypeNames[i], wcBuffer);
        }
        else
        {
            wprintf(L"  %s had error %d\n", NewTypeNames[i], GetLastError());
        }
    } 

    return (TRUE);
}

int __cdecl wmain(int argc, wchar_t* argv[])
{
    UNREFERENCED_PARAMETER(argc);
    // Enumerate all the locales and report on them 
    EnumSystemLocalesEx( MyFuncLocaleEx, LOCALE_ALL, (LPARAM)argv, NULL);

    // See which of the input locales are valid (if any) 
    if (*argv && argv[1])
    {
        // Check each argument to see if our locale matches 
        for (int i = 1; argv[i] != 0; i++)
        {
            // See if this is a valid locale name 
            if (!IsValidLocaleName(argv[i]))
            {
                wprintf(L"%s is not a valid locale name\n", argv[i]);
            }
        }
    }    
}

/*
The following is a portion of the results produced by this code example.

Locale en-US (English)
Locale en-US is the system locale!
LCID for en-US is 409
Date: Wednesday, February 03, 2010
  LOCALE_SNAME has value en-US
  LOCALE_SDURATION has value h:mm:ss
  LOCALE_SKEYBOARDSTOINSTALL has value 0409:00000409
  LOCALE_SSHORTESTDAYNAME1 has value Mo
  LOCALE_SSHORTESTDAYNAME2 has value Tu
  LOCALE_SSHORTESTDAYNAME3 has value We
  LOCALE_SSHORTESTDAYNAME4 has value Th
  LOCALE_SSHORTESTDAYNAME5 has value Fr
  LOCALE_SSHORTESTDAYNAME6 has value Sa
  LOCALE_SSHORTESTDAYNAME7 has value Su
  LOCALE_SISO639LANGNAME2 has value eng
  LOCALE_SISO3166CTRYNAME2 has value USA
  LOCALE_SNAN has value NaN
  LOCALE_SPOSINFINITY has value Infinity
  LOCALE_SNEGINFINITY has value -Infinity
  LOCALE_SSCRIPTS has value Latn;
Locale fr-FR (French)
LCID for fr-FR is 40c
Date: mercredi 3 f vrier 2010
  LOCALE_SNAME has value fr-FR
  LOCALE_SDURATION has value HH:mm:ss
  LOCALE_SKEYBOARDSTOINSTALL has value 040c:0000040c;0409:00000409
  LOCALE_SSHORTESTDAYNAME1 has value lu
  LOCALE_SSHORTESTDAYNAME2 has value ma
  LOCALE_SSHORTESTDAYNAME3 has value me
  LOCALE_SSHORTESTDAYNAME4 has value je
  LOCALE_SSHORTESTDAYNAME5 has value ve
  LOCALE_SSHORTESTDAYNAME6 has value sa
  LOCALE_SSHORTESTDAYNAME7 has value di
  LOCALE_SISO639LANGNAME2 has value fra
  LOCALE_SISO3166CTRYNAME2 has value FRA
  LOCALE_SNAN has value Non Num rique
  LOCALE_SPOSINFINITY has value +Infini
  LOCALE_SNEGINFINITY has value -Infini
  LOCALE_SSCRIPTS has value Latn;
Locale es-ES (Spanish)
LCID for es-ES is c0a
Date: mi rcoles, 03 de febrero de 2010
  LOCALE_SNAME has value es-ES
  LOCALE_SDURATION has value H:mm:ss
  LOCALE_SKEYBOARDSTOINSTALL has value 0c0a:0000040a;0409:00000409
  LOCALE_SSHORTESTDAYNAME1 has value lu
  LOCALE_SSHORTESTDAYNAME2 has value ma
  LOCALE_SSHORTESTDAYNAME3 has value mi
  LOCALE_SSHORTESTDAYNAME4 has value ju
  LOCALE_SSHORTESTDAYNAME5 has value vi
  LOCALE_SSHORTESTDAYNAME6 has value s 
  LOCALE_SSHORTESTDAYNAME7 has value do
  LOCALE_SISO639LANGNAME2 has value spa
  LOCALE_SISO3166CTRYNAME2 has value ESP
  LOCALE_SNAN has value NeuN
  LOCALE_SPOSINFINITY has value Infinito
  LOCALE_SNEGINFINITY has value -Infinito
  LOCALE_SSCRIPTS has value Latn;

*/
```



 

 



