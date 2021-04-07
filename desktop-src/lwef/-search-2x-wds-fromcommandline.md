---
title: Appel de WDS à partir de la ligne de commande
description: Vous pouvez lancer l’interface utilisateur de Microsoft Windows Desktop Search (WDS) avec un filtre, une banque et une requête spécifiques à partir d’une autre application ou d’une page Web qui utilise l’objet d’assistance du navigateur (BHO) à l’aide de la syntaxe de ligne de commande windowssearch.exe.
ms.assetid: fd62f7c9-08a9-4e05-b0bc-e2215cfff59e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efae7aebc13f578e9c5c32542b451d3600a93a2b
ms.sourcegitcommit: b9a94cea8f83153214af4c09509e1cc61a1bb616
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2020
ms.locfileid: "103724018"
---
# <a name="calling-wds-from-the-command-line"></a><span data-ttu-id="502f3-103">Appel de WDS à partir de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="502f3-103">Calling WDS from the Command Line</span></span>

> [!NOTE]
> <span data-ttu-id="502f3-104">Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="502f3-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="502f3-105">Dans les versions ultérieures, utilisez [Windows Search](../search/-search-3x-wds-overview.md) à la place.</span><span class="sxs-lookup"><span data-stu-id="502f3-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="502f3-106">Vous pouvez lancer l’interface utilisateur de Microsoft Windows Desktop Search (WDS) avec un filtre, une banque et une requête spécifiques à partir d’une autre application ou d’une page Web qui utilise l’objet d’assistance du navigateur (BHO) à l’aide de la syntaxe de ligne de commande windowssearch.exe.</span><span class="sxs-lookup"><span data-stu-id="502f3-106">You can launch the Microsoft Windows Desktop Search (WDS) user interface with a specific filter, store, and query from another application or a webpage that uses the Browser Helper Object (BHO) by using the windowssearch.exe command line syntax.</span></span> <span data-ttu-id="502f3-107">Lors de l’appel de WDS à partir de la ligne de commande, aucune information sur les actions ou la sélection de l’utilisateur dans la fenêtre WDS n’est retournée à l’application ou à la page Web appelante.</span><span class="sxs-lookup"><span data-stu-id="502f3-107">When calling WDS from the command line, no information about the user's actions or selection in the WDS window is returned to the calling application or webpage.</span></span>

<span data-ttu-id="502f3-108">Le chemin d’installation de WDS est spécifié dans le paramètre de Registre InstallDir sous HKEY_LOCAL_MACHINE \\ Software \\ Microsoft \\ Windows Desktop Search.</span><span class="sxs-lookup"><span data-stu-id="502f3-108">The WDS installation path is specified in the InstallDir registry setting under HKEY_LOCAL_MACHINE\\Software\\Microsoft\\Windows Desktop Search.</span></span> <span data-ttu-id="502f3-109">Le chemin d’accès par défaut dans lequel windowssearch.exe est installé est Program Files \\ Windows Desktop Search.</span><span class="sxs-lookup"><span data-stu-id="502f3-109">The default path that windowssearch.exe is installed to is Program Files\\Windows Desktop Search.</span></span>

## <a name="command-line-syntax"></a><span data-ttu-id="502f3-110">Syntaxe de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="502f3-110">Command Line Syntax</span></span>

<span data-ttu-id="502f3-111">La syntaxe suivante s’applique à l’interface de ligne de commande de Windows Desktop Search 2. x.</span><span class="sxs-lookup"><span data-stu-id="502f3-111">The following syntax applies to the Windows Desktop Search 2.x command-line interface.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="502f3-112">Options</span><span class="sxs-lookup"><span data-stu-id="502f3-112">Options</span></span></th>
<th><span data-ttu-id="502f3-113">Paramètre</span><span class="sxs-lookup"><span data-stu-id="502f3-113">Parameter</span></span></th>
<th><span data-ttu-id="502f3-114">Signification</span><span class="sxs-lookup"><span data-stu-id="502f3-114">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="502f3-115">/startup</span><span class="sxs-lookup"><span data-stu-id="502f3-115">/startup</span></span></td>

<td><span data-ttu-id="502f3-116">Initialise Windows Desktop Search</span><span class="sxs-lookup"><span data-stu-id="502f3-116">Initializes Windows Desktop Search</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="502f3-117">/indexnow</span><span class="sxs-lookup"><span data-stu-id="502f3-117">/indexnow</span></span></td>

<td><span data-ttu-id="502f3-118">Désactive l’indexation et analyse à nouveau tous les emplacements d’index</span><span class="sxs-lookup"><span data-stu-id="502f3-118">Turns off indexing back-off and rescans all index locations</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="502f3-119">/showstatus</span><span class="sxs-lookup"><span data-stu-id="502f3-119">/showstatus</span></span></td>

<td><span data-ttu-id="502f3-120">Affiche la fenêtre État de l’indexation</span><span class="sxs-lookup"><span data-stu-id="502f3-120">Shows the indexing status window</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="502f3-121">/launchsearchwindow ou/URL</span><span class="sxs-lookup"><span data-stu-id="502f3-121">/launchsearchwindow or /url</span></span></td>

<td><span data-ttu-id="502f3-122">Ouvre une fenêtre WDS avec une requête vide</span><span class="sxs-lookup"><span data-stu-id="502f3-122">Opens a WDS window with an empty query</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="502f3-123">/url</span><span class="sxs-lookup"><span data-stu-id="502f3-123">/url</span></span></td>
<td><span data-ttu-id="502f3-124">recherche : [Store | Show | requête] chaîne de requête</span><span class="sxs-lookup"><span data-stu-id="502f3-124">search:[store|show|query] query string</span></span></td>
<td><span data-ttu-id="502f3-125">Ouvre une fenêtre WDS avec une requête et un filtre en fonction des paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="502f3-125">Opens a WDS window with a query and filter based on the following parameters:</span></span>
<ul>
<li><p><span data-ttu-id="502f3-126">Store : spécifie la source de données à interroger : Files, Outlook, OutlookExpress.</span><span class="sxs-lookup"><span data-stu-id="502f3-126">store - Specifies the data source to query: files, outlook, outlookexpress.</span></span> <span data-ttu-id="502f3-127">S’il n’est pas spécifié, la recherche est effectuée dans tous les magasins.</span><span class="sxs-lookup"><span data-stu-id="502f3-127">If not specified all stores will be searched.</span></span> <br/></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="502f3-128">Bien que la syntaxe de requête avancée prenne en charge le référencement de Microsoft Outlook comme « OE », le paramètre Store sur la ligne de commande doit être « OutlookExpress ».</span><span class="sxs-lookup"><span data-stu-id="502f3-128">While Advanced Query Syntax supports referencing Microsoft Outlook as 'oe', the store parameter on the command line must be 'outlookexpress'.</span></span>
</blockquote>
<p><br/></p></li>
<li><p><span data-ttu-id="502f3-129">Show : spécifie le type de résultats perçus à retourner.</span><span class="sxs-lookup"><span data-stu-id="502f3-129">show - Specifies which perceived type of results to return.</span></span> <span data-ttu-id="502f3-130">Pour obtenir la liste complète des types, consultez <a href="-search-2x-wds-perceivedtype.md">types perçus</a> .</span><span class="sxs-lookup"><span data-stu-id="502f3-130">See <a href="-search-2x-wds-perceivedtype.md">Perceived Types</a> for a complete list of types.</span></span> <span data-ttu-id="502f3-131">S’il n’est pas spécifié, tous les types sont retournés.</span><span class="sxs-lookup"><span data-stu-id="502f3-131">If not specified, all types will be returned.</span></span> <br/></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="502f3-132">Il existe trois différences entre les valeurs de type perçues et les valeurs pour Show.</span><span class="sxs-lookup"><span data-stu-id="502f3-132">There are three differences between the perceived type values and the values for show.</span></span> <span data-ttu-id="502f3-133">Pour <code>show</code> , utilisez’documents’au lieu de’doc', 'images’au lieu de’pics’et’textdocuments’au lieu de’text'.</span><span class="sxs-lookup"><span data-stu-id="502f3-133">For <code>show</code>, use 'documents' instead of 'doc', 'pictures' instead of 'pics', and 'textdocuments' instead of 'text'.</span></span>
</blockquote>
<p><br/></p></li>
<li><span data-ttu-id="502f3-134">requête : spécifie les critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="502f3-134">query - Specifies the search criteria.</span></span> <span data-ttu-id="502f3-135">Cette valeur prend en charge les paramètres de <a href="-search-2x-wds-aqsreference.md">syntaxe de requête avancée</a> pour affiner les résultats.</span><span class="sxs-lookup"><span data-stu-id="502f3-135">This value supports <a href="-search-2x-wds-aqsreference.md">Advanced Query Syntax</a> parameters to refine the results.</span></span> <span data-ttu-id="502f3-136">Le paramètre de requête doit être le dernier paramètre de l’URL.</span><span class="sxs-lookup"><span data-stu-id="502f3-136">The query parameter must be the last parameter in the URL.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="example"></a><span data-ttu-id="502f3-137">Exemple</span><span class="sxs-lookup"><span data-stu-id="502f3-137">Example</span></span>

<span data-ttu-id="502f3-138">Par exemple, pour rechercher dans tous les fichiers les images correspondant au critère « papier peint », utilisez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="502f3-138">For example, to search all files for pictures matching the criteria 'wallpaper' use the following command:</span></span>

`WindowsSearch.exe /url search:store=files&show=pictures&query=wallpaper`

## <a name="related-topics"></a><span data-ttu-id="502f3-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="502f3-139">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="502f3-140">**Informations de référence**</span><span class="sxs-lookup"><span data-stu-id="502f3-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="502f3-141">Syntaxe de requête avancée</span><span class="sxs-lookup"><span data-stu-id="502f3-141">Advanced Query Syntax</span></span>](-search-2x-wds-aqsreference.md)
</dt> <dt>

[<span data-ttu-id="502f3-142">Types perçus</span><span class="sxs-lookup"><span data-stu-id="502f3-142">Perceived Types</span></span>](-search-2x-wds-perceivedtype.md)
</dt> <dt>

[<span data-ttu-id="502f3-143">Appel de WDS à partir de pages Web</span><span class="sxs-lookup"><span data-stu-id="502f3-143">Calling WDS from Web Pages</span></span>](-search-2x-wds-browserhelpobject.md)
</dt> </dl>

 

 





