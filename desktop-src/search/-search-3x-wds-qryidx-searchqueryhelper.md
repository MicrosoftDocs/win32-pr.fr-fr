---
description: 'Vous pouvez utiliser l’interface ISearchQueryHelper pour interroger l’index. Cette interface est implémentée en tant que classe d’assistance pour ISearchCatalogManager (et ISearchCatalogManager2), et est obtenue en appelant ISearchCatalogManager :: GetQueryHelper.'
ms.assetid: 6e567c09-8763-4866-bf02-ad6651b454db
title: Interrogation de l’index avec ISearchQueryHelper
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56b9d970a1e3f416081d3b7fd3e9d6c2af0a2bca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201301"
---
# <a name="querying-the-index-with-isearchqueryhelper"></a><span data-ttu-id="2c265-104">Interrogation de l’index avec ISearchQueryHelper</span><span class="sxs-lookup"><span data-stu-id="2c265-104">Querying the Index with ISearchQueryHelper</span></span>

<span data-ttu-id="2c265-105">Vous pouvez utiliser l’interface [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) pour interroger l’index.</span><span class="sxs-lookup"><span data-stu-id="2c265-105">You can use the [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) interface to query the index.</span></span> <span data-ttu-id="2c265-106">Cette interface est implémentée en tant que classe d’assistance pour [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) (et [**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)), et est obtenue en appelant [**ISearchCatalogManager :: GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper).</span><span class="sxs-lookup"><span data-stu-id="2c265-106">This interface is implemented as a helper class to [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) (and [**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)), and is obtained by calling [**ISearchCatalogManager::GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper).</span></span> <span data-ttu-id="2c265-107">Cette interface vous permet d’effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="2c265-107">This interface permits you to:</span></span>

-   <span data-ttu-id="2c265-108">Obtenez une chaîne de connexion OLE DB pour vous connecter à la base de données de recherche Windows.</span><span class="sxs-lookup"><span data-stu-id="2c265-108">Obtain an OLE DB connection string to connect to the Windows Search database.</span></span>
-   <span data-ttu-id="2c265-109">Convertit les requêtes utilisateur de la syntaxe de requête avancée (AQS) en langage SQL de recherche Windows (SQL).</span><span class="sxs-lookup"><span data-stu-id="2c265-109">Convert Advanced Query Syntax (AQS) user queries to Windows Search Structured Query Language (SQL).</span></span>
-   <span data-ttu-id="2c265-110">Spécifiez les restrictions de requête qui peuvent être exprimées en SQL, mais pas dans AQS.</span><span class="sxs-lookup"><span data-stu-id="2c265-110">Specify query restrictions that can be expressed in SQL, but not in AQS.</span></span>

<span data-ttu-id="2c265-111">Cette rubrique est organisée comme suit :</span><span class="sxs-lookup"><span data-stu-id="2c265-111">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="2c265-112">Prise en main avec ISearchQueryHelper</span><span class="sxs-lookup"><span data-stu-id="2c265-112">Getting Started with ISearchQueryHelper</span></span>](#getting-started-with-isearchqueryhelper)
-   [<span data-ttu-id="2c265-113">Utilisation de la méthode GenerateSqlFromUserQuery</span><span class="sxs-lookup"><span data-stu-id="2c265-113">Using the GenerateSqlFromUserQuery Method</span></span>](#using-the-generatesqlfromuserquery-method)
-   [<span data-ttu-id="2c265-114">Utilisation des identificateurs de paramètres régionaux</span><span class="sxs-lookup"><span data-stu-id="2c265-114">Working with Locale Identifiers</span></span>](#working-with-locale-identifiers)
-   [<span data-ttu-id="2c265-115">Utilisation des propriétés et des colonnes</span><span class="sxs-lookup"><span data-stu-id="2c265-115">Working with Properties and Columns</span></span>](#working-with-properties-and-columns)
-   [<span data-ttu-id="2c265-116">Utilisation de l’expansion de terme de requête</span><span class="sxs-lookup"><span data-stu-id="2c265-116">Working with Query Term Expansion</span></span>](#working-with-query-term-expansion)
-   [<span data-ttu-id="2c265-117">Utilisation d’autres méthodes ISearchQueryHelper</span><span class="sxs-lookup"><span data-stu-id="2c265-117">Working with Other ISearchQueryHelper Methods</span></span>](#working-with-other-isearchqueryhelper-methods)
-   [<span data-ttu-id="2c265-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2c265-118">Related topics</span></span>](#related-topics)

## <a name="getting-started-with-isearchqueryhelper"></a><span data-ttu-id="2c265-119">Prise en main avec ISearchQueryHelper</span><span class="sxs-lookup"><span data-stu-id="2c265-119">Getting Started with ISearchQueryHelper</span></span>

<span data-ttu-id="2c265-120">Il existe quelques méthodes et interfaces clés que vous devez connaître avant de commencer à interroger par programmation la recherche Windows à l’aide de l’interface [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) .</span><span class="sxs-lookup"><span data-stu-id="2c265-120">There are a few key interfaces and methods you should be aware of before you can start programmatically querying Windows Search using the [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) interface.</span></span> <span data-ttu-id="2c265-121">À un niveau élevé, vous devez suivre les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="2c265-121">At a high level, you need to follow these steps:</span></span>

1.  <span data-ttu-id="2c265-122">Instanciez une instance [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) .</span><span class="sxs-lookup"><span data-stu-id="2c265-122">Instantiate an [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) instance.</span></span>
    ```
    // Create ISearchManager instance
    ISearchManager* pSearchManager;

    // Use library SearchSDK.lib for CLSID_CSearchManager.
    hr = CoCreateInstance(CLSID_CSearchManager, NULL, CLSCTX_LOCAL_SERVER, IID_PPV_ARGS(&pSearchManager));      
    ```

    

2.  <span data-ttu-id="2c265-123">Obtenez une instance de [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) à l’aide de [**ISearchManager :: getCatalog,**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog).</span><span class="sxs-lookup"><span data-stu-id="2c265-123">Obtain an instance of [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) using [**ISearchManager::GetCatalog**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog).</span></span> <span data-ttu-id="2c265-124">Le nom du catalogue système pour la recherche Windows est `SYSTEMINDEX` .</span><span class="sxs-lookup"><span data-stu-id="2c265-124">The name of the system catalog for Windows Search is `SYSTEMINDEX`.</span></span>
    ```
    // Create ISearchCatalogManager instance 
    ISearchCatalogManager* pSearchCatalogManager;

    // Call ISearchManager::GetCatalog for "SystemIndex" to access the catalog to the ISearchCatalogManager
    hr = pSearchManager->GetCatalog(L"SystemIndex", &pSearchCatalogManager);
            
    ```

    

3.  <span data-ttu-id="2c265-125">Obtenez une instance de [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) à l’aide de [**ISearchCatalogManager :: GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper).</span><span class="sxs-lookup"><span data-stu-id="2c265-125">Obtain an instance of [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) using [**ISearchCatalogManager::GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper).</span></span>
    ```
    // Call ISearchCatalogManager::GetQueryHelper to get the ISearchQueryHelper interface
    ISearchQueryHelper* pQueryHelper;

    hr = pSearchCatalogManager->GetQueryHelper(&pQueryHelper);
            
    ```

    

4.  <span data-ttu-id="2c265-126">Une fois que vous disposez d’une instance de [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper), vous pouvez obtenir la chaîne de connexion utilisée pour se connecter à l’index de recherche Windows OLE DB connecteur.</span><span class="sxs-lookup"><span data-stu-id="2c265-126">After you have an instance of [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper), you can then get the connection string used to connect to the Windows Search index OLE DB connector.</span></span>
    ```
    // Call get_ConnectionString to get the OLE DB connection string
    LPWSTR pszConnectionString=NULL;

    hr = pQueryHelper->get_ConnectionString(&pszConnectionString);
    // NOTE: YOU MUST call CoTaskMemFree() on the string
        
    ```

    

## <a name="using-the-generatesqlfromuserquery-method"></a><span data-ttu-id="2c265-127">Utilisation de la méthode GenerateSqlFromUserQuery</span><span class="sxs-lookup"><span data-stu-id="2c265-127">Using the GenerateSqlFromUserQuery Method</span></span>

<span data-ttu-id="2c265-128">La méthode [**ISearchQueryHelper :: GenerateSQLFromUserQuery**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-generatesqlfromuserquery) transforme l’entrée d’utilisateur en une chaîne de requête SQL, qui peut ensuite être envoyée au fournisseur OLE DB pour la recherche Windows.</span><span class="sxs-lookup"><span data-stu-id="2c265-128">The [**ISearchQueryHelper::GenerateSQLFromUserQuery**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-generatesqlfromuserquery) method transforms user input into a SQL query string, which can then be submitted to the OLE DB provider for Windows Search.</span></span> <span data-ttu-id="2c265-129">Cette méthode traduit la requête de [syntaxe de requête avancée](-search-3x-advancedquerysyntax.md) (AQS) ou la syntaxe de requête naturelle (NQS) entrée par l’utilisateur en SQL, et vous permet d’ajouter d’autres fragments SQL en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="2c265-129">This method translates the [Advanced Query Syntax](-search-3x-advancedquerysyntax.md) (AQS) or Natural Query Syntax (NQS) query entered by the user into SQL, and lets you add other SQL fragments as needed.</span></span>

<span data-ttu-id="2c265-130">La chaîne de requête SQL est retournée sous la forme suivante :</span><span class="sxs-lookup"><span data-stu-id="2c265-130">The SQL query string is returned in the following form:</span></span>


```
SELECT <QuerySelectColumns> 
FROM <CatalogName that created query helper>
WHERE <Result of interpreting the user query passed into this function according to QuerySyntax>
      [ AND|OR <QueryWhereRestrictions> ]
    
```



<span data-ttu-id="2c265-131">Voici un exemple de la chaîne SQL retournée par l’appel `GenerateSQLFromUserQuery("comput")` :</span><span class="sxs-lookup"><span data-stu-id="2c265-131">The following is an example of the SQL string returned from the call `GenerateSQLFromUserQuery("comput")`:</span></span>


```
SELECT "System.ItemUrl" 
FROM "SystemIndex" 
WHERE ((CONTAINS(*,'"comput*"',1033) RANK BY COERCION(Absolute, 1)) OR 
       (FREETEXT(("System.ItemNameDisplay":0.9, *:0.1), 'comput', 1033) AND CONTAINS(*,'"comput"',1033)))
ORDER BY "System.ItemUrl"
```



> [!Note]  
> <span data-ttu-id="2c265-132">La méthode génère les prédicats FREETEXT et CONTAINs, car CONTAINs seul ne génère pas de classement significatif.</span><span class="sxs-lookup"><span data-stu-id="2c265-132">The method generates both the FREETEXT and the CONTAINS predicates because CONTAINS alone does not generate meaningful ranking.</span></span>

 

## <a name="working-with-locale-identifiers"></a><span data-ttu-id="2c265-133">Utilisation des identificateurs de paramètres régionaux</span><span class="sxs-lookup"><span data-stu-id="2c265-133">Working with Locale Identifiers</span></span>



| <span data-ttu-id="2c265-134">Méthode</span><span class="sxs-lookup"><span data-stu-id="2c265-134">Method</span></span>                                                                                                                                                                                                                                   | <span data-ttu-id="2c265-135">Description</span><span class="sxs-lookup"><span data-stu-id="2c265-135">Description</span></span>                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c265-136">[**ISearchQueryHelper :: obtient \_ QueryContentLocale**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querycontentlocale)/</span><span class="sxs-lookup"><span data-stu-id="2c265-136">[**ISearchQueryHelper::get\_QueryContentLocale**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querycontentlocale)/</span></span><br/> [<span data-ttu-id="2c265-137">**ISearchQueryHelper ::p ut \_ QueryContentLocale**</span><span class="sxs-lookup"><span data-stu-id="2c265-137">**ISearchQueryHelper::put\_QueryContentLocale**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querycontentlocale)<br/> | <span data-ttu-id="2c265-138">Obtient/place l’identificateur LCID (Language code identifier) de la requête.</span><span class="sxs-lookup"><span data-stu-id="2c265-138">Gets/Puts the language code identifier (LCID) of the query.</span></span> <span data-ttu-id="2c265-139">Cela permet d’obtenir le séparateur de mots et le biais corrects pour comparer les termes de requête à l’index catalogue/inversé.</span><span class="sxs-lookup"><span data-stu-id="2c265-139">This helps get the correct wordbreaker and stemmer to compare query terms against the catalog/inverted index.</span></span> <span data-ttu-id="2c265-140">La valeur par défaut est le paramètre régional d’entrée actuel.</span><span class="sxs-lookup"><span data-stu-id="2c265-140">The default is the current input locale.</span></span> |
| <span data-ttu-id="2c265-141">[**ISearchQueryHelper :: obtient \_ QueryKeywordLocale**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querykeywordlocale)/</span><span class="sxs-lookup"><span data-stu-id="2c265-141">[**ISearchQueryHelper::get\_QueryKeywordLocale**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querykeywordlocale)/</span></span><br/> [<span data-ttu-id="2c265-142">**ISearchQueryHelper ::p ut \_ QueryKeywordLocale**</span><span class="sxs-lookup"><span data-stu-id="2c265-142">**ISearchQueryHelper::put\_QueryKeywordLocale**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querykeywordlocale)<br/> | <span data-ttu-id="2c265-143">Obtient/place le LCID de la langue à utiliser lors de l’analyse des mots clés de la syntaxe de requête avancée (AQS).</span><span class="sxs-lookup"><span data-stu-id="2c265-143">Gets/Puts the LCID for the language to use when parsing Advanced Query Syntax (AQS) keywords.</span></span> <span data-ttu-id="2c265-144">La valeur par défaut est la valeur par défaut des paramètres régionaux utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2c265-144">The default is the default user locale.</span></span>                                                                              |



 

<span data-ttu-id="2c265-145">Les paramètres régionaux de **contenu** et les **Mots clés régionaux** sont des identificateurs de paramètres régionaux (LCID) qui aident le moteur de recherche à utiliser les analyseurs lexicaux appropriés en identifiant la langue des termes de la requête et la langue des mots clés AQS.</span><span class="sxs-lookup"><span data-stu-id="2c265-145">The **content locale** and **keyword locale** are locale identifiers (LCID) that help the search engine use the correct word breakers by identifying the language of the query terms and the language the AQS keywords.</span></span> <span data-ttu-id="2c265-146">Ce ne sont pas toujours les mêmes LCID, car Windows Search est proposé dans plusieurs versions internationales et comprend des packs MUI (Multilingual User Interface) pour d’autres langues.</span><span class="sxs-lookup"><span data-stu-id="2c265-146">These are not always the same LCIDs because Windows Search is offered in a number of international versions and also includes Multilingual User Interface (MUI) packs for more languages.</span></span> <span data-ttu-id="2c265-147">Les paramètres régionaux de contenu identifient le LCID pour les utilisateurs de langue qui saisissent leur requête de recherche dans, tandis que le mot clé local identifie le LCID utilisé par le moteur de recherche lors de l’analyse des mots clés de la syntaxe de requête avancée (AQS).</span><span class="sxs-lookup"><span data-stu-id="2c265-147">The content locale identifies the LCID for the language users input their search query in, while the keyword locale identifies the LCID the search engine uses when parsing Advanced Query Syntax (AQS) keywords.</span></span>

<span data-ttu-id="2c265-148">Par exemple, si vous disposez de la version anglaise (États-Unis) sans packs MUI, les paramètres régionaux de contenu et les paramètres régionaux de mot clé sont 1033.</span><span class="sxs-lookup"><span data-stu-id="2c265-148">For example, if you have the English-US version with no MUI packs, both the content locale and keyword locale are 1033.</span></span> <span data-ttu-id="2c265-149">Si vous disposez de la version allemande sans packs MUI, les paramètres régionaux de contenu et les paramètres régionaux de mot-clé sont 1031 (GR-gr).</span><span class="sxs-lookup"><span data-stu-id="2c265-149">If you have the German version with no MUI packs, then both the content locale and keyword locale are 1031 (gr-gr).</span></span> <span data-ttu-id="2c265-150">Toutefois, si vous disposez de la version anglaise avec le Pack MUI roumain, les paramètres régionaux de contenu sont 2072 (RO) et les mots clés régionaux sont 1033 (en-US).</span><span class="sxs-lookup"><span data-stu-id="2c265-150">However, if you have the English version with the Romanian MUI pack, the content locale is 2072 (ro) and the keyword locale is 1033 (en-us).</span></span>

## <a name="working-with-properties-and-columns"></a><span data-ttu-id="2c265-151">Utilisation des propriétés et des colonnes</span><span class="sxs-lookup"><span data-stu-id="2c265-151">Working with Properties and Columns</span></span>



| <span data-ttu-id="2c265-152">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2c265-152">Methods</span></span>                                                                                                                                                                                                                                                  | <span data-ttu-id="2c265-153">Description</span><span class="sxs-lookup"><span data-stu-id="2c265-153">Description</span></span>                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c265-154">[**ISearchQueryHelper :: obtient \_ QueryContentProperties**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querycontentproperties)/</span><span class="sxs-lookup"><span data-stu-id="2c265-154">[**ISearchQueryHelper::get\_QueryContentProperties**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querycontentproperties)/</span></span><br/> [<span data-ttu-id="2c265-155">**ISearchQueryHelper ::p ut \_ QueryContentProperties**</span><span class="sxs-lookup"><span data-stu-id="2c265-155">**ISearchQueryHelper::put\_QueryContentProperties**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querycontentproperties)<br/> | <span data-ttu-id="2c265-156">Obtient/définit les propriétés de contenu pour la recherche (colonne de propriété figurant dans les clauses CONTAINs ou FREETEXT).</span><span class="sxs-lookup"><span data-stu-id="2c265-156">Gets/Sets the content properties for the search (property column listed in the CONTAINS or FREETEXT clauses).</span></span>                                   |
| <span data-ttu-id="2c265-157">[**ISearchQueryHelper :: obtient \_ QuerySelectColumns**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_queryselectcolumns)/</span><span class="sxs-lookup"><span data-stu-id="2c265-157">[**ISearchQueryHelper::get\_QuerySelectColumns**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_queryselectcolumns)/</span></span><br/> [<span data-ttu-id="2c265-158">**ISearchQueryHelper ::p ut \_ QuerySelectColumns**</span><span class="sxs-lookup"><span data-stu-id="2c265-158">**ISearchQueryHelper::put\_QuerySelectColumns**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_queryselectcolumns)<br/>                 | <span data-ttu-id="2c265-159">Obtient/définit les colonnes (ou propriétés) demandées dans l’instruction SELECT.</span><span class="sxs-lookup"><span data-stu-id="2c265-159">Gets/Sets the columns (or properties) requested in the SELECT statement.</span></span> <span data-ttu-id="2c265-160">La valeur par défaut est System. ItemUrl et les propriétés utilisées dans la clause WHERE.</span><span class="sxs-lookup"><span data-stu-id="2c265-160">The default is System.ItemUrl and properties used in the WHERE clause.</span></span> |



 

<span data-ttu-id="2c265-161">Les éléments sont représentés dans le magasin de propriétés sous la forme d’une ligne.</span><span class="sxs-lookup"><span data-stu-id="2c265-161">Items are represented in the property store as a row.</span></span> <span data-ttu-id="2c265-162">Chaque ligne contient plusieurs colonnes qui représentent les propriétés de cet élément.</span><span class="sxs-lookup"><span data-stu-id="2c265-162">Each row contains a number of columns that represent properties for that item.</span></span> <span data-ttu-id="2c265-163">Tous les éléments n’ont pas de valeur pour une propriété donnée.</span><span class="sxs-lookup"><span data-stu-id="2c265-163">Not all items will have a value for a given property.</span></span> <span data-ttu-id="2c265-164">Par exemple, un fichier audio ne contient généralement pas de valeur pour la propriété System. Property. FromName, mais il peut contenir des informations relatives à System. Music. Artist.</span><span class="sxs-lookup"><span data-stu-id="2c265-164">For example, an audio file would typically not contain a value for the System.Property.FromName property but may contain information regarding the System.Music.Artist.</span></span>

<span data-ttu-id="2c265-165">Avec ces méthodes, vous accédez ou modifiez la propriété avec une chaîne Unicode délimitée par des virgules, se terminant par un caractère null, qui spécifie un ou plusieurs noms de colonnes de la Banque de propriétés : «System.Document. Auteur, System.Document. Titre».</span><span class="sxs-lookup"><span data-stu-id="2c265-165">With these methods, you access or modify the property with a comma delimited, null-terminated, Unicode string that specifies one or more column names of the property store: "System.Document.Author, System.Document.Title".</span></span>

## <a name="working-with-query-term-expansion"></a><span data-ttu-id="2c265-166">Utilisation de l’expansion de terme de requête</span><span class="sxs-lookup"><span data-stu-id="2c265-166">Working with Query Term Expansion</span></span>



| <span data-ttu-id="2c265-167">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2c265-167">Methods</span></span>                                                                                                                                                                                                                                 | <span data-ttu-id="2c265-168">Description</span><span class="sxs-lookup"><span data-stu-id="2c265-168">Description</span></span>                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="2c265-169">**ISearchQueryHelper :: obtient \_ QueryTermExpansion**</span><span class="sxs-lookup"><span data-stu-id="2c265-169">**ISearchQueryHelper::get\_QueryTermExpansion**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querytermexpansion)<br/> [<span data-ttu-id="2c265-170">**ISearchQueryHelper ::p ut \_ QueryTermExpansion**</span><span class="sxs-lookup"><span data-stu-id="2c265-170">**ISearchQueryHelper::put\_QueryTermExpansion**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querytermexpansion)<br/> | <span data-ttu-id="2c265-171">Obtient/définit l’indicateur de développement de terme de recherche.</span><span class="sxs-lookup"><span data-stu-id="2c265-171">Gets/Sets the search term expansion flag.</span></span> |



 

<span data-ttu-id="2c265-172">Cette méthode permet d’étendre certains termes de requête avec des caractères génériques, similaires à l’expansion d’expressions régulières.</span><span class="sxs-lookup"><span data-stu-id="2c265-172">This method enables the expansion of some query terms with wild card characters, similar to regular expression expansion.</span></span> <span data-ttu-id="2c265-173">L’expansion de préfixe recherche des mots avec le même préfixe (fun/entonnoir).</span><span class="sxs-lookup"><span data-stu-id="2c265-173">Prefix expansion searches for words with the same prefix (fun/funnel).</span></span> <span data-ttu-id="2c265-174">Si la valeur n’est pas définie, la valeur par défaut est le \_ préfixe de terme de recherche \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="2c265-174">If not set, the default value is SEARCH\_TERM\_PREFIX\_ALL.</span></span> <span data-ttu-id="2c265-175">Les valeurs prises en charge pour l’énumération de l' [**\_ \_ expansion des termes recherchés**](/windows/desktop/api/Searchapi/ne-searchapi-search_term_expansion) sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="2c265-175">The supported values of the [**SEARCH\_TERM\_EXPANSION**](/windows/desktop/api/Searchapi/ne-searchapi-search_term_expansion) enumeration are as follows:</span></span>

-   <span data-ttu-id="2c265-176">Rechercher \_ \_ le préfixe du terme \_ tous-tous les termes de recherche sont développés</span><span class="sxs-lookup"><span data-stu-id="2c265-176">SEARCH\_TERM\_PREFIX\_ALL - All search terms are expanded</span></span>
-   <span data-ttu-id="2c265-177">\_Terme \_ de recherche sans \_ expansion-aucun terme de recherche n’est développé</span><span class="sxs-lookup"><span data-stu-id="2c265-177">SEARCH\_TERM\_NO\_EXPANSION - No search terms are expanded</span></span>

## <a name="working-with-other-isearchqueryhelper-methods"></a><span data-ttu-id="2c265-178">Utilisation d’autres méthodes ISearchQueryHelper</span><span class="sxs-lookup"><span data-stu-id="2c265-178">Working with Other ISearchQueryHelper Methods</span></span>

<span data-ttu-id="2c265-179">La plupart des méthodes de l’interface [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) sont utilisées pour définir des arguments de requête ou définir les propriétés retournées.</span><span class="sxs-lookup"><span data-stu-id="2c265-179">Many of the methods in the [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) interface are used to set query arguments or define the properties returned.</span></span>



| <span data-ttu-id="2c265-180">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2c265-180">Methods</span></span>                                                                                                                                                                                                                                                 | <span data-ttu-id="2c265-181">Description</span><span class="sxs-lookup"><span data-stu-id="2c265-181">Description</span></span>                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2c265-182">**ISearchQueryHelper :: obtient \_ ConnectionString**</span><span class="sxs-lookup"><span data-stu-id="2c265-182">**ISearchQueryHelper::get\_ConnectionString**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_connectionstring)<br/>                                                                                                                                         | <span data-ttu-id="2c265-183">Retourne la chaîne de connexion OLE DB.</span><span class="sxs-lookup"><span data-stu-id="2c265-183">Returns the OLE DB connection string.</span></span> <span data-ttu-id="2c265-184">Il s’agit de la méthode recommandée pour obtenir une chaîne de connexion correctement mise en forme et correcte.</span><span class="sxs-lookup"><span data-stu-id="2c265-184">This is the preferred method of getting a properly formatted and correct connection string.</span></span>                                  |
| [<span data-ttu-id="2c265-185">**ISearchQueryHelper :: obtient \_ QueryMaxResults**</span><span class="sxs-lookup"><span data-stu-id="2c265-185">**ISearchQueryHelper::get\_QueryMaxResults**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querymaxresults)<br/> [<span data-ttu-id="2c265-186">**ISearchQueryHelper ::p ut \_ QueryMaxResults**</span><span class="sxs-lookup"><span data-stu-id="2c265-186">**ISearchQueryHelper::put\_QueryMaxResults**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querymaxresults)<br/>                             | <span data-ttu-id="2c265-187">Obtient/définit le nombre maximal de résultats qui doivent être retournés par une requête (autrement dit, sélectionnez TOP n).</span><span class="sxs-lookup"><span data-stu-id="2c265-187">Gets/Sets the maximum number of results to be returned by a query (that is, SELECT TOP n).</span></span> <span data-ttu-id="2c265-188">La valeur par défaut est-1, ce qui signifie qu’aucune clause de résultats maximale n’est générée.</span><span class="sxs-lookup"><span data-stu-id="2c265-188">The default is -1, meaning that no maximum results clause is generated.</span></span> |
| [<span data-ttu-id="2c265-189">**ISearchQueryHelper :: obtient \_ QuerySorting**</span><span class="sxs-lookup"><span data-stu-id="2c265-189">**ISearchQueryHelper::get\_QuerySorting**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querysorting)<br/> [<span data-ttu-id="2c265-190">**ISearchQueryHelper ::p ut \_ QuerySorting**</span><span class="sxs-lookup"><span data-stu-id="2c265-190">**ISearchQueryHelper::put\_QuerySorting**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querysorting)<br/>                                         | <span data-ttu-id="2c265-191">Obtient/définit l’ordre de tri du jeu de résultats de la requête (ORDER BY).</span><span class="sxs-lookup"><span data-stu-id="2c265-191">Gets/Sets the sort order for the query result set (ORDER BY).</span></span> <span data-ttu-id="2c265-192">S’il n’existe aucune clause ORDER BY, les résultats sont retournés dans un ordre non déterministe.</span><span class="sxs-lookup"><span data-stu-id="2c265-192">If no ORDER BY clause exists, the results are returned in non-deterministic order.</span></span>                   |
| [<span data-ttu-id="2c265-193">**ISearchQueryHelper :: obtient \_ QuerySyntax**</span><span class="sxs-lookup"><span data-stu-id="2c265-193">**ISearchQueryHelper::get\_QuerySyntax**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querysyntax)<br/> [<span data-ttu-id="2c265-194">**ISearchQueryHelper ::p ut \_ QuerySyntax**</span><span class="sxs-lookup"><span data-stu-id="2c265-194">**ISearchQueryHelper::put\_QuerySyntax**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querysyntax)<br/>                                             | <span data-ttu-id="2c265-195">Obtient/définit la syntaxe de la requête : la syntaxe de requête avancée ou la syntaxe de requête naturelle.</span><span class="sxs-lookup"><span data-stu-id="2c265-195">Gets/Sets the syntax of the query: Advanced Query Syntax or Natural Query Syntax.</span></span>                                                                                  |
| [<span data-ttu-id="2c265-196">**ISearchQueryHelper :: obtient \_ QueryWhereRestrictions**</span><span class="sxs-lookup"><span data-stu-id="2c265-196">**ISearchQueryHelper::get\_QueryWhereRestrictions**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querywhererestrictions)<br/> [<span data-ttu-id="2c265-197">**ISearchQueryHelper ::p ut \_ QueryWhereRestrictions**</span><span class="sxs-lookup"><span data-stu-id="2c265-197">**ISearchQueryHelper::put\_QueryWhereRestrictions**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querywhererestrictions)<br/> | <span data-ttu-id="2c265-198">Obtient/définit les restrictions ajoutées à l’aide des clauses WHERE.</span><span class="sxs-lookup"><span data-stu-id="2c265-198">Gets/Sets the restrictions appended via WHERE clauses.</span></span>                                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="2c265-199">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2c265-199">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c265-200">Interrogation de l’index programmatiquement</span><span class="sxs-lookup"><span data-stu-id="2c265-200">Querying the Index Programmatically</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="2c265-201">Utilisation des approches SQL et AQS pour interroger l’index</span><span class="sxs-lookup"><span data-stu-id="2c265-201">Using SQL and AQS Approaches to Query the Index</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="2c265-202">Interrogation de l’index avec le protocole search-ms</span><span class="sxs-lookup"><span data-stu-id="2c265-202">Querying the Index with the search-ms Protocol</span></span>](-search-3x-wds-qryidx-searchms.md)
</dt> <dt>

[<span data-ttu-id="2c265-203">Interrogation de l’index avec la syntaxe SQL de Windows Search</span><span class="sxs-lookup"><span data-stu-id="2c265-203">Querying the Index with Windows Search SQL Syntax</span></span>](-search-sql-windowssearch-entry.md)
</dt> <dt>

[<span data-ttu-id="2c265-204">Utilisation de la syntaxe de requête avancée par programmation</span><span class="sxs-lookup"><span data-stu-id="2c265-204">Using Advanced Query Syntax Programmatically</span></span>](-search-3x-advancedquerysyntax.md)
</dt> </dl>

 

 




