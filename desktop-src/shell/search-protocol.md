---
description: 'La recherche : le protocole d’application est une convention extensible pour l’appel de l’application Desktop Search sur Windows Vista avec Service Pack 1 (SP1) et versions ultérieures.'
title: Utilisation du protocole de recherche
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 91a1ec25-f6ab-4377-8478-20bc51a1d5df
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: a9223a2a30cab85f8e1b0dac0d0df2dc4fe8f80c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991737"
---
# <a name="using-the-search-protocol"></a><span data-ttu-id="e609d-103">Utilisation du protocole de recherche</span><span class="sxs-lookup"><span data-stu-id="e609d-103">Using the search Protocol</span></span>

<span data-ttu-id="e609d-104">La **recherche :** le [protocole d’application](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85)) est une convention extensible pour l’appel de l’application Desktop Search sur Windows Vista avec Service Pack 1 (SP1) et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e609d-104">The **search:** [application protocol](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85)) is an extensible convention for calling the desktop search application on Windows Vista with Service Pack 1 (SP1) and later versions.</span></span> <span data-ttu-id="e609d-105">Le protocole a été créé dans Windows Vista avec SP1 (pour plus d’informations, consultez l’article [vue d’ensemble de Windows Vista Desktop Search changes in Windows Vista Service Pack 1](https://support.microsoft.com/kb/941946)) afin de permettre à Windows de déterminer et d’appeler l’application Desktop Search par défaut.</span><span class="sxs-lookup"><span data-stu-id="e609d-105">The protocol was created in Windows Vista with SP1 (for information see the Knowledge Base article [Overview of Windows Vista desktop search Changes in Windows Vista Service Pack 1](https://support.microsoft.com/kb/941946)) to give Windows a way to determine and call the default desktop search application.</span></span>

<span data-ttu-id="e609d-106">La syntaxe du protocole fournit un certain nombre de paramètres utiles pour effectuer des recherches courantes sur le bureau, telles que des termes de recherche entrés par l’utilisateur ou l’emplacement où la recherche a commencé.</span><span class="sxs-lookup"><span data-stu-id="e609d-106">The protocol syntax provides a number of parameters useful for performing common desktop searches, such as user-entered search terms or the location on which the search was begun.</span></span> <span data-ttu-id="e609d-107">Lorsque les utilisateurs recherchent à partir de l’un des deux points d’entrée de recherche disponibles (le menu **Démarrer** ou l’Explorateur Windows), le système d’exploitation utilise le protocole de recherche pour lancer l’application Desktop Search par défaut.</span><span class="sxs-lookup"><span data-stu-id="e609d-107">When users search from one of the two available search entry points (either the **Start** menu or Windows Explorer), the operating system uses the search protocol to launch the default desktop search application.</span></span> <span data-ttu-id="e609d-108">Pour ce faire, il ajoute les termes de recherche entrés par l’utilisateur à la syntaxe du protocole de recherche standard et transmet ces informations à l’application inscrite en tant qu’application de recherche par défaut.</span><span class="sxs-lookup"><span data-stu-id="e609d-108">It does this by adding the user-entered search terms to the standard search protocol syntax and passing that information to the application registered as the default search application.</span></span>

<span data-ttu-id="e609d-109">Si aucune autre application Desktop Search n’est installée, une recherche entrée dans ces points d’entrée lance l’Explorateur de recherche Windows.</span><span class="sxs-lookup"><span data-stu-id="e609d-109">If no other desktop search applications are installed, a search entered into these entry points launches the Windows Search Explorer.</span></span> <span data-ttu-id="e609d-110">Toutefois, les développeurs tiers peuvent créer, installer et inscrire leurs applications pour gérer le protocole de recherche et être l’application de recherche par défaut.</span><span class="sxs-lookup"><span data-stu-id="e609d-110">However, third-party developers can create, install, and register their applications to handle the search protocol and to be the default search application.</span></span> <span data-ttu-id="e609d-111">De telles applications doivent prendre en charge la syntaxe du protocole de recherche et s’inscrire auprès de la fonctionnalité [programmes par défaut](default-programs.md) pour garantir une expérience transparente avec Windows.</span><span class="sxs-lookup"><span data-stu-id="e609d-111">Such applications need to support the search protocol syntax and register with the [Default Programs](default-programs.md) feature to ensure a seamless experience with Windows.</span></span>

<span data-ttu-id="e609d-112">Si vous développez une application destinée à utiliser ou à créer une application de recherche sur le bureau spécifique, vous ne devez pas dépendre exclusivement du protocole **Search :** .</span><span class="sxs-lookup"><span data-stu-id="e609d-112">If you develop an application that is intended to use or build upon a specific desktop search application, you should not depend exclusively on the **search:** protocol.</span></span> <span data-ttu-id="e609d-113">Étant donné que de nombreuses applications peuvent posséder le protocole **Search :** , il n’y a aucune garantie que votre application de recherche de bureau ciblée en sera propriétaire à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="e609d-113">Because many applications could own the **search:** protocol, there is no guarantee that your targeted desktop search application will own it at any given time.</span></span> <span data-ttu-id="e609d-114">Au lieu de cela, vous devez utiliser un protocole de recherche privé défini par cette application de recherche de bureau ciblée.</span><span class="sxs-lookup"><span data-stu-id="e609d-114">Instead, you should use a private search protocol defined by that targeted desktop search application.</span></span> <span data-ttu-id="e609d-115">Cela signifie que les applications Desktop Search destinées à être une plateforme pour les applications tierces doivent prendre en charge le protocole **Search :** et leur propre protocole de recherche propriétaire.</span><span class="sxs-lookup"><span data-stu-id="e609d-115">This means that desktop search applications intended to be a platform for third-party applications should support both the **search:** protocol and their own proprietary search protocol.</span></span>

> [!Note]  
> <span data-ttu-id="e609d-116">Le protocole **Search :** ne remplace pas la propriété [search-ms :](../search/-search-3x-wds-qryidx-searchms.md) Protocol.</span><span class="sxs-lookup"><span data-stu-id="e609d-116">The **search:** protocol does not replace the proprietary [search-ms:](../search/-search-3x-wds-qryidx-searchms.md) protocol.</span></span> <span data-ttu-id="e609d-117">Les applications peuvent toujours utiliser le protocole **search-ms :** Protocol pour lancer l’Explorateur de recherche dans la fenêtre ou pour interroger silencieusement l’indexeur de recherche Windows.</span><span class="sxs-lookup"><span data-stu-id="e609d-117">Applications can still use the **search-ms:** protocol to launch Window Search Explorer or to silently query the Windows Search indexer.</span></span>

 

<span data-ttu-id="e609d-118">Cette rubrique couvre les sujets suivants :</span><span class="sxs-lookup"><span data-stu-id="e609d-118">This topic covers the following:</span></span>

-   [<span data-ttu-id="e609d-119">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e609d-119">Syntax</span></span>](#syntax)
-   [<span data-ttu-id="e609d-120">Windows Vista avec SP1 utilisation du protocole Search :</span><span class="sxs-lookup"><span data-stu-id="e609d-120">Windows Vista with SP1 use of the search: protocol</span></span>](#windows-vista-with-sp1-use-of-the-search-protocol)
-   [<span data-ttu-id="e609d-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="e609d-121">Examples</span></span>](#examples)
-   [<span data-ttu-id="e609d-122">Inscription de l’application qui gère le protocole</span><span class="sxs-lookup"><span data-stu-id="e609d-122">Registering the Application that Handles the Protocol</span></span>](#registering-the-application-that-handles-the-protocol)
    -   [<span data-ttu-id="e609d-123">Entrées de Registre</span><span class="sxs-lookup"><span data-stu-id="e609d-123">Registry Entries</span></span>](#registry-entries)
-   [<span data-ttu-id="e609d-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e609d-124">Related topics</span></span>](#related-topics)

## <a name="syntax"></a><span data-ttu-id="e609d-125">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e609d-125">Syntax</span></span>

<span data-ttu-id="e609d-126">Le protocole de recherche utilise la syntaxe encodée par URL standard suivante :</span><span class="sxs-lookup"><span data-stu-id="e609d-126">The search protocol uses the following standard URL-encoded syntax:</span></span>


```C++
search:parameter=value[&parameter=value]&
```



<span data-ttu-id="e609d-127">La syntaxe commence par identifier le protocole lui-même (**Search :**).</span><span class="sxs-lookup"><span data-stu-id="e609d-127">The syntax begins by identifying the protocol itself (**search:**).</span></span> <span data-ttu-id="e609d-128">Les paires paramètre/valeur sont des arguments passés au moteur de recherche, comme décrit dans le tableau suivant, qui montre tous les paramètres possibles pour la syntaxe du protocole de recherche.</span><span class="sxs-lookup"><span data-stu-id="e609d-128">The parameter/value pairs are arguments passed to the Search engine, as described in the following table, which shows all of the possible parameters for the search protocol syntax.</span></span>



| <span data-ttu-id="e609d-129">Paramètre</span><span class="sxs-lookup"><span data-stu-id="e609d-129">Parameter</span></span>                                              | <span data-ttu-id="e609d-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="e609d-130">Value</span></span>                                                         | <span data-ttu-id="e609d-131">Description</span><span class="sxs-lookup"><span data-stu-id="e609d-131">Description</span></span>                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e609d-132">query</span><span class="sxs-lookup"><span data-stu-id="e609d-132">query</span></span>                                                  | <span data-ttu-id="e609d-133">Texte encodé URL</span><span class="sxs-lookup"><span data-stu-id="e609d-133">URL-encoded text</span></span>                                              | <span data-ttu-id="e609d-134">Texte de la requête entré par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e609d-134">The query text entered by the user.</span></span>                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="e609d-135">InputLocale</span><span class="sxs-lookup"><span data-stu-id="e609d-135">inputlocale</span></span>](search-protocol-localeidentifiers.md)   | <span data-ttu-id="e609d-136">Tout identificateur de code de langue (LCID) valide</span><span class="sxs-lookup"><span data-stu-id="e609d-136">Any valid language code identifier (LCID)</span></span>                     | <span data-ttu-id="e609d-137">LCID qui identifie la langue d’entrée de la requête.</span><span class="sxs-lookup"><span data-stu-id="e609d-137">The LCID that identifies the input language for the query.</span></span>                                                                                                                                                                                                                                     |
| [<span data-ttu-id="e609d-138">keywordlocale</span><span class="sxs-lookup"><span data-stu-id="e609d-138">keywordlocale</span></span>](search-protocol-localeidentifiers.md) | <span data-ttu-id="e609d-139">Tout LCID valide</span><span class="sxs-lookup"><span data-stu-id="e609d-139">Any valid LCID</span></span>                                                | <span data-ttu-id="e609d-140">LCID qui identifie la langue de la version internationale de l’indexeur.</span><span class="sxs-lookup"><span data-stu-id="e609d-140">The LCID that identifies the language of the international version of the Indexer.</span></span> <span data-ttu-id="e609d-141">La valeur par défaut est 1033 (en-US).</span><span class="sxs-lookup"><span data-stu-id="e609d-141">The default is 1033 (en-us).</span></span>                                                                                                                                                                                |
| [<span data-ttu-id="e609d-142">navigation</span><span class="sxs-lookup"><span data-stu-id="e609d-142">crumb</span></span>](search-protocol-crumb.md)                     | <span data-ttu-id="e609d-143">Instruction AQS</span><span class="sxs-lookup"><span data-stu-id="e609d-143">AQS statement</span></span>                                                 | <span data-ttu-id="e609d-144">Cet argument restreint l’étendue dans laquelle la recherche est effectuée.</span><span class="sxs-lookup"><span data-stu-id="e609d-144">This argument restricts the scope being searched.</span></span> <span data-ttu-id="e609d-145">Dans Windows Vista, le protocole de recherche prend en charge la AQS complète, ainsi qu’une implémentation spéciale pour un `location` argument.</span><span class="sxs-lookup"><span data-stu-id="e609d-145">In Windows Vista, the search protocol supports full AQS as well as a special implementation for a `location` argument.</span></span> <span data-ttu-id="e609d-146">Dans Windows XP, le protocole de recherche prend également en charge la AQS complète, à l’exception d’une implémentation spéciale de `kind` et `store` .</span><span class="sxs-lookup"><span data-stu-id="e609d-146">In Windows XP, the search protocol also supports full AQS, except for a special implementation of `kind` and `store`.</span></span> |
| [<span data-ttu-id="e609d-147">stockéesyntaxe</span><span class="sxs-lookup"><span data-stu-id="e609d-147">syntax</span></span>](search-protocol-syntaxargument.md)           | <span data-ttu-id="e609d-148">NQS, AQS (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="e609d-148">NQS, AQS (not case sensitive)</span></span>                                 | <span data-ttu-id="e609d-149">Syntaxe de requête à utiliser pour effectuer une recherche dans l’index : syntaxe de requête naturelle ou syntaxe de requête avancée (AQS).</span><span class="sxs-lookup"><span data-stu-id="e609d-149">The query syntax to use to search the index: either Natural Query Syntax or Advanced Query Syntax (AQS).</span></span> <span data-ttu-id="e609d-150">AQS est la valeur par défaut et est toujours supposé analysé et pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e609d-150">AQS is the default and is always assumed parsed and supported.</span></span>                                                                                                                        |
| [<span data-ttu-id="e609d-151">stackedby</span><span class="sxs-lookup"><span data-stu-id="e609d-151">stackedby</span></span>](search-protocol-stackedby.md)             | <span data-ttu-id="e609d-152">Toute propriété valide du système de propriétés</span><span class="sxs-lookup"><span data-stu-id="e609d-152">Any valid property from the property system</span></span>                   | <span data-ttu-id="e609d-153">Propriété qui spécifie la colonne par laquelle piler les résultats.</span><span class="sxs-lookup"><span data-stu-id="e609d-153">A property that specifies the column to stack results by.</span></span>                                                                                                                                                                                                                                      |
| [<span data-ttu-id="e609d-154">subquery</span><span class="sxs-lookup"><span data-stu-id="e609d-154">subquery</span></span>](search-protocol-subquery.md)               | <span data-ttu-id="e609d-155">Un chemin d’accès complètement spécifié pour un fichier de recherche enregistré ( \* . search-ms)</span><span class="sxs-lookup"><span data-stu-id="e609d-155">A fully specified path for a Saved Search file (\*.search-ms)</span></span> | <span data-ttu-id="e609d-156">Les résultats de la sous-requête sont utilisés en tant que source de la requête.</span><span class="sxs-lookup"><span data-stu-id="e609d-156">The results of the subquery are used as the source for the query.</span></span> <span data-ttu-id="e609d-157">Autrement dit, les termes de la requête sont recherchés par rapport aux résultats de la sous-requête.</span><span class="sxs-lookup"><span data-stu-id="e609d-157">That is, the query terms are searched for against the results of the subquery.</span></span>                                                                                                                                               |
| <span data-ttu-id="e609d-158">displayname</span><span class="sxs-lookup"><span data-stu-id="e609d-158">displayname</span></span>                                            | <span data-ttu-id="e609d-159">Chaîne encodée URL</span><span class="sxs-lookup"><span data-stu-id="e609d-159">URL-encoded string</span></span>                                            | <span data-ttu-id="e609d-160">Nom de la recherche actuelle.</span><span class="sxs-lookup"><span data-stu-id="e609d-160">The name of the current search.</span></span>                                                                                                                                                                                                                                                                |



 

## <a name="windows-vista-with-sp1-use-of-the-search-protocol"></a><span data-ttu-id="e609d-161">Windows Vista avec SP1 utilisation du protocole Search :</span><span class="sxs-lookup"><span data-stu-id="e609d-161">Windows Vista with SP1 use of the search: protocol</span></span>

<span data-ttu-id="e609d-162">Windows Vista avec SP1 possède plusieurs points d’entrée à partir desquels il appelle le protocole **Search :** .</span><span class="sxs-lookup"><span data-stu-id="e609d-162">Windows Vista with SP1 has several entry points from which it calls the **search:** protocol.</span></span> <span data-ttu-id="e609d-163">Ces points d’entrée sont présentés ci-dessous, ainsi que la syntaxe commune associée à chacun d’entre eux.</span><span class="sxs-lookup"><span data-stu-id="e609d-163">These entry points are outlined below as well as the common syntax associated with each.</span></span>



| <span data-ttu-id="e609d-164">Point d’entrée du protocole de recherche</span><span class="sxs-lookup"><span data-stu-id="e609d-164">Search protocol entry point</span></span> | <span data-ttu-id="e609d-165">Emplacement</span><span class="sxs-lookup"><span data-stu-id="e609d-165">Location</span></span>         | <span data-ttu-id="e609d-166">Requête appelée</span><span class="sxs-lookup"><span data-stu-id="e609d-166">Query called</span></span>                                                         |
|-----------------------------|------------------|----------------------------------------------------------------------|
| <span data-ttu-id="e609d-167">**Rechercher partout**</span><span class="sxs-lookup"><span data-stu-id="e609d-167">**Search Everywhere**</span></span>       | <span data-ttu-id="e609d-168">Menu **Démarrer**</span><span class="sxs-lookup"><span data-stu-id="e609d-168">**Start** menu</span></span>   | <span data-ttu-id="e609d-169">recherche : requête =<*terme de recherche*></span><span class="sxs-lookup"><span data-stu-id="e609d-169">search:query=<*Search Term*></span></span>                                   |
| <span data-ttu-id="e609d-170">**Rechercher partout**</span><span class="sxs-lookup"><span data-stu-id="e609d-170">**Search Everywhere**</span></span>       | <span data-ttu-id="e609d-171">Explorateur Windows</span><span class="sxs-lookup"><span data-stu-id="e609d-171">Windows Explorer</span></span> | <span data-ttu-id="e609d-172">recherche : requête =<*terme de recherche*>&de navigation = emplacement : *emplacement* du <></span><span class="sxs-lookup"><span data-stu-id="e609d-172">search:query=<*Search Term*>&crumb=location:<*LOCATION*></span></span> |
| <span data-ttu-id="e609d-173">Touche Windows + F</span><span class="sxs-lookup"><span data-stu-id="e609d-173">Windows logo key+F</span></span>          | <span data-ttu-id="e609d-174">N'importe où</span><span class="sxs-lookup"><span data-stu-id="e609d-174">Anywhere</span></span>         | <span data-ttu-id="e609d-175">recherche</span><span class="sxs-lookup"><span data-stu-id="e609d-175">search:</span></span>                                                              |
| <span data-ttu-id="e609d-176">Ctrl+F</span><span class="sxs-lookup"><span data-stu-id="e609d-176">CTRL+F</span></span>                      | <span data-ttu-id="e609d-177">Explorateur Windows</span><span class="sxs-lookup"><span data-stu-id="e609d-177">Windows Explorer</span></span> | <span data-ttu-id="e609d-178">recherche : requête =<*terme de recherche*>&de navigation = emplacement : *emplacement* du <></span><span class="sxs-lookup"><span data-stu-id="e609d-178">search:query=<*Search Term*>&crumb=location:<*LOCATION*></span></span> |
| <span data-ttu-id="e609d-179">F3</span><span class="sxs-lookup"><span data-stu-id="e609d-179">F3</span></span>                          | <span data-ttu-id="e609d-180">Menu **Démarrer**</span><span class="sxs-lookup"><span data-stu-id="e609d-180">**Start** menu</span></span>   | <span data-ttu-id="e609d-181">recherche</span><span class="sxs-lookup"><span data-stu-id="e609d-181">search:</span></span>                                                              |
| <span data-ttu-id="e609d-182">F3</span><span class="sxs-lookup"><span data-stu-id="e609d-182">F3</span></span>                          | <span data-ttu-id="e609d-183">Explorateur Windows</span><span class="sxs-lookup"><span data-stu-id="e609d-183">Windows Explorer</span></span> | <span data-ttu-id="e609d-184">recherche : requête =<*terme de recherche*>&de navigation = emplacement : *emplacement* du <></span><span class="sxs-lookup"><span data-stu-id="e609d-184">search:query=<*Search Term*>&crumb=location:<*LOCATION*></span></span> |



 

<span data-ttu-id="e609d-185">Les points d’entrée du protocole de recherche Windows Vista avec SP1 ne tirent pas parti de tous les paramètres possibles dans le protocole de recherche.</span><span class="sxs-lookup"><span data-stu-id="e609d-185">The Windows Vista with SP1 search protocol entry points do not take advantage of all the possible parameters in the search protocol.</span></span> <span data-ttu-id="e609d-186">Les applications qui sont uniquement concernées par le traitement des appels de protocole de recherche à partir de Windows Vista avec SP1 peuvent utiliser le tableau suivant comme guide sur le minimum qu’ils doivent implémenter.</span><span class="sxs-lookup"><span data-stu-id="e609d-186">Applications that are only concerned with handling search protocol calls from Windows Vista with SP1 can use the following table as a guide to the minimum they need to implement.</span></span>



| <span data-ttu-id="e609d-187">Paramètre</span><span class="sxs-lookup"><span data-stu-id="e609d-187">Parameter</span></span>                                              | <span data-ttu-id="e609d-188">Utilisé par Windows ?</span><span class="sxs-lookup"><span data-stu-id="e609d-188">Used by Windows?</span></span> | <span data-ttu-id="e609d-189">Comment Windows Vista avec SP1 l’utilise lors de l’appel de Search :</span><span class="sxs-lookup"><span data-stu-id="e609d-189">How Windows Vista with SP1 uses it when calling search:</span></span>                                                                                                                                                                                                                     |
|--------------------------------------------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e609d-190">query</span><span class="sxs-lookup"><span data-stu-id="e609d-190">query</span></span>                                                  | <span data-ttu-id="e609d-191">Oui</span><span class="sxs-lookup"><span data-stu-id="e609d-191">Yes</span></span>              | <span data-ttu-id="e609d-192">Texte de la requête entré par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e609d-192">The query text entered by the user.</span></span>                                                                                                                                                                                                                                         |
| [<span data-ttu-id="e609d-193">navigation</span><span class="sxs-lookup"><span data-stu-id="e609d-193">crumb</span></span>](search-protocol-crumb.md)                     | <span data-ttu-id="e609d-194">Oui</span><span class="sxs-lookup"><span data-stu-id="e609d-194">Yes</span></span>              | <span data-ttu-id="e609d-195">la [navigation](search-protocol-crumb.md) utilise l' `location` argument pour spécifier l’origine de la requête.</span><span class="sxs-lookup"><span data-stu-id="e609d-195">[crumb](search-protocol-crumb.md) uses the `location` argument to specify where the query came from.</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="e609d-196">subquery</span><span class="sxs-lookup"><span data-stu-id="e609d-196">subquery</span></span>](search-protocol-subquery.md)               | <span data-ttu-id="e609d-197">Oui</span><span class="sxs-lookup"><span data-stu-id="e609d-197">Yes</span></span>              | <span data-ttu-id="e609d-198">Les résultats de l’argument de [sous-requête](search-protocol-subquery.md) sont utilisés comme étendue des éléments à rechercher.</span><span class="sxs-lookup"><span data-stu-id="e609d-198">The results of the [Subquery](search-protocol-subquery.md) argument are used as the scope of items to search.</span></span> <span data-ttu-id="e609d-199">Cela est généralement utilisé si un utilisateur utilisait un fichier. search-ms pour effectuer une recherche, puis l’a appelé application Desktop Search par défaut à partir de cette recherche.</span><span class="sxs-lookup"><span data-stu-id="e609d-199">This would typically be used if a user was using a .search-ms file to search and then called the default desktop search application from within that search.</span></span> |
| [<span data-ttu-id="e609d-200">InputLocale</span><span class="sxs-lookup"><span data-stu-id="e609d-200">inputlocale</span></span>](search-protocol-localeidentifiers.md)   | <span data-ttu-id="e609d-201">Non</span><span class="sxs-lookup"><span data-stu-id="e609d-201">No</span></span>               | <span data-ttu-id="e609d-202">Pas utilisé pour l'instant.</span><span class="sxs-lookup"><span data-stu-id="e609d-202">Not currently used.</span></span>                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="e609d-203">keywordlocale</span><span class="sxs-lookup"><span data-stu-id="e609d-203">keywordlocale</span></span>](search-protocol-localeidentifiers.md) | <span data-ttu-id="e609d-204">Non</span><span class="sxs-lookup"><span data-stu-id="e609d-204">No</span></span>               | <span data-ttu-id="e609d-205">Pas utilisé pour l'instant.</span><span class="sxs-lookup"><span data-stu-id="e609d-205">Not currently used.</span></span>                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="e609d-206">stockéesyntaxe</span><span class="sxs-lookup"><span data-stu-id="e609d-206">syntax</span></span>](search-protocol-syntaxargument.md)           | <span data-ttu-id="e609d-207">Non</span><span class="sxs-lookup"><span data-stu-id="e609d-207">No</span></span>               | <span data-ttu-id="e609d-208">Pas utilisé pour l'instant.</span><span class="sxs-lookup"><span data-stu-id="e609d-208">Not currently used.</span></span>                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="e609d-209">stackedby</span><span class="sxs-lookup"><span data-stu-id="e609d-209">stackedby</span></span>](search-protocol-stackedby.md)             | <span data-ttu-id="e609d-210">Non</span><span class="sxs-lookup"><span data-stu-id="e609d-210">No</span></span>               | <span data-ttu-id="e609d-211">Pas utilisé pour l'instant.</span><span class="sxs-lookup"><span data-stu-id="e609d-211">Not currently used.</span></span>                                                                                                                                                                                                                                                         |
| <span data-ttu-id="e609d-212">displayname</span><span class="sxs-lookup"><span data-stu-id="e609d-212">displayname</span></span>                                            | <span data-ttu-id="e609d-213">Non</span><span class="sxs-lookup"><span data-stu-id="e609d-213">No</span></span>               | <span data-ttu-id="e609d-214">Pas utilisé pour l'instant.</span><span class="sxs-lookup"><span data-stu-id="e609d-214">Not currently used.</span></span>                                                                                                                                                                                                                                                         |



 

## <a name="examples"></a><span data-ttu-id="e609d-215">Exemples</span><span class="sxs-lookup"><span data-stu-id="e609d-215">Examples</span></span>

<span data-ttu-id="e609d-216">Si un utilisateur entre « Microsoft » dans le menu **Démarrer** et clique sur **Rechercher partout**, l’appel de protocole de recherche qui en résulte est effectué :</span><span class="sxs-lookup"><span data-stu-id="e609d-216">If a user enters "Microsoft" in the **Start** menu and clicks **Search Everywhere**, the resulting search protocol call is made:</span></span>


```C++
search:query=microsoft&
```



<span data-ttu-id="e609d-217">Si un utilisateur entre « Seattle » dans l’Explorateur Windows dans C : \\ mondossier, puis clique sur **Rechercher partout**, l’appel suivant est effectué, en utilisant des caractères d’échappement pour «  : » et « \\ » :</span><span class="sxs-lookup"><span data-stu-id="e609d-217">If a user enters "Seattle" in Windows Explorer within C:\\MyFolder and then clicks **Search Everywhere**, the following call is made, using escape characters for ':' and '\\':</span></span>


```C++
search:query=seattle&crumb=location:C%3A%5CMyFolder
```



## <a name="registering-the-application-that-handles-the-protocol"></a><span data-ttu-id="e609d-218">Inscription de l’application qui gère le protocole</span><span class="sxs-lookup"><span data-stu-id="e609d-218">Registering the Application that Handles the Protocol</span></span>

<span data-ttu-id="e609d-219">Étant donné que plusieurs applications peuvent rivaliser pour le protocole de recherche, vous devez inscrire votre application auprès de la fonctionnalité [programmes par défaut](default-programs.md) pendant l’installation pour permettre à l’utilisateur de configurer plus facilement la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="e609d-219">Because multiple applications can contend for the search protocol, you should register your application with the [Default Programs](default-programs.md) feature during installation to enable the user to configure the default more easily.</span></span> <span data-ttu-id="e609d-220">En plus des procédures d’installation normalement recommandées sous Windows XP, une application Windows Vista doit s’inscrire auprès de la fonctionnalité programmes par défaut afin que l’application et les utilisateurs puissent configurer les valeurs par défaut en toute transparence.</span><span class="sxs-lookup"><span data-stu-id="e609d-220">In addition to the installation procedures normally practiced under Windows XP, a Windows Vista-based application must register with the Default Programs feature so that the application and users can seamlessly configure defaults.</span></span>

<span data-ttu-id="e609d-221">Après l’installation des fichiers binaires nécessaires sur l’ordinateur de l’utilisateur, votre routine d’installation doit effectuer les tâches générales suivantes :</span><span class="sxs-lookup"><span data-stu-id="e609d-221">After installing the necessary binary files on the user's computer, your installation routine should complete these general tasks:</span></span>

1.  <span data-ttu-id="e609d-222">Écrivez les ProgID sur la **\_ \_ machine locale HKEY**, comme décrit ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="e609d-222">Write ProgIDs to **HKEY\_LOCAL\_MACHINE**, as described below.</span></span> <span data-ttu-id="e609d-223">Notez que les applications doivent créer des ProgID spécifiques à l’application pour le protocole de recherche.</span><span class="sxs-lookup"><span data-stu-id="e609d-223">Note that applications must create application-specific ProgIDs for the search protocol.</span></span>
2.  <span data-ttu-id="e609d-224">Demandez une association de protocole de recherche au niveau de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="e609d-224">Claim machine-level search protocol association.</span></span>
3.  <span data-ttu-id="e609d-225">Enregistrez l’application avec les [programmes par défaut](default-programs.md), comme expliqué dans la rubrique [inscription d’une application pour une utilisation avec les programmes par défaut](default-programs.md), en tant que contendeur pour le protocole de recherche.</span><span class="sxs-lookup"><span data-stu-id="e609d-225">Register the application with [Default Programs](default-programs.md), as explained in [Registering an Application for Use with Default Programs](default-programs.md), as a contender for the search protocol.</span></span>

### <a name="registry-entries"></a><span data-ttu-id="e609d-226">Entrées de Registre</span><span class="sxs-lookup"><span data-stu-id="e609d-226">Registry Entries</span></span>

<span data-ttu-id="e609d-227">Voici des exemples d’entrées de Registre requises pour une application de recherche de bureau fictive, contoso Search.</span><span class="sxs-lookup"><span data-stu-id="e609d-227">The following are examples of the required registry entries for a fictional desktop search application, Contoso Search.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         contoso-search
            URL Protocol = ""
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         contoso-search
            DefaultIcon
               (Default) = %ProgramFiles%\Contoso\Search\contososearch.exe,-7
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         contoso-search
            shell
               open
                  command
                     (Default) = %ProgramFiles%\Contoso\Search\contososearch.exe %1
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      RegisteredApplications
         Contoso Search = "Software\\Contoso\\Search\\Capabilities"
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Contoso
         Search
            Capabilities
               ApplicationName = "Contoso Search Test App"
               ApplicationDescription = "Contoso search is a great new desktop search application"
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Contoso
         Search
            Capabilities
               UrlAssociations
                  search = "contoso-search"
```

## <a name="related-topics"></a><span data-ttu-id="e609d-228">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e609d-228">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e609d-229">Syntaxe de requête avancée</span><span class="sxs-lookup"><span data-stu-id="e609d-229">Advanced Query Syntax</span></span>](../search/-search-3x-advancedquerysyntax.md)
</dt> <dt>

[<span data-ttu-id="e609d-230">Programmes par défaut</span><span class="sxs-lookup"><span data-stu-id="e609d-230">Default Programs</span></span>](default-programs.md)
</dt> </dl>

 

 
