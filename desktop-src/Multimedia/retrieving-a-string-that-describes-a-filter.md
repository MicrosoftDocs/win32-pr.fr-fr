---
title: Récupération d’une chaîne décrivant un filtre
description: Récupération d’une chaîne décrivant un filtre
ms.assetid: 47390448-eaa6-4bea-bd90-549fa37e739a
keywords:
- Audio Compression Manager (ACM), récupération de chaînes décrivant des filtres
- ACM (gestionnaire de compression audio), récupération de chaînes décrivant des filtres
- Exemples ACM, récupération de chaînes décrivant des filtres
- récupération de chaînes qui décrivent des filtres
- acmFilterTagDetails fonction)
- acmFilterDetails fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 641f2b9993d9c916113d14eaf92925e916409619
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106513489"
---
# <a name="retrieving-a-string-that-describes-a-filter"></a><span data-ttu-id="51bc0-109">Récupération d’une chaîne décrivant un filtre</span><span class="sxs-lookup"><span data-stu-id="51bc0-109">Retrieving a String That Describes a Filter</span></span>

<span data-ttu-id="51bc0-110">Une application doit souvent afficher une chaîne qui décrit le format actuel.</span><span class="sxs-lookup"><span data-stu-id="51bc0-110">An application often needs to display a string that describes the current format.</span></span> <span data-ttu-id="51bc0-111">Cette tâche peut être accomplie facilement avec les fonctions [**acmFilterTagDetails**](/windows/desktop/api/Msacm/nf-msacm-acmfiltertagdetails) et [**acmFilterDetails**](/windows/desktop/api/Msacm/nf-msacm-acmfilterdetails) .</span><span class="sxs-lookup"><span data-stu-id="51bc0-111">This task can be accomplished easily with the [**acmFilterTagDetails**](/windows/desktop/api/Msacm/nf-msacm-acmfiltertagdetails) and [**acmFilterDetails**](/windows/desktop/api/Msacm/nf-msacm-acmfilterdetails) functions.</span></span> <span data-ttu-id="51bc0-112">Ces fonctions doivent être appelées à l’aide du filtre ou de la balise de filtre appropriés.</span><span class="sxs-lookup"><span data-stu-id="51bc0-112">These functions must be called with the appropriate filter or filter tag.</span></span> <span data-ttu-id="51bc0-113">L’exemple suivant montre comment utiliser ces fonctions.</span><span class="sxs-lookup"><span data-stu-id="51bc0-113">The following example shows how to use these functions.</span></span>


```C++
#include <mmsystem.h>
#include <mmreg.h>
#include <msacm.h>

BOOL GetFilterDescription 
( 
    LPWAVEFILTER  pwfltr, 
    LPTSTR        pszFilterTag, 
    DWORD         cchFilterTag, // Size of pszFilterTag buffer.
    LPTSTR        pszFilter,
    DWORD         cchFilter     // Size of pszFilter buffer.

) 
{ 
    MMRESULT      mmr; 
    errno_t       errno;
 
    // Retrieve the name for the filter tag of the specified filter. 
    if (NULL != pszFilterTag) { 
        ACMFILTERTAGDETAILS aftd; 
 
        // Initialize all unused members of the ACMFILTERTAGDETAILS 
        // structure to zero. 
        memset(&aftd, 0, sizeof(aftd)); 
 
        // Fill in the required members of the ACMFILTERTAGDETAILS 
        // structure for the ACM_FILTERTAGDETAILSF_FILTERTAG query. 
        aftd.cbStruct = sizeof(aftd); 
        aftd.dwFilterTag = pwfltr->dwFilterTag; 
 
        // Ask the ACM to find the first available driver that 
        // supports the specified filter tag. 
        mmr = acmFilterTagDetails(NULL, &aftd, 
            ACM_FILTERTAGDETAILSF_FILTERTAG); 
        if (MMSYSERR_NOERROR != mmr) { 
            // No ACM driver is available that supports the 
            // specified filter tag. 
            return FALSE; 
        } 
 
        // Copy the filter tag name into the calling application's 
        // buffer. 

        errno = wcscpy_s(pszFilterTag, cchFilterTag, aftd.szFilterTag); 
        if (errno != 0)
        {
            return FALSE;
        }
    } 
 
    // Retrieve the description of the attributes for the specified 
    // filter. 
    if (NULL != pszFilter) { 
        ACMFILTERDETAILS afd; 
 
        // Initialize all unused members of the ACMFILTERDETAILS 
        // structure to zero. 
        memset(&afd, 0, sizeof(afd)); 
 
        // Fill in the required members of the ACMFILTERDETAILS 
        // structure for the ACM_FILTERDETAILSF_FILTER query. 
        afd.cbStruct    = sizeof(afd); 
        afd.dwFilterTag = pwfltr->dwFilterTag; 
        afd.pwfltr      = pwfltr; 
        afd.cbwfltr     = pwfltr->cbStruct; 
 
        // Ask the ACM to find the first available driver that 
        // supports the specified filter. 
        mmr = acmFilterDetails(NULL, &afd, ACM_FILTERDETAILSF_FILTER); 
        if (MMSYSERR_NOERROR != mmr) { 
            // No ACM driver is available that supports the 
            // specified filter. 
            return FALSE; 
        } 
 
        // Copy the description string into the caller's buffer. 
        errno = wcscpy_s(pszFilter, cchFilter, afd.szFilter); 
        if (errno != 0)
        {
            return FALSE;
        }
    } 
 
    return TRUE; 
}
 
```



 

 




