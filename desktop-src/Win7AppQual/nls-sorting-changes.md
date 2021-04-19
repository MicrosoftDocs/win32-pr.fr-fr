---
description: .
ms.assetid: 24617b5f-14f1-4f1b-a288-7d20a8166da0
title: Modifications de tri NLS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa4935a6874e28270e73904eb352cd6332e650b7
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314952"
---
# <a name="nls-sorting-changes"></a><span data-ttu-id="e3912-103">Modifications de tri NLS</span><span class="sxs-lookup"><span data-stu-id="e3912-103">NLS Sorting Changes</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="e3912-104">Plateformes affectées</span><span class="sxs-lookup"><span data-stu-id="e3912-104">Affected Platforms</span></span>

 <span data-ttu-id="e3912-105">**Clients** -Windows XP, Windows Vista, Windows 7</span><span class="sxs-lookup"><span data-stu-id="e3912-105">**Clients** - Windows XP, Windows Vista, Windows 7</span></span>  
<span data-ttu-id="e3912-106">**Serveurs** -windows Server 2003, windows Server 2008, windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e3912-106">**Servers** - Windows Server 2003, Windows Server 2008, Windows Server 2008 R2</span></span>  










## <a name="feature-impact"></a><span data-ttu-id="e3912-107">Impact sur les fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="e3912-107">Feature Impact</span></span>

 <span data-ttu-id="e3912-108">**Gravité** -haute</span><span class="sxs-lookup"><span data-stu-id="e3912-108">**Severity** - High</span></span>  
<span data-ttu-id="e3912-109">**Frequency** : faible (peu d’applications affectées, mais si elles sont affectées, toujours endommagées)</span><span class="sxs-lookup"><span data-stu-id="e3912-109">**Frequency** - Low (few apps impacted, but if impacted, always broken)</span></span>  


## <a name="description"></a><span data-ttu-id="e3912-110">Description</span><span class="sxs-lookup"><span data-stu-id="e3912-110">Description</span></span>

<span data-ttu-id="e3912-111">Les fonctions NLS (National Language Support) aident les applications à prendre en charge les différents besoins propres aux langues et aux paramètres régionaux des utilisateurs dans le monde entier.</span><span class="sxs-lookup"><span data-stu-id="e3912-111">The National Language Support (NLS) functions help applications support the different language- and locale-specific needs of users around the world.</span></span> <span data-ttu-id="e3912-112">Les nouvelles versions de Windows incluent presque invariablement les modifications NLS.</span><span class="sxs-lookup"><span data-stu-id="e3912-112">New Windows versions almost invariably include NLS changes.</span></span> <span data-ttu-id="e3912-113">Cette modification affecte le classement et le tri, et donc les applications qui ont des index persistants.</span><span class="sxs-lookup"><span data-stu-id="e3912-113">This change affects collation and sorting, and therefore applications that have persistent indexes.</span></span>

<span data-ttu-id="e3912-114">Une table de classement comporte deux nombres identifiant sa version (révision) : la version définie et la version NLS.</span><span class="sxs-lookup"><span data-stu-id="e3912-114">A collation table has two numbers that identify its version (revision): the defined version and the NLS version.</span></span> <span data-ttu-id="e3912-115">Les deux versions sont des valeurs DWORD, composées d’une version majeure et d’une version mineure.</span><span class="sxs-lookup"><span data-stu-id="e3912-115">Both versions are DWORD values, composed of a major version and a minor version.</span></span> <span data-ttu-id="e3912-116">Le premier octet d’une valeur est réservé, les deux octets suivants représentent la version principale et le dernier octet représente la version mineure.</span><span class="sxs-lookup"><span data-stu-id="e3912-116">The first byte of a value is reserved, the next two bytes represent the major version, and the last byte represents the minor version.</span></span> <span data-ttu-id="e3912-117">En termes hexadécimaux, le modèle est 0xRRMMMMmm, où R est égal à réservé, M est égal à principal et m est égal à mineur.</span><span class="sxs-lookup"><span data-stu-id="e3912-117">In hexadecimal terms, the pattern is 0xRRMMMMmm, where R equals Reserved, M equals major, and m equals minor.</span></span> <span data-ttu-id="e3912-118">Par exemple, une version majeure de 3 avec une version mineure de 4 est représentée sous la forme 0x304.</span><span class="sxs-lookup"><span data-stu-id="e3912-118">For example, a major version of 3 with a minor version of 4 is represented as 0x304.</span></span>

<span data-ttu-id="e3912-119">Pour une version majeure, un ou plusieurs points de code changent afin que l’application doive réindexer toutes les données pour que les comparaisons soient valides.</span><span class="sxs-lookup"><span data-stu-id="e3912-119">For a major version, one or more code points change so that the application must re-index all data for comparisons to be valid.</span></span> <span data-ttu-id="e3912-120">Pour une version mineure, rien ne se déplace, mais des points de code sont ajoutés.</span><span class="sxs-lookup"><span data-stu-id="e3912-120">For a minor version, nothing moves, but code points are added.</span></span> <span data-ttu-id="e3912-121">Pour ce type de version, l’application doit uniquement réindexer les chaînes avec des valeurs précédemment non triées.</span><span class="sxs-lookup"><span data-stu-id="e3912-121">For this type of version, the application only has to re-index strings with previously unsortable values.</span></span> <span data-ttu-id="e3912-122">En résumé, voici ce que signifient les numéros de version par rapport aux modifications apportées aux données dans les tables d’exceptions spécifiques aux paramètres régionaux et aux tables par défaut :</span><span class="sxs-lookup"><span data-stu-id="e3912-122">In summary, here is what the version numbers mean in relation to the data changes in the locale-specific exception tables and default tables:</span></span>

<span data-ttu-id="e3912-123">**NLSVersion majeures** : modification des points de code dans les tables « exception » ou spécifiques aux paramètres régionaux</span><span class="sxs-lookup"><span data-stu-id="e3912-123">**NLSVersion Major** – Changed code points in the 'exception,' or locale-specific tables</span></span>  
<span data-ttu-id="e3912-124">**NLSVersion mineur** – ajout de nouveaux points de code dans les tables « exception » ou spécifiques aux paramètres régionaux</span><span class="sxs-lookup"><span data-stu-id="e3912-124">**NLSVersion Minor** – Added new code points in the 'exception,' or locale-specific tables</span></span>  
<span data-ttu-id="e3912-125">**DefinedVersion majeures** : points de code modifiés dans la table par défaut</span><span class="sxs-lookup"><span data-stu-id="e3912-125">**DefinedVersion Major** – Changed code points in the default table</span></span>  
<span data-ttu-id="e3912-126">**DefinedVersion mineur** – ajout de nouveaux points de code dans la table par défaut</span><span class="sxs-lookup"><span data-stu-id="e3912-126">**DefinedVersion Minor** – Added new code points in the default table</span></span>  


<span data-ttu-id="e3912-127">**Tri des numéros de version pour les versions publiées :**</span><span class="sxs-lookup"><span data-stu-id="e3912-127">**Sorting version numbers for released versions:**</span></span>



| <span data-ttu-id="e3912-128">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="e3912-128">Operating System</span></span>    | <span data-ttu-id="e3912-129">Libérer</span><span class="sxs-lookup"><span data-stu-id="e3912-129">Release</span></span>           | <span data-ttu-id="e3912-130">Version (0xRRMMMMmm)</span><span class="sxs-lookup"><span data-stu-id="e3912-130">Version (0xRRMMMMmm)</span></span>         |
|---------------------|-------------------|------------------------------|
| <span data-ttu-id="e3912-131">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e3912-131">Windows XP</span></span>          | <span data-ttu-id="e3912-132">RTM/SP1/SP2/SP3/...</span><span class="sxs-lookup"><span data-stu-id="e3912-132">RTM/SP1/SP2/SP3/…</span></span> | <span data-ttu-id="e3912-133">N/A-aucune API GetNLSVersion ()</span><span class="sxs-lookup"><span data-stu-id="e3912-133">N/A - no GetNLSVersion() API</span></span> |
| <span data-ttu-id="e3912-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e3912-134">Windows Server 2003</span></span> | <span data-ttu-id="e3912-135">RTM/SP1</span><span class="sxs-lookup"><span data-stu-id="e3912-135">RTM/SP1</span></span>           | <span data-ttu-id="e3912-136">0x00 0000 01</span><span class="sxs-lookup"><span data-stu-id="e3912-136">0x00 0000 01</span></span>                 |
| <span data-ttu-id="e3912-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e3912-137">Windows Vista</span></span>       | <span data-ttu-id="e3912-138">RTM/SP1</span><span class="sxs-lookup"><span data-stu-id="e3912-138">RTM/SP1</span></span>           | <span data-ttu-id="e3912-139">0x00 0405 00</span><span class="sxs-lookup"><span data-stu-id="e3912-139">0x00 0405 00</span></span>                 |
| <span data-ttu-id="e3912-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e3912-140">Windows Server 2008</span></span> | <span data-ttu-id="e3912-141">RTM</span><span class="sxs-lookup"><span data-stu-id="e3912-141">RTM</span></span>               | <span data-ttu-id="e3912-142">0x00 0501 00/0x00 5001 00</span><span class="sxs-lookup"><span data-stu-id="e3912-142">0x00 0501 00 / 0x00 5001 00</span></span>  |
| <span data-ttu-id="e3912-143">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e3912-143">Windows 7</span></span>           | <span data-ttu-id="e3912-144">RTM</span><span class="sxs-lookup"><span data-stu-id="e3912-144">RTM</span></span>               | <span data-ttu-id="e3912-145">0x00060100</span><span class="sxs-lookup"><span data-stu-id="e3912-145">0x00060100</span></span>                   |



 

## <a name="manifestation"></a><span data-ttu-id="e3912-146">Manifestation</span><span class="sxs-lookup"><span data-stu-id="e3912-146">Manifestation</span></span>

<span data-ttu-id="e3912-147">Les applications (telles que les bases de données) avec des index persistants qui ne vérifient pas la version NLS et la réindexation lors de la modification de la version ne peuvent pas être triées correctement ou ne peuvent pas fournir les résultats demandés.</span><span class="sxs-lookup"><span data-stu-id="e3912-147">Applications (such as databases) with persistent indexes that do not check the NLS version and re-index upon version change will fail to sort correctly or may fail to provide requested results.</span></span>

<span data-ttu-id="e3912-148">Dans le cas d’interfaces utilisateur, les listes (par exemple, alphabétique, numérique, alphanumérique, symboles, etc.) peuvent être triées de manière incorrecte.</span><span class="sxs-lookup"><span data-stu-id="e3912-148">In the case of user interfaces, lists (for example, alphabetical, numeric, alphanumeric, symbols, and so on) may sort incorrectly.</span></span>

## <a name="solution"></a><span data-ttu-id="e3912-149">Solution</span><span class="sxs-lookup"><span data-stu-id="e3912-149">Solution</span></span>

<span data-ttu-id="e3912-150">Votre application peut appeler **GetNLSVersionEx** (Windows Vista ou version ultérieure) ou **GetNLSVersion** (avant Windows Vista) pour récupérer la version définie et la version nls pour une table de classement.</span><span class="sxs-lookup"><span data-stu-id="e3912-150">Your application can call either **GetNLSVersionEx** (Windows Vista or later) or **GetNLSVersion** (prior to Windows Vista) to retrieve both the defined version and the NLS version for a collation table.</span></span>

-   <span data-ttu-id="e3912-151">GetNLSVersionEx:</span><span class="sxs-lookup"><span data-stu-id="e3912-151">GetNLSVersionEx:</span></span>

<span data-ttu-id="e3912-152">*Récupère des informations sur la version actuelle d’une fonctionnalité NLS spécifiée pour les paramètres régionaux spécifiés par le nom*</span><span class="sxs-lookup"><span data-stu-id="e3912-152">*Retrieves information about the current version of a specified NLS capability for a locale specified by name*</span></span>  
<span data-ttu-id="e3912-153">Cette fonction permet à une application telle que Active Directory de déterminer si une modification NLS affecte les paramètres régionaux utilisés pour une table d’index particulière.</span><span class="sxs-lookup"><span data-stu-id="e3912-153">This function allows an application such as Active Directory to determine whether an NLS change affects the locale used for a particular index table.</span></span> <span data-ttu-id="e3912-154">Si ce n’est pas le cas, il n’est pas nécessaire de réindexer la table.</span><span class="sxs-lookup"><span data-stu-id="e3912-154">If it does not, there is no need to re-index the table.</span></span> <span data-ttu-id="e3912-155">Pour plus d’informations, consultez Gestion des paramètres régionaux et des informations de langue.</span><span class="sxs-lookup"><span data-stu-id="e3912-155">For more information, see Handling Locale and Language Information.</span></span>  
<span data-ttu-id="e3912-156">Cette fonction prend en charge les paramètres régionaux personnalisés.</span><span class="sxs-lookup"><span data-stu-id="e3912-156">This function supports custom locales.</span></span> <span data-ttu-id="e3912-157">Si *lpLocaleName* spécifie des paramètres régionaux supplémentaires, les données récupérées sont les données appropriées pour l’ordre de classement associé à ces paramètres régionaux supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="e3912-157">If *lpLocaleName* specifies a supplemental locale, the data retrieved is the correct data for the collation order associated with that supplemental locale.</span></span>  

<span data-ttu-id="e3912-158">**Remarque :** Les versions de Windows antérieures à Windows Vista ne prennent pas en charge **GetNLSVersionEx**.</span><span class="sxs-lookup"><span data-stu-id="e3912-158">**Note:** Versions of Windows prior to Windows Vista do not support **GetNLSVersionEx**.</span></span>  


-   <span data-ttu-id="e3912-159">GetNLSVersion (à utiliser pour les applications qui s’exécutent sur des versions de Windows antérieures à Windows Vista) :</span><span class="sxs-lookup"><span data-stu-id="e3912-159">GetNLSVersion (use for applications running on versions of Windows prior to Windows Vista):</span></span>

<span data-ttu-id="e3912-160">*Récupère des informations sur la version actuelle d’une fonctionnalité NLS spécifiée pour les paramètres régionaux spécifiés par l’identificateur*</span><span class="sxs-lookup"><span data-stu-id="e3912-160">*Retrieves information about the current version of a specified NLS capability for a locale specified by identifier*</span></span>  
<span data-ttu-id="e3912-161">Cette fonction permet à une application telle que Active Directory de déterminer si une modification NLS affecte l’identificateur de paramètres régionaux utilisé pour une table d’index particulière.</span><span class="sxs-lookup"><span data-stu-id="e3912-161">This function allows an application such as Active Directory to determine if an NLS change affects the locale identifier used for a particular index table.</span></span> <span data-ttu-id="e3912-162">Si ce n’est pas le cas, il n’est pas nécessaire de réindexer la table.</span><span class="sxs-lookup"><span data-stu-id="e3912-162">If it does not, there is no need to re-index the table.</span></span> <span data-ttu-id="e3912-163">Pour plus d’informations, consultez Gestion des paramètres régionaux et des informations de langue.</span><span class="sxs-lookup"><span data-stu-id="e3912-163">For more information, see Handling Locale and Language Information.</span></span>  
<span data-ttu-id="e3912-164">**Remarque :** Cette fonction récupère des informations uniquement sur les paramètres régionaux spécifiés par l’identificateur.</span><span class="sxs-lookup"><span data-stu-id="e3912-164">**Note:** This function retrieves information only about a locale specified by identifier.</span></span> <span data-ttu-id="e3912-165">La fonction **GetNLSVersionEx** prend en charge les paramètres régionaux, les fonctionnalités et les noms RFC 4646 supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="e3912-165">The **GetNLSVersionEx** function supports additional locales, features, and RFC 4646 names.</span></span> <span data-ttu-id="e3912-166">Toutefois, les versions de Windows antérieures à Windows Vista ne prennent pas en charge **GetNLSVersionEx**.</span><span class="sxs-lookup"><span data-stu-id="e3912-166">However, versions of Windows prior to Windows Vista do not support **GetNLSVersionEx**.</span></span>  
<span data-ttu-id="e3912-167">Les applications destinées à être exécutées uniquement sur Windows Vista et versions ultérieures doivent utiliser **GetNLSVersionEx** en préférence à cette fonction.</span><span class="sxs-lookup"><span data-stu-id="e3912-167">Applications meant to run only on Windows Vista and later should use **GetNLSVersionEx** in preference to this function.</span></span> <span data-ttu-id="e3912-168">**GetNLSVersionEx** fournit une prise en charge appropriée pour les paramètres régionaux supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="e3912-168">**GetNLSVersionEx** provides good support for supplemental locales.</span></span>  


## <a name="compatibility-test"></a><span data-ttu-id="e3912-169">Test de compatibilité</span><span class="sxs-lookup"><span data-stu-id="e3912-169">Compatibility Test</span></span>

<span data-ttu-id="e3912-170">**Procédure de vérification de la modification d’une version de classement (autrement dit, vous devez réindexer) :**</span><span class="sxs-lookup"><span data-stu-id="e3912-170">**Steps to tell if a collation version changed (that is, you need to re-index):**</span></span>

-   <span data-ttu-id="e3912-171">**Utilisez GetNLSVersionEx ()** pour récupérer une structure **NLSVERSIONINFOEX** lors de l’indexation d’origine de vos données.</span><span class="sxs-lookup"><span data-stu-id="e3912-171">**Use GetNLSVersionEx()** to retrieve an **NLSVERSIONINFOEX** structure when doing the original indexing of your data.</span></span>
-   <span data-ttu-id="e3912-172">Stockez les propriétés suivantes avec votre index pour identifier la version :  **NLSVERSIONINFOEX. dwNLSVersion** et **NLSVERSIONINFOEX. dwDefinedVersion** : ces deux propriétés spécifient la version de la table de tri que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="e3912-172">Store the following properties with your index to identify the version:  **NLSVERSIONINFOEX.dwNLSVersion** and **NLSVERSIONINFOEX.dwDefinedVersion** – These two properties together specify the version of the sorting table you are using.</span></span>  
    <span data-ttu-id="e3912-173">**NLSVERSIONINFOEX. dwEffectiveId** : spécifie les paramètres régionaux effectifs de votre tri.</span><span class="sxs-lookup"><span data-stu-id="e3912-173">**NLSVERSIONINFOEX.dwEffectiveId** - This specifies the effective locale of your sort.</span></span> <span data-ttu-id="e3912-174">Les paramètres régionaux personnalisés pointent vers un tri de paramètres régionaux dans la zone.</span><span class="sxs-lookup"><span data-stu-id="e3912-174">A custom locale will point to an in-box locale's sort.</span></span>  
    
-   <span data-ttu-id="e3912-175">Lorsque vous utilisez l’index **, utilisez GetNlsVersionEx ()** pour découvrir la version de vos données.</span><span class="sxs-lookup"><span data-stu-id="e3912-175">When using the index use **GetNlsVersionEx()** to discover the version of your data.</span></span>
-   <span data-ttu-id="e3912-176">Si l’une des trois propriétés a changé, les données de tri que vous utilisez peuvent retourner des résultats différents et n’importe quelle indexation peut ne pas aboutir à la recherche d’enregistrements.</span><span class="sxs-lookup"><span data-stu-id="e3912-176">If any of the three properties has changed, the sorting data you are using could return different results and any indexing you have may fail to find records.</span></span>
-   <span data-ttu-id="e3912-177">Si vous savez que vos données ne contiennent pas de points de code Unicode non valides (autrement dit, si toutes vos chaînes retournaient la **valeur true** à partir d’un appel à **IsNLSDefinedString ()**), vous pouvez les considérer comme étant identiques si seul l’octet de poids faible de **dwNLSVersion** et **dwDefinedVersion** a changé (les versions secondaires décrites ci-dessus).</span><span class="sxs-lookup"><span data-stu-id="e3912-177">If you KNOW that your data does not contain invalid Unicode code points (that is, all of your strings returned **TRUE** from a call to **IsNLSDefinedString()**), then you may consider them the same if ONLY the low byte of **dwNLSVersion** and **dwDefinedVersion** changed (the minor versions described above).</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="e3912-178">Liens vers d’autres ressources</span><span class="sxs-lookup"><span data-stu-id="e3912-178">Links to Other Resources</span></span>

-   [<span data-ttu-id="e3912-179">Internationalisation pour les applications Windows</span><span class="sxs-lookup"><span data-stu-id="e3912-179">Internationalization for Windows Applications</span></span>](../intl/international-support.md)
-   [<span data-ttu-id="e3912-180">GetNLSVersionEx fonction)</span><span class="sxs-lookup"><span data-stu-id="e3912-180">GetNLSVersionEx Function</span></span>](/windows/win32/api/winnls/nf-winnls-getnlsversionex)
-   [<span data-ttu-id="e3912-181">GetNLSVersion fonction)</span><span class="sxs-lookup"><span data-stu-id="e3912-181">GetNLSVersion Function</span></span>](/windows/win32/api/winnls/nf-winnls-getnlsversion)
-   [<span data-ttu-id="e3912-182">Comment savoir si la version de classement a changé</span><span class="sxs-lookup"><span data-stu-id="e3912-182">How to tell if the collation version changed</span></span>](/archive/blogs/shawnste/)

 

 
