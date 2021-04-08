---
title: Exemple de code pour la recherche d’attributs
description: L’exemple de code suivant montre comment utiliser la \_ préférence de \_ recherche SEARCHPREF ATTRIBTYPES de publicités \_ uniquement pour récupérer uniquement les noms des attributs auxquels des valeurs ont été assignées.
ms.assetid: 0e166f06-6030-4615-a46d-a282961d3b55
ms.tgt_platform: multiple
keywords:
- ADSI, exemple de code C/C++, recherche d’attributs
- Exemple de code pour la recherche d’attributs
- ADSI, recherche, IDirectorySearch, autres options de recherche, retournant uniquement des noms d’attributs, exemple de code
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 344ce99fe9de606212d786ff2e7b88b5eba34d14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671154"
---
# <a name="example-code-for-searching-for-attributes"></a>Exemple de code pour la recherche d’attributs

L’exemple de code suivant montre comment utiliser la préférence de recherche **\_ SEARCHPREF ATTRIBTYPES de publicités \_ \_ uniquement** pour récupérer uniquement les noms des attributs auxquels des valeurs ont été assignées. L’exemple Initialise une structure [**\_ \_ info SEARCHPREF ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) et définit la préférence de recherche en appelant la méthode [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) de l’interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) . L’exemple appelle ensuite la méthode [**ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) pour effectuer la recherche.


```C++
// Setting the search preference.
// m_pSearch is a valid pointer to an IDirectorySearch interface.
ADS_SEARCHPREF_INFO prefInfo[1];
LPWSTR pszColumn = NULL;

// Set the search preference to indicate attribute names only.
prefInfo[0].dwSearchPref = ADS_SEARCHPREF_ATTRIBTYPES_ONLY;
prefInfo[0].vValue.dwType = ADSTYPE_BOOLEAN;
prefInfo[0].vValue.Integer = TRUE;
hr = m_pSearch->SetSearchPreference(prefInfo, 1);

// Execute the search.
hr = m_pSearch->ExecuteSearch(
                L"(|(objectCategory=domainDNS)(objectCategory=organizationalUnit))", 
                NULL, -1, &hSearch );

if(FAILED(hr))
{
   return;
}

// Retrieve the column name.
hr = m_pSearch->GetNextRow(hSearch);

if(FAILED(hr))
{
   return;
}
    
while( m_pSearch->GetNextColumnName( hSearch, &pszColumn ) != S_ADS_NOMORE_COLUMNS )
{
   wprintf(L"%S ", pszColumn );
   FreeADsMem( pszColumn );
}
```



 

 




