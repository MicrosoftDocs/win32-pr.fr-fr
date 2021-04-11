---
title: Recherche de données binaires
description: Bien que la fonctionnalité de recherche ADSI ne prenne en charge que la recherche de données de type chaîne, il est possible de rechercher des données binaires.
ms.assetid: 52b75ae0-dbf1-4310-8b6b-a176de9f1b7d
ms.tgt_platform: multiple
keywords:
- Recherche de données binaires ADSI
- Données binaires ADSI
- Données binaires ADSI, recherche de données binaires
- ADSI ADSI, exemple de code C/C++, recherche de données binaires
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0973ff7a769d68abf85e6557fef2e1d434ba3ff4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028553"
---
# <a name="searching-binary-data"></a><span data-ttu-id="68e53-107">Recherche de données binaires</span><span class="sxs-lookup"><span data-stu-id="68e53-107">Searching Binary Data</span></span>

<span data-ttu-id="68e53-108">Bien que la fonctionnalité de recherche ADSI ne prenne en charge que la recherche de données de type chaîne, il est possible de rechercher des données binaires.</span><span class="sxs-lookup"><span data-stu-id="68e53-108">Even though the ADSI search feature only supports searching for string data, it is possible to search for binary data.</span></span> <span data-ttu-id="68e53-109">Pour ce faire, utilisez la fonction [**ADsEncodeBinaryData**](/windows/desktop/api/Adshlp/nf-adshlp-adsencodebinarydata) pour convertir les données binaires en une chaîne qui peut être utilisée avec les méthodes de recherche.</span><span class="sxs-lookup"><span data-stu-id="68e53-109">To do this, use the [**ADsEncodeBinaryData**](/windows/desktop/api/Adshlp/nf-adshlp-adsencodebinarydata) function to convert the binary data into a string that can be used with the search methods.</span></span> <span data-ttu-id="68e53-110">La recherche de données binaires est particulièrement utile lors de la recherche d’un GUID ou d’un SID, car ces types de données sont stockés sous forme de données binaires.</span><span class="sxs-lookup"><span data-stu-id="68e53-110">Searching for binary data is particularly useful when searching for a GUID or a SID because these data types are stored as binary data.</span></span>

<span data-ttu-id="68e53-111">Lors de l’utilisation de la fonction [**ADsEncodeBinaryData**](/windows/desktop/api/Adshlp/nf-adshlp-adsencodebinarydata) , la mémoire allouée doit être libérée à l’aide de la fonction [**FreeADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-freeadsmem) .</span><span class="sxs-lookup"><span data-stu-id="68e53-111">When using the [**ADsEncodeBinaryData**](/windows/desktop/api/Adshlp/nf-adshlp-adsencodebinarydata) function, the memory allocated must be freed using the [**FreeADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-freeadsmem) function.</span></span>

<span data-ttu-id="68e53-112">L’exemple de code C++ suivant montre comment créer une chaîne de requête pour rechercher un objet qui a une valeur **objectGUID** particulière.</span><span class="sxs-lookup"><span data-stu-id="68e53-112">The following C++ code example shows how to build a query string to search for an object that has a particular **objectGUID** value.</span></span>


```C++
LPWSTR pwszGuid = NULL;
LPWSTR pwszFormat = L"(objectGUID=%s)";
LPWSTR pwszSearch = NULL;
hr = ADsEncodeBinaryData((LPBYTE)pguid, sizeof(GUID), &pwszGuid);
if(FAILED(hr))
{
    goto cleanup;
}

pwszSearch = new WCHAR[lstrlenW(pwszFormat) + lstrlenW(pwszGuid) + 1];
if(NULL == pwszSearch)
{
    goto cleanup;
}
    
swprintf_s(pwszSearch, pwszFormat, pwszGuid);

// Use pwszSearch to perform a query for the object.

cleanup:    
if(pwszGuid)
{
    FreeADsMem(pwszGuid);
}
if(pwszSearch)
{
    delete pwszSearch;
}

```



 

 




