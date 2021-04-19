---
description: Cet exemple de code provient d’une action personnalisée ICE (ICE01). Il vérifie que le mécanisme de glace fonctionne en affichant l’heure. La glace publie un message indiquant l’heure à laquelle le programme d’installation a appelé la glace. Cette glace ne doit jamais retourner une erreur.
ms.assetid: 7e580f6b-8adf-4b11-9072-5b2e1506fabb
title: Exemple de code ICE en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91897d4d056052b27025c87f13105e2cc54657df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524913"
---
# <a name="sample-ice-in-c"></a><span data-ttu-id="62f78-106">Exemple de code ICE en C++</span><span class="sxs-lookup"><span data-stu-id="62f78-106">Sample ICE in C++</span></span>

<span data-ttu-id="62f78-107">Cet exemple de code provient d’une action personnalisée ICE ( [ICE01](ice01.md)).</span><span class="sxs-lookup"><span data-stu-id="62f78-107">This sample code is from an ICE custom action ( [ICE01](ice01.md)).</span></span> <span data-ttu-id="62f78-108">Il vérifie que le mécanisme de glace fonctionne en affichant l’heure.</span><span class="sxs-lookup"><span data-stu-id="62f78-108">It validates that the ICE mechanism is working by displaying the time.</span></span> <span data-ttu-id="62f78-109">La glace publie un message indiquant l’heure à laquelle le programme d’installation a appelé la glace.</span><span class="sxs-lookup"><span data-stu-id="62f78-109">The ICE posts a message giving the time the installer called the ICE.</span></span> <span data-ttu-id="62f78-110">Cette glace ne doit jamais retourner une erreur.</span><span class="sxs-lookup"><span data-stu-id="62f78-110">This ICE should never return an error.</span></span>


```C++
// 
// test of external database access
#include <windows.h>
#include <stdio.h>
#include <tchar.h>
#include <strsafe.h>
#include <MsiQuery.h>
#pragma comment(lib, "msi.lib")

///////////////////////////////////////////////////////////
// ICE01 - simple ICE that does not test anything
UINT __stdcall ICE01(MSIHANDLE hInstall)
{
    // setup the record to describe owner and date created
    PMSIHANDLE hRecCreated = ::MsiCreateRecord(1);
    ::MsiRecordSetString(hRecCreated, 0, TEXT("ICE01\t3\tCreated 04/29/1998 by <insert author's name here>"));

    // post the owner message
    ::MsiProcessMessage(hInstall, INSTALLMESSAGE(INSTALLMESSAGE_USER), hRecCreated); 
    // setup the record to describe the last time the ICE was modified
    ::MsiRecordSetString(hRecCreated, 0, TEXT("ICE01\t3\tLast modified 05/06/1998 by <insert author's name here>"));

    // post the last modification message
    ::MsiProcessMessage(hInstall, INSTALLMESSAGE(INSTALLMESSAGE_USER), hRecCreated);

    // setup the record to describe what the ICE evaluates
    ::MsiRecordSetString(hRecCreated, 0, TEXT("ICE01\t3\tSimple ICE illustrating the ICE concept"));

    // post the description of evaluation message
    ::MsiProcessMessage(hInstall, INSTALLMESSAGE(INSTALLMESSAGE_USER), hRecCreated);
    // time value to be sent on
    TCHAR szValue[200];
    DWORD cchValue = sizeof(szValue)/sizeof(TCHAR);

    // try to get the time of this call
    if (MsiGetProperty(hInstall, TEXT("Time"), szValue, &cchValue) != ERROR_SUCCESS)
        StringCchCopy(szValue,  sizeof("(none)")/sizeof(TCHAR)+1, TEXT("none"));// no time available

    // setup the record to be sent as a message
    PMSIHANDLE hRecTime = ::MsiCreateRecord(2);
    ::MsiRecordSetString(hRecTime, 0, TEXT("ICE01\t3\tCalled at [1]."));
    ::MsiRecordSetString(hRecTime, 1, szValue);

    // send the time
    ::MsiProcessMessage(hInstall, INSTALLMESSAGE(INSTALLMESSAGE_USER), hRecTime);

    return ERROR_SUCCESS; // allows other ICEs will continue
}
```



 

 



