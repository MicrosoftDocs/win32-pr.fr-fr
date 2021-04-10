---
description: Décrit comment créer un fichier de description OpenSearch (. fichier osdx) pour connecter des magasins de données externes au client Windows via le protocole OpenSearch.
ms.assetid: 62cd88cd-e6ff-4e46-887d-e62f7018c065
title: Création d’un fichier de description OpenSearch dans Windows Federated Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 406b166d6963517d692ef9de8292190d7eb92102
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951032"
---
# <a name="creating-an-opensearch-description-file-in-windows-federated-search"></a><span data-ttu-id="aea24-103">Création d’un fichier de description OpenSearch dans Windows Federated Search</span><span class="sxs-lookup"><span data-stu-id="aea24-103">Creating an OpenSearch Description File in Windows Federated Search</span></span>

<span data-ttu-id="aea24-104">Décrit comment créer un fichier de description OpenSearch (. fichier osdx) pour connecter des magasins de données externes au client Windows via le protocole [OpenSearch](https://github.com/dewitt/opensearch) .</span><span class="sxs-lookup"><span data-stu-id="aea24-104">Describes how to create an OpenSearch Description (.osdx) file to connect external data stores to the Windows Client via the [OpenSearch](https://github.com/dewitt/opensearch) protocol.</span></span> <span data-ttu-id="aea24-105">La recherche fédérée permet aux utilisateurs de rechercher dans un magasin de données distant et d’afficher les résultats à partir de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="aea24-105">Federated search enables users to search a remote data store and view the results from within Windows Explorer.</span></span>

<span data-ttu-id="aea24-106">Cette rubrique contient les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="aea24-106">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="aea24-107">Fichier de description OpenSearch</span><span class="sxs-lookup"><span data-stu-id="aea24-107">OpenSearch Description File</span></span>](#opensearch-description-file)
    -   [<span data-ttu-id="aea24-108">Minimale les éléments enfants requis</span><span class="sxs-lookup"><span data-stu-id="aea24-108">Mininum Required Child Elements</span></span>](#mininum-required-child-elements)
-   [<span data-ttu-id="aea24-109">Éléments standard dans Windows Federated Search</span><span class="sxs-lookup"><span data-stu-id="aea24-109">Standard Elements in Windows Federated Search</span></span>](#standard-elements-in-windows-federated-search)
    -   [<span data-ttu-id="aea24-110">Nom court</span><span class="sxs-lookup"><span data-stu-id="aea24-110">Shortname</span></span>](#shortname)
    -   [<span data-ttu-id="aea24-111">Description</span><span class="sxs-lookup"><span data-stu-id="aea24-111">Description</span></span>](#description)
    -   [<span data-ttu-id="aea24-112">Modèle d’URL pour les résultats RSS/Atom</span><span class="sxs-lookup"><span data-stu-id="aea24-112">URL Template for RSS/Atom Results</span></span>](#url-template-for-rssatom-results)
    -   [<span data-ttu-id="aea24-113">Modèle d’URL pour les résultats Web</span><span class="sxs-lookup"><span data-stu-id="aea24-113">URL Template for web Results</span></span>](#url-template-for-web-results)
    -   [<span data-ttu-id="aea24-114">Paramètres de modèle d’URL</span><span class="sxs-lookup"><span data-stu-id="aea24-114">URL Template Parameters</span></span>](#url-template-parameters)
    -   [<span data-ttu-id="aea24-115">Résultats paginés</span><span class="sxs-lookup"><span data-stu-id="aea24-115">Paged Results</span></span>](#paged-results)
    -   [<span data-ttu-id="aea24-116">Pagination à l’aide de l’index de l’élément</span><span class="sxs-lookup"><span data-stu-id="aea24-116">Paging Using the Item Index</span></span>](#paging-using-the-item-index)
    -   [<span data-ttu-id="aea24-117">Pagination à l’aide de l’index de page</span><span class="sxs-lookup"><span data-stu-id="aea24-117">Paging Using the Page Index</span></span>](#paging-using-the-page-index)
    -   [<span data-ttu-id="aea24-118">Taille de la page</span><span class="sxs-lookup"><span data-stu-id="aea24-118">Page Size</span></span>](#page-size)
-   [<span data-ttu-id="aea24-119">Éléments étendus dans la recherche fédérée Windows</span><span class="sxs-lookup"><span data-stu-id="aea24-119">Extended Elements in Windows Federated Search</span></span>](#extended-elements-in-windows-federated-search)
    -   [<span data-ttu-id="aea24-120">Nombre maximal de résultats</span><span class="sxs-lookup"><span data-stu-id="aea24-120">Maximum Result Count</span></span>](#maximum-result-count)
    -   [<span data-ttu-id="aea24-121">Mappage de propriétés</span><span class="sxs-lookup"><span data-stu-id="aea24-121">Property Mapping</span></span>](#property-mapping)
-   [<span data-ttu-id="aea24-122">Versions préliminaires</span><span class="sxs-lookup"><span data-stu-id="aea24-122">Previews</span></span>](#previews)
-   [<span data-ttu-id="aea24-123">Élément de menu ouvrir l’emplacement du fichier</span><span class="sxs-lookup"><span data-stu-id="aea24-123">Open File Location Menu Item</span></span>](#open-file-location-menu-item)
-   [<span data-ttu-id="aea24-124">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="aea24-124">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="aea24-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="aea24-125">Related topics</span></span>](#related-topics)

## <a name="opensearch-description-file"></a><span data-ttu-id="aea24-126">Fichier de description OpenSearch</span><span class="sxs-lookup"><span data-stu-id="aea24-126">OpenSearch Description File</span></span>

<span data-ttu-id="aea24-127">Un fichier de description OpenSearch (. fichier osdx) pour Windows Federated Search doit respecter les règles suivantes :</span><span class="sxs-lookup"><span data-stu-id="aea24-127">An OpenSearch Description (.osdx) file for Windows Federated Search must abide by the following rules:</span></span>

-   <span data-ttu-id="aea24-128">Être un document de description OpenSearch valide, tel que défini par la spécification [opensearch](https://github.com/dewitt/opensearch) 1,1.</span><span class="sxs-lookup"><span data-stu-id="aea24-128">Be a valid OpenSearch Description document, as defined by the [OpenSearch](https://github.com/dewitt/opensearch) 1.1 specification.</span></span>
-   <span data-ttu-id="aea24-129">Fournissez un modèle d’URL avec un type de format RSS ou Atom.</span><span class="sxs-lookup"><span data-stu-id="aea24-129">Provide a URL template with either an RSS or an Atom format type.</span></span>
-   <span data-ttu-id="aea24-130">Utilisez l’extension de nom de fichier. fichier osdx ou associez-la à l’extension de nom de fichier. fichier osdx lors du téléchargement à partir du Web.</span><span class="sxs-lookup"><span data-stu-id="aea24-130">Use the .osdx file name extension, or be associated with the .osdx file name extension when downloading from the web.</span></span> <span data-ttu-id="aea24-131">Par exemple, un serveur n’est pas obligé d’utiliser. fichier osdx.</span><span class="sxs-lookup"><span data-stu-id="aea24-131">For example, a server is not required to use .osdx.</span></span> <span data-ttu-id="aea24-132">Un serveur peut retourner le fichier avec n’importe quelle extension de nom de fichier, par exemple. xml, et traité comme s’il s’agissait d’un fichier. fichier osdx s’il utilise le type MIME correct pour les documents de description OpenSearch (fichiers. fichier osdx).</span><span class="sxs-lookup"><span data-stu-id="aea24-132">A server can return the file with any file name extension, such as .xml for example, and treated as if it were an .osdx file if it uses the correct MIME Type for OpenSearch Description documents (.osdx files).</span></span>
-   <span data-ttu-id="aea24-133">Fournissez une valeur de l’élément **ShortName** (recommandé).</span><span class="sxs-lookup"><span data-stu-id="aea24-133">Provide a **ShortName** element value (recommended).</span></span>

### <a name="mininum-required-child-elements"></a><span data-ttu-id="aea24-134">Minimale les éléments enfants requis</span><span class="sxs-lookup"><span data-stu-id="aea24-134">Mininum Required Child Elements</span></span>

<span data-ttu-id="aea24-135">L’exemple de fichier. fichier osdx suivant comprend les éléments **ShortName** et `Url` , qui sont les éléments enfants requis minimaux.</span><span class="sxs-lookup"><span data-stu-id="aea24-135">The following example .osdx file consists of **ShortName** and `Url` elements, which are the minimum required child elements.</span></span>


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    <ShortName>My web Service</ShortName>
    <Url format="application/rss+xml" 
        template="https://example.com/rss.php?query=
        {searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
</OpenSearchDescription>
```



## <a name="standard-elements-in-windows-federated-search"></a><span data-ttu-id="aea24-136">Éléments standard dans Windows Federated Search</span><span class="sxs-lookup"><span data-stu-id="aea24-136">Standard Elements in Windows Federated Search</span></span>

<span data-ttu-id="aea24-137">Outre les éléments enfants minimaux, la recherche fédérée prend en charge les éléments standard suivants.</span><span class="sxs-lookup"><span data-stu-id="aea24-137">In addition to the minimum child elements, federated search supports the following standard elements.</span></span>

### <a name="shortname"></a><span data-ttu-id="aea24-138">Nom court</span><span class="sxs-lookup"><span data-stu-id="aea24-138">Shortname</span></span>

<span data-ttu-id="aea24-139">Windows utilise la valeur de l’élément **ShortName** pour nommer le fichier. searchconnector-ms (connecteur de recherche) qui est créé lorsque l’utilisateur ouvre le fichier. fichier osdx.</span><span class="sxs-lookup"><span data-stu-id="aea24-139">Windows uses the **ShortName** element value to name the .searchconnector-ms (search connector) file that is created when the user opens the .osdx file.</span></span> <span data-ttu-id="aea24-140">Windows garantit que le nom de fichier généré utilise uniquement les caractères autorisés dans les noms de fichiers Windows.</span><span class="sxs-lookup"><span data-stu-id="aea24-140">Windows ensures that the generated file name uses only characters that are allowed in Windows file names.</span></span> <span data-ttu-id="aea24-141">Si aucune valeur **ShortName** n’est fournie, le fichier. searchconnector-MS essaie d’utiliser le nom de fichier du fichier. fichier osdx à la place.</span><span class="sxs-lookup"><span data-stu-id="aea24-141">If no **ShortName** value is provided, the .searchconnector-ms file tries to use the file name of the .osdx file instead.</span></span>

<span data-ttu-id="aea24-142">Le code suivant illustre l’utilisation de l’élément **ShortName** dans un fichier. fichier osdx.</span><span class="sxs-lookup"><span data-stu-id="aea24-142">The following code illustrates how to use the **ShortName** element in an .osdx file.</span></span>


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    <ShortName>My web Service</ShortName>
    ...
</OpenSearchDescription>
```



### <a name="description"></a><span data-ttu-id="aea24-143">Description</span><span class="sxs-lookup"><span data-stu-id="aea24-143">Description</span></span>

<span data-ttu-id="aea24-144">Windows utilise la valeur de l’élément **Description** pour renseigner la description du fichier affichée dans le volet Détails de l’Explorateur Windows lorsqu’un utilisateur sélectionne un fichier. searchconnector-ms.</span><span class="sxs-lookup"><span data-stu-id="aea24-144">Windows uses the **Description** element value to populate the file description shown in the Windows Explorer details pane when a user selects a .searchconnector-ms file.</span></span>


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    ...
    <Description>Searches the example company book catalog</Description>
</OpenSearchDescription>
```



### <a name="url-template-for-rssatom-results"></a><span data-ttu-id="aea24-145">Modèle d’URL pour les résultats RSS/Atom</span><span class="sxs-lookup"><span data-stu-id="aea24-145">URL Template for RSS/Atom Results</span></span>

<span data-ttu-id="aea24-146">Le fichier. fichier osdx doit inclure un élément de **format d’URL** et un attribut de **modèle** (un modèle d’URL) qui retourne les résultats au format RSS ou Atom.</span><span class="sxs-lookup"><span data-stu-id="aea24-146">The .osdx file must include one **Url format** element and **template** attribute (a URL template) that returns results in either RSS or Atom format.</span></span> <span data-ttu-id="aea24-147">L’attribut format doit avoir la valeur `application/rss+xml` pour les résultats au format RSS ou `application/atom+xml` pour les résultats au format Atom, comme indiqué dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="aea24-147">The format attribute must be set to `application/rss+xml` for RSS formatted results, or `application/atom+xml` for Atom formatted results, as shown in the following code.</span></span>

> [!Note]  
> <span data-ttu-id="aea24-148">L’élément de **format d’URL** et l’attribut de **modèle** sont communément appelés modèles d’URL.</span><span class="sxs-lookup"><span data-stu-id="aea24-148">The **Url format** element and **template** attribute are commonly known as a URL template.</span></span>

 


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
   ...
        <Url format="application/rss+xml" template="https://example.com/rss.php?query=
            {searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
</OpenSearchDescription>
```



### <a name="url-template-for-web-results"></a><span data-ttu-id="aea24-149">Modèle d’URL pour les résultats Web</span><span class="sxs-lookup"><span data-stu-id="aea24-149">URL Template for web Results</span></span>

<span data-ttu-id="aea24-150">Si une version des résultats de la recherche peut être affichée dans un navigateur Web, vous devez fournir un attribut **format d’URL =** `text/html` et un attribut de **modèle** , comme indiqué dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="aea24-150">If there is a version of the search results that can be viewed in a web browser, you should provide a **Url format=**`text/html` element, and **template** attribute, as shown in the following code.</span></span>


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    ...
    <Url format="text/html" template="https://example.com/html.php?query={searchTerms}" />
</OpenSearchDescription>
```



<span data-ttu-id="aea24-151">Si vous fournissez un élément **URL format = "text/html"** et un attribut de **modèle** , un bouton apparaît dans la barre de commandes de l’Explorateur Windows, comme illustré dans la capture d’écran suivante, qui permet à l’utilisateur d’ouvrir un navigateur Web pour afficher les résultats de la recherche lorsque l’utilisateur effectue une requête.</span><span class="sxs-lookup"><span data-stu-id="aea24-151">If you provide a **Url format="text/html"** element and **template** attribute, a button appears in the Windows Explorer command bar, as shown in the following screen shot, that enables the user to open a web browser to view the search results when the user performs a query.</span></span>

![capture d’écran montrant le bouton de restauration de recherche sur le Web.](images/websearchroll-overcommandbarbutton.png)

<span data-ttu-id="aea24-153">La restauration de la requête vers l’interface utilisateur Web du magasin de données est importante dans certains scénarios.</span><span class="sxs-lookup"><span data-stu-id="aea24-153">The roll-over of the query back to the data store's web UI is important in some scenarios.</span></span> <span data-ttu-id="aea24-154">Par exemple, un utilisateur peut souhaiter afficher plus de 100 résultats (le nombre par défaut d’éléments demandés par le fournisseur OpenSearch).</span><span class="sxs-lookup"><span data-stu-id="aea24-154">For example, a user may want to view more than 100 results (the default number of items the OpenSearch provider requests).</span></span> <span data-ttu-id="aea24-155">Dans ce cas, l’utilisateur peut également utiliser les fonctionnalités de recherche disponibles uniquement sur le site Web du magasin de données, telles que la nouvelle requête avec un ordre de tri différent, ou le pivotement et le filtrage de la requête avec les métadonnées associées.</span><span class="sxs-lookup"><span data-stu-id="aea24-155">If so, the user may also want to use search features that are available only on the data store's website, such as re-querying with a different sort order, or pivoting and filtering the query with related metadata.</span></span>

### <a name="url-template-parameters"></a><span data-ttu-id="aea24-156">Paramètres de modèle d’URL</span><span class="sxs-lookup"><span data-stu-id="aea24-156">URL Template Parameters</span></span>

<span data-ttu-id="aea24-157">Le fournisseur OpenSearch effectue toujours les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="aea24-157">The OpenSearch provider performs always the following actions:</span></span>

1.  <span data-ttu-id="aea24-158">Utilise le modèle d’URL pour envoyer la demande au service Web.</span><span class="sxs-lookup"><span data-stu-id="aea24-158">Uses the URL template to send the request to the web service.</span></span>
2.  <span data-ttu-id="aea24-159">Tente de remplacer les jetons trouvés dans le modèle d’URL avant d’envoyer la requête au service Web, comme suit :</span><span class="sxs-lookup"><span data-stu-id="aea24-159">Attempts to replace the tokens found in the URL template before sending the request to the web service, as follows:</span></span>
    -   <span data-ttu-id="aea24-160">Remplace les jetons OpenSearch standard répertoriés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="aea24-160">Replaces the standard OpenSearch tokens that are listed in the following table.</span></span>
    -   <span data-ttu-id="aea24-161">Supprime tous les jetons qui ne sont pas répertoriés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="aea24-161">Removes any tokens that are not listed in the following table.</span></span>



| <span data-ttu-id="aea24-162">Jeton pris en charge</span><span class="sxs-lookup"><span data-stu-id="aea24-162">Supported token</span></span>  | <span data-ttu-id="aea24-163">Utilisation par le fournisseur OpenSearch</span><span class="sxs-lookup"><span data-stu-id="aea24-163">How used by OpenSearch provider</span></span>                                                                                                                 |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aea24-164">{searchTerms}</span><span class="sxs-lookup"><span data-stu-id="aea24-164">{searchTerms}</span></span>    | <span data-ttu-id="aea24-165">Remplacé par les termes de recherche que l’utilisateur tape dans la zone de recherche de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="aea24-165">Replaced with the search terms that the user types in the Windows Explorer search input box.</span></span><br/>                                         |
| <span data-ttu-id="aea24-166">startIndex</span><span class="sxs-lookup"><span data-stu-id="aea24-166">{startIndex}</span></span>     | <span data-ttu-id="aea24-167">Utilisé lors de l’obtention des résultats dans des « pages ».</span><span class="sxs-lookup"><span data-stu-id="aea24-167">Used when getting results in "pages".</span></span><br/> <span data-ttu-id="aea24-168">Remplacé par l’index du premier élément de résultat à retourner.</span><span class="sxs-lookup"><span data-stu-id="aea24-168">Replaced with the index for the first result item to return.</span></span><br/>                        |
| <span data-ttu-id="aea24-169">StartPage</span><span class="sxs-lookup"><span data-stu-id="aea24-169">{startPage}</span></span>      | <span data-ttu-id="aea24-170">Utilisé lors de l’obtention des résultats dans des « pages ».</span><span class="sxs-lookup"><span data-stu-id="aea24-170">Used when getting results in "pages".</span></span><br/> <span data-ttu-id="aea24-171">Remplacé par le numéro de page de l’ensemble des résultats de recherche à retourner.</span><span class="sxs-lookup"><span data-stu-id="aea24-171">Replaced with the page number of the set of search results to return.</span></span><br/>               |
| <span data-ttu-id="aea24-172">saut</span><span class="sxs-lookup"><span data-stu-id="aea24-172">{count}</span></span>          | <span data-ttu-id="aea24-173">Utilisé lors de l’obtention des résultats dans des « pages ».</span><span class="sxs-lookup"><span data-stu-id="aea24-173">Used when getting results in "pages".</span></span><br/> <span data-ttu-id="aea24-174">Remplacé par le nombre de résultats de recherche par page demandés par l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="aea24-174">Replaced with the number of search results per page that Windows Explorer requests.</span></span><br/> |
| <span data-ttu-id="aea24-175">sous</span><span class="sxs-lookup"><span data-stu-id="aea24-175">{language}</span></span>       | <span data-ttu-id="aea24-176">Remplacé par une chaîne qui indique la langue de la requête en cours d’envoi.</span><span class="sxs-lookup"><span data-stu-id="aea24-176">Replaced with a string that indicates the language of the query being sent.</span></span><br/>                                                          |
| <span data-ttu-id="aea24-177">{inputEncoding}</span><span class="sxs-lookup"><span data-stu-id="aea24-177">{inputEncoding}</span></span>  | <span data-ttu-id="aea24-178">Remplacé par une chaîne (telle que « UTF-16 ») qui indique l’encodage de caractères de la requête en cours d’envoi.</span><span class="sxs-lookup"><span data-stu-id="aea24-178">Replaced with a string (such "UTF-16") that indicates the character encoding of the query being sent.</span></span><br/>                                |
| <span data-ttu-id="aea24-179">OutputEncoding</span><span class="sxs-lookup"><span data-stu-id="aea24-179">{outputEncoding}</span></span> | <span data-ttu-id="aea24-180">Remplacé par une chaîne (par exemple, « UTF-16 ») qui indique l’encodage de caractères souhaité pour la réponse du service Web.</span><span class="sxs-lookup"><span data-stu-id="aea24-180">Replaced with a string (such as "UTF-16") that indicates the desired character encoding for the response from the web service.</span></span><br/>       |



 

### <a name="paged-results"></a><span data-ttu-id="aea24-181">Résultats paginés</span><span class="sxs-lookup"><span data-stu-id="aea24-181">Paged Results</span></span>

<span data-ttu-id="aea24-182">Vous souhaiterez peut-être limiter le nombre de résultats retournés par requête.</span><span class="sxs-lookup"><span data-stu-id="aea24-182">You may want to limit the number of results returned per request.</span></span> <span data-ttu-id="aea24-183">Vous pouvez choisir de retourner une « page » de résultats à la fois, ou de faire en sorte que le fournisseur OpenSearch récupère des pages supplémentaires de résultats par numéro d’élément ou numéro de page.</span><span class="sxs-lookup"><span data-stu-id="aea24-183">You can opt to return a "page" of results at a time, or to have the OpenSearch provider get additional pages of results either by item number or page number.</span></span> <span data-ttu-id="aea24-184">Par exemple, si vous envoyez vingt résultats par page, la première page que vous envoyez commence à l’index d’élément 1 et à la page 1 ; la deuxième page que vous envoyez commence à l’index d’élément 21 et à la page 2.</span><span class="sxs-lookup"><span data-stu-id="aea24-184">For example, if you send twenty results per page, the first page you send starts at item index 1 and at page 1; the second page you send starts at item index 21 and at page 2.</span></span> <span data-ttu-id="aea24-185">Vous pouvez définir la façon dont vous souhaitez que le fournisseur OpenSearch demande des éléments à l’aide du `{startItem}` `{startPage}` jeton ou dans le modèle d’URL.</span><span class="sxs-lookup"><span data-stu-id="aea24-185">You can define how you want the OpenSearch provider to request items by using either the `{startItem}` or the `{startPage}` token in the URL template.</span></span>

### <a name="paging-using-the-item-index"></a><span data-ttu-id="aea24-186">Pagination à l’aide de l’index de l’élément</span><span class="sxs-lookup"><span data-stu-id="aea24-186">Paging Using the Item Index</span></span>

<span data-ttu-id="aea24-187">Un index d’élément identifie le premier élément de résultat dans une page de résultats.</span><span class="sxs-lookup"><span data-stu-id="aea24-187">An item index identifies the first result item in a page of results.</span></span> <span data-ttu-id="aea24-188">Si vous souhaitez que les clients envoient des requêtes à l’aide d’un index d’élément, vous pouvez utiliser le `{startIndex}` jeton dans votre attribut de **modèle** d’élément **URL** , comme indiqué dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="aea24-188">If you want clients to send requests using an item index, you can use the `{startIndex}` token in your **Url** element **template** attribute, as shown in the following code.</span></span>


```
<Url format="application/rss+xml" 
    template="https://example.com/rss.php?query={searchTerms}&amp;start={startIndex}" />
```



<span data-ttu-id="aea24-189">Le fournisseur [OpenSearch](https://github.com/dewitt/opensearch) remplace ensuite le jeton dans l’URL par une valeur d’index de départ.</span><span class="sxs-lookup"><span data-stu-id="aea24-189">The [OpenSearch](https://github.com/dewitt/opensearch) provider then replaces the token in the URL with a starting index value.</span></span> <span data-ttu-id="aea24-190">La première demande commence par le premier élément, comme illustré dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="aea24-190">The first request starts with the first item, as illustrated in the following example:</span></span>


```
https://example.com/rss.php?query=frogs&start=1
```



<span data-ttu-id="aea24-191">Le fournisseur OpenSearch peut obtenir des éléments supplémentaires en modifiant la `{startIndex}` valeur du paramètre et en émettant une nouvelle requête.</span><span class="sxs-lookup"><span data-stu-id="aea24-191">The OpenSearch provider can get additional items by changing the `{startIndex}` parameter value and issuing a new request.</span></span> <span data-ttu-id="aea24-192">Le fournisseur répète ce processus jusqu’à ce qu’il ait obtenu des résultats suffisants pour respecter sa limite, ou qu’il atteigne la fin des résultats.</span><span class="sxs-lookup"><span data-stu-id="aea24-192">The provider repeats this process until it gets enough results to satisfy its limit, or reaches the end of the results.</span></span> <span data-ttu-id="aea24-193">Le fournisseur OpenSearch examine le nombre d’éléments renvoyés par le service Web dans la première page de résultats et définit la taille de page attendue sur ce nombre.</span><span class="sxs-lookup"><span data-stu-id="aea24-193">The OpenSearch provider looks at the number of items returned by the web service in the first page of results, and sets the expected page size to that number.</span></span> <span data-ttu-id="aea24-194">Il utilise ce nombre pour incrémenter la `{startIndex}` valeur pour les demandes suivantes.</span><span class="sxs-lookup"><span data-stu-id="aea24-194">It uses that number to increment the `{startIndex}` value for subsequent requests.</span></span> <span data-ttu-id="aea24-195">Par exemple, si le service Web retourne 20 résultats dans la première requête, le fournisseur définit la taille de page attendue sur 20.</span><span class="sxs-lookup"><span data-stu-id="aea24-195">For example, if the web service returns 20 results in the first request, then the provider sets the expected page size to 20.</span></span> <span data-ttu-id="aea24-196">Pour la requête suivante, le fournisseur remplace `{startIndex}` par la valeur 21 pour obtenir les 20 éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="aea24-196">For the next request, the provider replaces `{startIndex}` with the value of 21 to get the next 20 items.</span></span>

> [!Note]  
> <span data-ttu-id="aea24-197">Si une page de résultats retournée par le service Web a moins d’éléments que la taille de page attendue, le fournisseur OpenSearch suppose qu’il a reçu la dernière page des résultats et arrête d’effectuer des requêtes.</span><span class="sxs-lookup"><span data-stu-id="aea24-197">If a page of results returned by the web service has fewer items than the expected page size, then the OpenSearch provider assumes it has received the last page of results and stops making requests.</span></span>

 

### <a name="paging-using-the-page-index"></a><span data-ttu-id="aea24-198">Pagination à l’aide de l’index de page</span><span class="sxs-lookup"><span data-stu-id="aea24-198">Paging Using the Page Index</span></span>

<span data-ttu-id="aea24-199">Un index de page identifie la page de résultats spécifiée.</span><span class="sxs-lookup"><span data-stu-id="aea24-199">A page index identifies the specified page of results.</span></span> <span data-ttu-id="aea24-200">Si vous souhaitez que les clients envoient des requêtes à l’aide d’un numéro de page, vous pouvez utiliser le `{startPage}` jeton dans votre attribut de **modèle** d’élément de **format d’URL** pour indiquer que, comme illustré dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="aea24-200">If you want clients to send requests using a page number, you can use the `{startPage}` token in your **Url format** element **template** attribute to indicate that, as illustrated in the following example:</span></span>


```
<Url format="application/rss+xml" 
    template="https://example.com/rss.php?query={searchTerms}&amp;page={startPage}" />
```



<span data-ttu-id="aea24-201">Le fournisseur OpenSearch remplace ensuite le jeton dans l’URL par un paramètre de numéro de page.</span><span class="sxs-lookup"><span data-stu-id="aea24-201">The OpenSearch provider then replaces the token in the URL with a page number parameter.</span></span> <span data-ttu-id="aea24-202">La première demande commence par la première page, comme illustré dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="aea24-202">The first request starts with the first page, as shown in the following example:</span></span>


```
https://example.com/rss.php?query=frogs&page=1
```



> [!Note]  
> <span data-ttu-id="aea24-203">Si une page de résultats retournée par le service Web a moins d’éléments que la taille de page attendue, le fournisseur OpenSearch suppose qu’il a reçu la dernière page des résultats et arrête d’effectuer des requêtes.</span><span class="sxs-lookup"><span data-stu-id="aea24-203">If a page of results returned by the web service has fewer items than the expected page size, then the OpenSearch provider assumes it has received the last page of results and stops making requests.</span></span>

 

### <a name="page-size"></a><span data-ttu-id="aea24-204">Taille de la page</span><span class="sxs-lookup"><span data-stu-id="aea24-204">Page Size</span></span>

<span data-ttu-id="aea24-205">Vous pouvez configurer votre service Web pour autoriser une requête à spécifier la taille des pages à l’aide d’un paramètre dans l’URL.</span><span class="sxs-lookup"><span data-stu-id="aea24-205">You may want to configure your web service to permit a request to specify the size of the pages by using some parameter in the URL.</span></span> <span data-ttu-id="aea24-206">Une demande doit être spécifiée dans le fichier. fichier osdx à l’aide du `{count}` jeton, comme suit :</span><span class="sxs-lookup"><span data-stu-id="aea24-206">A request must be specified in the .osdx file by using the `{count}` token, as follows:</span></span>


```
<Url format="application/rss+xml" 
    template="https://example.com/rss.php?query={searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
```



<span data-ttu-id="aea24-207">Le fournisseur [OpenSearch](https://github.com/dewitt/opensearch) peut ensuite définir la taille de page souhaitée, en nombre de résultats par page, comme indiqué dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="aea24-207">The [OpenSearch](https://github.com/dewitt/opensearch) provider can then set the desired page size, in number of results per page, as shown in the following example:</span></span>


```
https://example.com/rss.php?query=frogs&start=1&cnt=50
```



<span data-ttu-id="aea24-208">Par défaut, le fournisseur OpenSearch effectue des demandes à l’aide d’une taille de page de 50.</span><span class="sxs-lookup"><span data-stu-id="aea24-208">By default the OpenSearch provider makes requests using a page size of 50.</span></span> <span data-ttu-id="aea24-209">Si vous souhaitez une taille de page différente, ne fournissez pas de `{count}` jeton, et placez plutôt le nombre souhaité directement dans l’élément de **modèle d’URL** .</span><span class="sxs-lookup"><span data-stu-id="aea24-209">If you want a different page size, then do not provide a `{count}` token, and instead place the desired number directly in the **Url template** element.</span></span>

<span data-ttu-id="aea24-210">Le fournisseur OpenSearch détermine la taille de la page en fonction du nombre de résultats renvoyés lors de la première requête.</span><span class="sxs-lookup"><span data-stu-id="aea24-210">The OpenSearch provider determines the page size based on the number of results returned on the first request.</span></span> <span data-ttu-id="aea24-211">Si la première page de résultats reçue a moins d’éléments que le nombre demandé, le fournisseur réinitialise la taille de page pour toutes les demandes de page suivantes.</span><span class="sxs-lookup"><span data-stu-id="aea24-211">If the first page of results received has fewer items than the count requested, the provider resets the page size for any subsequent page requests.</span></span> <span data-ttu-id="aea24-212">Si les demandes de page suivantes retournent moins d’éléments que le nombre demandé, le fournisseur OpenSearch part du principe qu’il a atteint la fin des résultats.</span><span class="sxs-lookup"><span data-stu-id="aea24-212">If subsequent page requests return fewer items than requested, the OpenSearch provider assumes that it has reached the end of the results.</span></span>

## <a name="extended-elements-in-windows-federated-search"></a><span data-ttu-id="aea24-213">Éléments étendus dans la recherche fédérée Windows</span><span class="sxs-lookup"><span data-stu-id="aea24-213">Extended Elements in Windows Federated Search</span></span>

<span data-ttu-id="aea24-214">Outre les éléments standard, la recherche fédérée prend en charge les éléments étendus suivants : **MaximumResultCount** et **ResultsProcessing**.</span><span class="sxs-lookup"><span data-stu-id="aea24-214">In addition to the standard elements, federated search supports the following extended elements: **MaximumResultCount** and **ResultsProcessing**.</span></span>

<span data-ttu-id="aea24-215">Étant donné que ces éléments enfants étendus ne sont pas pris en charge dans la spécification [OpenSearch](https://github.com/dewitt/opensearch) v 1.1, ils doivent être ajoutés à l’aide de l’espace de noms suivant :</span><span class="sxs-lookup"><span data-stu-id="aea24-215">Because these extended child elements are not supported in the [OpenSearch](https://github.com/dewitt/opensearch) v1.1 specification, they must be added by using the following namespace:</span></span>


```
http://schemas.microsoft.com/opensearchext/2009/
```



### <a name="maximum-result-count"></a><span data-ttu-id="aea24-216">Nombre maximal de résultats</span><span class="sxs-lookup"><span data-stu-id="aea24-216">Maximum Result Count</span></span>

<span data-ttu-id="aea24-217">Par défaut, les connecteurs de recherche sont limités à 100 résultats par requête utilisateur.</span><span class="sxs-lookup"><span data-stu-id="aea24-217">By default, search connectors are limited to 100 results per user query.</span></span> <span data-ttu-id="aea24-218">Cette limite peut être personnalisée en incluant l’élément **MaximumResultCount** dans le fichier OSD, comme indiqué dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="aea24-218">This limit can be customized by including the **MaximumResultCount** element within the OSD file as shown in the following example:</span></span>


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/" 
    xmlns:ms-ose="http://schemas.microsoft.com/opensearchext/2009/">
        ...
        <ms-ose:MaximumResultCount>200</ms-ose:MaximumResultCount>
</OpenSearchDescription>
```



<span data-ttu-id="aea24-219">L’exemple précédent déclare le préfixe de l’espace `ms-ose` de noms dans l’élément **OpenSearchDescription** de niveau supérieur, puis l’utilise comme préfixe dans le nom de l’élément.</span><span class="sxs-lookup"><span data-stu-id="aea24-219">The preceding example declares the namespace prefix `ms-ose` in the top-level **OpenSearchDescription** element, and then uses it as a prefix in the element name.</span></span> <span data-ttu-id="aea24-220">Cette déclaration est obligatoire, car **MaximumResultCount** n’est pas pris en charge dans la spécification de la version 1.1 de [OpenSearch](https://github.com/dewitt/opensearch) .</span><span class="sxs-lookup"><span data-stu-id="aea24-220">This declaration is required because the **MaximumResultCount** is not supported in the [OpenSearch](https://github.com/dewitt/opensearch) v1.1 specification.</span></span>

### <a name="property-mapping"></a><span data-ttu-id="aea24-221">Mappage de propriétés</span><span class="sxs-lookup"><span data-stu-id="aea24-221">Property Mapping</span></span>

<span data-ttu-id="aea24-222">Lorsque les résultats sont retournés par le service Web sous la forme d’un flux RSS ou Atom, le fournisseur OpenSearch doit mapper les métadonnées de l’élément dans les flux aux propriétés que le shell Windows peut utiliser.</span><span class="sxs-lookup"><span data-stu-id="aea24-222">When results are returned by the web service as an RSS or Atom feed, the OpenSearch provider must map the item metadata in the feeds to properties that the Windows Shell can use.</span></span> <span data-ttu-id="aea24-223">La capture d’écran suivante illustre la façon dont le fournisseur OpenSearch mappe certains des éléments RSS par défaut.</span><span class="sxs-lookup"><span data-stu-id="aea24-223">The following screen shot illustrates how the OpenSearch provider maps some of the default RSS elements.</span></span>

![capture d’écran montrant les mappages de propriétés RSS vers Windows-Shell intégrés](images/built-inrsstowindowsshellpropertymappings.png)

### <a name="default-mappings"></a><span data-ttu-id="aea24-225">Mappages par défaut</span><span class="sxs-lookup"><span data-stu-id="aea24-225">Default Mappings</span></span>

<span data-ttu-id="aea24-226">Les mappages par défaut des éléments XML RSS aux propriétés système de l’interpréteur de commandes Windows, sont répertoriés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="aea24-226">The default mappings of RSS XML elements to Windows Shell system properties, are listed in the following table.</span></span> <span data-ttu-id="aea24-227">Les chemins d’accès XML sont relatifs à l’élément item.</span><span class="sxs-lookup"><span data-stu-id="aea24-227">XML paths are relative to the item element.</span></span> <span data-ttu-id="aea24-228">Le `"media:"` préfixe est défini par l’espace de noms de l' [espace de noms de recherche Yahoo](https://www.rssboard.org/media-rss) .</span><span class="sxs-lookup"><span data-stu-id="aea24-228">The `"media:"` prefix is defined by the [Yahoo Search Namespace](https://www.rssboard.org/media-rss) namespace.</span></span>



| <span data-ttu-id="aea24-229">Chemin d’accès XML RSS</span><span class="sxs-lookup"><span data-stu-id="aea24-229">RSS XML path</span></span>                  | <span data-ttu-id="aea24-230">Propriété de l’interpréteur de commandes Windows (nom canonique)</span><span class="sxs-lookup"><span data-stu-id="aea24-230">Windows Shell property (canonical name)</span></span> |
|-------------------------------|-----------------------------------------|
| <span data-ttu-id="aea24-231">Lien</span><span class="sxs-lookup"><span data-stu-id="aea24-231">Link</span></span>                          | <span data-ttu-id="aea24-232">System. ItemUrl</span><span class="sxs-lookup"><span data-stu-id="aea24-232">System.ItemUrl</span></span>                          |
| <span data-ttu-id="aea24-233">Intitulé</span><span class="sxs-lookup"><span data-stu-id="aea24-233">Title</span></span>                         | <span data-ttu-id="aea24-234">System. ItemName</span><span class="sxs-lookup"><span data-stu-id="aea24-234">System.ItemName</span></span>                         |
| <span data-ttu-id="aea24-235">Auteur</span><span class="sxs-lookup"><span data-stu-id="aea24-235">Author</span></span>                        | <span data-ttu-id="aea24-236">System.Author</span><span class="sxs-lookup"><span data-stu-id="aea24-236">System.Author</span></span>                           |
| <span data-ttu-id="aea24-237">pubDate</span><span class="sxs-lookup"><span data-stu-id="aea24-237">pubDate</span></span>                       | <span data-ttu-id="aea24-238">System. DateModified</span><span class="sxs-lookup"><span data-stu-id="aea24-238">System.DateModified</span></span>                     |
| <span data-ttu-id="aea24-239">Description</span><span class="sxs-lookup"><span data-stu-id="aea24-239">Description</span></span>                   | <span data-ttu-id="aea24-240">Résumé système.</span><span class="sxs-lookup"><span data-stu-id="aea24-240">System.AutoSummary</span></span>                      |
| <span data-ttu-id="aea24-241">Category</span><span class="sxs-lookup"><span data-stu-id="aea24-241">Category</span></span>                      | <span data-ttu-id="aea24-242">System.Keywords</span><span class="sxs-lookup"><span data-stu-id="aea24-242">System.Keywords</span></span>                         |
| enclosure/@type               | <span data-ttu-id="aea24-243">System. MIMEType</span><span class="sxs-lookup"><span data-stu-id="aea24-243">System.MIMEType</span></span>                         |
| enclosure/@length             | <span data-ttu-id="aea24-244">System. Size</span><span class="sxs-lookup"><span data-stu-id="aea24-244">System.Size</span></span>                             |
| enclosure/@url                | <span data-ttu-id="aea24-245">System. ContentUrl</span><span class="sxs-lookup"><span data-stu-id="aea24-245">System.ContentUrl</span></span>                       |
| <span data-ttu-id="aea24-246">média : catégorie</span><span class="sxs-lookup"><span data-stu-id="aea24-246">media:category</span></span>                | <span data-ttu-id="aea24-247">System.Keywords</span><span class="sxs-lookup"><span data-stu-id="aea24-247">System.Keywords</span></span>                         |
| media:content/@fileSize       | <span data-ttu-id="aea24-248">System. Size</span><span class="sxs-lookup"><span data-stu-id="aea24-248">System.Size</span></span>                             |
| media:content/@type           | <span data-ttu-id="aea24-249">System. MIMEType</span><span class="sxs-lookup"><span data-stu-id="aea24-249">System.MIMEType</span></span>                         |
| media:content/@url            | <span data-ttu-id="aea24-250">System. ContentUrl</span><span class="sxs-lookup"><span data-stu-id="aea24-250">System.ContentUrl</span></span>                       |
| media:group/content/@fileSize | <span data-ttu-id="aea24-251">System. Size</span><span class="sxs-lookup"><span data-stu-id="aea24-251">System.Size</span></span>                             |
| media:group/content/@type     | <span data-ttu-id="aea24-252">System. MIMEType</span><span class="sxs-lookup"><span data-stu-id="aea24-252">System.MIMEType</span></span>                         |
| media:group/content/@url      | <span data-ttu-id="aea24-253">System. ContentUrl</span><span class="sxs-lookup"><span data-stu-id="aea24-253">System.ContentUrl</span></span>                       |
| media:thumbnail/@url          | <span data-ttu-id="aea24-254">System. ItemThumbnailUrl</span><span class="sxs-lookup"><span data-stu-id="aea24-254">System.ItemThumbnailUrl</span></span>                 |



 

> [!Note]  
> <span data-ttu-id="aea24-255">Outre les mappages par défaut des éléments RSS ou Atom standard, vous pouvez mapper d’autres propriétés système de l’interpréteur de commandes Windows en incluant des éléments XML supplémentaires dans l’espace de noms Windows pour chacune des propriétés.</span><span class="sxs-lookup"><span data-stu-id="aea24-255">In addition to the default mappings of standard RSS or Atom elements, you can map other Windows Shell system properties by including additional XML elements in the Windows namespace for each of the properties.</span></span> <span data-ttu-id="aea24-256">Vous pouvez également mapper des éléments à partir d’autres espaces de noms XML existants tels que MediaRSS, iTunes, etc., en ajoutant un mappage de propriété personnalisée dans le fichier. fichier osdx.</span><span class="sxs-lookup"><span data-stu-id="aea24-256">You can also map elements from other existing XML namespaces such as MediaRSS, iTunes, and so forth, by adding custom property mapping in the .osdx file.</span></span>

 

### <a name="custom-property-mappings"></a><span data-ttu-id="aea24-257">Mappages de propriétés personnalisées</span><span class="sxs-lookup"><span data-stu-id="aea24-257">Custom Property Mappings</span></span>

<span data-ttu-id="aea24-258">Vous pouvez personnaliser le mappage des éléments de votre sortie RSS vers les propriétés système de l’interpréteur de commandes Windows en spécifiant le mappage dans le fichier. fichier osdx.</span><span class="sxs-lookup"><span data-stu-id="aea24-258">You can customize the mapping of elements from your RSS output to Windows Shell system properties by specifying the mapping in the .osdx file.</span></span>

<span data-ttu-id="aea24-259">La sortie RSS spécifie :</span><span class="sxs-lookup"><span data-stu-id="aea24-259">The RSS output specifies:</span></span>

-   <span data-ttu-id="aea24-260">Un espace de noms XML, et</span><span class="sxs-lookup"><span data-stu-id="aea24-260">An XML namespace, and</span></span>
-   <span data-ttu-id="aea24-261">Pour tout élément enfant d’un élément, nom d’élément à mapper.</span><span class="sxs-lookup"><span data-stu-id="aea24-261">For any child element of an item, an element name to map against.</span></span>

<span data-ttu-id="aea24-262">Le fichier. fichier osdx identifie une propriété de l’interpréteur de commandes Windows pour chaque nom d’élément dans un espace de noms.</span><span class="sxs-lookup"><span data-stu-id="aea24-262">The .osdx file identifies a Windows Shell property for each element name in a namespace.</span></span> <span data-ttu-id="aea24-263">Les mappages de propriétés que vous définissez dans votre fichier. fichier osdx remplacent les mappages par défaut, s’ils existent, pour les propriétés spécifiées.</span><span class="sxs-lookup"><span data-stu-id="aea24-263">The property mappings that you define in your .osdx file override the default mappings, if they exist, for those specified properties.</span></span>

<span data-ttu-id="aea24-264">Le diagramme suivant illustre la façon dont une extension RSS est mappée aux propriétés Windows (nom canonique).</span><span class="sxs-lookup"><span data-stu-id="aea24-264">The following diagram illustrates how an RSS extension maps to Windows properties (canonical name).</span></span>

![Diagramme montrant que la combinaison de l’espace de noms XML et du chemin XML produit le nom canonique](images/rssextensionsusexmlnamespaceandpathstomaptowindowsproperties.png)

### <a name="example-rss-results-and-osd-property-mapping"></a><span data-ttu-id="aea24-266">Exemples de résultats RSS et mappage des propriétés OSD</span><span class="sxs-lookup"><span data-stu-id="aea24-266">Example RSS results and OSD Property Mapping</span></span>

<span data-ttu-id="aea24-267">L’exemple de sortie RSS suivant identifie `https://example.com/schema/2009` en tant qu’espace de noms XML avec le préfixe « example ».</span><span class="sxs-lookup"><span data-stu-id="aea24-267">The following example RSS output identifies `https://example.com/schema/2009` as the XML namespace with the prefix "example".</span></span> <span data-ttu-id="aea24-268">Ce préfixe doit apparaître à nouveau avant l’élément **e-mail** .</span><span class="sxs-lookup"><span data-stu-id="aea24-268">This prefix must appear again before the **email** element.</span></span>


```
<rss version="2.0" xmlns:example="https://example.com/schema/2009">
   ...
    <item>
      <title>Someone</title>
      <example:email>Someone@example.com</example:email>
    </item>
```



<span data-ttu-id="aea24-269">Dans l’exemple de fichier. fichier osdx suivant, l’élément **email** XML est mappé à la propriété shell Windows [. contact. EmailAddress](../properties/props-system-contact-emailaddress.md).</span><span class="sxs-lookup"><span data-stu-id="aea24-269">In the following example .osdx file, the XML **email** element maps to the Windows Shell property [System.Contact.EmailAddress](../properties/props-system-contact-emailaddress.md).</span></span>


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/"
    xmlns:ms-ose="http://schemas.microsoft.com/opensearchext/2009/">
...
 <ms-ose:ResultsProcessing format="application/rss+xml">
   <ms-ose:PropertyMapList>
     <ms-ose:PropertyMap sourceNamespaceURI="https://example.com/schema/2009/" >
       <ms-ose:Source path="email">
         <ms-ose:Property schema="http://schemas.microsoft.com/windows/2008/propertynamespace" name="System.Contact.EmailAddress" />
       </ms-ose:Source>
     </ms-ose:PropertyMap>
   </ms-ose:PropertyMapList>
 </ms-ose:ResultsProcessing>
...
</OpenSearchDescription>
```



<span data-ttu-id="aea24-270">Certaines propriétés ne peuvent pas être mappées, car leurs valeurs sont remplacées ultérieurement ou ne sont pas modifiables.</span><span class="sxs-lookup"><span data-stu-id="aea24-270">There are some properties that cannot be mapped because values for them are either overridden later or are not editable.</span></span> <span data-ttu-id="aea24-271">Par exemple, [System. ItemFolderPathDisplay](../properties/props-system-itempathdisplay.md) ou [System. ItemPathDisplayNarrow](../properties/props-system-itempathdisplaynarrow.md) ne peuvent pas être mappés, car ils sont calculés à partir de la valeur URL fournie dans les éléments Link ou Enclosure.</span><span class="sxs-lookup"><span data-stu-id="aea24-271">For example, [System.ItemFolderPathDisplay](../properties/props-system-itempathdisplay.md) or [System.ItemPathDisplayNarrow](../properties/props-system-itempathdisplaynarrow.md) cannot be mapped because they are calculated from the URL value provided in either the link or enclosure elements.</span></span>

### <a name="thumbnails"></a><span data-ttu-id="aea24-272">Miniatures</span><span class="sxs-lookup"><span data-stu-id="aea24-272">Thumbnails</span></span>

<span data-ttu-id="aea24-273">Les URL d’image miniature peuvent être fournies pour n’importe quel élément à l’aide de l’élément **Media : thumbnail URL = ""** .</span><span class="sxs-lookup"><span data-stu-id="aea24-273">Thumbnail image URLs can be provided for any item by using the **media:thumbnail url=""** element.</span></span> <span data-ttu-id="aea24-274">La résolution idéale est 150 x 150 pixels.</span><span class="sxs-lookup"><span data-stu-id="aea24-274">The ideal resolution is 150 x 150 pixels.</span></span> <span data-ttu-id="aea24-275">Les plus grandes miniatures prises en charge sont 256 x 256 pixels.</span><span class="sxs-lookup"><span data-stu-id="aea24-275">The largest thumbnails supported are 256 x 256 pixels.</span></span> <span data-ttu-id="aea24-276">Le fait de fournir des images de grande taille prend plus de bande passante sans avantage supplémentaire pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="aea24-276">Providing larger images takes more bandwidth for no extra benefit to the user.</span></span>

### <a name="open-file-location-context-menu"></a><span data-ttu-id="aea24-277">Ouvrir le menu contextuel de l’emplacement du fichier</span><span class="sxs-lookup"><span data-stu-id="aea24-277">Open File Location Context Menu</span></span>

<span data-ttu-id="aea24-278">Windows fournit un menu contextuel nommé **emplacement du fichier ouvert** pour les éléments de résultat.</span><span class="sxs-lookup"><span data-stu-id="aea24-278">Windows provides a shortcut menu named **Open file location** for result items.</span></span> <span data-ttu-id="aea24-279">Si l’utilisateur sélectionne un élément dans ce menu, l’URL « parent » pour l’élément sélectionné est ouverte.</span><span class="sxs-lookup"><span data-stu-id="aea24-279">If the user selects an item from that menu, the "parent" URL for the selected item is opened.</span></span> <span data-ttu-id="aea24-280">Si l’URL est une URL Web, par exemple `https://...` , le navigateur Web est ouvert et navigue vers cette URL.</span><span class="sxs-lookup"><span data-stu-id="aea24-280">If the URL is a web URL, such as `https://...`, the web browser is opened and navigated to that URL.</span></span> <span data-ttu-id="aea24-281">Votre flux doit fournir une URL personnalisée pour chaque élément afin de s’assurer que Windows ouvre une URL valide.</span><span class="sxs-lookup"><span data-stu-id="aea24-281">Your feed should provide a custom URL for each item to ensure that Windows opens a valid URL.</span></span> <span data-ttu-id="aea24-282">Pour ce faire, vous pouvez inclure l’URL dans un élément à l’intérieur du code XML de l’élément, comme illustré dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="aea24-282">This can be accomplished by including the URL within an element inside the item's XML, as illustrated in the following example:</span></span>


```
<rss version="2.0" xmlns:example="https://example.com/schema/2009" 
    xmlns:win="http://schemas.microsoft.com/windows/2008/propertynamespace">
...
   <item>
      <title>Someone</title>
      <link>https://example.com/pictures.aspx?id=01</link>
      <win:System.ItemFolderPathDisplay>https://example.com/pictures_list.aspx
   </win:System.ItemFolderPathDisplay>
   </item>
...
```



<span data-ttu-id="aea24-283">Si cette propriété n’est pas définie explicitement dans le XML de l’élément, le fournisseur OpenSearch le définit sur le dossier parent de l’URL de l’élément.</span><span class="sxs-lookup"><span data-stu-id="aea24-283">If this property is not explicitly set in the item's XML, the OpenSearch provider sets it to the parent folder of the URL of the item.</span></span> <span data-ttu-id="aea24-284">Dans l’exemple ci-dessus, le fournisseur OpenSearch utilise la valeur de lien et définit la valeur de la propriété d’environnement Windows [System. ItemFolderPathDisplay](../properties/props-system-itemfolderpathdisplay.md) sur `"https://example.com/"` .</span><span class="sxs-lookup"><span data-stu-id="aea24-284">In the example above, the OpenSearch provider would use the link value, and set the [System.ItemFolderPathDisplay](../properties/props-system-itemfolderpathdisplay.md) Windows Shell property value to `"https://example.com/"`.</span></span>

### <a name="customize-windows-explorer-views-with-property-description-lists"></a><span data-ttu-id="aea24-285">Personnaliser les affichages de l’Explorateur Windows avec les listes de description des propriétés</span><span class="sxs-lookup"><span data-stu-id="aea24-285">Customize Windows Explorer Views with Property Description Lists</span></span>

<span data-ttu-id="aea24-286">Certaines dispositions de vue de l’Explorateur Windows sont définies par les listes de description des propriétés ou par les exemples de configuration.</span><span class="sxs-lookup"><span data-stu-id="aea24-286">Some Windows Explorer view layouts are defined by property description lists, or proplists.</span></span> <span data-ttu-id="aea24-287">Un PropList est une liste de propriétés délimitées par des points-virgules, telles que `"prop:System.ItemName; System.Author"` , qui est utilisée pour contrôler l’affichage de vos résultats dans l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="aea24-287">A proplist is a semicolon-delimited list of properties, such as `"prop:System.ItemName; System.Author"`, that is used to control how your results appear in Windows Explorer.</span></span>

<span data-ttu-id="aea24-288">Les zones de l’interface utilisateur de l’Explorateur Windows qui peuvent être personnalisées à l’aide de PropList sont illustrées dans la capture d’écran suivante :</span><span class="sxs-lookup"><span data-stu-id="aea24-288">The UI areas of Windows Explorer that can be customized by using proplists are illustrated in the following screen shot:</span></span>

![capture d’écran montrant les zones de l’interface utilisateur de l’Explorateur Windows qui peuvent être personnalisées à l’aide de PropList](images/areasofwindowsexplorerthatyoucancontrolwithproplists.png)

<span data-ttu-id="aea24-290">Chaque zone de l’Explorateur Windows est associée à un ensemble de PropList, qui sont eux-mêmes spécifiés en tant que propriétés.</span><span class="sxs-lookup"><span data-stu-id="aea24-290">Each area of Windows Explorer has an associated set of proplists, which themselves are specified as properties.</span></span> <span data-ttu-id="aea24-291">Vous pouvez spécifier des proplis personnalisés pour des éléments individuels dans vos jeux de résultats ou pour tous les éléments d’un ensemble de résultats.</span><span class="sxs-lookup"><span data-stu-id="aea24-291">You can specify custom proplists for individual items in your result sets or for all items in a set of results.</span></span>



| <span data-ttu-id="aea24-292">Zone de l’interface utilisateur à personnaliser</span><span class="sxs-lookup"><span data-stu-id="aea24-292">UI Area to customize</span></span>               | <span data-ttu-id="aea24-293">Propriété de l’interpréteur de commandes Windows qui implémente la personnalisation</span><span class="sxs-lookup"><span data-stu-id="aea24-293">Windows Shell property that implements the customization</span></span> |
|------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="aea24-294">Mode d’affichage de contenu (lors de la recherche)</span><span class="sxs-lookup"><span data-stu-id="aea24-294">Content view mode (when searching)</span></span> | <span data-ttu-id="aea24-295">System. PropList. ContentViewModeForSearch</span><span class="sxs-lookup"><span data-stu-id="aea24-295">System.PropList.ContentViewModeForSearch</span></span>                 |
| <span data-ttu-id="aea24-296">Mode d’affichage de contenu (lors de la navigation)</span><span class="sxs-lookup"><span data-stu-id="aea24-296">Content view mode (when browsing)</span></span>  | <span data-ttu-id="aea24-297">System. PropList. ContentViewModeForBrowse</span><span class="sxs-lookup"><span data-stu-id="aea24-297">System.PropList.ContentViewModeForBrowse</span></span>                 |
| <span data-ttu-id="aea24-298">Mode d’affichage en mosaïque</span><span class="sxs-lookup"><span data-stu-id="aea24-298">Tile view mode</span></span>                     | <span data-ttu-id="aea24-299">System. PropList. TileInfo</span><span class="sxs-lookup"><span data-stu-id="aea24-299">System.PropList.TileInfo</span></span>                                 |
| <span data-ttu-id="aea24-300">Volet Détails</span><span class="sxs-lookup"><span data-stu-id="aea24-300">Details pane</span></span>                       | <span data-ttu-id="aea24-301">System. PropList. PreviewDetails</span><span class="sxs-lookup"><span data-stu-id="aea24-301">System.PropList.PreviewDetails</span></span>                           |
| <span data-ttu-id="aea24-302">Info-bulle (info-bulle de pointage de l’élément)</span><span class="sxs-lookup"><span data-stu-id="aea24-302">Infotip (item's hover tooltip)</span></span>     | <span data-ttu-id="aea24-303">System. PropList. info-bulle</span><span class="sxs-lookup"><span data-stu-id="aea24-303">System.PropList.Infotip</span></span>                                  |



 

 

<span data-ttu-id="aea24-304">**Pour spécifier un PropList unique pour un élément individuel :**</span><span class="sxs-lookup"><span data-stu-id="aea24-304">**To specify a unique proplist for an individual item:**</span></span>

1.  <span data-ttu-id="aea24-305">Dans votre sortie RSS, ajoutez un élément personnalisé représentant l’PropList que vous souhaitez personnaliser.</span><span class="sxs-lookup"><span data-stu-id="aea24-305">In your RSS output, add a custom element representing the proplist you want to customize.</span></span> <span data-ttu-id="aea24-306">Par exemple, l’exemple suivant définit la liste pour le volet d’informations :</span><span class="sxs-lookup"><span data-stu-id="aea24-306">For example, the following example sets the list for the details pane:</span></span>
    ```
    <win:System.PropList.PreviewDetails>
        prop:System.ItemName;System.Author</win:System.PropList.PreviewDetails>
    ```

    

2.  <span data-ttu-id="aea24-307">Pour appliquer une propriété à chaque élément dans les résultats de la recherche sans modifier la sortie RSS, spécifiez un PropList dans un élément **MS-ose : PropertyDefaultValues** dans le fichier. fichier osdx, comme indiqué dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="aea24-307">To apply a property to every item in the search results without modifying the RSS output, specify a proplist within an **ms-ose:PropertyDefaultValues** element in the .osdx file, as shown in the following example:</span></span>

    ```
    <ms-ose:ResultsProcessing format="application/rss+xml">
        <ms-ose:PropertyDefaultValues>
          <ms-ose:Property schema="http://schemas.microsoft.com/windows/2008/propertynamespace"
            name="System.PropList.ContentViewModeForSearch">prop:~System.ItemNameDisplay;System.Photo.DateTaken;
            ~System.ItemPathDisplay;~System.Search.AutoSummary;System.Size;System.Author;System.Keywords</ms-ose:Property>
        </ms-ose:PropertyDefaultValues>
      </ms-ose:ResultsProcessing>
    ```

    

### <a name="content-view-mode-layout-of-properties"></a><span data-ttu-id="aea24-308">Disposition du mode d’affichage du contenu des propriétés</span><span class="sxs-lookup"><span data-stu-id="aea24-308">Content View Mode Layout of Properties</span></span>

<span data-ttu-id="aea24-309">La liste des propriétés spécifiées dans **System. PropList. ContentViewModeForSearch** et **System. PropList. ContentViewModeForBrowse** PropList détermine ce qui est affiché en mode d’affichage de contenu.</span><span class="sxs-lookup"><span data-stu-id="aea24-309">The list of properties specified in the **System.PropList.ContentViewModeForSearch** and **System.PropList.ContentViewModeForBrowse** proplists determines what is shown in Content view mode.</span></span> <span data-ttu-id="aea24-310">Pour plus d’informations sur les listes de propriétés, consultez [PropList](/windows/win32/api/propsys/nf-propsys-ipropertysystem-getpropertydescriptionlistfromstring).</span><span class="sxs-lookup"><span data-stu-id="aea24-310">For more information about property lists, see [PropList](/windows/win32/api/propsys/nf-propsys-ipropertysystem-getpropertydescriptionlistfromstring).</span></span>

<span data-ttu-id="aea24-311">Les propriétés sont présentées selon les nombres indiqués dans le modèle de disposition suivant :</span><span class="sxs-lookup"><span data-stu-id="aea24-311">The properties are laid out according to the numbers shown in the following layout pattern:</span></span>

![capture d’écran montrant le modèle de disposition par défaut dans l’affichage du contenu](images/propertiesnumberslayoutpattern.png)

<span data-ttu-id="aea24-313">Si nous utilisons la liste de propriétés suivante,</span><span class="sxs-lookup"><span data-stu-id="aea24-313">If we use the following list of properties,</span></span>


```
prop:~System.ItemNameDisplay;System.Author;System.ItemPathDisplay;~System.Search.AutoSummary;
    System.Size;System.Photo.DateTaken;System.Keywords
```



<span data-ttu-id="aea24-314">L’affichage suivant s’affiche :</span><span class="sxs-lookup"><span data-stu-id="aea24-314">Then we see the following display:</span></span>

![capture d’écran montrant l’exemple de disposition des propriétés.](images/samplepropertylayout.png)

> [!Note]  
> <span data-ttu-id="aea24-316">Pour une meilleure lisibilité, les propriétés affichées dans la colonne la plus à droite doivent être étiquetées.</span><span class="sxs-lookup"><span data-stu-id="aea24-316">For the best readability, the properties shown in the right-most column should be labeled.</span></span>

 

### <a name="property-list-flags"></a><span data-ttu-id="aea24-317">Indicateurs de liste de propriétés</span><span class="sxs-lookup"><span data-stu-id="aea24-317">Property List Flags</span></span>

<span data-ttu-id="aea24-318">Seul l’un des indicateurs définis dans la documentation de PropList s’applique à l’affichage des éléments en mode d’affichage de contenu : ` "~"` .</span><span class="sxs-lookup"><span data-stu-id="aea24-318">Only one of the flags defined in the proplists documentation applies to the display of items in Content View mode layouts:` "~"`.</span></span> <span data-ttu-id="aea24-319">Dans les exemples précédents, la vue de l’Explorateur Windows étiquette certaines des propriétés, telles que `Tags: animals; zoo; lion` .</span><span class="sxs-lookup"><span data-stu-id="aea24-319">In the previous examples, the Windows Explorer view labels some of the properties, such as `Tags: animals; zoo; lion`.</span></span> <span data-ttu-id="aea24-320">C’est le comportement par défaut lorsque vous spécifiez une propriété dans la liste.</span><span class="sxs-lookup"><span data-stu-id="aea24-320">That is the default behavior when you specify a property in the list.</span></span> <span data-ttu-id="aea24-321">Par exemple, le PropList `"System.Author"` est affiché sous la forme `"Authors: value"` .</span><span class="sxs-lookup"><span data-stu-id="aea24-321">For example, the proplist has `"System.Author"` which is displayed as `"Authors: value"`.</span></span> <span data-ttu-id="aea24-322">Lorsque vous souhaitez masquer l’étiquette de la propriété, placez un `"~"` devant le nom de la propriété.</span><span class="sxs-lookup"><span data-stu-id="aea24-322">When you want to hide the property label, place a `"~"` in front of the property name.</span></span> <span data-ttu-id="aea24-323">Par exemple, si PropList a la `"~System.Size"` valeur, la propriété est affichée comme une seule valeur, sans l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="aea24-323">For example, if the proplist has `"~System.Size"`, the property is displayed as just a value, without the label.</span></span>

## <a name="previews"></a><span data-ttu-id="aea24-324">Versions préliminaires</span><span class="sxs-lookup"><span data-stu-id="aea24-324">Previews</span></span>

<span data-ttu-id="aea24-325">Lorsque l’utilisateur sélectionne un élément de résultat dans l’Explorateur Windows et que le volet de visualisation est ouvert, le contenu de l’élément est aperçu.</span><span class="sxs-lookup"><span data-stu-id="aea24-325">When the user selects a result item in Windows Explorer and the preview pane is open, the content of the item is previewed.</span></span>

<span data-ttu-id="aea24-326">Le contenu à afficher dans l’aperçu est spécifié par une URL, qui est déterminée comme suit :</span><span class="sxs-lookup"><span data-stu-id="aea24-326">The content to show in the preview is specified by a URL, that is determined as follows:</span></span>

1.  <span data-ttu-id="aea24-327">Si la propriété de l’interpréteur de commandes Windows **System. WebPreviewUrl** est définie pour l’élément, utilisez cette URL.</span><span class="sxs-lookup"><span data-stu-id="aea24-327">If the **System.WebPreviewUrl** Windows Shell property is set for the item, then use that URL.</span></span>
    > [!Note]  
    > <span data-ttu-id="aea24-328">La propriété doit être fournie dans le RSS à l’aide de l’espace de noms du shell Windows ou mappée explicitement dans le fichier. fichier osdx.</span><span class="sxs-lookup"><span data-stu-id="aea24-328">The property needs to be provided in the RSS by using the Windows Shell namespace, or explicitly mapped in the .osdx file.</span></span>

     

2.  <span data-ttu-id="aea24-329">Si ce n’est pas le cas, utilisez l’URL du lien à la place.</span><span class="sxs-lookup"><span data-stu-id="aea24-329">If not, then use the link URL instead.</span></span>

<span data-ttu-id="aea24-330">L’organigramme suivant illustre cette logique.</span><span class="sxs-lookup"><span data-stu-id="aea24-330">The following flowchart shows this logic.</span></span>

![Organigramme illustrant la manière dont l’Explorateur Windows sélectionne l’URL à utiliser pour les aperçus](images/howwindowsexploreridentifieswhichurltouseforpreviews.png)

<span data-ttu-id="aea24-332">Il est possible d’utiliser une URL différente pour la version préliminaire que pour l’élément lui-même.</span><span class="sxs-lookup"><span data-stu-id="aea24-332">It is possible to use a different URL for the preview than for the item itself.</span></span> <span data-ttu-id="aea24-333">Cela signifie que si vous fournissez des URL différentes pour l’URL de lien et le boîtier ou `media:content URL` , l’Explorateur Windows utilise l’URL de lien pour les aperçus de l’élément, mais utilise l’autre URL pour la détection de type de fichier, l’ouverture, le téléchargement, etc.</span><span class="sxs-lookup"><span data-stu-id="aea24-333">This means that if you provide different URLs for the link URL and the enclosure or `media:content URL`, Windows Explorer uses the link URL for previews of the item but uses the other URL for file type detection, opening, downloading, and so forth.</span></span>

<span data-ttu-id="aea24-334">Comment l’Explorateur Windows détermine l’URL à utiliser :</span><span class="sxs-lookup"><span data-stu-id="aea24-334">How Windows Explorer determines what URL to use:</span></span>

1.  <span data-ttu-id="aea24-335">Si vous fournissez un mappage à [System. ItemFolderPathDisplay](../properties/props-system-itemfolderpathdisplay.md), l’Explorateur Windows utilise cette URL</span><span class="sxs-lookup"><span data-stu-id="aea24-335">If you provide a mapping to [System.ItemFolderPathDisplay](../properties/props-system-itemfolderpathdisplay.md), then Windows Explorer uses that URL</span></span>
2.  <span data-ttu-id="aea24-336">Si vous ne fournissez pas de mappage, l’Explorateur Windows indique si les URL de lien et de boîtier sont différentes.</span><span class="sxs-lookup"><span data-stu-id="aea24-336">If you do not provide a mapping, then Windows Explorer identifies whether the link and enclosure URLs are different.</span></span> <span data-ttu-id="aea24-337">Dans ce cas, l’Explorateur Windows utilise l’URL du lien.</span><span class="sxs-lookup"><span data-stu-id="aea24-337">If so, then Windows Explorer uses the link URL.</span></span>
3.  <span data-ttu-id="aea24-338">Si les URL sont identiques ou s’il existe uniquement une URL de lien, l’Explorateur Windows analyse le lien pour rechercher le conteneur parent en supprimant le nom de fichier de l’URL complète.</span><span class="sxs-lookup"><span data-stu-id="aea24-338">If the URLs are the same or if there is only a link URL, then Windows Explorer parses the link to find the parent container by removing the file name from the full URL.</span></span>
    > [!Note]  
    > <span data-ttu-id="aea24-339">Si vous reconnaissez que l’analyse d’URL entraînerait des liens inactifs pour votre service, vous devez fournir un mappage explicite pour la propriété.</span><span class="sxs-lookup"><span data-stu-id="aea24-339">If you recognize that the URL parsing would result in dead links for your service, you should provide an explicit mapping for the property.</span></span>

     

## <a name="open-file-location-menu-item"></a><span data-ttu-id="aea24-340">Élément de menu ouvrir l’emplacement du fichier</span><span class="sxs-lookup"><span data-stu-id="aea24-340">Open File Location Menu Item</span></span>

<span data-ttu-id="aea24-341">Quand vous cliquez avec le bouton droit sur un élément, la commande de menu **ouvrir l’emplacement du fichier** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="aea24-341">When a right-clicks an item, the **Open file location** menu command appears.</span></span> <span data-ttu-id="aea24-342">Cette commande dirige l’utilisateur vers le conteneur ou l’emplacement de cet élément.</span><span class="sxs-lookup"><span data-stu-id="aea24-342">This command takes the user to the container for or location of that item.</span></span> <span data-ttu-id="aea24-343">Par exemple, dans une recherche SharePoint, si vous sélectionnez cette option pour un fichier dans une bibliothèque de documents, la racine de la bibliothèque de documents s’ouvre dans le navigateur Web.</span><span class="sxs-lookup"><span data-stu-id="aea24-343">For example, in a SharePoint search, selecting this option for a file in a document library would open the document library root in the web browser.</span></span>

<span data-ttu-id="aea24-344">Lorsqu’un utilisateur clique sur **ouvrir l’emplacement du fichier**, l’Explorateur Windows tente de trouver un conteneur parent, à l’aide de la logique illustrée dans l’organigramme suivant :</span><span class="sxs-lookup"><span data-stu-id="aea24-344">When a user clicks **Open file location**, Windows Explorer attempts to find a parent container, by using the logic shown in the following flowchart:</span></span>

![Organigramme illustrant comment l’Explorateur Windows identifie un conteneur parent](images/howwindowsexploreridentifiesaparentcontainer.png)

## <a name="additional-resources"></a><span data-ttu-id="aea24-346">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="aea24-346">Additional Resources</span></span>

<span data-ttu-id="aea24-347">Pour plus d’informations sur l’implémentation de la Fédération de recherche dans des magasins de données distants à l’aide des technologies OpenSearch dans Windows 7 et versions ultérieures, consultez « ressources supplémentaires » dans la rubrique [recherche fédérée dans Windows](/previous-versions//dd742958(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="aea24-347">For additional information about implementing search federation to remote data stores using OpenSearch technologies in Windows 7 and later, see "Additional Resources" at [Federated Search in Windows](/previous-versions//dd742958(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="aea24-348">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="aea24-348">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aea24-349">Recherche fédérée dans Windows</span><span class="sxs-lookup"><span data-stu-id="aea24-349">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> <dt>

[<span data-ttu-id="aea24-350">Prise en main avec la recherche fédérée dans Windows</span><span class="sxs-lookup"><span data-stu-id="aea24-350">Getting Started with Federated Search in Windows</span></span>](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[<span data-ttu-id="aea24-351">Connexion de votre service Web dans la recherche fédérée Windows</span><span class="sxs-lookup"><span data-stu-id="aea24-351">Connecting Your web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)
</dt> <dt>

[<span data-ttu-id="aea24-352">Activation de votre magasin de données dans la recherche fédérée Windows</span><span class="sxs-lookup"><span data-stu-id="aea24-352">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)
</dt> <dt>

[<span data-ttu-id="aea24-353">Meilleures pratiques suivantes dans Windows Federated Search</span><span class="sxs-lookup"><span data-stu-id="aea24-353">Following Best Practices in Windows Federated Search</span></span>](-search-fedsearch-best.md)
</dt> <dt>

[<span data-ttu-id="aea24-354">Déploiement de connecteurs de recherche dans la recherche fédérée Windows</span><span class="sxs-lookup"><span data-stu-id="aea24-354">Deploying Search Connectors in Windows Federated Search</span></span>](-search-federated-search-deploying.md)
</dt> </dl>

 

 
