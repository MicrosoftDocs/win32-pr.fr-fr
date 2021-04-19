---
description: La syntaxe de requête avancée (AQS) est la syntaxe de requête par défaut utilisée par Windows Search pour interroger l’index et affiner et limiter les paramètres de recherche.
ms.assetid: 76e33903-d063-48c0-9afe-912c3daa8237
title: Utilisation de la syntaxe de requête avancée par programmation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc8fa69a5a5ccaa37b84a10abd367e5a29656455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515619"
---
# <a name="using-advanced-query-syntax-programmatically"></a><span data-ttu-id="dec46-103">Utilisation de la syntaxe de requête avancée par programmation</span><span class="sxs-lookup"><span data-stu-id="dec46-103">Using Advanced Query Syntax Programmatically</span></span>

<span data-ttu-id="dec46-104">La syntaxe de requête avancée (AQS) est la syntaxe de requête par défaut utilisée par Windows Search pour interroger l’index et affiner et limiter les paramètres de recherche.</span><span class="sxs-lookup"><span data-stu-id="dec46-104">Advanced Query Syntax (AQS) is the default query syntax used by Windows Search to query the index and to refine and narrow search parameters.</span></span> <span data-ttu-id="dec46-105">AQS est utilisé par les développeurs pour créer des requêtes par programme (et par les utilisateurs pour affiner leurs paramètres de recherche).</span><span class="sxs-lookup"><span data-stu-id="dec46-105">AQS is employed by developers to build queries programmatically (and by users to narrow their search parameters).</span></span> <span data-ttu-id="dec46-106">Le AQS canonique a été introduit dans Windows 7 et doit être utilisé dans Windows 7 et versions ultérieures pour générer par programmation des requêtes AQS.</span><span class="sxs-lookup"><span data-stu-id="dec46-106">Canonical AQS was introduced in Windows 7 and must be used in Windows 7 and later to programmatically generate AQS queries.</span></span>

<span data-ttu-id="dec46-107">Cette rubrique est organisée comme suit :</span><span class="sxs-lookup"><span data-stu-id="dec46-107">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="dec46-108">À propos de la syntaxe de requête avancée</span><span class="sxs-lookup"><span data-stu-id="dec46-108">About Advanced Query Syntax</span></span>](#about-advanced-query-syntax)
    -   [<span data-ttu-id="dec46-109">Exemples</span><span class="sxs-lookup"><span data-stu-id="dec46-109">Examples</span></span>](#examples)
    -   [<span data-ttu-id="dec46-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="dec46-110">Properties</span></span>](#properties)
-   [<span data-ttu-id="dec46-111">Utilisation de mots clés dans les langues locales</span><span class="sxs-lookup"><span data-stu-id="dec46-111">Keyword Use in Local Languages</span></span>](#keyword-use-in-local-languages)
-   [<span data-ttu-id="dec46-112">Syntaxe de requête avancée canonique dans Windows 7</span><span class="sxs-lookup"><span data-stu-id="dec46-112">Canonical Advanced Query Syntax in Windows 7</span></span>](#canonical-advanced-query-syntax-in-windows-7)
    -   [<span data-ttu-id="dec46-113">Exemples</span><span class="sxs-lookup"><span data-stu-id="dec46-113">Examples</span></span>](#examples)
    -   [<span data-ttu-id="dec46-114">Opérateurs de requête</span><span class="sxs-lookup"><span data-stu-id="dec46-114">Query Operators</span></span>](#query-operators)
    -   [<span data-ttu-id="dec46-115">Valeurs de requête</span><span class="sxs-lookup"><span data-stu-id="dec46-115">Query Values</span></span>](#query-values)
-   [<span data-ttu-id="dec46-116">Restrictions d’étendue</span><span class="sxs-lookup"><span data-stu-id="dec46-116">Scope Restrictions</span></span>](#scope-restrictions)
-   [<span data-ttu-id="dec46-117">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="dec46-117">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="dec46-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dec46-118">Related topics</span></span>](#related-topics)

## <a name="about-advanced-query-syntax"></a><span data-ttu-id="dec46-119">À propos de la syntaxe de requête avancée</span><span class="sxs-lookup"><span data-stu-id="dec46-119">About Advanced Query Syntax</span></span>

<span data-ttu-id="dec46-120">Une requête se compose de requêtes de base connectées avec et, ou, et non, comme indiqué dans l’exemple de syntaxe suivant :</span><span class="sxs-lookup"><span data-stu-id="dec46-120">A query consists of basic queries connected with AND, OR, and NOT, as shown in the following example syntax:</span></span>

``` syntax
<query> ::=
     <basic query>
| ( <query> )
| <query> AND <query>  
| <query> <query>    // Same as <query> AND <query>
| <query> OR <query> 
| NOT <query>
```

> [!Note]  
> <span data-ttu-id="dec46-121">AQS ne respecte pas la casse, à l’exception de AND, OR et NOT, qui doit être en majuscules.</span><span class="sxs-lookup"><span data-stu-id="dec46-121">AQS is not case sensitive, with the exception of AND, OR, and NOT, which must be in all uppercase.</span></span>

 

<span data-ttu-id="dec46-122">Si une requête a deux ou plusieurs utilisations de et ou ou, elles sont liées de gauche à droite, qu’il s’agisse de et ou ou.</span><span class="sxs-lookup"><span data-stu-id="dec46-122">If a query has two or more uses of AND or OR, they will bind from left to right, regardless of whether it is AND or OR.</span></span> <span data-ttu-id="dec46-123">Autrement dit, la requête, « Apple et Poir ou prune », est interprétée comme si elle était écrite comme « (Apple et Poir) ou prune », et la requête, « Apple ou Poir et Plum », sera interprétée comme si elle était écrite comme « (Apple ou Poir) et prune ».</span><span class="sxs-lookup"><span data-stu-id="dec46-123">That is, the query, "apple AND pear OR plum" will be interpreted as if it were written as "(apple AND pear) OR plum", and the query, "apple OR pear AND plum", will be interpreted as if it were written as "(apple OR pear) AND plum".</span></span> <span data-ttu-id="dec46-124">Par conséquent, si un document contient le mot Plum, mais ni Apple, ni Poirier, la première requête le retourne, contrairement à la deuxième requête.</span><span class="sxs-lookup"><span data-stu-id="dec46-124">So if a document contains the word plum but neither apple, nor pear, the first query will return it but the second query will not.</span></span> <span data-ttu-id="dec46-125">Par conséquent, nous vous recommandons d’utiliser des parenthèses explicites pour toute requête qui mélange et et ou pour éviter les erreurs ou les interprétations erronées.</span><span class="sxs-lookup"><span data-stu-id="dec46-125">Hence, we recommend that you use explicit parentheses for any query that mixes AND and OR to avoid mistakes or misinterpretations.</span></span>

<span data-ttu-id="dec46-126">Une requête de base recherche les éléments qui répondent à une restriction sur une propriété.</span><span class="sxs-lookup"><span data-stu-id="dec46-126">A basic query searches for items that satisfy a restriction over a property.</span></span> <span data-ttu-id="dec46-127">La seule partie obligatoire d’une requête de base est la valeur de la restriction ou de la recherche.</span><span class="sxs-lookup"><span data-stu-id="dec46-127">The only required portion of a basic query is the restriction or search value.</span></span> <span data-ttu-id="dec46-128">Si vous ne spécifiez pas de propriété, la recherche Windows recherche toutes les propriétés.</span><span class="sxs-lookup"><span data-stu-id="dec46-128">If you do not specify a property, Windows Search searches all properties.</span></span> <span data-ttu-id="dec46-129"><restr> représente la restriction de recherche.</span><span class="sxs-lookup"><span data-stu-id="dec46-129"><restr> represents the search restriction.</span></span>

<span data-ttu-id="dec46-130">Les formulaires suivants pour une requête de base sont valides :</span><span class="sxs-lookup"><span data-stu-id="dec46-130">The following forms for a basic query are valid:</span></span>

``` syntax
<basic query> ::=
     <prop>:<basic restr>
| <restr>
```

<span data-ttu-id="dec46-131">Une propriété est désignée par un mot clé tel que auteur ou taille, ou par un nom de propriété canonique tel que [System. DateModified](../properties/props-system-datemodified.md).</span><span class="sxs-lookup"><span data-stu-id="dec46-131">A property is designated by a keyword such as author or size, or by a canonical property name such as [System.DateModified](../properties/props-system-datemodified.md).</span></span> <span data-ttu-id="dec46-132">Les formulaires valides pour une propriété sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="dec46-132">Valid forms for a property are as follows:</span></span>

``` syntax
<prop> ::= 
     <canonical property name>
| <property label in UI language>
```

<span data-ttu-id="dec46-133">Un opérateur indique une opération telle que < ou =.</span><span class="sxs-lookup"><span data-stu-id="dec46-133">An operator indicates an operation such as < or =.</span></span> <span data-ttu-id="dec46-134">Pour obtenir la liste des opérateurs valides, consultez la section opérateurs de requête plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="dec46-134">For a list of valid operators, see the Query Operators section later in this topic.</span></span>

<span data-ttu-id="dec46-135">Une restriction de base est une restriction simple sur une propriété qui peut être écrite sans parenthèses :</span><span class="sxs-lookup"><span data-stu-id="dec46-135">A basic restriction is a simple restriction on a property that can be written without parentheses:</span></span>

``` syntax
<basic restr> ::=
     <value>
| <op><value>
| NOT <basic restr>
| ( <restr> )
```

<span data-ttu-id="dec46-136">Une restriction est une valeur de recherche telle qu’une valeur numérique ou une valeur de chaîne, éventuellement avec un opérateur.</span><span class="sxs-lookup"><span data-stu-id="dec46-136">A restriction is a search value such as a number value or string value, optionally with an operator.</span></span> <span data-ttu-id="dec46-137">Les formulaires valides pour une restriction sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="dec46-137">Valid forms for a restriction are as follows:</span></span>

``` syntax
<restr> ::=
    <basic restr>
| <restr> AND <restr>
| <restr> <restr>      // Same as <restr> AND <restr>
| <restr> OR <restr>
```

<span data-ttu-id="dec46-138">Si vous ne spécifiez pas d’opérateur, Windows Search choisit l’opérateur le plus approprié pour votre requête :</span><span class="sxs-lookup"><span data-stu-id="dec46-138">If you do not specify an operator, Windows Search chooses the most appropriate operator for your query:</span></span>

-   <span data-ttu-id="dec46-139">Pour une propriété de type chaîne, \_ l' \_ opérateur COP Word STARTSWITH $< est supposé.</span><span class="sxs-lookup"><span data-stu-id="dec46-139">For a string property, the COP\_WORD\_STARTSWITH $< operator is assumed.</span></span>
-   <span data-ttu-id="dec46-140">Pour toutes les autres propriétés, l' \_ opérateur COP EQUAL = est supposé.</span><span class="sxs-lookup"><span data-stu-id="dec46-140">For all other properties, the COP\_EQUAL = operator is assumed.</span></span>

<span data-ttu-id="dec46-141">Pour l’utilisation par programme de AQS, nous vous recommandons de toujours disposer d’un opérateur explicite.</span><span class="sxs-lookup"><span data-stu-id="dec46-141">For the programmatic use of AQS, we recommend that you always have an explicit operator.</span></span> <span data-ttu-id="dec46-142">Le formulaire valide pour la recherche d’une valeur simple ou d’une plage de valeurs est le suivant :</span><span class="sxs-lookup"><span data-stu-id="dec46-142">The valid form for searching a simple value or value range is as follows:</span></span>

``` syntax
<value> ::=
    <simplevalue>
| <simplevalue> .. <simplevalue>
```

<span data-ttu-id="dec46-143">Une valeur simple peut être constituée de l’un des types suivants :</span><span class="sxs-lookup"><span data-stu-id="dec46-143">A simple value can consist of any of the following types:</span></span>

``` syntax
<simplevalue> ::=
  []         // No value, or a null value
| <word>     // A sequence of characters without whitespace
| <number>   // An integer or a floating point number
| <datetime> // A relative date, or an absolute date and/or time
| <Boolean>
| "..."      // A phrase
| <enumeration range>
```

### <a name="examples"></a><span data-ttu-id="dec46-144">Exemples</span><span class="sxs-lookup"><span data-stu-id="dec46-144">Examples</span></span>

<span data-ttu-id="dec46-145">Une requête qui recherche un document contenant la phase « dernier trimestre », créée par Theresa ou Lee, et enregistrée dans le dossier MyDocs, combine trois requêtes de base comme suit :</span><span class="sxs-lookup"><span data-stu-id="dec46-145">A query that searches for a document containing the phase "last quarter," authored by Theresa or Lee, and that was saved to the folder MyDocs, combines three basic queries as follows:</span></span>

``` syntax
"last quarter" author:(theresa OR lee) folder:MyDocs
```

<span data-ttu-id="dec46-146">Les trois requêtes de base sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="dec46-146">The three basic queries are:</span></span>

-   <span data-ttu-id="dec46-147">« dernier trimestre »</span><span class="sxs-lookup"><span data-stu-id="dec46-147">"last quarter"</span></span>
-   <span data-ttu-id="dec46-148">Auteur : (Theresa ou Lee)</span><span class="sxs-lookup"><span data-stu-id="dec46-148">author:(theresa OR lee)</span></span>
-   <span data-ttu-id="dec46-149">dossier : MyDocs</span><span class="sxs-lookup"><span data-stu-id="dec46-149">folder:MyDocs</span></span>

<span data-ttu-id="dec46-150">Une requête de base qui utilise la syntaxe canonique est la suivante :</span><span class="sxs-lookup"><span data-stu-id="dec46-150">A basic query that uses canonical syntax is:</span></span>

``` syntax
System.Size:>1kb
```

### <a name="properties"></a><span data-ttu-id="dec46-151">Propriétés</span><span class="sxs-lookup"><span data-stu-id="dec46-151">Properties</span></span>

<span data-ttu-id="dec46-152">Les propriétés sont référencées par un mot clé, qui peut être un nom de propriété canonique dans Windows 7 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="dec46-152">Properties are referred to by a keyword, which can be a canonical property name in Windows 7 and later.</span></span> <span data-ttu-id="dec46-153">AQS dans l’interface utilisateur de Windows peut utiliser l’étiquette au lieu du nom de propriété canonique, tel que auteur au lieu de [System. Author](../properties/props-system-author.md).</span><span class="sxs-lookup"><span data-stu-id="dec46-153">AQS in the Windows UI can use the label instead of the canonical property name, such as author instead of [System.Author](../properties/props-system-author.md).</span></span> <span data-ttu-id="dec46-154">Dans Windows Vista et les versions antérieures, il était possible d’utiliser des étiquettes en anglais, quelle que soit la langue de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="dec46-154">In Windows Vista and earlier it was possible to use English labels regardless of the UI language.</span></span> <span data-ttu-id="dec46-155">Dans Windows 7 et versions ultérieures, Windows Search reconnaît uniquement les mots clés dans la langue actuelle de l’interface utilisateur par défaut.</span><span class="sxs-lookup"><span data-stu-id="dec46-155">In Windows 7 and later, Windows Search recognizes keywords in the current default UI language only.</span></span>

### <a name="support-for-custom-properties"></a><span data-ttu-id="dec46-156">Prise en charge des propriétés personnalisées</span><span class="sxs-lookup"><span data-stu-id="dec46-156">Support for Custom Properties</span></span>

<span data-ttu-id="dec46-157">Dans Windows Vista et les versions antérieures, les propriétés personnalisées n’étaient pas disponibles dans AQS.</span><span class="sxs-lookup"><span data-stu-id="dec46-157">In Windows Vista and earlier, custom properties were not available in AQS.</span></span> <span data-ttu-id="dec46-158">Dans Windows 7 et versions ultérieures, AQS fonctionne avec des propriétés personnalisées qui sont inscrites auprès du système de propriétés.</span><span class="sxs-lookup"><span data-stu-id="dec46-158">In Windows 7 and later, AQS works with custom properties that are registered with the property system.</span></span> <span data-ttu-id="dec46-159">Pour plus d’informations sur la création de propriétés personnalisées, consultez [système de propriétés](../properties/building-property-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="dec46-159">For more information on creating custom properties, see [Property System](../properties/building-property-handlers.md).</span></span>

### <a name="datetime-properties-in-windows-8"></a><span data-ttu-id="dec46-160">Propriétés DateTime dans Windows 8</span><span class="sxs-lookup"><span data-stu-id="dec46-160">DateTime properties in Windows 8</span></span>

<span data-ttu-id="dec46-161">À compter de Windows 8, les propriétés DateTime (comme [System. DateModified](../properties/props-system-datemodified.md)) prennent en charge le format de date et d’heure canonique spécifié par [ISO-8601](https://www.w3.org/TR/NOTE-datetime), en incluant éventuellement le fuseau horaire UTC.</span><span class="sxs-lookup"><span data-stu-id="dec46-161">As of Windows 8, DateTime properties (like [System.DateModified](../properties/props-system-datemodified.md)) support the canonical date and time format specified by [ISO-8601](https://www.w3.org/TR/NOTE-datetime), optionally including the UTC time zone.</span></span>

-   <span data-ttu-id="dec46-162">**Windows 8 et versions antérieures, date-heure sans fuseau horaire UTC :** *yyyy* - *mm* - *jjThh*:*mm*:*SS*</span><span class="sxs-lookup"><span data-stu-id="dec46-162">**Windows 8 and earlier, date-time without UTC time zone:** *YYYY*-*MM*-*DDThh*:*mm*:*ss*</span></span>

    <span data-ttu-id="dec46-163">Ce format spécifie une heure locale, quels que soient les paramètres régionaux utilisateur ou système.</span><span class="sxs-lookup"><span data-stu-id="dec46-163">This format specifies a local time, regardless of the user or system locale.</span></span>

-   <span data-ttu-id="dec46-164">**Windows 8, date-heure avec fuseau horaire UTC :** *yyyy* - *mm* - *jjThh*:*mm*:*ssTZD*</span><span class="sxs-lookup"><span data-stu-id="dec46-164">**Windows 8, date-time with UTC time zone:** *YYYY*-*MM*-*DDThh*:*mm*:*ssTZD*</span></span>

    <span data-ttu-id="dec46-165">Ce format spécifie une heure au fuseau horaire UTC spécifié.</span><span class="sxs-lookup"><span data-stu-id="dec46-165">This format specifies a time at the specified UTC time zone.</span></span>

## <a name="keyword-use-in-local-languages"></a><span data-ttu-id="dec46-166">Utilisation de mots clés dans les langues locales</span><span class="sxs-lookup"><span data-stu-id="dec46-166">Keyword Use in Local Languages</span></span>

<span data-ttu-id="dec46-167">Dans Windows 7 et versions ultérieures, les mots clés mnémoniques fonctionnent uniquement dans la langue du système, tels que les mots clés allemands uniquement sur un système d’exploitation allemand et les mots clés en anglais uniquement sur un système d’exploitation anglais.</span><span class="sxs-lookup"><span data-stu-id="dec46-167">In Windows 7 and later, mnemonic keywords work in the system language only, such as German keywords only on a German operating system, and English keywords only on an English operating system.</span></span> <span data-ttu-id="dec46-168">[System. Author](../properties/props-system-author.md) est un mot clé canonique et la valeur mnémonique pour la propriété System. Author est Author, par exemple.</span><span class="sxs-lookup"><span data-stu-id="dec46-168">[System.Author](../properties/props-system-author.md) is a canonical keyword, and the mnemonic value for the System.Author property is Author, for example.</span></span> <span data-ttu-id="dec46-169">L’introduction des mots clés canoniques compense le fait que les mots clés mnémoniques anglais ne sont plus reconnus universellement sur tous les systèmes d’exploitation, quelle que soit la langue, comme c’était le cas dans Windows Vista et les versions antérieures.</span><span class="sxs-lookup"><span data-stu-id="dec46-169">The introduction of canonical keywords compensates for the fact that English mnemonic keywords are no longer universally recognized on all operating systems regardless of language, as was the case in Windows Vista and earlier.</span></span>

> [!Note]  
> <span data-ttu-id="dec46-170">Dans Windows 7 et versions ultérieures, Windows Search reconnaît les mots clés dans la langue par défaut actuelle uniquement, et non en anglais, sauf si l’anglais est la valeur par défaut actuelle.</span><span class="sxs-lookup"><span data-stu-id="dec46-170">In Windows 7 and later, Windows Search recognizes keywords in the current default language only, and not in English unless English is the current default.</span></span> <span data-ttu-id="dec46-171">Nous recommandons que les développeurs utilisent toujours la syntaxe canonique afin que leur application n’ait pas de problèmes de langue avec les mots clés.</span><span class="sxs-lookup"><span data-stu-id="dec46-171">We recommend that developers always use canonical syntax so that their application won't have language problems with keywords.</span></span>

 

## <a name="canonical-advanced-query-syntax-in-windows-7"></a><span data-ttu-id="dec46-172">Syntaxe de requête avancée canonique dans Windows 7</span><span class="sxs-lookup"><span data-stu-id="dec46-172">Canonical Advanced Query Syntax in Windows 7</span></span>

<span data-ttu-id="dec46-173">La syntaxe canonique a été introduite pour les mots clés dans Windows 7.</span><span class="sxs-lookup"><span data-stu-id="dec46-173">Canonical syntax was introduced for keywords in Windows 7.</span></span> <span data-ttu-id="dec46-174">Un exemple de requête avec une propriété canonique est `System.Message.FromAddress:=me@microsoft.com` .</span><span class="sxs-lookup"><span data-stu-id="dec46-174">An example of a query with a canonical property is `System.Message.FromAddress:=me@microsoft.com`.</span></span> <span data-ttu-id="dec46-175">Lors du codage de requêtes dans des applications qui s’exécutent sur Windows 7 et versions ultérieures, vous devez utiliser la syntaxe canonique pour générer par programmation des requêtes AQS.</span><span class="sxs-lookup"><span data-stu-id="dec46-175">When coding queries in applications running on Windows 7 and later, you must use canonical syntax to programmatically generate AQS queries.</span></span> <span data-ttu-id="dec46-176">Si vous n’utilisez pas la syntaxe canonique et que votre application est déployée dans une langue locale ou d’interface utilisateur différente de celle du code de l’application, vos requêtes ne seront pas interprétées correctement.</span><span class="sxs-lookup"><span data-stu-id="dec46-176">If you do not use canonical syntax and your application is deployed in a locale or UI language different from the language in the application code, your queries will not be interpreted correctly.</span></span>

<span data-ttu-id="dec46-177">Les conventions pour la syntaxe de mot clé canonique sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="dec46-177">The conventions for canonical keyword syntax are as follows:</span></span>

-   <span data-ttu-id="dec46-178">La syntaxe canonique d’une propriété est son nom canonique, tel que `System.Photo.LightSource` .</span><span class="sxs-lookup"><span data-stu-id="dec46-178">The canonical syntax for a property is its canonical name, such as `System.Photo.LightSource`.</span></span> <span data-ttu-id="dec46-179">Les noms canoniques ne respectent pas la casse.</span><span class="sxs-lookup"><span data-stu-id="dec46-179">Canonical names are not case sensitive.</span></span>
-   <span data-ttu-id="dec46-180">La syntaxe canonique pour les opérateurs booléens se compose des mots clés AND, OR et NOT, en majuscules.</span><span class="sxs-lookup"><span data-stu-id="dec46-180">The canonical syntax for the Boolean operators consists of the keywords AND, OR, and NOT, in all uppercase.</span></span>
-   <span data-ttu-id="dec46-181">Les opérateurs <, >, =, et ainsi de suite, ne sont pas localisés et font donc également partie de la syntaxe canonique.</span><span class="sxs-lookup"><span data-stu-id="dec46-181">The operators <, >, =, and so forth, are not localized and are thus also part of the canonical syntax.</span></span>
-   <span data-ttu-id="dec46-182">Si une propriété `P` a des valeurs énumérées ou des plages nommées N ₁ à l’aide de NK, la syntaxe canonique pour la valeur ou la plage *i* est le nom canonique de P, suivi du caractère \# , suivi de N <sub>I</sub>, comme illustré dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="dec46-182">If a property `P` has enumerated values or ranges named N₁ through Nₖ, the canonical syntax for the *I* th value or range is the canonical name for P, followed by the character \#, followed by N<sub>I</sub>, as illustrated in the following example:</span></span>
    -   <span data-ttu-id="dec46-183">`System.Photo.LightSource#Daylight`, `System.Photo.LightSource#StandardA` , et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="dec46-183">`System.Photo.LightSource#Daylight`, `System.Photo.LightSource#StandardA`, and so forth.</span></span>
-   <span data-ttu-id="dec46-184">Pour un type sémantique défini T avec des valeurs ou des plages nommées N ₁ à l’aide de NK, la syntaxe canonique pour la valeur ou la plage *i* est le nom canonique de T, suivi du caractère \# , suivi de N <sub>i</sub>, comme illustré dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="dec46-184">For a defined semantic type T with values or ranges named N₁ through Nₖ, the canonical syntax for the *I* th value or range is the canonical name for T, followed by the character \#, followed by N<sub>I</sub>, as illustrated in the following example:</span></span>
    -   `System.Devices.LaunchDeviceStageFromExplorer:=System.StructuredQueryType.Boolean#True`
-   <span data-ttu-id="dec46-185">Pour les valeurs littérales telles que des mots ou des expressions, la syntaxe canonique est la même que la syntaxe normale.</span><span class="sxs-lookup"><span data-stu-id="dec46-185">For literal values such as words or phrases, the canonical syntax is the same as the regular syntax.</span></span> <span data-ttu-id="dec46-186">Voici quelques exemples de requêtes avec des valeurs littérales dans la syntaxe canonique :</span><span class="sxs-lookup"><span data-stu-id="dec46-186">Examples of queries with literal values in canonical syntax are:</span></span>
    -   `System.Author:sanjay`
    -   `System.Keywords:"Animal"`
    -   `System.FileCount:>100`

> [!Note]  
> <span data-ttu-id="dec46-187">Il n’existe aucune syntaxe canonique pour les nombres dans Windows 7 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="dec46-187">There is no canonical syntax for numbers in Windows 7 and later.</span></span> <span data-ttu-id="dec46-188">Étant donné que les formats à virgule flottante varient selon les paramètres régionaux, l’utilisation d’une requête canonique qui implique une constante à virgule flottante n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="dec46-188">Because floating point formats vary among locales, the use of a canonical query that involves a floating point constant is not supported.</span></span> <span data-ttu-id="dec46-189">Les constantes entières, en revanche, peuvent être écrites en utilisant uniquement des chiffres (pas de séparateurs pour les milliers) et peuvent être utilisées en toute sécurité dans des requêtes canoniques dans Windows 7 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="dec46-189">Integer constants, in contrast, can be written using only digits (no separators for thousands) and can be safely used in canonical queries in Windows 7 and later.</span></span>

 

### <a name="examples"></a><span data-ttu-id="dec46-190">Exemples</span><span class="sxs-lookup"><span data-stu-id="dec46-190">Examples</span></span>

<span data-ttu-id="dec46-191">Le tableau suivant présente quelques exemples de propriétés canoniques et la syntaxe permettant de les utiliser.</span><span class="sxs-lookup"><span data-stu-id="dec46-191">The following table shows some examples of canonical properties and the syntax for using them.</span></span>



| <span data-ttu-id="dec46-192">Type de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="dec46-192">Type of canonical property</span></span> | <span data-ttu-id="dec46-193">Exemple</span><span class="sxs-lookup"><span data-stu-id="dec46-193">Example</span></span>                                                                                     | <span data-ttu-id="dec46-194">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dec46-194">Syntax</span></span>                                                                                                                                                                                                                                                  |
|----------------------------|---------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dec46-195">Valeur de chaîne</span><span class="sxs-lookup"><span data-stu-id="dec46-195">String value</span></span>               | [<span data-ttu-id="dec46-196">System.Author</span><span class="sxs-lookup"><span data-stu-id="dec46-196">System.Author</span></span>](../properties/props-system-author.md)<br/>    | <span data-ttu-id="dec46-197">La valeur de chaîne est recherchée dans la propriété auteur :</span><span class="sxs-lookup"><span data-stu-id="dec46-197">The string value is searched for in the author property:</span></span> <br/>`System.Author:Jacobs`                                                                                                                                                              |
| <span data-ttu-id="dec46-198">Plage d’énumération</span><span class="sxs-lookup"><span data-stu-id="dec46-198">Enumeration range</span></span>          | [<span data-ttu-id="dec46-199">System. Priority</span><span class="sxs-lookup"><span data-stu-id="dec46-199">System.Priority</span></span>](../properties/props-system-priority.md)             | <span data-ttu-id="dec46-200">La propriété Priority peut avoir une plage de valeurs numériques :</span><span class="sxs-lookup"><span data-stu-id="dec46-200">The priority property can have a numerical value range:</span></span><br/>`System.Priority:System.Priority#High`                                                                                                                                                |
| <span data-ttu-id="dec46-201">Boolean</span><span class="sxs-lookup"><span data-stu-id="dec46-201">Boolean</span></span>                    | [<span data-ttu-id="dec46-202">System. IsDeleted</span><span class="sxs-lookup"><span data-stu-id="dec46-202">System.IsDeleted</span></span>](../properties/props-system-isdeleted.md)<br/> | <span data-ttu-id="dec46-203">Les valeurs booléennes peuvent être utilisées avec n’importe quelle propriété booléenne :</span><span class="sxs-lookup"><span data-stu-id="dec46-203">Boolean values can be used with any Boolean property:</span></span><br/><span data-ttu-id="dec46-204">`System.IsDeleted:System.StructuredQueryType.Boolean#True`, et `System.IsDeleted:System.StructuredQueryType.Boolean#False`</span><span class="sxs-lookup"><span data-stu-id="dec46-204">`System.IsDeleted:System.StructuredQueryType.Boolean#True`, and `System.IsDeleted:System.StructuredQueryType.Boolean#False`</span></span>                                                             |
| <span data-ttu-id="dec46-205">Numérique</span><span class="sxs-lookup"><span data-stu-id="dec46-205">Numerical</span></span>                  | [<span data-ttu-id="dec46-206">System. Size</span><span class="sxs-lookup"><span data-stu-id="dec46-206">System.Size</span></span>](../properties/props-system-size.md)<br/>      | <span data-ttu-id="dec46-207">Il n’est pas possible d’écrire en toute sécurité une requête canonique qui implique une constante à virgule flottante, car les formats à virgule flottante varient selon les paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="dec46-207">It is not possible to write safely a canonical query that involves a floating point constant, because floating point formats vary among locales.</span></span> <span data-ttu-id="dec46-208">Les entiers doivent être écrits sans séparateurs pour les milliers.</span><span class="sxs-lookup"><span data-stu-id="dec46-208">Integers must be written with no separators for thousands.</span></span> <span data-ttu-id="dec46-209">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="dec46-209">For example:</span></span><br/>`System.Size:<12345` |



 

<span data-ttu-id="dec46-210">Pour plus d’informations sur les propriétés canoniques et le système de propriétés, consultez [Propriétés système](../properties/props.md).</span><span class="sxs-lookup"><span data-stu-id="dec46-210">For more information about canonical properties and the property system generally, see [System Properties](../properties/props.md).</span></span> <span data-ttu-id="dec46-211">Vous pouvez également faire référence aux fichiers d’en-tête publics.</span><span class="sxs-lookup"><span data-stu-id="dec46-211">Alternatively, refer to the public header files.</span></span>

### <a name="query-operators"></a><span data-ttu-id="dec46-212">Opérateurs de requête</span><span class="sxs-lookup"><span data-stu-id="dec46-212">Query Operators</span></span>

<span data-ttu-id="dec46-213">Si une propriété, p, a plusieurs valeurs pour un élément, une requête AQS pour p : <restr> retourne l’élément si <restr> a la **valeur true** pour au moins l’une des valeurs.</span><span class="sxs-lookup"><span data-stu-id="dec46-213">If a property, p, has multiple values for some item, an AQS query for p:<restr> returns the item if <restr> is **true** for at least one of the values.</span></span> <span data-ttu-id="dec46-214">( <restr> représente une restriction.)</span><span class="sxs-lookup"><span data-stu-id="dec46-214">(<restr> represents a restriction.)</span></span>

<span data-ttu-id="dec46-215">La syntaxe indiquée dans le tableau ci-dessous se compose d’un opérateur, d’un symbole d’opérateur, d’un exemple et d’une description d’exemple.</span><span class="sxs-lookup"><span data-stu-id="dec46-215">The syntax listed in the following table consists of an operator, operator symbol, example and example description.</span></span> <span data-ttu-id="dec46-216">L’opérateur et le symbole peuvent être utilisés dans n’importe quel langage et inclus dans n’importe quelle requête.</span><span class="sxs-lookup"><span data-stu-id="dec46-216">The operator and symbol can be used in any language and included in any query.</span></span> <span data-ttu-id="dec46-217">N’utilisez pas les \_ opérateurs spécifiques à l’application COP implicite ou COP \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="dec46-217">Do not use the COP\_IMPLICIT or COP\_APPLICATION\_SPECIFIC operators.</span></span> <span data-ttu-id="dec46-218">Certains des opérateurs ont des symboles interchangeables.</span><span class="sxs-lookup"><span data-stu-id="dec46-218">Some of the operators have interchangeable symbols.</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="dec46-219">Opérateur</span><span class="sxs-lookup"><span data-stu-id="dec46-219">Operator</span></span></th>
<th><span data-ttu-id="dec46-220">Symbole</span><span class="sxs-lookup"><span data-stu-id="dec46-220">Symbol</span></span></th>
<th><span data-ttu-id="dec46-221">Exemple</span><span class="sxs-lookup"><span data-stu-id="dec46-221">Example</span></span></th>
<th><span data-ttu-id="dec46-222">Description</span><span class="sxs-lookup"><span data-stu-id="dec46-222">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dec46-223">COP_EQUAL</span><span class="sxs-lookup"><span data-stu-id="dec46-223">COP_EQUAL</span></span></td>
<td>=<br/></td>
<td><span data-ttu-id="dec46-224">System. FileExtension : = &quot; . txt&quot;</span><span class="sxs-lookup"><span data-stu-id="dec46-224">System.FileExtension:=&quot;.txt&quot;</span></span><br/></td>
<td><span data-ttu-id="dec46-225">La valeur est le String &quot; <em>. txt</em> &quot; .</span><span class="sxs-lookup"><span data-stu-id="dec46-225">The value is the string &quot;<em>.txt</em>&quot;.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dec46-226">COP_NOTEQUAL</span><span class="sxs-lookup"><span data-stu-id="dec46-226">COP_NOTEQUAL</span></span></td>
<td><span data-ttu-id="dec46-227">≠</span><span class="sxs-lookup"><span data-stu-id="dec46-227">≠</span></span><br/> -<br/> &lt;&gt;<br/> <span data-ttu-id="dec46-228">NOT</span><span class="sxs-lookup"><span data-stu-id="dec46-228">NOT</span></span><br/> - -<br/></td>
<td><span data-ttu-id="dec46-229">System. Kind : image ≠</span><span class="sxs-lookup"><span data-stu-id="dec46-229">System.Kind:≠picture</span></span><br/> <span data-ttu-id="dec46-230">System. photo. DateTaken :-[] ¹</span><span class="sxs-lookup"><span data-stu-id="dec46-230">System.Photo.DateTaken:-[]¹</span></span><br/> <span data-ttu-id="dec46-231">System. Kind : &lt; &gt; image</span><span class="sxs-lookup"><span data-stu-id="dec46-231">System.Kind:&lt;&gt;picture</span></span><br/> <span data-ttu-id="dec46-232">System. Kind : pas d’image</span><span class="sxs-lookup"><span data-stu-id="dec46-232">System.Kind:NOT picture</span></span><br/> <span data-ttu-id="dec46-233">System. Kind :--image</span><span class="sxs-lookup"><span data-stu-id="dec46-233">System.Kind:- -picture</span></span><br/></td>
<td><span data-ttu-id="dec46-234">La propriété <a href="/windows/desktop/properties/props-system-kind">System. Kind</a> n’est pas une image.</span><span class="sxs-lookup"><span data-stu-id="dec46-234">The <a href="/windows/desktop/properties/props-system-kind">System.Kind</a> property is not a picture.</span></span><br/> <span data-ttu-id="dec46-235">La propriété <a href="/windows/desktop/properties/props-system-photo-datetaken">System. photo. DateTaken</a> a une valeur.</span><span class="sxs-lookup"><span data-stu-id="dec46-235">The <a href="/windows/desktop/properties/props-system-photo-datetaken">System.Photo.DateTaken</a> property has a value.</span></span><br/> <span data-ttu-id="dec46-236">La propriété <a href="/windows/desktop/properties/props-system-kind">System. Kind</a> n’est pas une image.</span><span class="sxs-lookup"><span data-stu-id="dec46-236">The <a href="/windows/desktop/properties/props-system-kind">System.Kind</a> property is not a picture.</span></span> <br/> <span data-ttu-id="dec46-237">La propriété <a href="/windows/desktop/properties/props-system-kind">System. Kind</a> n’est pas une image.</span><span class="sxs-lookup"><span data-stu-id="dec46-237">The <a href="/windows/desktop/properties/props-system-kind">System.Kind</a> property is not a picture.</span></span> <br/> <span data-ttu-id="dec46-238">Les opérateurs double NOT appliqués à la même propriété n’annulent pas. Par conséquent, System. Kind :--image est équivalent à System. Kind :-image et System. Kind : pas Picture.</span><span class="sxs-lookup"><span data-stu-id="dec46-238">Double NOT operators applied to the same property do not cancel out. Hence, System.Kind:- -picture is equivalent to System.Kind:-picture and System.Kind:NOT picture.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dec46-239">COP_LESSTHAN</span><span class="sxs-lookup"><span data-stu-id="dec46-239">COP_LESSTHAN</span></span></td>
<td>&lt;<br/></td>
<td><span data-ttu-id="dec46-240">System. taille : 1 &lt; Ko</span><span class="sxs-lookup"><span data-stu-id="dec46-240">System.Size:&lt;1kb</span></span><br/></td>
<td><span data-ttu-id="dec46-241">Cette valeur est inférieure à 1 <em>Ko</em>.</span><span class="sxs-lookup"><span data-stu-id="dec46-241">This value is less than <em>1kb</em>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dec46-242">COP_GREATERTHAN</span><span class="sxs-lookup"><span data-stu-id="dec46-242">COP_GREATERTHAN</span></span></td>
<td>&gt;<br/></td>
<td><span data-ttu-id="dec46-243">System. ItemDate : &gt; System. StructuredQueryType. DateTime # Today</span><span class="sxs-lookup"><span data-stu-id="dec46-243">System.ItemDate:&gt;System.StructuredQueryType.DateTime#Today</span></span><br/></td>
<td><span data-ttu-id="dec46-244">Cette valeur est supérieure à la <em>date du jour</em>.</span><span class="sxs-lookup"><span data-stu-id="dec46-244">This value is greater than <em>today</em>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dec46-245">COP_LESSTHANOREQUAL</span><span class="sxs-lookup"><span data-stu-id="dec46-245">COP_LESSTHANOREQUAL</span></span></td>
<td>&lt;=<br/> <span data-ttu-id="dec46-246">≤</span><span class="sxs-lookup"><span data-stu-id="dec46-246">≤</span></span><br/></td>
<td><span data-ttu-id="dec46-247">System. Size : &lt; = 1 Ko</span><span class="sxs-lookup"><span data-stu-id="dec46-247">System.Size:&lt;=1kb</span></span><br/></td>
<td><span data-ttu-id="dec46-248">Cette valeur est inférieure ou égale à 1 <em>Ko</em>.</span><span class="sxs-lookup"><span data-stu-id="dec46-248">This value is less than or equal to <em>1kb</em>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dec46-249">COP_GREATERTHANOREQUAL</span><span class="sxs-lookup"><span data-stu-id="dec46-249">COP_GREATERTHANOREQUAL</span></span></td>
<td>&gt;=<br/> <span data-ttu-id="dec46-250">≥</span><span class="sxs-lookup"><span data-stu-id="dec46-250">≥</span></span><br/></td>
<td><span data-ttu-id="dec46-251">System. Size : &gt; = 1 Ko</span><span class="sxs-lookup"><span data-stu-id="dec46-251">System.Size:&gt;=1kb</span></span><br/></td>
<td><span data-ttu-id="dec46-252">Cette valeur est supérieure ou égale à 1 <em>Ko</em>.</span><span class="sxs-lookup"><span data-stu-id="dec46-252">This value is equal to or greater than <em>1kb</em>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dec46-253">COP_VALUE_STARTSWITH</span><span class="sxs-lookup"><span data-stu-id="dec46-253">COP_VALUE_STARTSWITH</span></span></td>
<td>~&lt;<br/></td>
<td><span data-ttu-id="dec46-254">System. FileName : ~ &lt; &quot; Introduction à C++&quot;</span><span class="sxs-lookup"><span data-stu-id="dec46-254">System.FileName:~&lt;&quot;C++ Primer&quot;</span></span><br/></td>
<td><span data-ttu-id="dec46-255">Recherche les éléments dont le nom de fichier commence par les caractères de l' &quot; <em>initiation C++</em> &quot; .</span><span class="sxs-lookup"><span data-stu-id="dec46-255">Finds items where the file name begins with the characters &quot;<em>C++ Primer</em>&quot;.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dec46-256">COP_VALUE_ENDSWITH</span><span class="sxs-lookup"><span data-stu-id="dec46-256">COP_VALUE_ENDSWITH</span></span></td>
<td>~&gt;<br/></td>
<td><span data-ttu-id="dec46-257">System. photo. CameraModel : ~ &gt; non</span><span class="sxs-lookup"><span data-stu-id="dec46-257">System.Photo.CameraModel:~&gt;non</span></span><br/></td>
<td><span data-ttu-id="dec46-258">Recherche les éléments dont la valeur de propriété se termine par les caractères <em>non</em>.</span><span class="sxs-lookup"><span data-stu-id="dec46-258">Finds items where the property value ends with the characters <em>non</em>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dec46-259">COP_VALUE_CONTAINS</span><span class="sxs-lookup"><span data-stu-id="dec46-259">COP_VALUE_CONTAINS</span></span></td>
<td>~=<br/> ~~<br/></td>
<td><span data-ttu-id="dec46-260">System. Subject. ~ = arrondi</span><span class="sxs-lookup"><span data-stu-id="dec46-260">System.Subject.~=round</span></span> <br/> <span data-ttu-id="dec46-261">System. Search. AutoSummary : ~ ~ Round</span><span class="sxs-lookup"><span data-stu-id="dec46-261">System.Search.Autosummary:~~round</span></span><br/></td>
<td><span data-ttu-id="dec46-262">Recherche un message qui a cette chaîne dans l’objet et correspond aux &quot; règles d'<em>arrondi</em> g, &quot; par exemple.</span><span class="sxs-lookup"><span data-stu-id="dec46-262">Finds a message that has this string in the subject, and will match &quot;g<em>round</em> rules&quot; for example.</span></span><br/> <span data-ttu-id="dec46-263">Recherche tous les éléments avec un résumé qui contient les caractères <em>arrondis</em>.</span><span class="sxs-lookup"><span data-stu-id="dec46-263">Finds all items with an Autosummary that contains the characters <em>round</em>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dec46-264">COP_VALUE_NOTCONTAINS</span><span class="sxs-lookup"><span data-stu-id="dec46-264">COP_VALUE_NOTCONTAINS</span></span></td>
<td><span data-ttu-id="dec46-265">~!</span><span class="sxs-lookup"><span data-stu-id="dec46-265">~!</span></span><br/></td>
<td><span data-ttu-id="dec46-266">System. Author : ~ ! &quot; Sanjay&quot;</span><span class="sxs-lookup"><span data-stu-id="dec46-266">System.Author:~!&quot;sanjay&quot;</span></span><br/></td>
<td><span data-ttu-id="dec46-267">Recherche les auteurs qui n’ont pas de séquence &quot; de caractères<em>Sanjay</em> &quot; .</span><span class="sxs-lookup"><span data-stu-id="dec46-267">Finds authors that do not have the character sequence&quot;<em>sanjay</em>&quot; in them.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dec46-268">COP_DOSWILDCARDS</span><span class="sxs-lookup"><span data-stu-id="dec46-268">COP_DOSWILDCARDS</span></span></td>
<td>~ <br/></td>
<td><span data-ttu-id="dec46-269">System. FileName : ~ &quot; MIC ? osoft W \* d&quot;</span><span class="sxs-lookup"><span data-stu-id="dec46-269">System.FileName:~&quot;Mic?osoft W\*d&quot;</span></span><br/></td>
<td><span data-ttu-id="dec46-270">Recherche les fichiers dont le nom de fichier commence par <em>MIC</em>, suivi d’un caractère, suivi de <em>osoft w</em>, suivi de tous les caractères se terminant par <em>d</em>.</span><span class="sxs-lookup"><span data-stu-id="dec46-270">Finds files where the file name starts with <em>Mic</em>, followed by some character, followed by <em>osoft w</em>, followed by any characters ending with <em>d</em>.</span></span> <br/> <span data-ttu-id="dec46-271">Le point d’interrogation, ?,</span><span class="sxs-lookup"><span data-stu-id="dec46-271">The ?</span></span> <span data-ttu-id="dec46-272">les caractères et \* ne sont pas interprétés littéralement, et fonctionnent comme des caractères génériques de type DOS :</span><span class="sxs-lookup"><span data-stu-id="dec46-272">and \* characters are not interpreted literally, and work like DOS-style wildcard characters:</span></span><br/>
<ul>
<li><span data-ttu-id="dec46-273">?</span><span class="sxs-lookup"><span data-stu-id="dec46-273">?</span></span> <span data-ttu-id="dec46-274">correspond à un caractère arbitraire.</span><span class="sxs-lookup"><span data-stu-id="dec46-274">matches one arbitrary character.</span></span></li>
<li><span data-ttu-id="dec46-275">\* correspond à zéro ou plusieurs caractères arbitraires.</span><span class="sxs-lookup"><span data-stu-id="dec46-275">\* matches zero or more arbitrary characters.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dec46-276">COP_WORD_EQUAL</span><span class="sxs-lookup"><span data-stu-id="dec46-276">COP_WORD_EQUAL</span></span></td>
<td>$=<br/> $$<br/></td>
<td><span data-ttu-id="dec46-277">System. StructuredQuery. Virtual. from : $ = &quot; Sanjay Jacobs&quot;</span><span class="sxs-lookup"><span data-stu-id="dec46-277">System.StructuredQuery.Virtual.From:$=&quot;Sanjay Jacobs&quot;</span></span><br/></td>
<td><span data-ttu-id="dec46-278">Pour Windows 7 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="dec46-278">For Windows 7 and later.</span></span> <span data-ttu-id="dec46-279">Recherche l’expression &quot; <em>Sanjay Jacobs</em> &quot; dans toutes les propriétés.</span><span class="sxs-lookup"><span data-stu-id="dec46-279">Finds the phrase &quot;<em>Sanjay Jacobs</em>&quot; in all From properties.</span></span> <span data-ttu-id="dec46-280">Le mot <em>Sanjay</em> doit être suivi du mot <em>Jacobs</em>.</span><span class="sxs-lookup"><span data-stu-id="dec46-280">The word <em>Sanjay</em> must be followed by the word <em>Jacobs</em>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dec46-281">COP_WORD_STARTSWITH</span><span class="sxs-lookup"><span data-stu-id="dec46-281">COP_WORD_STARTSWITH</span></span></td>
<td>$<<br/></td>
<td><span data-ttu-id="dec46-282">System. Author : $</span><span class="sxs-lookup"><span data-stu-id="dec46-282">System.Author:$</span></span><&quot;San&quot; System.Filename:$<&quot;Micro Exe&quot;<br/></td>
<td><span data-ttu-id="dec46-283">Pour Windows 7 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="dec46-283">For Windows 7 and later.</span></span> <span data-ttu-id="dec46-284">Recherche un élément où Author contient un mot commençant par les caractères &quot; <em>San</em> &quot; .</span><span class="sxs-lookup"><span data-stu-id="dec46-284">Finds any item where Author contains a word starting with the characters &quot;<em>San</em>&quot;.</span></span><br/> <span data-ttu-id="dec46-285">Recherche tout fichier dans lequel le nom de fichier contient un mot commençant par <em>micro</em>, suivi d’un mot commençant par <em>exe</em>.</span><span class="sxs-lookup"><span data-stu-id="dec46-285">Finds any file in which the file name contains a word starting with <em>micro</em>, followed by a word starting with <em>exe</em>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="dec46-286">¹ les crochets vides ( \[ \] ) indiquent « aucune valeur ».</span><span class="sxs-lookup"><span data-stu-id="dec46-286">¹ Empty square brackets (\[\]) denote "no value".</span></span>

<span data-ttu-id="dec46-287">Pour les propriétés de type chaîne, l’opération par défaut est COP \_ Word \_ commence \_ par ou COP \_ Word \_ EQUAL.</span><span class="sxs-lookup"><span data-stu-id="dec46-287">For string properties the default operation is either COP\_WORD\_STARTS\_WITH or COP\_WORD\_EQUAL.</span></span>

### <a name="query-values"></a><span data-ttu-id="dec46-288">Valeurs de requête</span><span class="sxs-lookup"><span data-stu-id="dec46-288">Query Values</span></span>

<span data-ttu-id="dec46-289">Le tableau suivant répertorie des exemples utiles de restriction des valeurs de requête.</span><span class="sxs-lookup"><span data-stu-id="dec46-289">Useful examples of how query values can be restricted are listed in the following table.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="dec46-290">Valeur/symbole</span><span class="sxs-lookup"><span data-stu-id="dec46-290">Value/symbol</span></span></th>
<th><span data-ttu-id="dec46-291">Exemples</span><span class="sxs-lookup"><span data-stu-id="dec46-291">Examples</span></span></th>
<th><span data-ttu-id="dec46-292">Description</span><span class="sxs-lookup"><span data-stu-id="dec46-292">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dec46-293">String</span><span class="sxs-lookup"><span data-stu-id="dec46-293">String</span></span></td>
<td><span data-ttu-id="dec46-294">auto</span><span class="sxs-lookup"><span data-stu-id="dec46-294">auto</span></span><br/></td>
<td><span data-ttu-id="dec46-295">Séquence de caractères qui peut être recherchée.</span><span class="sxs-lookup"><span data-stu-id="dec46-295">Any sequence of characters that can be searched for.</span></span> <span data-ttu-id="dec46-296">La chaîne ne doit pas contenir d’espaces blancs ou de combinaisons de caractères qui font partie de la syntaxe.</span><span class="sxs-lookup"><span data-stu-id="dec46-296">The string must not contain whitespace or character combinations that are part of the syntax.</span></span> <span data-ttu-id="dec46-297">Cet exemple recherche un mot commençant par <em>auto</em>.</span><span class="sxs-lookup"><span data-stu-id="dec46-297">This example searches for a word beginning with <em>auto</em>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dec46-298">Chaîne entre guillemets &quot;&quot;</span><span class="sxs-lookup"><span data-stu-id="dec46-298">Quoted string &quot;&quot;</span></span></td>
<td><span data-ttu-id="dec46-299">&quot;Conclusions : validez &quot; &quot; l' &quot; &quot; &quot; &quot; équipe Blue Team&quot;</span><span class="sxs-lookup"><span data-stu-id="dec46-299">&quot;Conclusions: valid&quot; &quot;The &quot;&quot;blue&quot;&quot; team&quot;</span></span><br/></td>
<td><span data-ttu-id="dec46-300">Toute séquence de caractères.</span><span class="sxs-lookup"><span data-stu-id="dec46-300">Any sequence of characters.</span></span> <span data-ttu-id="dec46-301">La chaîne n’est pas interprétée dans le cadre de la syntaxe.</span><span class="sxs-lookup"><span data-stu-id="dec46-301">The string is not interpreted as part of the syntax.</span></span><br/> <span data-ttu-id="dec46-302">Les guillemets peuvent être inclus dans une requête s’ils sont doublés.</span><span class="sxs-lookup"><span data-stu-id="dec46-302">Quotation marks can be included in a query if they are doubled.</span></span> <span data-ttu-id="dec46-303">Cet exemple recherche <em>l' &quot; &quot; équipe bleue</em>.</span><span class="sxs-lookup"><span data-stu-id="dec46-303">This example searches for <em>The &quot;blue&quot; team</em>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dec46-304">Integer</span><span class="sxs-lookup"><span data-stu-id="dec46-304">Integer</span></span></td>
<td><span data-ttu-id="dec46-305">5678</span><span class="sxs-lookup"><span data-stu-id="dec46-305">5678</span></span><br/></td>
<td><span data-ttu-id="dec46-306">Utilisez uniquement des chiffres pour les entiers.</span><span class="sxs-lookup"><span data-stu-id="dec46-306">Use only digits for integers.</span></span> <span data-ttu-id="dec46-307">N’utilisez pas de séparateurs pour les milliers.</span><span class="sxs-lookup"><span data-stu-id="dec46-307">Do not use any separators for thousands.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dec46-308">Nombre à virgule flottante</span><span class="sxs-lookup"><span data-stu-id="dec46-308">Floating point number</span></span></td>
<td><span data-ttu-id="dec46-309">5678,1234</span><span class="sxs-lookup"><span data-stu-id="dec46-309">5678.1234</span></span><br/></td>
<td><span data-ttu-id="dec46-310">Étant donné que les formats à virgule flottante varient selon les paramètres régionaux, une requête canonique ne peut pas utiliser une constante à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="dec46-310">Because floating point formats vary among locales, a canonical query cannot use a floating point constant.</span></span> <span data-ttu-id="dec46-311">L’utilisation de la syntaxe canonique avec des nombres à virgule flottante n’est pas sécurisée pour la localisation.</span><span class="sxs-lookup"><span data-stu-id="dec46-311">The use of canonical syntax with floating point numbers is not localization safe.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dec46-312">Booléen <strong>true</strong> / <strong>false</strong></span><span class="sxs-lookup"><span data-stu-id="dec46-312">Boolean <strong>true</strong>/<strong>false</strong></span></span></td>
<td><span data-ttu-id="dec46-313">System. IsRead : = System. StructuredQueryType. Boolean # true</span><span class="sxs-lookup"><span data-stu-id="dec46-313">System.IsRead:=System.StructuredQueryType.Boolean#True</span></span><br/> <span data-ttu-id="dec46-314">System. IsEncrypted :-System. StructuredQueryType. Boolean # False</span><span class="sxs-lookup"><span data-stu-id="dec46-314">System.IsEncrypted:-System.StructuredQueryType.Boolean#False</span></span><br/></td>
<td><span data-ttu-id="dec46-315">Valeur booléenne <strong>true</strong> .</span><span class="sxs-lookup"><span data-stu-id="dec46-315">The <strong>TRUE</strong> Boolean value.</span></span><br/> <span data-ttu-id="dec46-316">Valeur booléenne <strong>false</strong> .</span><span class="sxs-lookup"><span data-stu-id="dec46-316">The <strong>FALSE</strong> Boolean value.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dec46-317">[]</span><span class="sxs-lookup"><span data-stu-id="dec46-317">[]</span></span></td>
<td><span data-ttu-id="dec46-318">System. Keywords : = []</span><span class="sxs-lookup"><span data-stu-id="dec46-318">System.Keywords:=[]</span></span><br/></td>
<td><span data-ttu-id="dec46-319">Les crochets vides indiquent qu’il n’y a aucune valeur.</span><span class="sxs-lookup"><span data-stu-id="dec46-319">Empty square brackets denote that there is no value.</span></span> <span data-ttu-id="dec46-320">Cet exemple recherche tous les éléments qui n’ont pas été balisés.</span><span class="sxs-lookup"><span data-stu-id="dec46-320">This example finds all items that have not been tagged.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dec46-321">Dates absolues</span><span class="sxs-lookup"><span data-stu-id="dec46-321">Absolute dates</span></span></td>
<td><span data-ttu-id="dec46-322">System. ItemDate : 1/26/2010</span><span class="sxs-lookup"><span data-stu-id="dec46-322">System.ItemDate:1/26/2010</span></span><br/> <span data-ttu-id="dec46-323">SystemDateModified 10/15/2002 19:00</span><span class="sxs-lookup"><span data-stu-id="dec46-323">SystemDateModified 10/15/2002 19:00</span></span><br/></td>
<td><span data-ttu-id="dec46-324">Recherche les éléments dont la date est le 26 janvier 2010.</span><span class="sxs-lookup"><span data-stu-id="dec46-324">Finds items with a date of 26 January 2010.</span></span><br/> <span data-ttu-id="dec46-325">Recherche les éléments qui ont été modifiés le 15 octobre 2002 entre les heures 19:00:00 et 19:00:59.</span><span class="sxs-lookup"><span data-stu-id="dec46-325">Finds items that were modified on 15 October 2002 between the hours 19:00:00 and 19:00:59.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="dec46-326">Étant donné que les formats de date (comme les formats à virgule flottante) varient selon les paramètres régionaux, l’utilisation de la syntaxe canonique avec des dates absolues n’est pas prise en charge et n’est pas sécurisée pour la localisation.</span><span class="sxs-lookup"><span data-stu-id="dec46-326">Because date formats (like floating point formats) vary among locales, the use of canonical syntax with absolute dates is not supported and is not localization safe.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dec46-327">Dates relatives</span><span class="sxs-lookup"><span data-stu-id="dec46-327">Relative dates</span></span></td>
<td><span data-ttu-id="dec46-328">System. ItemDate : System. StructuredQueryType. DateTime # Today</span><span class="sxs-lookup"><span data-stu-id="dec46-328">System.ItemDate:System.StructuredQueryType.DateTime#Today</span></span><br/> <span data-ttu-id="dec46-329">System. DateAcquired : System. StructuredQueryType. DateTime # NextMonth</span><span class="sxs-lookup"><span data-stu-id="dec46-329">System.DateAcquired:System.StructuredQueryType.DateTime#NextMonth</span></span><br/> <span data-ttu-id="dec46-330">System. message. DateReceived : System. StructuredQueryType. DateTime # LastYear</span><span class="sxs-lookup"><span data-stu-id="dec46-330">System.Message.DateReceived:System.StructuredQueryType.DateTime#LastYear</span></span><br/></td>
<td><span data-ttu-id="dec46-331">Recherche des éléments avec la date du jour.</span><span class="sxs-lookup"><span data-stu-id="dec46-331">Finds items with today's date.</span></span><br/> <span data-ttu-id="dec46-332">Recherche les éléments dont la date est le mois suivant.</span><span class="sxs-lookup"><span data-stu-id="dec46-332">Finds items with a date in the next month.</span></span><br/> <span data-ttu-id="dec46-333">Recherche les éléments dont la date est l’année dernière.</span><span class="sxs-lookup"><span data-stu-id="dec46-333">Finds items with a date in the last year.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="dec46-334">En plus de la recherche de dates et de plages de dates spécifiques, AQS reconnaît les valeurs de date relatives (comme <em>aujourd’hui</em>, <em>demain</em>, <em>nextweek</em>, <em>nextMonth</em>) et le jour (par exemple, <em>mardi</em> ou <em>lundi. Mercredi</em>) et mois (<em>février</em>).</span><span class="sxs-lookup"><span data-stu-id="dec46-334">In addition to searching on specific dates and date ranges, AQS recognizes relative date values (like <em>today</em>, <em>tomorrow</em>, <em>nextweek</em>, <em>nextmonth</em>), and day (like <em>Tuesday</em> or <em>Monday..Wednesday</em>), and month (<em>February</em>).</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dec46-335">..</span><span class="sxs-lookup"><span data-stu-id="dec46-335">..</span></span></td>
<td><span data-ttu-id="dec46-336">System. ItemDate : 11/05/04.. 11/10/04 System. Size : 5 Ko.. 10 Ko</span><span class="sxs-lookup"><span data-stu-id="dec46-336">System.ItemDate:11/05/04..11/10/04 System.Size:5kb..10kb</span></span><br/></td>
<td><span data-ttu-id="dec46-337">Les doubles périodes indiquent une plage de valeurs.</span><span class="sxs-lookup"><span data-stu-id="dec46-337">Double periods indicate a value range.</span></span> <span data-ttu-id="dec46-338">Recherche les éléments dont la date est comprise entre 11/05/04 et 11/10/04 inclus.</span><span class="sxs-lookup"><span data-stu-id="dec46-338">Finds items with a date between 11/05/04 and 11/10/04, inclusive.</span></span><br/> <span data-ttu-id="dec46-339">Recherche les éléments d’une taille comprise entre 5 et 10KO.</span><span class="sxs-lookup"><span data-stu-id="dec46-339">Finds items between 5 and 10kb in size.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="scope-restrictions"></a><span data-ttu-id="dec46-340">Restrictions d’étendue</span><span class="sxs-lookup"><span data-stu-id="dec46-340">Scope Restrictions</span></span>

<span data-ttu-id="dec46-341">Les utilisateurs peuvent limiter l’étendue de leurs recherches à des emplacements de dossiers ou des magasins de données spécifiques.</span><span class="sxs-lookup"><span data-stu-id="dec46-341">Users can limit the scope of their searches to specific folder locations or data stores.</span></span> <span data-ttu-id="dec46-342">Par exemple, si vous utilisez plusieurs comptes de messagerie et que vous souhaitez limiter une requête à Microsoft Outlook ou Microsoft Outlook Express, vous pouvez utiliser `System.Search.Store:mapi` ou `System.Search.Store:oe` respectivement.</span><span class="sxs-lookup"><span data-stu-id="dec46-342">For example, if you use several email accounts and you want to limit a query to either Microsoft Outlook or Microsoft Outlook Express, you can use `System.Search.Store:mapi` or `System.Search.Store:oe` respectively.</span></span> <span data-ttu-id="dec46-343">Le tableau suivant présente quelques exemples de la manière de limiter une recherche par magasin de données.</span><span class="sxs-lookup"><span data-stu-id="dec46-343">The following table shows some examples of how to restrict a search by data store.</span></span>



| <span data-ttu-id="dec46-344">Limiter la recherche par le magasin de données</span><span class="sxs-lookup"><span data-stu-id="dec46-344">Restrict search by data store</span></span>  | <span data-ttu-id="dec46-345">Mot clé</span><span class="sxs-lookup"><span data-stu-id="dec46-345">Keyword</span></span> | <span data-ttu-id="dec46-346">Exemple</span><span class="sxs-lookup"><span data-stu-id="dec46-346">Example</span></span>                                     |
|--------------------------------|---------|---------------------------------------------|
| <span data-ttu-id="dec46-347">Fichiers</span><span class="sxs-lookup"><span data-stu-id="dec46-347">Files</span></span>                          | <span data-ttu-id="dec46-348">fichier</span><span class="sxs-lookup"><span data-stu-id="dec46-348">file</span></span>    | <span data-ttu-id="dec46-349">System. Search. Store : fichier</span><span class="sxs-lookup"><span data-stu-id="dec46-349">System.Search.Store:file</span></span>                    |
| <span data-ttu-id="dec46-350">Outlook</span><span class="sxs-lookup"><span data-stu-id="dec46-350">Outlook</span></span>                        | <span data-ttu-id="dec46-351">Protocole</span><span class="sxs-lookup"><span data-stu-id="dec46-351">mapi</span></span>    | <span data-ttu-id="dec46-352">System. Search. Store : MAPI</span><span class="sxs-lookup"><span data-stu-id="dec46-352">System.Search.Store:mapi</span></span>                    |
| <span data-ttu-id="dec46-353">Outlook Express</span><span class="sxs-lookup"><span data-stu-id="dec46-353">Outlook Express</span></span>                | <span data-ttu-id="dec46-354">oe</span><span class="sxs-lookup"><span data-stu-id="dec46-354">oe</span></span>      | <span data-ttu-id="dec46-355">System. Search. Store : oe</span><span class="sxs-lookup"><span data-stu-id="dec46-355">System.Search.Store:oe</span></span>                      |
| <span data-ttu-id="dec46-356">Fichiers hors connexion</span><span class="sxs-lookup"><span data-stu-id="dec46-356">Offline files</span></span>                  | <span data-ttu-id="dec46-357">CSC</span><span class="sxs-lookup"><span data-stu-id="dec46-357">csc</span></span>     | <span data-ttu-id="dec46-358">System. Search. Store : CSC</span><span class="sxs-lookup"><span data-stu-id="dec46-358">System.Search.Store:csc</span></span>                     |
| <span data-ttu-id="dec46-359">Dossier spécifique sur le lecteur local</span><span class="sxs-lookup"><span data-stu-id="dec46-359">Specific folder on local drive</span></span> | <span data-ttu-id="dec46-360">dossier</span><span class="sxs-lookup"><span data-stu-id="dec46-360">folder</span></span>  | <span data-ttu-id="dec46-361">System. ItemFolderNameDisplay : C : " \\ mondossier"</span><span class="sxs-lookup"><span data-stu-id="dec46-361">System.ItemFolderNameDisplay:C:"\\MyFolder"</span></span> |



 

## <a name="additional-resources"></a><span data-ttu-id="dec46-362">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="dec46-362">Additional Resources</span></span>

-   <span data-ttu-id="dec46-363">Dans Windows 7 et versions ultérieures, une option de menu contextuel peut être disponible selon qu’une condition AQS est remplie ou non.</span><span class="sxs-lookup"><span data-stu-id="dec46-363">In Windows 7 and later, a shortcut menu option can be available based on whether an AQS condition is met.</span></span> <span data-ttu-id="dec46-364">Pour plus d’informations, consultez « obtention du comportement dynamique pour les verbes statiques à l’aide de la syntaxe de requête avancée » dans [création de gestionnaires de menus contextuels](../shell/context-menu-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="dec46-364">For more information, see "Getting Dynamic Behavior for Static Verbs by Using Advanced Query Syntax" in [Creating Context Menu Handlers](../shell/context-menu-handlers.md).</span></span>
-   <span data-ttu-id="dec46-365">Les requêtes AQS peuvent être limitées à des types de fichiers spécifiques, connus sous le nom de types de fichiers.</span><span class="sxs-lookup"><span data-stu-id="dec46-365">AQS queries can be limited to specific types of files, which are known as file kinds.</span></span> <span data-ttu-id="dec46-366">Pour plus d’informations, consultez [types de fichiers et associations](../shell/fa-intro.md).</span><span class="sxs-lookup"><span data-stu-id="dec46-366">For more information, see [File Types and Associations](../shell/fa-intro.md).</span></span> <span data-ttu-id="dec46-367">Pour obtenir une documentation de référence sur les propriétés, consultez [System. Kind](../properties/props-system-kind.md)et [System. KindText](../properties/props-system-kindtext.md).</span><span class="sxs-lookup"><span data-stu-id="dec46-367">For property reference documentation, see [System.Kind](../properties/props-system-kind.md), and [System.KindText](../properties/props-system-kindtext.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="dec46-368">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dec46-368">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dec46-369">Interrogation de l’index programmatiquement</span><span class="sxs-lookup"><span data-stu-id="dec46-369">Querying the Index Programmatically</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="dec46-370">Utilisation des approches SQL et AQS pour interroger l’index</span><span class="sxs-lookup"><span data-stu-id="dec46-370">Using SQL and AQS Approaches to Query the Index</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="dec46-371">Interrogation de l’index avec ISearchQueryHelper</span><span class="sxs-lookup"><span data-stu-id="dec46-371">Querying the Index with ISearchQueryHelper</span></span>](-search-3x-wds-qryidx-searchqueryhelper.md)
</dt> <dt>

[<span data-ttu-id="dec46-372">Interrogation de l’index avec le protocole search-ms</span><span class="sxs-lookup"><span data-stu-id="dec46-372">Querying the Index with the search-ms Protocol</span></span>](-search-3x-wds-qryidx-searchms.md)
</dt> <dt>

[<span data-ttu-id="dec46-373">Interrogation de l’index avec la syntaxe SQL de Windows Search</span><span class="sxs-lookup"><span data-stu-id="dec46-373">Querying the Index with Windows Search SQL Syntax</span></span>](-search-sql-windowssearch-entry.md)
</dt> </dl>

 

 
