---
title: Syntaxe de filtre de recherche
description: Les filtres de recherche vous permettent de définir des critères de recherche et de fournir des recherches plus efficaces et efficaces.
ms.assetid: 3ce4709c-5ef7-4713-8fb7-b46ab284339f
ms.tgt_platform: multiple
keywords:
- Syntaxe de filtre de recherche ADSI
- requêtes, syntaxe de filtre de recherche
ms.topic: article
ms.date: 09/25/2020
ms.openlocfilehash: 28875bd49a3d1df7418c37706e58852066bbe08a
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/26/2021
ms.locfileid: "106521782"
---
# <a name="search-filter-syntax"></a><span data-ttu-id="0ed22-105">Syntaxe de filtre de recherche</span><span class="sxs-lookup"><span data-stu-id="0ed22-105">Search Filter Syntax</span></span>

<span data-ttu-id="0ed22-106">Les filtres de recherche vous permettent de définir des critères de recherche et de fournir des recherches plus efficaces et efficaces.</span><span class="sxs-lookup"><span data-stu-id="0ed22-106">Search filters enable you to define search criteria and provide more efficient and effective searches.</span></span>

<span data-ttu-id="0ed22-107">ADSI prend en charge les filtres de recherche LDAP tels que définis dans RFC2254.</span><span class="sxs-lookup"><span data-stu-id="0ed22-107">ADSI supports the LDAP search filters as defined in RFC2254.</span></span> <span data-ttu-id="0ed22-108">Ces filtres de recherche sont représentés par des chaînes Unicode.</span><span class="sxs-lookup"><span data-stu-id="0ed22-108">These search filters are represented by Unicode strings.</span></span> <span data-ttu-id="0ed22-109">Le tableau suivant répertorie quelques exemples de filtres de recherche LDAP.</span><span class="sxs-lookup"><span data-stu-id="0ed22-109">The following table lists some examples of LDAP search filters.</span></span>



| <span data-ttu-id="0ed22-110">Filtre de recherche</span><span class="sxs-lookup"><span data-stu-id="0ed22-110">Search filter</span></span>                                                               | <span data-ttu-id="0ed22-111">Description</span><span class="sxs-lookup"><span data-stu-id="0ed22-111">Description</span></span>                                                |
|-----------------------------------------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="0ed22-112">"(objectClass = \* )"</span><span class="sxs-lookup"><span data-stu-id="0ed22-112">"(objectClass=\*)"</span></span>                                                          | <span data-ttu-id="0ed22-113">Tous les objets.</span><span class="sxs-lookup"><span data-stu-id="0ed22-113">All objects.</span></span>                                               |
| <span data-ttu-id="0ed22-114">"(& (objectCategory = person) (objectClass = user) ( ! ( CN = Andy)))»</span><span class="sxs-lookup"><span data-stu-id="0ed22-114">"(&(objectCategory=person)(objectClass=user)(!(cn=andy)))"</span></span>                  | <span data-ttu-id="0ed22-115">Tous les objets utilisateur, mais « Andy ».</span><span class="sxs-lookup"><span data-stu-id="0ed22-115">All user objects but "andy".</span></span>                               |
| <span data-ttu-id="0ed22-116">« (SN = SM \* ) »</span><span class="sxs-lookup"><span data-stu-id="0ed22-116">"(sn=sm\*)"</span></span>                                                                 | <span data-ttu-id="0ed22-117">Tous les objets dont le nom commence par « SM ».</span><span class="sxs-lookup"><span data-stu-id="0ed22-117">All objects with a surname that starts with "sm".</span></span>          |
| <span data-ttu-id="0ed22-118">« (& (objectCategory = person) (objectClass = contact) ( \| (SN = Smith) (SN = Johnson))) »</span><span class="sxs-lookup"><span data-stu-id="0ed22-118">"(&(objectCategory=person)(objectClass=contact)(\|(sn=Smith)(sn=Johnson)))"</span></span> | <span data-ttu-id="0ed22-119">Tous les contacts dont le nom est égal à « Smith » ou « Johnson ».</span><span class="sxs-lookup"><span data-stu-id="0ed22-119">All contacts with a surname equal to "Smith" or "Johnson".</span></span> |



 

<span data-ttu-id="0ed22-120">Ces filtres de recherche utilisent l’un des formats suivants.</span><span class="sxs-lookup"><span data-stu-id="0ed22-120">These search filters use one of the following formats.</span></span>


```C++
<filter>=(<attribute><operator><value>)
```



<span data-ttu-id="0ed22-121">ou</span><span class="sxs-lookup"><span data-stu-id="0ed22-121">or</span></span>


```C++
(<operator><filter1><filter2>)
```



<span data-ttu-id="0ed22-122">Les filtres de recherche ADSI sont utilisés de deux manières.</span><span class="sxs-lookup"><span data-stu-id="0ed22-122">The ADSI search filters are used in two ways.</span></span> <span data-ttu-id="0ed22-123">Ils constituent une partie du dialecte LDAP pour l’envoi de requêtes via le fournisseur OLE DB.</span><span class="sxs-lookup"><span data-stu-id="0ed22-123">They form a part of the LDAP dialect for submitting queries through the OLE DB provider.</span></span> <span data-ttu-id="0ed22-124">Ils sont également utilisés avec l’interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) .</span><span class="sxs-lookup"><span data-stu-id="0ed22-124">They are also used with the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface.</span></span>

## <a name="operators"></a><span data-ttu-id="0ed22-125">Opérateurs</span><span class="sxs-lookup"><span data-stu-id="0ed22-125">Operators</span></span>

<span data-ttu-id="0ed22-126">Le tableau suivant répertorie les opérateurs de filtre de recherche fréquemment utilisés.</span><span class="sxs-lookup"><span data-stu-id="0ed22-126">The following table lists frequently used search filter operators.</span></span>



| <span data-ttu-id="0ed22-127">Opérateur logique</span><span class="sxs-lookup"><span data-stu-id="0ed22-127">Logical operator</span></span> | <span data-ttu-id="0ed22-128">Description</span><span class="sxs-lookup"><span data-stu-id="0ed22-128">Description</span></span>                                |
|------------------|--------------------------------------------|
| =                | <span data-ttu-id="0ed22-129">Égal à</span><span class="sxs-lookup"><span data-stu-id="0ed22-129">Equal to</span></span>                                   |
| ~=               | <span data-ttu-id="0ed22-130">Approximativement égal à</span><span class="sxs-lookup"><span data-stu-id="0ed22-130">Approximately equal to</span></span>                     |
| <=            | <span data-ttu-id="0ed22-131">Vue lexicographique inférieur ou égal à</span><span class="sxs-lookup"><span data-stu-id="0ed22-131">Lexicographically less than or equal to</span></span>    |
| >=            | <span data-ttu-id="0ed22-132">Vue lexicographique supérieur ou égal à</span><span class="sxs-lookup"><span data-stu-id="0ed22-132">Lexicographically greater than or equal to</span></span> |
| &                | <span data-ttu-id="0ed22-133">AND</span><span class="sxs-lookup"><span data-stu-id="0ed22-133">AND</span></span>                                        |
| \|               | <span data-ttu-id="0ed22-134">OR</span><span class="sxs-lookup"><span data-stu-id="0ed22-134">OR</span></span>                                         |
| <span data-ttu-id="0ed22-135">!</span><span class="sxs-lookup"><span data-stu-id="0ed22-135">!</span></span>                | <span data-ttu-id="0ed22-136">NOT</span><span class="sxs-lookup"><span data-stu-id="0ed22-136">NOT</span></span>                                        |



 

<span data-ttu-id="0ed22-137">En plus des opérateurs ci-dessus, LDAP définit deux identificateurs d’objet de règle de correspondance (OID) qui peuvent être utilisés pour effectuer des comparaisons au niveau du bit des valeurs numériques.</span><span class="sxs-lookup"><span data-stu-id="0ed22-137">In addition to the operators above, LDAP defines two matching rule object identifiers (OIDs) that can be used to perform bitwise comparisons of numeric values.</span></span> <span data-ttu-id="0ed22-138">Les règles de correspondance ont la syntaxe suivante.</span><span class="sxs-lookup"><span data-stu-id="0ed22-138">Matching rules have the following syntax.</span></span>


```C++
<attribute name>:<matching rule OID>:=<value>
```



<span data-ttu-id="0ed22-139">« &lt; nom &gt; d’attribut » est le **lDAPDisplayName** de l’attribut, « &lt; la règle OID &gt; » est l’OID de la règle de correspondance et « &lt; valeur &gt; » est la valeur à utiliser pour la comparaison.</span><span class="sxs-lookup"><span data-stu-id="0ed22-139">"&lt;attribute name&gt;" is the **lDAPDisplayName** of the attribute, "&lt;rule OID&gt;" is the OID for the matching rule, and "&lt;value&gt;" is the value to use for comparison.</span></span> <span data-ttu-id="0ed22-140">N’oubliez pas que les espaces ne peuvent pas être utilisés dans cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="0ed22-140">Be aware that spaces cannot be used in this string.</span></span> <span data-ttu-id="0ed22-141">« &lt; value &gt; » doit être un nombre décimal ; il ne peut pas s’agir d’un nombre hexadécimal ou d’un nom de constante, tel que la **\_ sécurité du type de groupe ADS \_ \_ \_ activée**.</span><span class="sxs-lookup"><span data-stu-id="0ed22-141">"&lt;value&gt;" must be a decimal number; it cannot be a hexadecimal number or a constant name such as **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED**.</span></span> <span data-ttu-id="0ed22-142">Pour plus d’informations sur les attributs de Active Directory disponibles, consultez [tous les attributs](/windows/desktop/ADSchema/attributes-all).</span><span class="sxs-lookup"><span data-stu-id="0ed22-142">For more information about the available Active Directory attributes, see [All Attributes](/windows/desktop/ADSchema/attributes-all).</span></span>

<span data-ttu-id="0ed22-143">Le tableau suivant répertorie les OID de règles de correspondance implémentés par LDAP.</span><span class="sxs-lookup"><span data-stu-id="0ed22-143">The following table lists the matching rule OIDs implemented by LDAP.</span></span>



| <span data-ttu-id="0ed22-144">OID de règle de correspondance</span><span class="sxs-lookup"><span data-stu-id="0ed22-144">Matching rule OID</span></span>       | <span data-ttu-id="0ed22-145">Identificateur de chaîne (à partir de Ntldap. h)</span><span class="sxs-lookup"><span data-stu-id="0ed22-145">String identifier (from Ntldap.h)</span></span>   | <span data-ttu-id="0ed22-146">Description</span><span class="sxs-lookup"><span data-stu-id="0ed22-146">Description</span></span>                                                                                                                                                                                   |
|-------------------------|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ed22-147">1.2.840.113556.1.4.803</span><span class="sxs-lookup"><span data-stu-id="0ed22-147">1.2.840.113556.1.4.803</span></span>  | <span data-ttu-id="0ed22-148">**\_ \_ \_ bit de règle de correspondance LDAP \_ et**</span><span class="sxs-lookup"><span data-stu-id="0ed22-148">**LDAP\_MATCHING\_RULE\_BIT\_AND**</span></span>  | <span data-ttu-id="0ed22-149">Une correspondance est trouvée uniquement si tous les bits de l’attribut correspondent à la valeur.</span><span class="sxs-lookup"><span data-stu-id="0ed22-149">A match is found only if all bits from the attribute match the value.</span></span> <span data-ttu-id="0ed22-150">Cette règle est équivalente à un opérateur **de bits and** .</span><span class="sxs-lookup"><span data-stu-id="0ed22-150">This rule is equivalent to a bitwise **AND** operator.</span></span>                                                                  |
| <span data-ttu-id="0ed22-151">1.2.840.113556.1.4.804</span><span class="sxs-lookup"><span data-stu-id="0ed22-151">1.2.840.113556.1.4.804</span></span>  | <span data-ttu-id="0ed22-152">**\_ \_ \_ bit de règle de correspondance LDAP \_ ou**</span><span class="sxs-lookup"><span data-stu-id="0ed22-152">**LDAP\_MATCHING\_RULE\_BIT\_OR**</span></span>   | <span data-ttu-id="0ed22-153">Une correspondance est trouvée si des bits de l’attribut correspondent à la valeur.</span><span class="sxs-lookup"><span data-stu-id="0ed22-153">A match is found if any bits from the attribute match the value.</span></span> <span data-ttu-id="0ed22-154">Cette règle est équivalente à un opérateur **de bits or** .</span><span class="sxs-lookup"><span data-stu-id="0ed22-154">This rule is equivalent to a bitwise **OR** operator.</span></span>                                                                        |
| <span data-ttu-id="0ed22-155">1.2.840.113556.1.4.1941</span><span class="sxs-lookup"><span data-stu-id="0ed22-155">1.2.840.113556.1.4.1941</span></span> | <span data-ttu-id="0ed22-156">**\_ \_ règle de correspondance LDAP dans la \_ \_ chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ed22-156">**LDAP\_MATCHING\_RULE\_IN\_CHAIN**</span></span> | <span data-ttu-id="0ed22-157">Cette règle est limitée aux filtres qui s’appliquent au DN.</span><span class="sxs-lookup"><span data-stu-id="0ed22-157">This rule is limited to filters that apply to the DN.</span></span> <span data-ttu-id="0ed22-158">Il s’agit d’un opérateur de correspondance « étendu » spécial qui parcourt la chaîne de ascendance dans des objets jusqu’à la racine jusqu’à ce qu’il trouve une correspondance.</span><span class="sxs-lookup"><span data-stu-id="0ed22-158">This is a special "extended" match operator that walks the chain of ancestry in objects all the way to the root until it finds a match.</span></span> |



 

<span data-ttu-id="0ed22-159">L’exemple suivant de chaîne de requête recherche les objets de groupe pour lesquels l’indicateur de **sécurité de type de groupe ADS est \_ \_ \_ \_ activé** est défini.</span><span class="sxs-lookup"><span data-stu-id="0ed22-159">The following example query string searches for group objects that have the **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED** flag set.</span></span> <span data-ttu-id="0ed22-160">Sachez que la valeur décimale de la **\_ sécurité de type de groupe ADS \_ \_ \_ activée** (0x80000000 = 2147483648) est utilisée pour la valeur de comparaison.</span><span class="sxs-lookup"><span data-stu-id="0ed22-160">Be aware that the decimal value of **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED** (0x80000000 = 2147483648) is used for the comparison value.</span></span>


```C++
(&(objectCategory=group)(groupType:1.2.840.113556.1.4.803:=2147483648))
```



<span data-ttu-id="0ed22-161">La **\_ \_ règle de correspondance LDAP de la \_ \_ chaîne** est un OID de règle de correspondance conçu pour fournir une méthode permettant de rechercher le ascendance d’un objet.</span><span class="sxs-lookup"><span data-stu-id="0ed22-161">The **LDAP\_MATCHING\_RULE\_IN\_CHAIN** is a matching rule OID that is designed to provide a method to look up the ancestry of an object.</span></span> <span data-ttu-id="0ed22-162">De nombreuses applications qui utilisent Active Directory et AD LDS fonctionnent généralement avec des données hiérarchiques, classées par relations parent-enfant.</span><span class="sxs-lookup"><span data-stu-id="0ed22-162">Many applications using AD and AD LDS usually work with hierarchical data, which is ordered by parent-child relationships.</span></span> <span data-ttu-id="0ed22-163">Auparavant, les applications effectuaient une expansion de groupe transitives pour déterminer l’appartenance à un groupe, qui utilisait trop de bande passante réseau. les applications devaient effectuer plusieurs allers-retours pour déterminer si un objet a baissé « dans la chaîne » si un lien est parcouru jusqu’à la fin.</span><span class="sxs-lookup"><span data-stu-id="0ed22-163">Previously, applications performed transitive group expansion to figure out group membership, which used too much network bandwidth; applications needed to make multiple roundtrips to figure out if an object fell "in the chain" if a link is traversed through to the end.</span></span>

<span data-ttu-id="0ed22-164">Un exemple d’une telle requête est conçu pour vérifier si un utilisateur « utilisateur1 » est membre du groupe « Group1 ».</span><span class="sxs-lookup"><span data-stu-id="0ed22-164">An example of such a query is one designed to check if a user "user1" is a member of group "group1".</span></span> <span data-ttu-id="0ed22-165">Vous devez définir la base sur le nom unique de l’utilisateur `(cn=user1, cn=users, dc=x)` et l’étendue sur `base` , et utiliser la requête suivante.</span><span class="sxs-lookup"><span data-stu-id="0ed22-165">You would set the base to the user DN `(cn=user1, cn=users, dc=x)` and the scope to `base`, and use the following query.</span></span>


```C++
(memberof:1.2.840.113556.1.4.1941:=cn=Group1,OU=groupsOU,DC=x)
```



<span data-ttu-id="0ed22-166">De même, pour rechercher tous les groupes dont est membre « utilisateur1 », définissez la base sur le nom unique du conteneur de groupes ; par exemple `(OU=groupsOU, dc=x)` , et l’étendue à `subtree` , et utilisez le filtre suivant.</span><span class="sxs-lookup"><span data-stu-id="0ed22-166">Similarly, to find all the groups that "user1" is a member of, set the base to the groups container DN; for example `(OU=groupsOU, dc=x)` and the scope to `subtree`, and use the following filter.</span></span>


```C++
(member:1.2.840.113556.1.4.1941:=cn=user1,cn=users,DC=x)
```



<span data-ttu-id="0ed22-167">Notez que lors de l’utilisation **\_ d’une \_ règle de correspondance LDAP dans la \_ \_ chaîne**, l’étendue n’est pas limitée ; il peut s’agir de `base` , `one-level` ou `subtree` .</span><span class="sxs-lookup"><span data-stu-id="0ed22-167">Note that when using **LDAP\_MATCHING\_RULE\_IN\_CHAIN**, scope is not limited—it can be `base`, `one-level`, or `subtree`.</span></span> <span data-ttu-id="0ed22-168">Certaines de ces requêtes sur les sous-arborescences peuvent être plus gourmandes en processeur, telles que la recherche de liens avec un grand éventail de ventilation ; autrement dit, répertorie tous les groupes dont un utilisateur est membre.</span><span class="sxs-lookup"><span data-stu-id="0ed22-168">Some such queries on subtrees may be more processor intensive, such as chasing links with a high fan-out; that is, listing all the groups that a user is a member of.</span></span> <span data-ttu-id="0ed22-169">Les recherches inefficaces consignent les messages du journal des événements appropriés, comme avec tout autre type de requête.</span><span class="sxs-lookup"><span data-stu-id="0ed22-169">Inefficient searches will log appropriate event log messages, as with any other type of query.</span></span>

## <a name="wildcards"></a><span data-ttu-id="0ed22-170">Caractères génériques</span><span class="sxs-lookup"><span data-stu-id="0ed22-170">Wildcards</span></span>

<span data-ttu-id="0ed22-171">Vous pouvez également ajouter des caractères génériques et des conditions à un filtre de recherche LDAP.</span><span class="sxs-lookup"><span data-stu-id="0ed22-171">You can also add wildcards and conditions to an LDAP search filter.</span></span> <span data-ttu-id="0ed22-172">Les exemples suivants montrent des sous-chaînes qui peuvent être utilisées pour effectuer des recherches dans l’annuaire.</span><span class="sxs-lookup"><span data-stu-id="0ed22-172">The following examples show substrings that can be used to search the directory.</span></span>

<span data-ttu-id="0ed22-173">Récupérer toutes les entrées :</span><span class="sxs-lookup"><span data-stu-id="0ed22-173">Get all entries:</span></span>


```C++
(objectClass=*)
```



<span data-ttu-id="0ed22-174">Récupérez les entrées contenant « Bob » quelque part dans le nom commun :</span><span class="sxs-lookup"><span data-stu-id="0ed22-174">Get entries containing "bob" somewhere in the common name:</span></span>


```C++
(cn=*bob*)
```



<span data-ttu-id="0ed22-175">Obtenir les entrées avec un nom commun supérieur ou égal à « Bob » :</span><span class="sxs-lookup"><span data-stu-id="0ed22-175">Get entries with a common name greater than or equal to "bob":</span></span>


```C++
(cn>='bob')
```



<span data-ttu-id="0ed22-176">Obtient tous les utilisateurs avec un attribut de messagerie :</span><span class="sxs-lookup"><span data-stu-id="0ed22-176">Get all users with an email attribute:</span></span>


```C++
(&(objectClass=user)(email=*))
```



<span data-ttu-id="0ed22-177">Obtenir toutes les entrées d’utilisateur avec un attribut de messagerie et un nom égal à « Smith » :</span><span class="sxs-lookup"><span data-stu-id="0ed22-177">Get all user entries with an email attribute and a surname equal to "smith":</span></span>


```C++
(&(sn=smith)(objectClass=user)(email=*))
```



<span data-ttu-id="0ed22-178">Obtient toutes les entrées d’utilisateur avec un nom commun qui commence par « Andy », « Steve » ou « Margaret » :</span><span class="sxs-lookup"><span data-stu-id="0ed22-178">Get all user entries with a common name that starts with "andy", "steve", or "margaret":</span></span>


```C++
(&(objectClass=user)(| (cn=andy*)(cn=steve*)(cn=margaret*)))
```



<span data-ttu-id="0ed22-179">Récupération de toutes les entrées sans attribut de messagerie :</span><span class="sxs-lookup"><span data-stu-id="0ed22-179">Get all entries without an email attribute:</span></span>


```C++
(!(email=*))
```



<span data-ttu-id="0ed22-180">La définition formelle du filtre de recherche est la suivante (à partir de la [RFC 2254](https://tools.ietf.org/html/rfc2254)) :</span><span class="sxs-lookup"><span data-stu-id="0ed22-180">The formal definition of the search filter is as follows (from [RFC 2254](https://tools.ietf.org/html/rfc2254)):</span></span>


```C++
<filter> ::= '(' <filtercomp> ')'
<filtercomp> ::= <and> | <or> | <not> | <item>
<and> ::= '&' <filterlist>
<or> ::= '|' <filterlist>
<not> ::= '!' <filter>
<filterlist> ::= <filter> | <filter> <filterlist>
<item>::= <simple> | <present> | <substring>
<simple> ::= <attr> <filtertype> <value><filtertype> ::= <equal> | <approx> | <ge> | <le>
<equal> ::= '='
<approx> ::= '~='
<ge> ::= '>='
<le> ::= '<='
<present> ::= <attr> '=*'
<substring> ::= <attr> '=' <initial> <any> <final>
<initial> ::= NULL | <value><any> ::= '*' <starval>
<starval> ::= NULL | <value>'*' <starval>
<final> ::= NULL | <value>
```



<span data-ttu-id="0ed22-181">Le jeton &lt; attr &gt; est une chaîne qui représente un attributeType.</span><span class="sxs-lookup"><span data-stu-id="0ed22-181">The token &lt;attr&gt; is a string that represents an AttributeType.</span></span> <span data-ttu-id="0ed22-182">La valeur de jeton &lt; &gt; est une chaîne qui représente un AttributeValue dont le format est défini par le service d’annuaire sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="0ed22-182">The token &lt;value&gt; is a string that represents an AttributeValue whose format is defined by the underlying directory service.</span></span>

<span data-ttu-id="0ed22-183">Si une &lt; valeur &gt; doit contenir le caractère astérisque ( \* ), de parenthèse ouvrante (() ou de parenthèse fermante ()), le caractère doit être précédé du caractère d’échappement barre oblique inverse ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="0ed22-183">If a &lt;value&gt; must contain the asterisk (\*), left parenthesis ((), or right parenthesis ()) character, the character should be preceded by the backslash escape character (\\).</span></span>

## <a name="special-characters"></a><span data-ttu-id="0ed22-184">Caractères spéciaux</span><span class="sxs-lookup"><span data-stu-id="0ed22-184">Special Characters</span></span>

<span data-ttu-id="0ed22-185">Si l’un des caractères spéciaux suivants doit apparaître dans le filtre de recherche en tant que littéraux, ils doivent être remplacés par la séquence d’échappement indiquée.</span><span class="sxs-lookup"><span data-stu-id="0ed22-185">If any of the following special characters must appear in the search filter as literals, they must be replaced by the listed escape sequence.</span></span>



| <span data-ttu-id="0ed22-186">Caractère ASCII</span><span class="sxs-lookup"><span data-stu-id="0ed22-186">ASCII character</span></span> | <span data-ttu-id="0ed22-187">Substitution de séquence d’échappement</span><span class="sxs-lookup"><span data-stu-id="0ed22-187">Escape sequence substitute</span></span> |
|-----------------|----------------------------|
| \*              | <span data-ttu-id="0ed22-188">\\2a</span><span class="sxs-lookup"><span data-stu-id="0ed22-188">\\2a</span></span>                       |
| <span data-ttu-id="0ed22-189">(</span><span class="sxs-lookup"><span data-stu-id="0ed22-189">(</span></span>               | <span data-ttu-id="0ed22-190">\\28/08/03</span><span class="sxs-lookup"><span data-stu-id="0ed22-190">\\28</span></span>                       |
| <span data-ttu-id="0ed22-191">)</span><span class="sxs-lookup"><span data-stu-id="0ed22-191">)</span></span>               | <span data-ttu-id="0ed22-192">\\28</span><span class="sxs-lookup"><span data-stu-id="0ed22-192">\\29</span></span>                       |
| \\              | <span data-ttu-id="0ed22-193">\\5C</span><span class="sxs-lookup"><span data-stu-id="0ed22-193">\\5c</span></span>                       |
| <span data-ttu-id="0ed22-194">NUL</span><span class="sxs-lookup"><span data-stu-id="0ed22-194">NUL</span></span>             | <span data-ttu-id="0ed22-195">\\producteurs</span><span class="sxs-lookup"><span data-stu-id="0ed22-195">\\00</span></span>                       |
| /               | <span data-ttu-id="0ed22-196">\\2F</span><span class="sxs-lookup"><span data-stu-id="0ed22-196">\\2f</span></span>                       |



 

> [!Note]  
> <span data-ttu-id="0ed22-197">Dans les cas où un jeu de caractères multioctets est utilisé, les séquences d’échappement listées ci-dessus doivent être utilisées si la recherche est effectuée par ADO avec le dialecte SQL.</span><span class="sxs-lookup"><span data-stu-id="0ed22-197">In cases where a MultiByte Character Set is being used, the escape sequences listed above must be used if the search is performed by ADO with the SQL dialect.</span></span>

 

<span data-ttu-id="0ed22-198">En outre, les données binaires arbitraires peuvent être représentées à l’aide de la syntaxe de séquence d’échappement en encodant chaque octet de données binaires avec la barre oblique inverse ( \\ ) suivie de deux chiffres hexadécimaux.</span><span class="sxs-lookup"><span data-stu-id="0ed22-198">In addition, arbitrary binary data may be represented by using the escape sequence syntax by encoding each byte of binary data with the backslash (\\) followed by two hexadecimal digits.</span></span> <span data-ttu-id="0ed22-199">Par exemple, la valeur de 4 octets 0x00000004 est encodée sous la forme \\ 00 00 \\ \\ 00 \\ 04 dans une chaîne de filtrage.</span><span class="sxs-lookup"><span data-stu-id="0ed22-199">For example, the four-byte value 0x00000004 is encoded as \\00\\00\\00\\04 in a filter string.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0ed22-200">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0ed22-200">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ed22-201">Dialecte LDAP</span><span class="sxs-lookup"><span data-stu-id="0ed22-201">LDAP dialect</span></span>](ldap-dialect.md)
</dt> <dt>

[<span data-ttu-id="0ed22-202">Dialecte SQL</span><span class="sxs-lookup"><span data-stu-id="0ed22-202">SQL dialect</span></span>](sql-dialect.md)
</dt> <dt>

[<span data-ttu-id="0ed22-203">Recherche avec l’interface IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="0ed22-203">Searching with the IDirectorySearch Interface</span></span>](searching-with-idirectorysearch.md)
</dt> <dt>

[<span data-ttu-id="0ed22-204">Recherche avec ActiveX Data Objects</span><span class="sxs-lookup"><span data-stu-id="0ed22-204">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
</dt> <dt>

[<span data-ttu-id="0ed22-205">Recherche avec OLE DB</span><span class="sxs-lookup"><span data-stu-id="0ed22-205">Searching with OLE DB</span></span>](searching-with-ole-db.md)
</dt> </dl>

 

 
