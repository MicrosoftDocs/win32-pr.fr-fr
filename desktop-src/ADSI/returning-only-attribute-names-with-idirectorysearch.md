---
title: Retour uniquement des noms d’attributs avec IDirectorySearch
description: Vous pouvez effectuer une recherche pour déterminer le type de données disponibles pour un objet particulier.
ms.assetid: 47e78b79-2063-420b-aa41-f4f0c35f87ea
ms.tgt_platform: multiple
keywords:
- Retour uniquement des noms d’attributs avec l’ADSI IDirectorySearch
- ADSI, recherche, IDirectorySearch, autres options de recherche, en retournant uniquement les noms d’attributs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 055acbb3fe19969ce95ea77a633e20b195c0257d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509362"
---
# <a name="returning-only-attribute-names-with-idirectorysearch"></a><span data-ttu-id="ea725-105">Retour uniquement des noms d’attributs avec IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="ea725-105">Returning Only Attribute Names with IDirectorySearch</span></span>

<span data-ttu-id="ea725-106">Vous pouvez effectuer une recherche pour déterminer le type de données disponibles pour un objet particulier.</span><span class="sxs-lookup"><span data-stu-id="ea725-106">You can perform a search to determine what type of data is available for a particular object.</span></span> <span data-ttu-id="ea725-107">Dans ce cas, vous vous intéressez uniquement aux noms d’attributs, et non aux valeurs d’attribut de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ea725-107">In this case, you are only interested in the attributes names, not the attribute values of the object.</span></span> <span data-ttu-id="ea725-108">L’option **ad \_ SEARCHPREF \_ ATTRIBTYPES \_ only** indique au serveur de retourner uniquement les noms d’attributs et non les valeurs d’attribut.</span><span class="sxs-lookup"><span data-stu-id="ea725-108">The **ADS\_SEARCHPREF\_ATTRIBTYPES\_ONLY** option causes the server to only return the attribute names and not the attribute values.</span></span> <span data-ttu-id="ea725-109">Toutefois, le jeu de résultats comprend uniquement les attributs qui ont des valeurs affectées.</span><span class="sxs-lookup"><span data-stu-id="ea725-109">However, the result set includes only those attributes that have values assigned.</span></span> <span data-ttu-id="ea725-110">Par exemple, considérez un objet avec les attributs suivants :</span><span class="sxs-lookup"><span data-stu-id="ea725-110">For example, consider an object with the following attributes:</span></span>

``` syntax
name = Jeff
sn = Smith
department = Empty
phone = 206-555-0111
```

<span data-ttu-id="ea725-111">Lorsque l’option **ad \_ SEARCHPREF \_ ATTRIBTYPES \_ only** est définie, le jeu de résultats comprend les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="ea725-111">When the **ADS\_SEARCHPREF\_ATTRIBTYPES\_ONLY** option is set, the result set includes:</span></span>

``` syntax
name
sn
department
phone
```

<span data-ttu-id="ea725-112">La valeur par défaut est pour le retour des valeurs et des noms d’attribut.</span><span class="sxs-lookup"><span data-stu-id="ea725-112">The default is for both attribute values and names to be returned.</span></span>

<span data-ttu-id="ea725-113">Pour récupérer uniquement des noms d’attributs, définissez une option de recherche **\_ SEARCHPREF \_ ATTRIBTYPES ADS \_ uniquement** avec une valeur **\_ booléenne ADSTYPE** **true** dans le tableau d' [**\_ \_ informations SEARCHPREF ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passé à la méthode [**IDirectorySearch :: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .</span><span class="sxs-lookup"><span data-stu-id="ea725-113">To retrieve only attribute names, set an **ADS\_SEARCHPREF\_ATTRIBTYPES\_ONLY** search option with an **ADSTYPE\_BOOLEAN** value of **TRUE** in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span>

<span data-ttu-id="ea725-114">L’exemple de code suivant montre comment récupérer uniquement des noms d’attributs.</span><span class="sxs-lookup"><span data-stu-id="ea725-114">The following code example shows how to retrieve attribute names only.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_ATTRIBTYPES_ONLY;
SearchPref.vValue.dwType = ADSTYPE_BOOLEAN;
SearchPref.vValue.Boolean = TRUE;
```



<span data-ttu-id="ea725-115">Pour plus d’informations et pour obtenir un exemple de code qui montre comment utiliser l’option de recherche **\_ ATTRIBTYPES SEARCHPREF ADS \_ \_ uniquement** , consultez l' [exemple de code pour rechercher des attributs](example-code-for-searching-for-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="ea725-115">For more information and a code example that shows how to use the **ADS\_SEARCHPREF\_ATTRIBTYPES\_ONLY** search option, see [Example Code for Searching for Attributes](example-code-for-searching-for-attributes.md).</span></span>

 

 




