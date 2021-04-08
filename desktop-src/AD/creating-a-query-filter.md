---
title: Création d’un filtre de requête
description: Un filtre de requête demande à Active Directory Domain Services de rechercher des données dans une syntaxe de requête LDAP. Toutes les technologies d’accès aux données indiquées dans la rubrique choix de la technologie de recherche prennent en charge la syntaxe de requête LDAP.
ms.assetid: 0bd652f0-41a6-4a0d-8742-9d6a2a7f168a
ms.tgt_platform: multiple
keywords:
- Active Directory des exemples Active Directory, création d’un filtre de requête
- filtres de requête
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2e0a4e4a02312fcc9affb681407044ba0d8e18
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839086"
---
# <a name="creating-a-query-filter"></a><span data-ttu-id="31160-106">Création d’un filtre de requête</span><span class="sxs-lookup"><span data-stu-id="31160-106">Creating a Query Filter</span></span>

<span data-ttu-id="31160-107">Un filtre de requête demande à Active Directory Domain Services de rechercher des données dans une syntaxe de requête LDAP.</span><span class="sxs-lookup"><span data-stu-id="31160-107">A query filter instructs Active Directory Domain Services to find data in an LDAP query syntax.</span></span> <span data-ttu-id="31160-108">Toutes les technologies d’accès aux données indiquées dans la rubrique [choix de la technologie de recherche](choosing-the-search-technology.md) prennent en charge la syntaxe de requête LDAP.</span><span class="sxs-lookup"><span data-stu-id="31160-108">All the specified data access technologies listed in the [Choosing the Search Technology](choosing-the-search-technology.md) topic support LDAP query syntax.</span></span>

<span data-ttu-id="31160-109">La syntaxe de la requête LDAP est la suivante :</span><span class="sxs-lookup"><span data-stu-id="31160-109">The LDAP query syntax is as follows:</span></span>


```C++
<expression><expression>...
```



<span data-ttu-id="31160-110">Un filtre peut contenir une ou plusieurs expressions.</span><span class="sxs-lookup"><span data-stu-id="31160-110">A filter can contain one, or more, expressions.</span></span> <span data-ttu-id="31160-111">Une expression se présente sous la forme suivante :</span><span class="sxs-lookup"><span data-stu-id="31160-111">An expression has the following form:</span></span>


```C++
(<logicaloperator><comparison><comparison...>)
```



<span data-ttu-id="31160-112">où « &lt; LogicalOperator &gt; » est l’un des éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="31160-112">where "&lt;logicaloperator&gt;" is one of the following.</span></span>



| <span data-ttu-id="31160-113">Opérateur</span><span class="sxs-lookup"><span data-stu-id="31160-113">Operator</span></span>        | <span data-ttu-id="31160-114">Description</span><span class="sxs-lookup"><span data-stu-id="31160-114">Description</span></span>                |
|-----------------|----------------------------|
| <span data-ttu-id="31160-115">"\|"</span><span class="sxs-lookup"><span data-stu-id="31160-115">"\|"</span></span><br/> | <span data-ttu-id="31160-116">**Ou** logique</span><span class="sxs-lookup"><span data-stu-id="31160-116">Logical **OR**</span></span><br/>  |
| <span data-ttu-id="31160-117">"&"</span><span class="sxs-lookup"><span data-stu-id="31160-117">"&"</span></span><br/>  | <span data-ttu-id="31160-118">**And** logique</span><span class="sxs-lookup"><span data-stu-id="31160-118">Logical **AND**</span></span><br/> |
| <span data-ttu-id="31160-119">"!"</span><span class="sxs-lookup"><span data-stu-id="31160-119">"!"</span></span><br/>  | <span data-ttu-id="31160-120">**Not** logique</span><span class="sxs-lookup"><span data-stu-id="31160-120">Logical **NOT**</span></span><br/> |



 

<span data-ttu-id="31160-121">et « &lt; comparaison &gt; » est le suivant :</span><span class="sxs-lookup"><span data-stu-id="31160-121">and "&lt;comparison&gt;" is the following:</span></span>


```C++
(<attribute><operator><value>)
```



<span data-ttu-id="31160-122">où « &lt; attribute &gt; » est le **lDAPDisplayName** de l’attribut à évaluer, « &lt; value &gt; » est la valeur à comparer et « &lt; Operator &gt; » est l’un des opérateurs de comparaison suivants.</span><span class="sxs-lookup"><span data-stu-id="31160-122">where "&lt;attribute&gt;" is the **lDAPDisplayName** of the attribute to evaluate, "&lt;value&gt;" is the value to compare against, and "&lt;operator&gt;" is one of the following comparison operators.</span></span>



| <span data-ttu-id="31160-123">Opérateur</span><span class="sxs-lookup"><span data-stu-id="31160-123">Operator</span></span>           | <span data-ttu-id="31160-124">Description</span><span class="sxs-lookup"><span data-stu-id="31160-124">Description</span></span>                         |
|--------------------|-------------------------------------|
| <span data-ttu-id="31160-125">"="</span><span class="sxs-lookup"><span data-stu-id="31160-125">"="</span></span><br/>     | <span data-ttu-id="31160-126">Égal à</span><span class="sxs-lookup"><span data-stu-id="31160-126">Equals</span></span><br/>                   |
| <span data-ttu-id="31160-127">"~="</span><span class="sxs-lookup"><span data-stu-id="31160-127">"~="</span></span><br/>    | <span data-ttu-id="31160-128">Approximativement égal à</span><span class="sxs-lookup"><span data-stu-id="31160-128">Approximately equals</span></span><br/>     |
| <span data-ttu-id="31160-129">"<="</span><span class="sxs-lookup"><span data-stu-id="31160-129">"<="</span></span><br/> | <span data-ttu-id="31160-130">Inférieur ou égal à</span><span class="sxs-lookup"><span data-stu-id="31160-130">Less than or equal to</span></span><br/>    |
| <span data-ttu-id="31160-131">">="</span><span class="sxs-lookup"><span data-stu-id="31160-131">">="</span></span><br/> | <span data-ttu-id="31160-132">Supérieur ou égal à</span><span class="sxs-lookup"><span data-stu-id="31160-132">Greater than or equal to</span></span><br/> |



 

<span data-ttu-id="31160-133">En outre, selon la syntaxe d’attribut, la « &lt; valeur &gt; » peut contenir le caractère générique (« \* »).</span><span class="sxs-lookup"><span data-stu-id="31160-133">In addition, depending on the attribute syntax, the "&lt;value&gt;" may contain the wildcard symbol ("\*").</span></span> <span data-ttu-id="31160-134">Une « &lt; valeur &gt; » qui contient uniquement un caractère générique vérifie l’existence d’une valeur dans « &lt; attribut &gt; ».</span><span class="sxs-lookup"><span data-stu-id="31160-134">A "&lt;value&gt;" that contains only a wildcard will check for the existence of any value in "&lt;attribute&gt;".</span></span> <span data-ttu-id="31160-135">Si aucune valeur n’est définie pour « &lt; attribute &gt; », le test échoue.</span><span class="sxs-lookup"><span data-stu-id="31160-135">If no value is set for "&lt;attribute&gt;", the test will fail.</span></span>

<span data-ttu-id="31160-136">Si l’un des caractères spéciaux suivants doit apparaître dans le filtre de requête comme littéraux, ils doivent être remplacés par la séquence d’échappement répertoriée.</span><span class="sxs-lookup"><span data-stu-id="31160-136">If any of the following special characters must appear in the query filter as literals, they must be replaced by the listed escape sequence.</span></span>



| <span data-ttu-id="31160-137">Caractère ASCII</span><span class="sxs-lookup"><span data-stu-id="31160-137">ASCII character</span></span>    | <span data-ttu-id="31160-138">Substitution de séquence d’échappement</span><span class="sxs-lookup"><span data-stu-id="31160-138">Escape sequence substitute</span></span> |
|--------------------|----------------------------|
| \*<br/>      | <span data-ttu-id="31160-139">« \\ 2A »</span><span class="sxs-lookup"><span data-stu-id="31160-139">"\\2a"</span></span><br/>          |
| <span data-ttu-id="31160-140">(</span><span class="sxs-lookup"><span data-stu-id="31160-140">(</span></span><br/>       | <span data-ttu-id="31160-141">" \\ 28"</span><span class="sxs-lookup"><span data-stu-id="31160-141">"\\28"</span></span><br/>          |
| <span data-ttu-id="31160-142">)</span><span class="sxs-lookup"><span data-stu-id="31160-142">)</span></span><br/>       | <span data-ttu-id="31160-143">« \\ 29 »</span><span class="sxs-lookup"><span data-stu-id="31160-143">"\\29"</span></span><br/>          |
| \\<br/>      | <span data-ttu-id="31160-144">« \\ 5C »</span><span class="sxs-lookup"><span data-stu-id="31160-144">"\\5c"</span></span><br/>          |
| <span data-ttu-id="31160-145">**NUL**</span><span class="sxs-lookup"><span data-stu-id="31160-145">**NUL**</span></span><br/> | <span data-ttu-id="31160-146">« \\ 00 »</span><span class="sxs-lookup"><span data-stu-id="31160-146">"\\00"</span></span><br/>          |



 

<span data-ttu-id="31160-147">En outre, les données binaires arbitraires peuvent être représentées à l’aide de la syntaxe de séquence d’échappement en encodant chaque octet de données binaires avec la barre oblique inverse suivie de deux chiffres hexadécimaux.</span><span class="sxs-lookup"><span data-stu-id="31160-147">In addition, arbitrary binary data may be represented using the escape sequence syntax by encoding each byte of binary data with the backslash followed by two hexadecimal digits.</span></span> <span data-ttu-id="31160-148">Par exemple, la valeur de 4 octets 0x00000004 est encodée sous la forme « \\ 00 \\ 00 \\ 00 \\ 04 » dans une chaîne de filtrage.</span><span class="sxs-lookup"><span data-stu-id="31160-148">For example, the four-byte value 0x00000004 is encoded as "\\00\\00\\00\\04" in a filter string.</span></span>

## <a name="examples"></a><span data-ttu-id="31160-149">Exemples</span><span class="sxs-lookup"><span data-stu-id="31160-149">Examples</span></span>

<span data-ttu-id="31160-150">La chaîne de requête suivante recherche tous les objets de type « Computer ».</span><span class="sxs-lookup"><span data-stu-id="31160-150">The following query string will search for all objects of type "computer".</span></span>


```C++
(objectCategory=computer)
```



<span data-ttu-id="31160-151">La chaîne de requête suivante recherche tous les objets de type « Computer » dont le nom commence par « Desktop ».</span><span class="sxs-lookup"><span data-stu-id="31160-151">The following query string will search for all objects of type "computer" with a name that begins with "desktop".</span></span>


```C++
(&(objectCategory=computer)(name=desktop*))
```



<span data-ttu-id="31160-152">La chaîne de requête suivante recherche tous les objets de type « Computer » dont le nom commence par « Desktop » ou un nom commençant par « Notebook ».</span><span class="sxs-lookup"><span data-stu-id="31160-152">The following query string will search for all objects of type "computer" with a name that begins with "desktop" or a name that begins with "notebook".</span></span>


```C++
(&(objectCategory=computer)(|(name=desktop*)(name=notebook*)))
```



<span data-ttu-id="31160-153">La chaîne de requête suivante recherche tous les objets de type « utilisateur » qui ont un numéro de téléphone privé.</span><span class="sxs-lookup"><span data-stu-id="31160-153">The following query string will search for all objects of type "user" that have a home phone number.</span></span>


```C++
(&(objectCategory=user)(homePhone=*))
```



<span data-ttu-id="31160-154">Pour plus d’informations sur les chaînes de filtre de requête et des exemples d’utilisation, consultez :</span><span class="sxs-lookup"><span data-stu-id="31160-154">For more information about query filter strings, and usage examples, see:</span></span>

-   [<span data-ttu-id="31160-155">Rechercher des objets par classe</span><span class="sxs-lookup"><span data-stu-id="31160-155">Finding Objects by Class</span></span>](finding-objects-by-class.md)
-   [<span data-ttu-id="31160-156">Recherche d’objets par nom</span><span class="sxs-lookup"><span data-stu-id="31160-156">Finding Objects by Name</span></span>](finding-objects-by-name.md)
-   [<span data-ttu-id="31160-157">Recherche d’une liste d’attributs à interroger</span><span class="sxs-lookup"><span data-stu-id="31160-157">Finding a List of Attributes To Query</span></span>](finding-a-list-of-attributes-to-query.md)
-   [<span data-ttu-id="31160-158">Vérification de la syntaxe du filtre de requête</span><span class="sxs-lookup"><span data-stu-id="31160-158">Checking the Query Filter Syntax</span></span>](checking-the-query-filter-syntax.md)
-   [<span data-ttu-id="31160-159">Comment spécifier des valeurs de comparaison</span><span class="sxs-lookup"><span data-stu-id="31160-159">How to Specify Comparison Values</span></span>](how-to-specify-comparison-values.md)

 

 





