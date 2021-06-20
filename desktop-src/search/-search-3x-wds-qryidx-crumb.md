---
description: Découvrez comment utiliser l’argument de navigation dans Windows Search comme moyen de contrôler l’étendue d’une recherche.
ms.assetid: b0b974ae-0573-45e4-888e-07138604b62e
title: Argument de navigation (Windows Search)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f56287c7182c0cf370250d53075a1c951ddf28b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403732"
---
# <a name="crumb-argument-windows-search"></a><span data-ttu-id="d75e7-103">Argument de navigation (Windows Search)</span><span class="sxs-lookup"><span data-stu-id="d75e7-103">CRUMB Argument (Windows Search)</span></span>

<span data-ttu-id="d75e7-104">L' `crumb` argument prend en charge les instructions de syntaxe de requête avancée (AQS) complète et est particulièrement utile pour contrôler l’étendue d’une recherche.</span><span class="sxs-lookup"><span data-stu-id="d75e7-104">The `crumb` argument supports full Advanced Query Syntax (AQS) statements and is especially useful as a means of controlling the scope of a search.</span></span> <span data-ttu-id="d75e7-105">En plus de AQS ements, l' `crumb` argument peut accepter un `location` paramètre spécial sur Windows Vista et `kind` les `store` paramètres et sur XP, comme décrit plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="d75e7-105">In addition to AQS ements, the `crumb` argument can take a special `location` parameter on Windows Vista and `kind` and `store` parameters on XP, as described later in this topic.</span></span>

<span data-ttu-id="d75e7-106">Cette rubrique est organisée comme suit :</span><span class="sxs-lookup"><span data-stu-id="d75e7-106">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="d75e7-107">Syntaxe de la navigation</span><span class="sxs-lookup"><span data-stu-id="d75e7-107">Crumb Syntax</span></span>](#crumb-syntax)
    -   [<span data-ttu-id="d75e7-108">Exemples généraux</span><span class="sxs-lookup"><span data-stu-id="d75e7-108">General Examples</span></span>](#general-examples)
-   [<span data-ttu-id="d75e7-109">Utilisation de la navigation avec Vista (emplacement)</span><span class="sxs-lookup"><span data-stu-id="d75e7-109">Using crumb with Vista (location)</span></span>](#using-crumb-with-vista-location)
    -   [<span data-ttu-id="d75e7-110">Exemples Vista</span><span class="sxs-lookup"><span data-stu-id="d75e7-110">Vista Examples</span></span>](#vista-examples)
    -   [<span data-ttu-id="d75e7-111">Constantes pour les dossiers communs</span><span class="sxs-lookup"><span data-stu-id="d75e7-111">Constants for Common Folders</span></span>](#constants-for-common-folders)
-   [<span data-ttu-id="d75e7-112">Utilisation de la navigation avec Windows XP (genre et Store)</span><span class="sxs-lookup"><span data-stu-id="d75e7-112">Using crumb with Windows XP (kind and store)</span></span>](#using-crumb-with-windows-xp-kind-and-store)
    -   [<span data-ttu-id="d75e7-113">Exemples XP</span><span class="sxs-lookup"><span data-stu-id="d75e7-113">XP Examples</span></span>](#xp-examples)
-   [<span data-ttu-id="d75e7-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d75e7-114">Related topics</span></span>](#related-topics)

 

## <a name="crumb-syntax"></a><span data-ttu-id="d75e7-115">Syntaxe de la navigation</span><span class="sxs-lookup"><span data-stu-id="d75e7-115">Crumb Syntax</span></span>

<span data-ttu-id="d75e7-116">La syntaxe de la navigation est la suivante :</span><span class="sxs-lookup"><span data-stu-id="d75e7-116">The crumb syntax is as follows:</span></span>


```
crumb=<column>:<value>[,<label>][,<column>:<value>[,<label>]]& 
```



<span data-ttu-id="d75e7-117">La <column> partie est toute propriété dans le système de propriétés, et le</span><span class="sxs-lookup"><span data-stu-id="d75e7-117">The <column> portion is any property in the property system, and the</span></span> <value> <span data-ttu-id="d75e7-118">la partie est une valeur valide pour cette propriété.</span><span class="sxs-lookup"><span data-stu-id="d75e7-118">portion is a valid value for that property.</span></span> <span data-ttu-id="d75e7-119">La <label> partie est un alias facultatif pour la propriété qui s’affiche comme un indicateur d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d75e7-119">The <label> portion is an optional alias for the property that displays as a user interface hint.</span></span>

### <a name="general-examples"></a><span data-ttu-id="d75e7-120">Exemples généraux</span><span class="sxs-lookup"><span data-stu-id="d75e7-120">General Examples</span></span>


```
crumb=System.Author:paolo&
crumb=store:mapi&
crumb=location:c%3a%5cMyVacationPix,Vacation&
```



 

## <a name="using-crumb-with-vista-location"></a><span data-ttu-id="d75e7-121">Utilisation de la navigation avec Vista (emplacement)</span><span class="sxs-lookup"><span data-stu-id="d75e7-121">Using crumb with Vista (location)</span></span>

<span data-ttu-id="d75e7-122">Dans le paramètre de navigation, Windows Vista prend en charge la AQS complète et également la `location` propriété, qui a une implémentation spéciale disponible uniquement sur Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d75e7-122">In the crumb parameter, Windows Vista supports full AQS and also the `location` property, which has a special implementation available only on Windows Vista.</span></span> <span data-ttu-id="d75e7-123">Vous pouvez utiliser une chaîne AQS ou la `location` propriété dans un seul paramètre de navigation, mais pas les deux.</span><span class="sxs-lookup"><span data-stu-id="d75e7-123">You can use either an AQS string or the `location` property within a single crumb parameter, but not both.</span></span> <span data-ttu-id="d75e7-124">Si le paramètre de navigation inclut AQS, tout le reste dans ce paramètre de navigation est ignoré.</span><span class="sxs-lookup"><span data-stu-id="d75e7-124">If the crumb parameter includes AQS, everything else in that crumb parameter is ignored.</span></span>

<span data-ttu-id="d75e7-125">La `location` propriété vous permet de spécifier un chemin d’accès à rechercher.</span><span class="sxs-lookup"><span data-stu-id="d75e7-125">The `location` property enables you to specify a path to search.</span></span> <span data-ttu-id="d75e7-126">Windows Vista peut contourner l’indexeur et traverser le répertoire directement si l’emplacement se trouve en dehors de la portée de l’analyse de l’indexeur.</span><span class="sxs-lookup"><span data-stu-id="d75e7-126">Windows Vista can bypass the Indexer and traverse the directory directly if the location is outside the Indexer's crawl scope.</span></span> <span data-ttu-id="d75e7-127">Par conséquent, ces recherches peuvent être plus lentes que les recherches qui utilisent l’indexeur.</span><span class="sxs-lookup"><span data-stu-id="d75e7-127">Consequently, these searches may be slower than searches that use the Indexer.</span></span>

<span data-ttu-id="d75e7-128">Lorsque vous spécifiez une `location` propriété, deux paramètres supplémentaires sont pris en charge et facultatifs :</span><span class="sxs-lookup"><span data-stu-id="d75e7-128">When you specify a `location` property, two additional parameters are supported and optional:</span></span>



| <span data-ttu-id="d75e7-129">Paramètre</span><span class="sxs-lookup"><span data-stu-id="d75e7-129">Parameter</span></span> | <span data-ttu-id="d75e7-130">Valeurs</span><span class="sxs-lookup"><span data-stu-id="d75e7-130">Values</span></span>                  | <span data-ttu-id="d75e7-131">Description</span><span class="sxs-lookup"><span data-stu-id="d75e7-131">Description</span></span>                                                                                                                                                                       |
|-----------|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d75e7-132">inclusion</span><span class="sxs-lookup"><span data-stu-id="d75e7-132">inclusion</span></span> | <span data-ttu-id="d75e7-133">inclure, exclure</span><span class="sxs-lookup"><span data-stu-id="d75e7-133">include, exclude</span></span>        | <span data-ttu-id="d75e7-134">Spécifie si la requête doit inclure ou exclure des éléments de ce chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="d75e7-134">Specifies whether the query should include or exclude items from that path.</span></span> <span data-ttu-id="d75e7-135">« Include » est la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="d75e7-135">"Include" is the default.</span></span> <span data-ttu-id="d75e7-136">Windows Vista ne prend pas en charge les exclusions sans inclusions.</span><span class="sxs-lookup"><span data-stu-id="d75e7-136">Windows Vista does not support exclusions without inclusions.</span></span> <span data-ttu-id="d75e7-137">(Voir l’exemple)</span><span class="sxs-lookup"><span data-stu-id="d75e7-137">(See example)</span></span> |
| <span data-ttu-id="d75e7-138">récursivité</span><span class="sxs-lookup"><span data-stu-id="d75e7-138">recursion</span></span> | <span data-ttu-id="d75e7-139">récursif, récursif</span><span class="sxs-lookup"><span data-stu-id="d75e7-139">recursive, nonrecursive</span></span> | <span data-ttu-id="d75e7-140">Spécifie si la recherche doit recurseiser tous les sous-dossiers à partir de la valeur définie dans l’emplacement :</span><span class="sxs-lookup"><span data-stu-id="d75e7-140">Specifies whether the search should recurse all subfolders starting from the value defined in the location:</span></span><value><span data-ttu-id="d75e7-141">.</span><span class="sxs-lookup"><span data-stu-id="d75e7-141">.</span></span> <span data-ttu-id="d75e7-142">« Recursive » est la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="d75e7-142">"Recursive" is the default.</span></span>                             |



 

<span data-ttu-id="d75e7-143">Pour étendre une recherche à l’aide du protocole search-ms :, vous disposez de différentes options en fonction de la cible de l’étendue.</span><span class="sxs-lookup"><span data-stu-id="d75e7-143">To scope a search using the search-ms: protocol, you have different options depending on the target of the scope.</span></span>

<span data-ttu-id="d75e7-144">Dossier sur un ordinateur local :</span><span class="sxs-lookup"><span data-stu-id="d75e7-144">Folder on a local machine:</span></span>

-   <span data-ttu-id="d75e7-145">Utilisez AQS (navigation = dossier : <chemin d’accès encodé URL>)</span><span class="sxs-lookup"><span data-stu-id="d75e7-145">Use AQS (crumb=folder:<URL-encoded path>)</span></span>
-   <span data-ttu-id="d75e7-146">Use location argument (navigation = Location : <chemin d’accès encodé URL>)</span><span class="sxs-lookup"><span data-stu-id="d75e7-146">Use location argument (crumb=location:<URL-encoded path>)</span></span>

<span data-ttu-id="d75e7-147">Dossier sur un ordinateur/réseau distant :</span><span class="sxs-lookup"><span data-stu-id="d75e7-147">Folder on a remote machine/network:</span></span>

-   <span data-ttu-id="d75e7-148">Use location argument (navigation = Location : <chemin d’accès encodé URL>)</span><span class="sxs-lookup"><span data-stu-id="d75e7-148">Use location argument (crumb=location:<URL-encoded path>)</span></span>

<span data-ttu-id="d75e7-149">Dossier accessible via un gestionnaire de protocole UNC connu :</span><span class="sxs-lookup"><span data-stu-id="d75e7-149">Folder accessed via a known UNC protocol handler:</span></span>

-   <span data-ttu-id="d75e7-150">Utilisez AQS (navigation = Store : <UNC protocol handler name> )</span><span class="sxs-lookup"><span data-stu-id="d75e7-150">Use AQS (crumb=store:<UNC protocol handler name>)</span></span>
-   <span data-ttu-id="d75e7-151">Use location argument (navigation = Location : <chemin d’accès encodé URL>)</span><span class="sxs-lookup"><span data-stu-id="d75e7-151">Use location argument (crumb=location:<URL-encoded path>)</span></span>

### <a name="vista-examples"></a><span data-ttu-id="d75e7-152">Exemples Vista</span><span class="sxs-lookup"><span data-stu-id="d75e7-152">Vista Examples</span></span>


```
search-ms:query=vacation&crumb=location:shell%3aPersonal,include,recursive&

search-ms:crumb=location:c%3a%5cPictures&crumb=location:c%3a%5cPictures%5cDuplicates,,exclude& 

search-ms:crumb=location:c%3a%5cDocuments&crumb=kind:pics&
```



<span data-ttu-id="d75e7-153">Le premier exemple exécute une recherche de « vacances » en commençant à l’emplacement shell://Personal (un raccourci spécial vers le dossier Mes documents de l’utilisateur), y compris ce dossier et tous ses sous-dossiers.</span><span class="sxs-lookup"><span data-stu-id="d75e7-153">The first example executes a search for "vacation" starting at the shell://Personal location (a special shortcut to the user's My Documents folder), including that folder and all subfolders.</span></span> <span data-ttu-id="d75e7-154">Consultez le tableau ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="d75e7-154">See table below.</span></span>

<span data-ttu-id="d75e7-155">Le deuxième exemple exécute une recherche dans C : \\ images, mais pas dans c : \\ images \\ en double.</span><span class="sxs-lookup"><span data-stu-id="d75e7-155">The second example executes a search within C:\\Pictures, but not in C:\\Pictures\\Duplicates.</span></span>

<span data-ttu-id="d75e7-156">Le troisième exemple exécute une recherche dans les documents C : \\ , limitée à des fichiers dont la propriété Kind a la valeur pics.</span><span class="sxs-lookup"><span data-stu-id="d75e7-156">The third example executes a search within C:\\Documents, limited to files with the kind property set to pics.</span></span>

### <a name="constants-for-common-folders"></a><span data-ttu-id="d75e7-157">Constantes pour les dossiers communs</span><span class="sxs-lookup"><span data-stu-id="d75e7-157">Constants for Common Folders</span></span>

<span data-ttu-id="d75e7-158">Windows Vista permet l’utilisation de valeurs [KNOWNFOLDERID](/previous-versions//bb762584(v=vs.85)) qui fournissent une méthode unique indépendante du système pour identifier les dossiers spéciaux utilisés fréquemment par les applications, mais qui peuvent ne pas avoir le même nom ou emplacement sur un système donné.</span><span class="sxs-lookup"><span data-stu-id="d75e7-158">Windows Vista enables the use of [KNOWNFOLDERID](/previous-versions//bb762584(v=vs.85)) values that provide a unique system-independent way to identify special folders used frequently by applications, but which may not have the same name or location on any given system.</span></span> <span data-ttu-id="d75e7-159">Par exemple, le dossier système peut être « C : \\ Windows » sur un système et « c : \\ winnt » sur un autre.</span><span class="sxs-lookup"><span data-stu-id="d75e7-159">For example, the system folder may be "C:\\Windows" on one system and "C:\\Winnt" on another.</span></span> <span data-ttu-id="d75e7-160">Avant Windows Vista, [CSIDLs](/windows/desktop/shell/csidl) étaient utilisés.</span><span class="sxs-lookup"><span data-stu-id="d75e7-160">Prior to Windows Vista, [CSIDLs](/windows/desktop/shell/csidl) were used.</span></span>

<span data-ttu-id="d75e7-161">Utilisez ces emplacements avec la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="d75e7-161">Use these locations with this syntax:</span></span>


```
crumb=location:shell%3a<LocationName>&
```



 

## <a name="using-crumb-with-windows-xp-kind-and-store"></a><span data-ttu-id="d75e7-162">Utilisation de la navigation avec Windows XP (genre et Store)</span><span class="sxs-lookup"><span data-stu-id="d75e7-162">Using crumb with Windows XP (kind and store)</span></span>

<span data-ttu-id="d75e7-163">Pour Windows Search sur Windows XP (WDS 3. x), les termes de AQS « genre » et « Store » ont une implémentation spéciale.</span><span class="sxs-lookup"><span data-stu-id="d75e7-163">For Windows Search on Windows XP (WDS 3.x), the AQS terms "kind" and "store" have a special implementation.</span></span> <span data-ttu-id="d75e7-164">Les valeurs « Kind » sont les mêmes que [celles utilisées dans WDS 2. x](../lwef/-search-2x-wds-perceivedtype.md).</span><span class="sxs-lookup"><span data-stu-id="d75e7-164">The "kind" values are the same [values used in WDS 2.x](../lwef/-search-2x-wds-perceivedtype.md).</span></span> <span data-ttu-id="d75e7-165">Les valeurs « Store » sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="d75e7-165">The "store" values include the following:</span></span>

-   <span data-ttu-id="d75e7-166">Protocole</span><span class="sxs-lookup"><span data-stu-id="d75e7-166">mapi</span></span>
-   <span data-ttu-id="d75e7-167">fichier</span><span class="sxs-lookup"><span data-stu-id="d75e7-167">file</span></span>
-   <span data-ttu-id="d75e7-168">outlookexpress</span><span class="sxs-lookup"><span data-stu-id="d75e7-168">outlookexpress</span></span>
-   <span data-ttu-id="d75e7-169">n'importe laquelle</span><span class="sxs-lookup"><span data-stu-id="d75e7-169">any</span></span>

### <a name="xp-examples"></a><span data-ttu-id="d75e7-170">Exemples XP</span><span class="sxs-lookup"><span data-stu-id="d75e7-170">XP Examples</span></span>


```
search-ms:query=from:john&crumb=store:outlookexpress,OE%20Mail&
search-ms:query=from:john&crumb=kind:communications&
```



<span data-ttu-id="d75e7-171">Le premier exemple retourne les e-mails Microsoft Outlook Express de John avec l’étiquette personnalisée « OE Mail ».</span><span class="sxs-lookup"><span data-stu-id="d75e7-171">The first example returns Microsoft Outlook Express emails from John with the custom label, "OE Mail".</span></span> <span data-ttu-id="d75e7-172">Le deuxième exemple exécute une recherche de toutes les communications de John.</span><span class="sxs-lookup"><span data-stu-id="d75e7-172">The second example executes a search for any communication from John.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d75e7-173">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d75e7-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d75e7-174">Prise en main avec des arguments Parameter-Value</span><span class="sxs-lookup"><span data-stu-id="d75e7-174">Getting Started with Parameter-Value Arguments</span></span>](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[<span data-ttu-id="d75e7-175">Arguments de l’identificateur de paramètres régionaux</span><span class="sxs-lookup"><span data-stu-id="d75e7-175">Locale Identifier Arguments</span></span>](-search-3x-wds-qryidx-localeidentifiers.md)
</dt> <dt>

[<span data-ttu-id="d75e7-176">Argument de syntaxe</span><span class="sxs-lookup"><span data-stu-id="d75e7-176">SYNTAX Argument</span></span>](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[<span data-ttu-id="d75e7-177">Argument STACKEDBY</span><span class="sxs-lookup"><span data-stu-id="d75e7-177">STACKEDBY Argument</span></span>](-search-3x-wds-qryidx-stackedby.md)
</dt> <dt>

[<span data-ttu-id="d75e7-178">Argument de sous-requête</span><span class="sxs-lookup"><span data-stu-id="d75e7-178">SUBQUERY Argument</span></span>](-search-3x-wds-qryidx-subquery.md)
</dt> </dl>

 

 
