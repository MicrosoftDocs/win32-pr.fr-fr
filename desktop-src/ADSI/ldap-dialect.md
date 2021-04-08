---
title: Dialecte LDAP
description: Le dialecte LDAP est un format pour les instructions de requête qui utilisent la syntaxe de filtre de recherche LDAP.
ms.assetid: 29aca7e6-3ed5-4efd-8b03-6a2ee0571f1f
ms.tgt_platform: multiple
keywords:
- Interface ADSI de dialecte LDAP
- dialectes ADSI, dialecte LDAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15f7d1f65a41655596d0a14cf6e2a3595916c2cc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839173"
---
# <a name="ldap-dialect"></a><span data-ttu-id="72200-105">Dialecte LDAP</span><span class="sxs-lookup"><span data-stu-id="72200-105">LDAP Dialect</span></span>

<span data-ttu-id="72200-106">Le dialecte LDAP est un format pour les instructions de requête qui utilisent la [syntaxe de filtre de recherche LDAP](search-filter-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="72200-106">The LDAP dialect is a format for query statements that use the [LDAP search filter syntax](search-filter-syntax.md).</span></span> <span data-ttu-id="72200-107">Utilisez une instruction de requête LDAP avec les interfaces de recherche ADSI suivantes :</span><span class="sxs-lookup"><span data-stu-id="72200-107">Use an LDAP query statement with the following ADSI search interfaces:</span></span>

-   <span data-ttu-id="72200-108">Interfaces [ADO (ActiveX Data Object)](searching-with-activex-data-objects-ado.md) , qui sont des interfaces Automation qui utilisent OLE DB.</span><span class="sxs-lookup"><span data-stu-id="72200-108">The [ActiveX Data Object (ADO)](searching-with-activex-data-objects-ado.md) interfaces, which are Automation interfaces that use OLE DB.</span></span>
-   <span data-ttu-id="72200-109">[OLE DB](searching-with-ole-db.md), qui est un ensemble d’interfaces C/C++ pour interroger des bases de données.</span><span class="sxs-lookup"><span data-stu-id="72200-109">[OLE DB](searching-with-ole-db.md), which is a set of C/C++ interfaces for querying databases.</span></span>
-   <span data-ttu-id="72200-110">[**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch), qui est l’interface C/C++ pour Active Directory.</span><span class="sxs-lookup"><span data-stu-id="72200-110">[**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch), which is the C/C++ interface for Active Directory.</span></span>

<span data-ttu-id="72200-111">Une chaîne de dialecte LDAP se compose de quatre parties séparées par des points-virgules (;).</span><span class="sxs-lookup"><span data-stu-id="72200-111">An LDAP dialect string consists of four parts separated by semicolons (;).</span></span>

-   <span data-ttu-id="72200-112">Nom unique de base.</span><span class="sxs-lookup"><span data-stu-id="72200-112">Base distinguished name.</span></span> <span data-ttu-id="72200-113">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="72200-113">For example:</span></span>

    ```VB
    <LDAP://DC=Fabrikam,DC=COM>
    ```

    

-   <span data-ttu-id="72200-114">Filtres de recherche LDAP.</span><span class="sxs-lookup"><span data-stu-id="72200-114">LDAP search filters.</span></span> <span data-ttu-id="72200-115">Pour plus d’informations sur les filtres de recherche, consultez [syntaxe de filtre de recherche](search-filter-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="72200-115">For more information about search filters, see [Search Filter Syntax](search-filter-syntax.md).</span></span>
-   <span data-ttu-id="72200-116">Nom complet LDAP des attributs à récupérer.</span><span class="sxs-lookup"><span data-stu-id="72200-116">The LDAP display name of the attributes to retrieve.</span></span> <span data-ttu-id="72200-117">Plusieurs attributs sont séparés par une virgule.</span><span class="sxs-lookup"><span data-stu-id="72200-117">Multiple attributes are separated by a comma.</span></span>
-   <span data-ttu-id="72200-118">Spécifie l’étendue de la recherche.</span><span class="sxs-lookup"><span data-stu-id="72200-118">Specifies the scope of the search.</span></span> <span data-ttu-id="72200-119">Les valeurs valides sont « base », « onelevel » et « sous-arborescence ».</span><span class="sxs-lookup"><span data-stu-id="72200-119">Valid values are "base", "onelevel", and "subtree".</span></span> <span data-ttu-id="72200-120">L’étendue spécifiée dans une chaîne de requête LDAP remplace toute étendue de recherche spécifiée par la propriété « SearchScope » de l’objet de commande ADO.</span><span class="sxs-lookup"><span data-stu-id="72200-120">The scope specified in an LDAP query string overrides any search scope specified with the "SearchScope" property of the ADO Command object.</span></span>

<span data-ttu-id="72200-121">Voici un exemple de code du dialecte LDAP dans ADSI qui effectue une recherche dans tous les objets de la sous-arborescence.</span><span class="sxs-lookup"><span data-stu-id="72200-121">The following is a code example of the LDAP dialect in ADSI that searches all the objects in the subtree.</span></span>


```VB
"<LDAP://DC=Fabrikam,DC=com>;(objectClass=*);AdsPath, cn;subTree"
```



<span data-ttu-id="72200-122">Toutes les options de recherche (taille de page de recherche, par exemple) ne peuvent pas être exprimées dans le dialecte LDAP. vous devez donc définir les options avant le démarrage de l’exécution de la requête réelle.</span><span class="sxs-lookup"><span data-stu-id="72200-122">Not all search options (search page size, for example) can be expressed in the LDAP dialect, so you must set the options before the actual query execution starts.</span></span>

## <a name="example-code-for-performing-an-ldap-query"></a><span data-ttu-id="72200-123">Exemple de code pour exécuter une requête LDAP</span><span class="sxs-lookup"><span data-stu-id="72200-123">Example Code for Performing an LDAP Query</span></span>

<span data-ttu-id="72200-124">L’exemple de code suivant montre comment utiliser une requête LDAP.</span><span class="sxs-lookup"><span data-stu-id="72200-124">The following code example shows how to use an LDAP query</span></span>


```VB
Dim con As New Connection, rs As New Recordset
Dim adVariant
Dim i 'Used for counter
Dim j 'Used for counter
Dim Com As New Command
Dim strDomain As String
Dim strPassword As String
 
' Open a Connection object.
con.Provider = "ADsDSOObject"
con.Properties("ADSI Flag") = 1
con.Properties("User ID") = strDomain + "\" + strUserID
con.Properties("Password") = strPassword

con.Open "Active Directory Provider"
 
' Create a command object on this connection.
Set Com.ActiveConnection = con
 
' Set the query string.
Com.CommandText = "<LDAP://MyServer/DC=MyDomain,DC=Fabrikam,DC=com>;
     (objectClass=*);ADsPath, objectclass;base"
 
' Set search preferences.
Com.Properties("Page Size") = 1000
Com.Properties("Timeout") = 30 'seconds
 
' Execute the query.
Set rs = Com.Execute
 
' Navigate the record set.
rs.MoveFirst
While Not rs.EOF
    For i = 0 To rs.Fields.Count - 1
        If rs.Fields(i).Type = adVariant And Not (IsNull(rs.Fields(i).Value)) Then
            Debug.Print rs.Fields(i).Name, " = "
            For j = LBound(rs.Fields(i).Value) To UBound(rs.Fields(i).Value)
                Debug.Print rs.Fields(i).Value(j), " # "
            Next j
        Else
            Debug.Print rs.Fields(i).Name, " = ", rs.Fields(i).Value
        End If
    Next i
    rs.MoveNext
Wend
 
rs.MoveLast
Debug.Print "No. of rows = ", rs.RecordCount
```



<span data-ttu-id="72200-125">Pour plus d’informations sur la syntaxe de requête, consultez [syntaxe de filtre de recherche](search-filter-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="72200-125">For details about the query syntax, see [Search Filter Syntax](search-filter-syntax.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="72200-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="72200-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72200-127">Syntaxe de filtre de recherche</span><span class="sxs-lookup"><span data-stu-id="72200-127">Search Filter Syntax</span></span>](search-filter-syntax.md)
</dt> <dt>

[<span data-ttu-id="72200-128">Dialecte SQL</span><span class="sxs-lookup"><span data-stu-id="72200-128">SQL dialect</span></span>](sql-dialect.md)
</dt> <dt>

[<span data-ttu-id="72200-129">Recherche avec l’interface IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="72200-129">Searching with the IDirectorySearch Interface</span></span>](searching-with-idirectorysearch.md)
</dt> <dt>

[<span data-ttu-id="72200-130">Recherche avec ActiveX Data Objects</span><span class="sxs-lookup"><span data-stu-id="72200-130">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
</dt> <dt>

[<span data-ttu-id="72200-131">Recherche avec OLE DB</span><span class="sxs-lookup"><span data-stu-id="72200-131">Searching with OLE DB</span></span>](searching-with-ole-db.md)
</dt> </dl>

 

 




