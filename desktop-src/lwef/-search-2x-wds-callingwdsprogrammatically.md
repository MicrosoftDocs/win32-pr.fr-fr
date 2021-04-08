---
title: Appeler WDS par programmation
description: Microsoft Windows Desktop Search (WDS) 2. x peut être interrogé par programme à l’aide des méthodes ExecuteQuery et ExecuteSQLQuery dans l’interface ISearchDesktop.
ms.assetid: 38426f63-2039-410e-8c70-ebd9fc269d74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dc76264b7939311273fbda334292dfb255cde8f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103727052"
---
# <a name="calling-wds-programmatically"></a><span data-ttu-id="083e6-103">Appeler WDS par programmation</span><span class="sxs-lookup"><span data-stu-id="083e6-103">Calling WDS Programmatically</span></span>

> [!NOTE]
> <span data-ttu-id="083e6-104">Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="083e6-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="083e6-105">Dans les versions ultérieures, utilisez [Windows Search](../search/-search-3x-wds-overview.md) à la place.</span><span class="sxs-lookup"><span data-stu-id="083e6-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="083e6-106">Microsoft Windows Desktop Search (WDS) 2. x peut être interrogé par programme à l’aide des méthodes **ExecuteQuery** et **ExecuteSQLQuery** dans l’interface [**ISearchDesktop**](/previous-versions//aa965729(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="083e6-106">Microsoft Windows Desktop Search (WDS) 2.x can be queried programmatically using the **ExecuteQuery** and **ExecuteSQLQuery** methods in the [**ISearchDesktop**](/previous-versions//aa965729(v=vs.85)) interface.</span></span> <span data-ttu-id="083e6-107">La méthode **ExecuteQuery** retourne un jeu d’enregistrements à partir de l’index en fonction du texte de la requête, des colonnes et des restrictions passées en tant que paramètres.</span><span class="sxs-lookup"><span data-stu-id="083e6-107">The **ExecuteQuery** method returns a record set from the index based on the query text, columns, and restrictions passed as parameters.</span></span> <span data-ttu-id="083e6-108">La méthode **ExecuteSQLQuery** retourne également un jeu d’enregistrements de résultats, mais requiert la transmission de la commande exacte langage SQL (SQL).</span><span class="sxs-lookup"><span data-stu-id="083e6-108">The **ExecuteSQLQuery** method also returns a record set of results but requires the exact Structured Query Language (SQL) command to be passed in.</span></span> <span data-ttu-id="083e6-109">**ExecuteQuery** doit être utilisé dans la plupart des scénarios.</span><span class="sxs-lookup"><span data-stu-id="083e6-109">**ExecuteQuery** should be used in most scenarios.</span></span>

## <a name="regular-queries"></a><span data-ttu-id="083e6-110">Requêtes régulières</span><span class="sxs-lookup"><span data-stu-id="083e6-110">Regular Queries</span></span>

<span data-ttu-id="083e6-111">Les requêtes régulières sont celles qui sont tapées dans la zone d’entrée WDS par l’utilisateur, y compris la [syntaxe de requête avancée](-search-2x-wds-aqsreference.md).</span><span class="sxs-lookup"><span data-stu-id="083e6-111">Regular queries are those typed into the WDS input box by the user including all [Advanced Query Syntax](-search-2x-wds-aqsreference.md).</span></span> <span data-ttu-id="083e6-112">La requête est transmise à **ExecuteQuery** avec les colonnes de [schéma](-search-2x-wds-schematable.md) WDS 2. x à retourner, la colonne et l’ordre de tri des résultats et toutes les clauses pour limiter les résultats par.</span><span class="sxs-lookup"><span data-stu-id="083e6-112">The query is passed to **ExecuteQuery** along with the WDS 2.x [schema](-search-2x-wds-schematable.md) columns to return, the column and order to sort results, and any clauses to restrict results by.</span></span>

<span data-ttu-id="083e6-113">La méthode se présente sous la forme :</span><span class="sxs-lookup"><span data-stu-id="083e6-113">The method has the form:</span></span>

`HRESULT ExecuteQuery(LPCWSTR lpcwstrQuery, LPCWSTR lpcwstrColumn, LPCWSTR lpcwstrSort, LPCWSTR lpcwstrRestriction, Recordset **ppiRs);`



| <span data-ttu-id="083e6-114">Sens</span><span class="sxs-lookup"><span data-stu-id="083e6-114">Direction</span></span> | <span data-ttu-id="083e6-115">Variable</span><span class="sxs-lookup"><span data-stu-id="083e6-115">Variable</span></span>           | <span data-ttu-id="083e6-116">Description</span><span class="sxs-lookup"><span data-stu-id="083e6-116">Description</span></span>                                                                                                                                                                                   |
|-----------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="083e6-117">Dans</span><span class="sxs-lookup"><span data-stu-id="083e6-117">In</span></span>        | <span data-ttu-id="083e6-118">lpcwstrQuery</span><span class="sxs-lookup"><span data-stu-id="083e6-118">lpcwstrQuery</span></span>       | <span data-ttu-id="083e6-119">Texte de la requête.</span><span class="sxs-lookup"><span data-stu-id="083e6-119">The query text.</span></span> <span data-ttu-id="083e6-120">Cette requête est identique à une requête tapée dans la zone de texte Rechercher de l’interface utilisateur de Windows Desktop Search.</span><span class="sxs-lookup"><span data-stu-id="083e6-120">This query is the same as a query typed into the search text box in the Windows Desktop Search user interface.</span></span> <br/> <span data-ttu-id="083e6-121">Par exemple : `"from:Zara dinner plans"`</span><span class="sxs-lookup"><span data-stu-id="083e6-121">For example: `"from:Zara dinner plans"`</span></span><br/> |
| <span data-ttu-id="083e6-122">Dans</span><span class="sxs-lookup"><span data-stu-id="083e6-122">In</span></span>        | <span data-ttu-id="083e6-123">lpcwstrColumn</span><span class="sxs-lookup"><span data-stu-id="083e6-123">lpcwstrColumn</span></span>      | <span data-ttu-id="083e6-124">Colonnes à inclure, séparées par des virgules.</span><span class="sxs-lookup"><span data-stu-id="083e6-124">The columns to include, separated by commas.</span></span> <br/> <span data-ttu-id="083e6-125">Par exemple : `"DocTitle, Url"`</span><span class="sxs-lookup"><span data-stu-id="083e6-125">For example: `"DocTitle, Url"`</span></span><br/>                                                                                            |
| <span data-ttu-id="083e6-126">Dans</span><span class="sxs-lookup"><span data-stu-id="083e6-126">In</span></span>        | <span data-ttu-id="083e6-127">lpcwstrSort</span><span class="sxs-lookup"><span data-stu-id="083e6-127">lpcwstrSort</span></span>        | <span data-ttu-id="083e6-128">Colonne de remplacement dans laquelle effectuer le tri, suivi de ASC pour l’ordre croissant ou DESC pour l’ordre décroissant.</span><span class="sxs-lookup"><span data-stu-id="083e6-128">The Override Column to sort by followed by ASC for ascending or DESC for descending.</span></span> <br/> <span data-ttu-id="083e6-129">Par exemple : `"LastAuthor DESC"`</span><span class="sxs-lookup"><span data-stu-id="083e6-129">For example: `"LastAuthor DESC"`</span></span><br/>                                                  |
| <span data-ttu-id="083e6-130">Dans</span><span class="sxs-lookup"><span data-stu-id="083e6-130">In</span></span>        | <span data-ttu-id="083e6-131">lpcwstrRestriction</span><span class="sxs-lookup"><span data-stu-id="083e6-131">lpcwstrRestriction</span></span> | <span data-ttu-id="083e6-132">Restrictions relatives à l’ajout de clauses WHERE dans la recherche Windows Desktop Select.</span><span class="sxs-lookup"><span data-stu-id="083e6-132">Restrictions to append through WHERE clauses in the Windows Desktop Search select.</span></span> <br/> <span data-ttu-id="083e6-133">Par exemple : `"Contains(LastAuthor, 'Bill')"`</span><span class="sxs-lookup"><span data-stu-id="083e6-133">For example: `"Contains(LastAuthor, 'Bill')"`</span></span><br/>                                       |
| <span data-ttu-id="083e6-134">Sortie</span><span class="sxs-lookup"><span data-stu-id="083e6-134">Out</span></span>       | <span data-ttu-id="083e6-135">ppiRs</span><span class="sxs-lookup"><span data-stu-id="083e6-135">ppiRs</span></span>              | <span data-ttu-id="083e6-136">Jeu d’enregistrements résultant</span><span class="sxs-lookup"><span data-stu-id="083e6-136">The resulting record set</span></span><br/>                                                                                                                                                           |



 

## <a name="sql-queries"></a><span data-ttu-id="083e6-137">Requêtes SQL</span><span class="sxs-lookup"><span data-stu-id="083e6-137">SQL Queries</span></span>

<span data-ttu-id="083e6-138">La méthode **ISearchDesktop.ExecuteSQLQuery** est utilisée pour envoyer des requêtes de base de données WDS directes.</span><span class="sxs-lookup"><span data-stu-id="083e6-138">The **ISearchDesktop.ExecuteSQLQuery** method is used to send direct WDS database queries.</span></span> <span data-ttu-id="083e6-139">La syntaxe des requêtes est similaire à celle utilisée pour SharePoint Server, ainsi que la possibilité d’utiliser des clauses GROUP BY de style Monarch.</span><span class="sxs-lookup"><span data-stu-id="083e6-139">The syntax for the queries is similar to that used for SharePoint Server, along with the ability to use Monarch-style SQL GROUP BY clauses.</span></span> <span data-ttu-id="083e6-140">La requête est exécutée sur l’index exactement telle qu’elle est transmise sans traitement supplémentaire de la syntaxe de requête avancée comme le fait l’API ExecuteQuery.</span><span class="sxs-lookup"><span data-stu-id="083e6-140">The query is executed against the index exactly as it is passed in with no additional processing of Advanced Query Syntax as the ExecuteQuery API does.</span></span>

https://msdn.microsoft.com/library/default.asp?url=/library/spssdk/html/\_tahoe\_search\_sql\_syntax.asp

<span data-ttu-id="083e6-141">La méthode se présente sous la forme :</span><span class="sxs-lookup"><span data-stu-id="083e6-141">The method has the form:</span></span>

`HRESULT ExecuteSQLQuery(LPCWSTR lpcwstrSQL, Recordset **ppiRs);`



| <span data-ttu-id="083e6-142">Sens</span><span class="sxs-lookup"><span data-stu-id="083e6-142">Direction</span></span> | <span data-ttu-id="083e6-143">Variable</span><span class="sxs-lookup"><span data-stu-id="083e6-143">Variable</span></span>   | <span data-ttu-id="083e6-144">Description</span><span class="sxs-lookup"><span data-stu-id="083e6-144">Description</span></span>                                    |
|-----------|------------|------------------------------------------------|
| <span data-ttu-id="083e6-145">Dans</span><span class="sxs-lookup"><span data-stu-id="083e6-145">In</span></span>        | <span data-ttu-id="083e6-146">lpcwstrSQL</span><span class="sxs-lookup"><span data-stu-id="083e6-146">lpcwstrSQL</span></span> | <span data-ttu-id="083e6-147">Requête SQL à exécuter sur l’index WDS</span><span class="sxs-lookup"><span data-stu-id="083e6-147">The SQL query to execute against the WDS index</span></span> |
| <span data-ttu-id="083e6-148">Sortie</span><span class="sxs-lookup"><span data-stu-id="083e6-148">Out</span></span>       | <span data-ttu-id="083e6-149">ppiRs</span><span class="sxs-lookup"><span data-stu-id="083e6-149">ppiRs</span></span>      | <span data-ttu-id="083e6-150">Jeu d’enregistrements résultant</span><span class="sxs-lookup"><span data-stu-id="083e6-150">The resulting record set</span></span>                       |



 

<span data-ttu-id="083e6-151">Ressources :</span><span class="sxs-lookup"><span data-stu-id="083e6-151">Resources:</span></span>

-   <span data-ttu-id="083e6-152">Fichiers de prise en charge pour l’interface ISearchDesktop : https://addins.msn.com/support/WDSSDK.zip</span><span class="sxs-lookup"><span data-stu-id="083e6-152">Support files for the ISearchDesktop interface: https://addins.msn.com/support/WDSSDK.zip</span></span>
-   <span data-ttu-id="083e6-153">Exemple C# ISearchDesktop : https://addins.msn.com/support/WDSSample.zip</span><span class="sxs-lookup"><span data-stu-id="083e6-153">ISearchDesktop C# Sample: https://addins.msn.com/support/WDSSample.zip</span></span>

## <a name="sample-c-code"></a><span data-ttu-id="083e6-154">Exemple de code C++</span><span class="sxs-lookup"><span data-stu-id="083e6-154">Sample C++ Code</span></span>

> [!Note]
>
> <span data-ttu-id="083e6-155">CE CODE ET CES INFORMATIONS SONT FOURNIS « EN L’ÉTAT », SANS GARANTIE D’AUCUNE SORTE, EXPRESSE OU IMPLICITE, Y COMPRIS, MAIS SANS S’Y LIMITER, LES GARANTIES IMPLICITES DE QUALITÉ MARCHANDE ET/OU D’ADÉQUATION À UN USAGE PARTICULIER.</span><span class="sxs-lookup"><span data-stu-id="083e6-155">THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A PARTICULAR PURPOSE.</span></span>
>
> <span data-ttu-id="083e6-156">Copyright (C) Microsoft.</span><span class="sxs-lookup"><span data-stu-id="083e6-156">Copyright (C) Microsoft.</span></span> <span data-ttu-id="083e6-157">Tous droits réservés.</span><span class="sxs-lookup"><span data-stu-id="083e6-157">All rights reserved.</span></span>

 


```
#include <stdio.h>
#include <wchar.h>
#include <windows.h>
#include <msnldl.h>
#include <adoint.h>
#include <adoguids.h>
 
HRESULT TestExecuteQuery(ISearchDesktop *psd)
{
ADORecordset *prs = NULL;
 
    HRESULT hr;
 
    hr = psd->ExecuteQuery( L"ToName:Moishe", 
                            L"DocTitle,DocFormat", 
                            L"PrimaryDate DESC", 
                            L"Contains('text')", 
                            &prs);
    if (SUCCEEDED(hr))
        prs->Release();
    return hr;
}
 
HRESULT TestExecuteSQLQuery(ISearchDesktop *psd)
{
    ADORecordset *prs = NULL;
    HRESULT hr;

    hr = psd->ExecuteSQLQuery(L"select DocTitle from MyIndex..Scope() where contains('text')", &prs);

    if (SUCCEEDED(hr))
      prs->Release();
    return hr;
}
 
extern "C" int __cdecl wmain( int argc, WCHAR * argv[] )
{
    SCODE sc = CoInitialize(0);
    ISearchDesktop *psd = NULL;
    HRESULT         hr;
     
    if (SUCCEEDED(hr = CoCreateInstance(__uuidof(SearchDesktop), NULL, CLSCTX_INPROC_SERVER, 
                                        __uuidof(ISearchDesktop), (void**)&psd)))
          {
             TestExecuteSQLQuery(psd);
             TestExecuteQuery(psd);
             psd->Release();
          }
          CoUninitialize();
}
```



## <a name="related-topics"></a><span data-ttu-id="083e6-158">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="083e6-158">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="083e6-159">**Informations de référence**</span><span class="sxs-lookup"><span data-stu-id="083e6-159">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="083e6-160">Syntaxe de requête avancée</span><span class="sxs-lookup"><span data-stu-id="083e6-160">Advanced Query Syntax</span></span>](-search-2x-wds-aqsreference.md)
</dt> <dt>

[<span data-ttu-id="083e6-161">Types perçus</span><span class="sxs-lookup"><span data-stu-id="083e6-161">Perceived Types</span></span>](-search-2x-wds-perceivedtype.md)
</dt> <dt>

[<span data-ttu-id="083e6-162">Appel de WDS à partir de pages Web</span><span class="sxs-lookup"><span data-stu-id="083e6-162">Calling WDS from Web Pages</span></span>](-search-2x-wds-browserhelpobject.md)
</dt> </dl>

 

