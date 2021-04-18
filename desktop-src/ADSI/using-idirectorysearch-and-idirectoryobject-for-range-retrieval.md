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
# <a name="using-idirectorysearch-and-idirectoryobject-for-range-retrieval"></a><span data-ttu-id="496e4-107">Utilisation de IDirectorySearch et IDirectoryObject pour la récupération de plages</span><span class="sxs-lookup"><span data-stu-id="496e4-107">Using IDirectorySearch and IDirectoryObject for Range Retrieval</span></span>

<span data-ttu-id="496e4-108">Les interfaces [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) ou [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) peuvent être utilisées pour récupérer une plage de valeurs de propriété.</span><span class="sxs-lookup"><span data-stu-id="496e4-108">The [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) or [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interfaces can be used to retrieve a range of property values.</span></span> <span data-ttu-id="496e4-109">Pour ce faire, spécifiez l’attribut et la plage de l’un des attributs demandés dans la requête.</span><span class="sxs-lookup"><span data-stu-id="496e4-109">To do this, specify the attribute and range for one of the attributes requested in the query.</span></span>

## <a name="range-retrieval-with-idirectoryobject"></a><span data-ttu-id="496e4-110">Récupération de plage avec IDirectoryObject</span><span class="sxs-lookup"><span data-stu-id="496e4-110">Range Retrieval with IDirectoryObject</span></span>

<span data-ttu-id="496e4-111">L’interface [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) peut être utilisée pour la récupération de plages en spécifiant l’attribut et la plage de l’un des attributs du tableau *pAttributesName* lors de l’appel de la méthode [**IDirectoryObject :: GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) .</span><span class="sxs-lookup"><span data-stu-id="496e4-111">The [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) interface can be used for range retrieval by specifying the attribute and range for one of the attributes in the *pAttributesName* array when calling the [**IDirectoryObject::GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) method.</span></span>


```C++
PADS_ATTR_INFO pAttrInfo;
DWORD dwRetrieved;
LPWSTR pszAttrs[2];
 
pszAttrs[0] = L"Name";
pszAttrs[1] = L"member;range=0-100";

hr = pdo->GetObjectAttributes(pszAttrs, 2, &pAttrInfo, &dwRetrieved);
```



<span data-ttu-id="496e4-112">Pour plus d’informations et pour obtenir un exemple de code qui montre comment utiliser l’interface [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) pour la récupération de plages, consultez l' [exemple de code pour](example-code-for-ranging-with-idirectoryobject.md)plus de détails avec IDirectoryObject.</span><span class="sxs-lookup"><span data-stu-id="496e4-112">For more information and a code example that shows how to use the [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) interface for range retrieval, see [Example Code for Ranging with IDirectoryObject](example-code-for-ranging-with-idirectoryobject.md).</span></span>

## <a name="range-retrieval-with-idirectorysearch"></a><span data-ttu-id="496e4-113">Récupération de plage avec IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="496e4-113">Range Retrieval with IDirectorySearch</span></span>

<span data-ttu-id="496e4-114">L’interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) peut être utilisée pour la récupération de plages en spécifiant l’attribut et la plage de l’un des attributs récupérés dans le tableau *pAttributesName* lors de l’appel de la méthode [**IDirectorySearch :: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) .</span><span class="sxs-lookup"><span data-stu-id="496e4-114">The [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface can be used for range retrieval by specifying the attribute and range for one of the retrieved attributes in the *pAttributesName* array when calling the [**IDirectorySearch::ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) method.</span></span>


```C++
ADS_SEARCH_HANDLE hSearch;
LPWSTR pszAttrs[2];
 
pszAttrs[0] = L"Name";
pszAttrs[1] = L"member;range=0-100";

hr = pdo->ExecuteSearch(L"(objectClass=user)", pszAttrs, 2, &hSearch);
```



<span data-ttu-id="496e4-115">Lors de l’utilisation de l’interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) pour la récupération de plages, il existe un problème qui doit être traité spécifiquement.</span><span class="sxs-lookup"><span data-stu-id="496e4-115">When using the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface for range retrieval, there is one problem that must be specifically addressed.</span></span> <span data-ttu-id="496e4-116">Lorsque la plage demandée dépasse le nombre de valeurs restantes, [**IDirectorySearch :: GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) retourne la **\_ colonne E ADS \_ \_ non \_ définie**.</span><span class="sxs-lookup"><span data-stu-id="496e4-116">When the range requested exceeds the number of remaining values, [**IDirectorySearch::GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) will return **E\_ADS\_COLUMN\_NOT\_SET**.</span></span> <span data-ttu-id="496e4-117">Pour récupérer les valeurs restantes, il est nécessaire d’utiliser le caractère générique de plage « \* ».</span><span class="sxs-lookup"><span data-stu-id="496e4-117">To retrieve the remaining values, it is necessary to use the range wildcard '\*'.</span></span> <span data-ttu-id="496e4-118">Par exemple, si un groupe contient 150 membres, les valeurs de membre 0-100 peuvent être récupérées normalement à l’aide d’une récupération étendue.</span><span class="sxs-lookup"><span data-stu-id="496e4-118">For example, if a group contains 150 members, member values 0-100 can be retrieved normally using ranged retrieval.</span></span> <span data-ttu-id="496e4-119">Si la plage 101-200 est ensuite demandée, **IDirectorySearch :: GetColumn** retourne **la \_ colonne E ADS \_ \_ non \_ définie**.</span><span class="sxs-lookup"><span data-stu-id="496e4-119">If range 101-200 is then requested, **IDirectorySearch::GetColumn** will return **E\_ADS\_COLUMN\_NOT\_SET**.</span></span> <span data-ttu-id="496e4-120">Ce problème peut être évité à l’aide de la méthode [**IDirectorySearch :: GetNextColumnName**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextcolumnname) .</span><span class="sxs-lookup"><span data-stu-id="496e4-120">This problem can be avoided by using the [**IDirectorySearch::GetNextColumnName**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextcolumnname) method.</span></span> <span data-ttu-id="496e4-121">Normalement, **GetNextColumnName** retourne la chaîne de requête d’origine.</span><span class="sxs-lookup"><span data-stu-id="496e4-121">Normally, **GetNextColumnName** will return the original query string.</span></span> <span data-ttu-id="496e4-122">Toutefois, lorsque la plage demandée dépasse le nombre de valeurs restantes, **GetNextColumnName** retourne une version modifiée de la chaîne de requête en remplaçant la valeur de la plage supérieure par le caractère générique de la plage « \* ».</span><span class="sxs-lookup"><span data-stu-id="496e4-122">However, when the range requested exceeds the number of remaining values, **GetNextColumnName** will return a modified version of the query string by replacing the high range value with the range wildcard '\*'.</span></span> <span data-ttu-id="496e4-123">Dans l’exemple ci-dessus, la première requête est exécutée avec une chaîne d’attribut "Member ; Range = 0-100" et **GetNextColumnName** retourne "Member ; Range = 0-100".</span><span class="sxs-lookup"><span data-stu-id="496e4-123">In the example above, the first query would be performed with an attribute string of "member;range=0-100" and **GetNextColumnName** will return "member;range=0-100".</span></span> <span data-ttu-id="496e4-124">Dans la deuxième requête, la chaîne d’attribut est "Member ; Range = 101-200", mais **GetNextColumnName** retourne "Member ; Range = 101- \* ".</span><span class="sxs-lookup"><span data-stu-id="496e4-124">In the second query, the attribute string would be "member;range=101-200", but **GetNextColumnName** will return "member;range=101-\*".</span></span> <span data-ttu-id="496e4-125">Ce cas peut être déterminé en comparant la chaîne d’attribut d’origine au résultat de **GetNextColumnName**.</span><span class="sxs-lookup"><span data-stu-id="496e4-125">This case can be determined by comparing the original attribute string to the result of **GetNextColumnName**.</span></span> <span data-ttu-id="496e4-126">Si les chaînes sont différentes, le dernier bloc de valeurs doit être redemandé avec le caractère générique de la plage.</span><span class="sxs-lookup"><span data-stu-id="496e4-126">If the strings are different, the last block of values should be requested again with the range wildcard.</span></span>

<span data-ttu-id="496e4-127">Pour plus d’informations et pour obtenir un exemple de code qui montre comment utiliser l’interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) pour la récupération de plages, consultez l' [exemple de code pour](example-code-for-ranging-with-idirectorysearch.md)plus d’informations sur IDirectorySearch.</span><span class="sxs-lookup"><span data-stu-id="496e4-127">For more information and a code example that shows how to use the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface for range retrieval, see [Example Code for Ranging with IDirectorySearch](example-code-for-ranging-with-idirectorysearch.md).</span></span>

 

 




