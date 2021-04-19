---
title: Dialecte SQL
description: Le dialecte SQL, dérivé de l’langage SQL, utilise des expressions explicites pour définir des instructions de requête.
ms.assetid: c1032268-e0f5-4d74-ab72-864cdd36851d
ms.tgt_platform: multiple
keywords:
- Langage SQL (ADSI)
- dialecte ADSI, dialecte SQL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b0936a54bc7bd0028717967ce779fe2f2048a33
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106508956"
---
# <a name="sql-dialect"></a><span data-ttu-id="46603-105">Dialecte SQL</span><span class="sxs-lookup"><span data-stu-id="46603-105">SQL Dialect</span></span>

<span data-ttu-id="46603-106">Le dialecte SQL, dérivé de l’langage SQL, utilise des expressions explicites pour définir des instructions de requête.</span><span class="sxs-lookup"><span data-stu-id="46603-106">The SQL dialect, derived from the Structured Query Language, uses human-readable expressions to define query statements.</span></span> <span data-ttu-id="46603-107">Utilisez une instruction de requête SQL avec les interfaces de recherche ADSI suivantes :</span><span class="sxs-lookup"><span data-stu-id="46603-107">Use a SQL query statement with the following ADSI search interfaces:</span></span>

-   <span data-ttu-id="46603-108">Interfaces [ADO (ActiveX Data Object)](searching-with-activex-data-objects-ado.md) , qui sont des interfaces Automation qui utilisent OLE DB.</span><span class="sxs-lookup"><span data-stu-id="46603-108">The [ActiveX Data Object (ADO)](searching-with-activex-data-objects-ado.md) interfaces, which are Automation interfaces that use OLE DB.</span></span>
-   <span data-ttu-id="46603-109">[OLE DB](searching-with-ole-db.md), qui est un ensemble d’interfaces C/C++ pour interroger des bases de données.</span><span class="sxs-lookup"><span data-stu-id="46603-109">[OLE DB](searching-with-ole-db.md), which is a set of C/C++ interfaces for querying databases.</span></span>

<span data-ttu-id="46603-110">Les instructions SQL requièrent la syntaxe suivante.</span><span class="sxs-lookup"><span data-stu-id="46603-110">SQL statements require the following syntax.</span></span>


```sql
SELECT [ALL] * | select-list FROM 'ADsPath' [WHERE search-condition] [ORDER BY sort-list]
```



<span data-ttu-id="46603-111">Le tableau suivant répertorie les mots clés des instructions de requête SQL.</span><span class="sxs-lookup"><span data-stu-id="46603-111">The following table lists SQL query statement keywords.</span></span>



| <span data-ttu-id="46603-112">Mot clé</span><span class="sxs-lookup"><span data-stu-id="46603-112">Keyword</span></span>  | <span data-ttu-id="46603-113">Description</span><span class="sxs-lookup"><span data-stu-id="46603-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46603-114">SELECT</span><span class="sxs-lookup"><span data-stu-id="46603-114">SELECT</span></span>   | <span data-ttu-id="46603-115">Spécifie une liste d’attributs séparés par des virgules à récupérer pour chaque objet.</span><span class="sxs-lookup"><span data-stu-id="46603-115">Specifies a comma-separated list of attributes to retrieve for each object.</span></span> <span data-ttu-id="46603-116">Si vous spécifiez \* , la requête récupère uniquement l’ADsPath de chaque objet.</span><span class="sxs-lookup"><span data-stu-id="46603-116">If you specify \*, the query retrieves only the ADsPath of each object.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="46603-117">FROM</span><span class="sxs-lookup"><span data-stu-id="46603-117">FROM</span></span>     | <span data-ttu-id="46603-118">Spécifie l’ADsPath de la base de la recherche.</span><span class="sxs-lookup"><span data-stu-id="46603-118">Specifies the ADsPath of the base of the search.</span></span> <span data-ttu-id="46603-119">Par exemple, l’ADsPath du conteneur Users dans un domaine Active Directory peut être’LDAP :As = Users, DC = fabrikam, DC = COM'.</span><span class="sxs-lookup"><span data-stu-id="46603-119">For example, the ADsPath of the Users container in an Active Directory domain might be 'LDAP://CN=Users,DC=Fabrikam,DC=COM'.</span></span> <span data-ttu-id="46603-120">Notez que le chemin d’accès est placé entre deux guillemets simples (').</span><span class="sxs-lookup"><span data-stu-id="46603-120">Be aware that the path is enclosed in a pair of single quotation marks (').</span></span>                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="46603-121">WHERE</span><span class="sxs-lookup"><span data-stu-id="46603-121">WHERE</span></span>    | <span data-ttu-id="46603-122">Mot clé facultatif qui spécifie le filtre de requête.</span><span class="sxs-lookup"><span data-stu-id="46603-122">An optional keyword that specifies the query filter.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="46603-123">ORDER BY</span><span class="sxs-lookup"><span data-stu-id="46603-123">ORDER BY</span></span> | <span data-ttu-id="46603-124">Mot clé facultatif qui génère un tri côté serveur si le serveur prend en charge le contrôle de tri LDAP.</span><span class="sxs-lookup"><span data-stu-id="46603-124">An optional keyword that generates a server-side sort if the server supports the LDAP sort control.</span></span> <span data-ttu-id="46603-125">Active Directory prend en charge le contrôle de tri, mais il peut avoir un impact sur les performances du serveur, en particulier si le jeu de résultats est volumineux.</span><span class="sxs-lookup"><span data-stu-id="46603-125">Active Directory supports the sort control, but it can impact server performance, particularly if the results set is large.</span></span> <span data-ttu-id="46603-126">La liste de tri est une liste séparée par des virgules d’attributs sur lesquels effectuer le tri.</span><span class="sxs-lookup"><span data-stu-id="46603-126">The sort-list is a comma-separated list of attributes on which to sort.</span></span> <span data-ttu-id="46603-127">N’oubliez pas que Active Directory ne prend en charge qu’une seule clé de tri.</span><span class="sxs-lookup"><span data-stu-id="46603-127">Be aware that Active Directory supports only a single sort key.</span></span> <span data-ttu-id="46603-128">Vous pouvez utiliser les mots clés facultatifs ASC et DESC pour spécifier l’ordre de tri croissant ou décroissant ; la valeur par défaut est l’ordre croissant.</span><span class="sxs-lookup"><span data-stu-id="46603-128">You can use the optional ASC and DESC keywords to specify ascending or descending sort order; the default is ascending.</span></span> <span data-ttu-id="46603-129">Le mot clé ORDER BY remplace toute clé de tri spécifiée par la propriété « sort on » de l’objet Command ADO.</span><span class="sxs-lookup"><span data-stu-id="46603-129">The ORDER BY keyword overrides any sort key specified with the "Sort on" property of the ADO Command object.</span></span> |



 

> [!Note]  
> <span data-ttu-id="46603-130">Dans les cas où un jeu de caractères multioctets est utilisé, si la recherche est effectuée par ADO avec le dialecte SQL, une barre oblique inverse ne peut pas être utilisée pour échapper des caractères.</span><span class="sxs-lookup"><span data-stu-id="46603-130">In cases where a MultiByte Character Set is being used, if the search is performed by ADO with the SQL dialect, then a backslash cannot be used to escape characters.</span></span> <span data-ttu-id="46603-131">Au lieu de cela, les séquences d’échappement listées dans les [caractères spéciaux](search-filter-syntax.md) doivent être utilisées.</span><span class="sxs-lookup"><span data-stu-id="46603-131">Instead, the escape sequences listed in [Special Characters](search-filter-syntax.md) must be used.</span></span> <span data-ttu-id="46603-132">Par exemple, pour une instruction qui a utilisé la syntaxe « samAccountName = \( test », qui utilise la barre oblique inverse « \\ », pour échapper la parenthèse ouvrante « ( », à la place, vous devez remplacer la barre oblique inverse par le caractère spécial « \\ 28 », comme suit : « sAMAccountName = \\ 28Test ».</span><span class="sxs-lookup"><span data-stu-id="46603-132">For example, for a statement that used the syntax "samAccountName=\(Test", which uses the backslash, "\\", to escape the open parenthesis, "(", instead, you would replace the backslash with the special character "\\28", as follows: "samAccountName=\\28Test".</span></span>

 

<span data-ttu-id="46603-133">Les instructions de requête suivantes sont des exemples de dialecte SQL dans ADSI.</span><span class="sxs-lookup"><span data-stu-id="46603-133">The following query statements are examples of SQL dialect in ADSI.</span></span>

<span data-ttu-id="46603-134">Pour rechercher tous les objets de groupe.</span><span class="sxs-lookup"><span data-stu-id="46603-134">To search for all the group objects.</span></span>


```sql
SELECT ADsPath, cn FROM 'LDAP://DC=Fabrikam,DC=COM' WHERE objectCategory='group'
```



<span data-ttu-id="46603-135">Pour rechercher tous les utilisateurs dont le nom commence par la lettre H.</span><span class="sxs-lookup"><span data-stu-id="46603-135">To search for all the users whose Last Name starts with letter H.</span></span>


```sql
SELECT ADsPath, cn FROM 'LDAP://OU=Sales,DC=Fabrikam,DC=COM' WHERE objectCategory='person' AND objectClass='user' AND sn = 'H*' ORDER BY sn
```



<span data-ttu-id="46603-136">La grammaire formelle pour les requêtes SQL est définie dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="46603-136">The formal grammar for SQL queries is defined in the following code example.</span></span> <span data-ttu-id="46603-137">Tous les mots clés ne respectent pas la casse.</span><span class="sxs-lookup"><span data-stu-id="46603-137">All keywords are case-insensitive.</span></span>


```sql
statement ::= select-statement
select-statement ::= SELECT [ALL] select-list FROM table-identifier [WHERE search-condition] [ORDER BY sort-list]
select-list ::= * | select-sublist [, select-sublist]... 
select-sublist ::= column-identifier
column-identifier ::= user-defined-name 
table-identifier ::= string-literal
search-condition ::= boolean-term [OR search-condition]
sort-list ::= column-identifier [ASC | DESC] [,column-identifier [ASC | DESC]]... 
boolean-term ::= boolean-factor [AND boolean-term]
boolean-factor ::= [NOT] boolean-primary
boolean-primary ::= comparison-predicate | (search-condition)
comparison-predicate ::= column-identifier comparison-operator literal
comparison-operator ::= < | > | <= | >= | = | <>
user-defined-name ::= letter [letter | digit]...
literal ::= string-literal | numeric-literal | boolean-literal 
string-literal ::= '{character}...' (Any sequence of characters delimited by quotes)
numeric-literal ::= digits [fraction] [exponent]
digits ::= digit [digit]...
fraction ::= . digits 
exponent ::= E digits
boolean-literal ::= TRUE | FALSE | YES | NO | ON | OFF
```



<span data-ttu-id="46603-138">Les jointures internes SQL ne sont pas prises en charge par le fournisseur de OLE DB Active Directory, mais vous pouvez utiliser SQL pour joindre des données SQL et Active Directory.</span><span class="sxs-lookup"><span data-stu-id="46603-138">SQL inner joins are not supported by the Active Directory OLE DB provider, but you can use SQL to join SQL and Active Directory data.</span></span> <span data-ttu-id="46603-139">Pour plus d’informations, consultez [création d’une jointure hétérogène entre SQL Server et Active Directory](creating-a-heterogeneous-join-between-sql-server-and-active-directory.md).</span><span class="sxs-lookup"><span data-stu-id="46603-139">For more information, see [Creating a Heterogeneous Join between SQL Server and Active Directory](creating-a-heterogeneous-join-between-sql-server-and-active-directory.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="46603-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="46603-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46603-141">Syntaxe de filtre de recherche</span><span class="sxs-lookup"><span data-stu-id="46603-141">Search Filter Syntax</span></span>](search-filter-syntax.md)
</dt> <dt>

[<span data-ttu-id="46603-142">Dialecte LDAP</span><span class="sxs-lookup"><span data-stu-id="46603-142">LDAP dialect</span></span>](ldap-dialect.md)
</dt> <dt>

[<span data-ttu-id="46603-143">Recherche avec l’interface IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="46603-143">Searching with the IDirectorySearch Interface</span></span>](searching-with-idirectorysearch.md)
</dt> <dt>

[<span data-ttu-id="46603-144">Recherche avec ActiveX Data Objects</span><span class="sxs-lookup"><span data-stu-id="46603-144">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
</dt> <dt>

[<span data-ttu-id="46603-145">Recherche avec OLE DB</span><span class="sxs-lookup"><span data-stu-id="46603-145">Searching with OLE DB</span></span>](searching-with-ole-db.md)
</dt> </dl>

 

 




