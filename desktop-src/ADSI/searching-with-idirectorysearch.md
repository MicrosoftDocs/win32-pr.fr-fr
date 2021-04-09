---
title: Recherche avec l’interface IDirectorySearch
description: L’interface IDirectorySearch fournit une interface de haut niveau et de faible surcharge pour l’interrogation des données d’un répertoire ou d’un catalogue global.
ms.assetid: da415cb2-f320-4be4-b5bd-053cd6a6b2fd
ms.tgt_platform: multiple
keywords:
- Recherche à l’aide de l’interface ADSI de l’interface IDirectorySearch
- Requêtes ADSI, interfaces de requête, IDirectorySearch
- ADSI ADSI, exemple de code C/C++, recherche dans un répertoire avec IDirectorySearch
- Interface ADSI IDirectorySearch, utilisation de pour rechercher un répertoire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2738e163f672fb0000275e2fb9d885442ae6693
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103842742"
---
# <a name="searching-with-the-idirectorysearch-interface"></a><span data-ttu-id="e52cc-107">Recherche avec l’interface IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="e52cc-107">Searching with the IDirectorySearch Interface</span></span>

<span data-ttu-id="e52cc-108">L’interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) fournit une interface de haut niveau et de faible surcharge pour l’interrogation des données d’un répertoire ou d’un catalogue global.</span><span class="sxs-lookup"><span data-stu-id="e52cc-108">The [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface provides a high-level and low-overhead interface for querying data of a directory or a global catalog.</span></span> <span data-ttu-id="e52cc-109">L’interface com **IDirectorySearch** ne peut être utilisée qu’avec un vtable et, par conséquent, n’est pas disponible pour les environnements de développement basés sur Automation.</span><span class="sxs-lookup"><span data-stu-id="e52cc-109">The **IDirectorySearch** COM interface can be used only with a vtable, and thus, is not available to Automation-based development environments.</span></span>

<span data-ttu-id="e52cc-110">**Pour effectuer une recherche**</span><span class="sxs-lookup"><span data-stu-id="e52cc-110">**To perform a search**</span></span>

1.  <span data-ttu-id="e52cc-111">Effectuer une liaison à un objet dans l’annuaire.</span><span class="sxs-lookup"><span data-stu-id="e52cc-111">Bind to an object in the directory.</span></span>
2.  <span data-ttu-id="e52cc-112">Appelez [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pour récupérer le pointeur [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) .</span><span class="sxs-lookup"><span data-stu-id="e52cc-112">Call [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to get the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) pointer.</span></span>
3.  <span data-ttu-id="e52cc-113">Exécutez la recherche à l’aide du pointeur [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) .</span><span class="sxs-lookup"><span data-stu-id="e52cc-113">Run the search using the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) pointer.</span></span> <span data-ttu-id="e52cc-114">Appelez la méthode [**IDirectorySearch :: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) et transmettez un filtre de recherche, les noms d’attributs demandés et d’autres paramètres.</span><span class="sxs-lookup"><span data-stu-id="e52cc-114">Call the [**IDirectorySearch::ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) method, and pass a search filter, the requested attribute names, and other parameters.</span></span>

<span data-ttu-id="e52cc-115">Pour plus d’informations sur la syntaxe de filtre de recherche, consultez [syntaxe de filtre de recherche](search-filter-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="e52cc-115">For more information about the search filter syntax, see [Search Filter Syntax](search-filter-syntax.md).</span></span>

<span data-ttu-id="e52cc-116">L’exécution de la requête est spécifique au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="e52cc-116">Query execution is provider-specific.</span></span> <span data-ttu-id="e52cc-117">Avec certains fournisseurs, l’exécution réelle de la requête ne se produit pas tant que [**IDirectorySearch :: GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) ou [**IDirectorySearch :: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) n’est pas appelé.</span><span class="sxs-lookup"><span data-stu-id="e52cc-117">With some providers, the actual query execution does not occur until [**IDirectorySearch::GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) or [**IDirectorySearch::GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) is called.</span></span> <span data-ttu-id="e52cc-118">L’interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) fonctionne avec les filtres de recherche directement.</span><span class="sxs-lookup"><span data-stu-id="e52cc-118">The [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface works with search filters directly.</span></span> <span data-ttu-id="e52cc-119">Ni le dialecte SQL ni le dialecte LDAP ne sont requis.</span><span class="sxs-lookup"><span data-stu-id="e52cc-119">Neither the SQL dialect nor the LDAP dialect are required.</span></span>

<span data-ttu-id="e52cc-120">L’interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) fournit des méthodes pour énumérer le jeu de résultats, ligne par ligne.</span><span class="sxs-lookup"><span data-stu-id="e52cc-120">The [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface provides methods to enumerate the result set, row by row.</span></span> <span data-ttu-id="e52cc-121">La méthode [**IDirectorySearch :: GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) récupère la première ligne et [**IDirectorySearch :: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) vous ramène à la ligne suivante de la ligne actuelle.</span><span class="sxs-lookup"><span data-stu-id="e52cc-121">The [**IDirectorySearch::GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) method retrieves the first row and [**IDirectorySearch::GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) moves you to the next row from the current row.</span></span> <span data-ttu-id="e52cc-122">Une fois que vous avez atteint la dernière ligne, l’appel de ces méthodes retourne le code d’erreur S de \_ \_ \_ lignes.</span><span class="sxs-lookup"><span data-stu-id="e52cc-122">When you have reached the last row, calling these methods returns the S\_ADS\_NOMORE\_ROWS error code.</span></span> <span data-ttu-id="e52cc-123">À l’inverse, [**IDirectorySearch :: GetPreviousRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getpreviousrow) vous ramène une ligne à la fois.</span><span class="sxs-lookup"><span data-stu-id="e52cc-123">Conversely, [**IDirectorySearch::GetPreviousRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getpreviousrow) moves you back one row at a time.</span></span> <span data-ttu-id="e52cc-124">\_ \_ \_ La valeur renvoyée par des lignes est trop grande pour indiquer que vous avez atteint la première ligne du jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="e52cc-124">An S\_ADS\_NOMORE\_ROWS return value indicates that you have reached the first row of the result set.</span></span> <span data-ttu-id="e52cc-125">Ces méthodes opèrent sur le jeu de résultats, résidant en mémoire, sur le client.</span><span class="sxs-lookup"><span data-stu-id="e52cc-125">These methods operate on the result set, resident in memory, on the client.</span></span> <span data-ttu-id="e52cc-126">Ainsi, lorsque des recherches paginées et asynchrones sont effectuées et que l' \_ option des résultats du cache \_ est désactivée, le défilement vers l’arrière peut avoir des conséquences inattendues.</span><span class="sxs-lookup"><span data-stu-id="e52cc-126">Thus, when paged and asynchronous searches are performed and the \_CACHE\_RESULTS option is turned off, backward scrolling can have unexpected consequences.</span></span>

<span data-ttu-id="e52cc-127">Une fois que vous avez localisé la ligne appropriée, appelez [**IDirectorySearch :: GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) pour obtenir des éléments de données, colonne par colonne.</span><span class="sxs-lookup"><span data-stu-id="e52cc-127">When you have located the appropriate row, call [**IDirectorySearch::GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) to obtain data items, column by column.</span></span> <span data-ttu-id="e52cc-128">Pour chaque appel, vous transmettez le nom de la colonne qui vous intéresse.</span><span class="sxs-lookup"><span data-stu-id="e52cc-128">For each call, you pass the name of the column of interest.</span></span> <span data-ttu-id="e52cc-129">L’élément de données retourné est un pointeur vers une structure de [**\_ \_ colonne de recherche ADS**](/windows/desktop/api/Iads/ns-iads-ads_search_column) .</span><span class="sxs-lookup"><span data-stu-id="e52cc-129">The data item returned is a pointer to an [**ADS\_SEARCH\_COLUMN**](/windows/desktop/api/Iads/ns-iads-ads_search_column) structure.</span></span> <span data-ttu-id="e52cc-130">**GetColumn** alloue cette structure pour vous, mais vous devez la libérer à l’aide de [**FreeColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-freecolumn).</span><span class="sxs-lookup"><span data-stu-id="e52cc-130">**GetColumn** allocates this structure for you, but you must free it using [**FreeColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-freecolumn).</span></span> <span data-ttu-id="e52cc-131">Appelez [**CloseSearchHandle**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-closesearchhandle) pour terminer l’opération de recherche.</span><span class="sxs-lookup"><span data-stu-id="e52cc-131">Call [**CloseSearchHandle**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-closesearchhandle) to complete the search operation.</span></span>

<span data-ttu-id="e52cc-132">**Pour effectuer une recherche dans les annuaires**</span><span class="sxs-lookup"><span data-stu-id="e52cc-132">**To perform a directory search**</span></span>

1.  <span data-ttu-id="e52cc-133">Liaison à un fournisseur LDAP.</span><span class="sxs-lookup"><span data-stu-id="e52cc-133">Bind to an LDAP provider.</span></span> <span data-ttu-id="e52cc-134">Il peut s’agir d’un contrôleur de domaine ou d’un fournisseur de catalogue global.</span><span class="sxs-lookup"><span data-stu-id="e52cc-134">It may be a domain controller or a global catalog provider.</span></span>
2.  <span data-ttu-id="e52cc-135">Récupérez l’interface com [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) à l’aide d’un appel à [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)); Cette opération a peut-être été effectuée à l’étape 1 pendant la liaison initiale.</span><span class="sxs-lookup"><span data-stu-id="e52cc-135">Retrieve the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) COM Interface with a call to [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)); this operation may have been done in Step 1 during the initial binding.</span></span>

    <span data-ttu-id="e52cc-136">Si vous le souhaitez, appelez [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) pour sélectionner les options de gestion des résultats de votre recherche.</span><span class="sxs-lookup"><span data-stu-id="e52cc-136">Optionally, call [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) to select options for handling the results of your search.</span></span>

3.  <span data-ttu-id="e52cc-137">Appelez [**ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch).</span><span class="sxs-lookup"><span data-stu-id="e52cc-137">Call [**ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch).</span></span> <span data-ttu-id="e52cc-138">Selon les options définies dans [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) , cela peut ou non commencer à exécuter la requête.</span><span class="sxs-lookup"><span data-stu-id="e52cc-138">Depending on the options set in [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) this may, or may not, begin query execution.</span></span>
4.  <span data-ttu-id="e52cc-139">Appelez [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) pour déplacer l’index de ligne (interne vers [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)) vers la première ligne.</span><span class="sxs-lookup"><span data-stu-id="e52cc-139">Call [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) to move the row index (internal to [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)) to the first row.</span></span>
5.  <span data-ttu-id="e52cc-140">Lisez les données de la ligne à l’aide de [**GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn), puis appelez [**FreeColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-freecolumn) pour libérer la mémoire allouée par **GetColumn**.</span><span class="sxs-lookup"><span data-stu-id="e52cc-140">Read the data from the row using [**GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn), then call [**FreeColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-freecolumn) to release the memory allocated by **GetColumn**.</span></span>
6.  <span data-ttu-id="e52cc-141">Répétez l’étape 5 jusqu’à ce que toutes les données soient récupérées à partir du résultat de la recherche, ou jusqu’à ce que la méthode [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) renvoie des \_ lignes de publicités \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e52cc-141">Repeat Step 5 until all data is retrieved from the search result, or until [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) returns S\_ADS\_NOMORE\_ROWS.</span></span>
7.  <span data-ttu-id="e52cc-142">Appelez [**AbandonSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-abandonsearch) et [**CloseSearchHandle**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-closesearchhandle) lorsque vous avez terminé.</span><span class="sxs-lookup"><span data-stu-id="e52cc-142">Call [**AbandonSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-abandonsearch) and [**CloseSearchHandle**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-closesearchhandle) when complete.</span></span>

<span data-ttu-id="e52cc-143">L’exemple de code suivant illustre ce scénario.</span><span class="sxs-lookup"><span data-stu-id="e52cc-143">The following code example shows this scenario.</span></span> <span data-ttu-id="e52cc-144">Pour démarrer la liaison à ADSI, appelez la fonction [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) .</span><span class="sxs-lookup"><span data-stu-id="e52cc-144">To start binding to ADSI, call the [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) function.</span></span>


```C++
HRESULT hr = S_OK; // COM result variable
ADS_SEARCH_COLUMN col;  // COL for iterations
LPWSTR szUsername = NULL; // user name
LPWSTR szPassword = NULL; // password
 
// Interface Pointers.
IDirectorySearch     *pDSSearch    =NULL;
 
// Initialize COM.
CoInitialize(0);

// Add code to securely retrieve the user name and password or
// leave both as NULL to use the default security context.
 
// Open a connection with server.
hr = ADsOpenObject(L"LDAP://coho.salmon.Fabrikam.com", 
szUsername,
szPassword,
ADS_SECURE_AUTHENTICATION,
IID_IDirectorySearch,
(void **)&pDSSearch);
```



<span data-ttu-id="e52cc-145">Cela fournit un pointeur vers l’interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) .</span><span class="sxs-lookup"><span data-stu-id="e52cc-145">This provides a pointer to the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface.</span></span>

<span data-ttu-id="e52cc-146">Maintenant qu’il existe une interface COM pour une instance IDirectoryInterface, appelez [**IDirectorySearch :: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference).</span><span class="sxs-lookup"><span data-stu-id="e52cc-146">Now that there is a COM interface for an IDirectoryInterface instance, call [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference).</span></span>

<span data-ttu-id="e52cc-147">Générez un tableau de noms d’attributs pour préparer l’appel de la fonction [**IDirectorySearch :: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) .</span><span class="sxs-lookup"><span data-stu-id="e52cc-147">Build an array of attribute names to prepare to call the [**IDirectorySearch::ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) function.</span></span> <span data-ttu-id="e52cc-148">Les noms d’attributs sont définis dans le schéma de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e52cc-148">The attribute names are defined within the schema of Active Directory.</span></span> <span data-ttu-id="e52cc-149">Pour plus d’informations sur la définition de schéma, consultez [modèle de schéma ADSI](adsi-schema-model.md).</span><span class="sxs-lookup"><span data-stu-id="e52cc-149">For more information about the schema definition, see [ADSI Schema Model](adsi-schema-model.md).</span></span> <span data-ttu-id="e52cc-150">Les noms d’attributs répertoriés sont retournés, s’ils sont pris en charge par l’objet, comme le jeu de résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="e52cc-150">The attribute names listed are returned, if supported by the object, as the result set of the search.</span></span>


```C++
LPWSTR pszAttr[] = { L"description", L"Name", L"distinguishedname" };
ADS_SEARCH_HANDLE hSearch;
DWORD dwCount = 0;
DWORD dwAttrNameSize = sizeof(pszAttr)/sizeof(LPWSTR);
```



<span data-ttu-id="e52cc-151">À présent, appelez la fonction [**ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) .</span><span class="sxs-lookup"><span data-stu-id="e52cc-151">Now, call the [**ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) function.</span></span> <span data-ttu-id="e52cc-152">La recherche ne s’exécute pas tant que vous n’avez pas appelé la méthode [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) .</span><span class="sxs-lookup"><span data-stu-id="e52cc-152">The search does not run until you call the [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) method.</span></span>


```C++
// Search for all objects with the 'cn' property that start with c.
hr = pDSSearch->ExecuteSearch(L"(cn=c*)",pszAttr ,dwAttrNameSize,&hSearch );
```



<span data-ttu-id="e52cc-153">Appelez [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) pour itérer les lignes dans le résultat.</span><span class="sxs-lookup"><span data-stu-id="e52cc-153">Call [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) to iterate rows in the result.</span></span> <span data-ttu-id="e52cc-154">Chaque ligne est ensuite interrogée pour obtenir l’attribut « Description ».</span><span class="sxs-lookup"><span data-stu-id="e52cc-154">Each row is then queried for the "description" attribute.</span></span> <span data-ttu-id="e52cc-155">Si l’attribut est trouvé, il est affiché.</span><span class="sxs-lookup"><span data-stu-id="e52cc-155">If the attribute is found, it is displayed.</span></span>


```C++
LPWSTR pszColumn;
    while( pDSSearch->GetNextRow( hSearch) != S_ADS_NOMORE_ROWS )
    {
        // Get the property.
        hr = pDSSearch->GetColumn( hSearch, L"description", &col );
 
        // If this object supports this attribute, display it.
        if ( SUCCEEDED(hr) )
        { 
           if (col.dwADsType == ADSTYPE_CASE_IGNORE_STRING)
              wprintf(L"The description property:%s\r\n", col.pADsValues->CaseIgnoreString); 
           pDSSearch->FreeColumn( &col );
        }
        else
            puts("description property NOT available");
        puts("------------------------------------------------");
        dwCount++;
    }
    pDSSearch->CloseSearchHandle(hSearch);
    pDSSearch->Release();
```



<span data-ttu-id="e52cc-156">Pour mettre fin à la recherche, appelez la méthode [**AbandonSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-abandonsearch) .</span><span class="sxs-lookup"><span data-stu-id="e52cc-156">To end the search, call the [**AbandonSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-abandonsearch) method.</span></span>

<span data-ttu-id="e52cc-157">Sachez que si une taille de page n’est pas définie, la valeur de [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) se bloque jusqu’à ce que le jeu de résultats entier soit renvoyé au client.</span><span class="sxs-lookup"><span data-stu-id="e52cc-157">Be aware that if a page size is not set, [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) blocks until the entire result set is returned to the client.</span></span> <span data-ttu-id="e52cc-158">Si la taille de la page est définie, la valeur de **GetNextRow** se bloque jusqu’à ce que la première page (taille de page = nombre de lignes dans une page) soit retournée.</span><span class="sxs-lookup"><span data-stu-id="e52cc-158">If page size is set, then **GetNextRow** blocks until the first page (page size = number of rows in a page) is returned.</span></span> <span data-ttu-id="e52cc-159">Si la taille de la page est définie et que la requête doit être triée et que vous n’effectuez pas de recherche sur au moins un attribut indexé, la valeur taille de la page est ignorée et le serveur calcule le jeu de résultats entier avant de retourner les données.</span><span class="sxs-lookup"><span data-stu-id="e52cc-159">If page size is set and the query is to be sorted and you are not searching on at least one indexed attribute, then the page size value is ignored, and the server calculates the entire result set prior to returning the data.</span></span> <span data-ttu-id="e52cc-160">Cela a pour effet de bloquer la **GetNextRow** jusqu’à la fin de la requête.</span><span class="sxs-lookup"><span data-stu-id="e52cc-160">This has the effect of **GetNextRow** blocking until the query completes.</span></span>

> [!Note]  
> <span data-ttu-id="e52cc-161">Pour modifier cette requête d’une recherche de répertoire à une recherche de catalogue global, l’appel [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) est modifié.</span><span class="sxs-lookup"><span data-stu-id="e52cc-161">To change this query from a directory search to a global catalog search, the [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) call is changed.</span></span>

 


```C++
// Open a connection with the server.
hr = ADsOpenObject(L"GC://coho.salmon.Fabrikam.com", 
szUsername, 
szPassword, 
ADS_SECURE_AUTHENTICATION,
IID_IDirectorySearch,
(void **)&pDSSearch);
```



 

 