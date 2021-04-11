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
# <a name="searching-binary-data"></a>Recherche de données binaires

Bien que la fonctionnalité de recherche ADSI ne prenne en charge que la recherche de données de type chaîne, il est possible de rechercher des données binaires. Pour ce faire, utilisez la fonction [**ADsEncodeBinaryData**](/windows/desktop/api/Adshlp/nf-adshlp-adsencodebinarydata) pour convertir les données binaires en une chaîne qui peut être utilisée avec les méthodes de recherche. La recherche de données binaires est particulièrement utile lors de la recherche d’un GUID ou d’un SID, car ces types de données sont stockés sous forme de données binaires.

Lors de l’utilisation de la fonction [**ADsEncodeBinaryData**](/windows/desktop/api/Adshlp/nf-adshlp-adsencodebinarydata) , la mémoire allouée doit être libérée à l’aide de la fonction [**FreeADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-freeadsmem) .

L’exemple de code C++ suivant montre comment créer une chaîne de requête pour rechercher un objet qui a une valeur **objectGUID** particulière.


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



 

 




