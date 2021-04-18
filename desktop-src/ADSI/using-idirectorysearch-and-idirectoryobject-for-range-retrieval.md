---
title: Utilisation de IDirectorySearch et IDirectoryObject pour la récupération de plages
description: Les interfaces IDirectoryObject ou IDirectorySearch peuvent être utilisées pour récupérer une plage de valeurs de propriété. Pour ce faire, spécifiez l’attribut et la plage de l’un des attributs demandés dans la requête.
ms.assetid: 4d9d2a98-51d5-4326-b43e-a2ac3bc54a75
ms.tgt_platform: multiple
keywords:
- Interface ADSI IDirectorySearch, utilisant pour récupérer les membres d’un groupe
- IDirectoryObject ADSI, utilisant pour récupérer les membres d’un groupe
- ADSI de récupération de plage, avec IDirectorySearch et IDirectoryObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 591d2cf7b65b7a8159a92de324f18fbe93164f0e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512017"
---
# <a name="using-idirectorysearch-and-idirectoryobject-for-range-retrieval"></a>Utilisation de IDirectorySearch et IDirectoryObject pour la récupération de plages

Les interfaces [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) ou [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) peuvent être utilisées pour récupérer une plage de valeurs de propriété. Pour ce faire, spécifiez l’attribut et la plage de l’un des attributs demandés dans la requête.

## <a name="range-retrieval-with-idirectoryobject"></a>Récupération de plage avec IDirectoryObject

L’interface [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) peut être utilisée pour la récupération de plages en spécifiant l’attribut et la plage de l’un des attributs du tableau *pAttributesName* lors de l’appel de la méthode [**IDirectoryObject :: GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) .


```C++
PADS_ATTR_INFO pAttrInfo;
DWORD dwRetrieved;
LPWSTR pszAttrs[2];
 
pszAttrs[0] = L"Name";
pszAttrs[1] = L"member;range=0-100";

hr = pdo->GetObjectAttributes(pszAttrs, 2, &pAttrInfo, &dwRetrieved);
```



Pour plus d’informations et pour obtenir un exemple de code qui montre comment utiliser l’interface [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) pour la récupération de plages, consultez l' [exemple de code pour](example-code-for-ranging-with-idirectoryobject.md)plus de détails avec IDirectoryObject.

## <a name="range-retrieval-with-idirectorysearch"></a>Récupération de plage avec IDirectorySearch

L’interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) peut être utilisée pour la récupération de plages en spécifiant l’attribut et la plage de l’un des attributs récupérés dans le tableau *pAttributesName* lors de l’appel de la méthode [**IDirectorySearch :: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) .


```C++
ADS_SEARCH_HANDLE hSearch;
LPWSTR pszAttrs[2];
 
pszAttrs[0] = L"Name";
pszAttrs[1] = L"member;range=0-100";

hr = pdo->ExecuteSearch(L"(objectClass=user)", pszAttrs, 2, &hSearch);
```



Lors de l’utilisation de l’interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) pour la récupération de plages, il existe un problème qui doit être traité spécifiquement. Lorsque la plage demandée dépasse le nombre de valeurs restantes, [**IDirectorySearch :: GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) retourne la **\_ colonne E ADS \_ \_ non \_ définie**. Pour récupérer les valeurs restantes, il est nécessaire d’utiliser le caractère générique de plage « \* ». Par exemple, si un groupe contient 150 membres, les valeurs de membre 0-100 peuvent être récupérées normalement à l’aide d’une récupération étendue. Si la plage 101-200 est ensuite demandée, **IDirectorySearch :: GetColumn** retourne **la \_ colonne E ADS \_ \_ non \_ définie**. Ce problème peut être évité à l’aide de la méthode [**IDirectorySearch :: GetNextColumnName**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextcolumnname) . Normalement, **GetNextColumnName** retourne la chaîne de requête d’origine. Toutefois, lorsque la plage demandée dépasse le nombre de valeurs restantes, **GetNextColumnName** retourne une version modifiée de la chaîne de requête en remplaçant la valeur de la plage supérieure par le caractère générique de la plage « \* ». Dans l’exemple ci-dessus, la première requête est exécutée avec une chaîne d’attribut "Member ; Range = 0-100" et **GetNextColumnName** retourne "Member ; Range = 0-100". Dans la deuxième requête, la chaîne d’attribut est "Member ; Range = 101-200", mais **GetNextColumnName** retourne "Member ; Range = 101- \* ". Ce cas peut être déterminé en comparant la chaîne d’attribut d’origine au résultat de **GetNextColumnName**. Si les chaînes sont différentes, le dernier bloc de valeurs doit être redemandé avec le caractère générique de la plage.

Pour plus d’informations et pour obtenir un exemple de code qui montre comment utiliser l’interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) pour la récupération de plages, consultez l' [exemple de code pour](example-code-for-ranging-with-idirectorysearch.md)plus d’informations sur IDirectorySearch.

 

 




