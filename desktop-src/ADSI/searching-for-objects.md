---
title: Recherche d’objets
description: Julie Bankert doit trouver les numéros de téléphone de tous les chefs de programme qui travaillent dans le service 101. Elle peut créer un script qui utilise ADO et ADSI pour y parvenir.
ms.assetid: c6325068-4ae2-4348-9938-96402262cd43
ms.tgt_platform: multiple
keywords:
- recherche d’objets ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb3c26f05b63524e3a657c0c460efb921978bd19
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "103841926"
---
# <a name="searching-for-objects"></a><span data-ttu-id="120d5-105">Recherche d’objets</span><span class="sxs-lookup"><span data-stu-id="120d5-105">Searching for Objects</span></span>

<span data-ttu-id="120d5-106">Julie Bankert doit trouver les numéros de téléphone de tous les chefs de programme qui travaillent dans le service 101.</span><span class="sxs-lookup"><span data-stu-id="120d5-106">Julie Bankert must find telephone numbers for all Program Managers who work in Department 101.</span></span> <span data-ttu-id="120d5-107">Elle peut créer un script qui utilise ADO et ADSI pour y parvenir.</span><span class="sxs-lookup"><span data-stu-id="120d5-107">She can create a script that uses ADO and ADSI to accomplish this.</span></span>

<span data-ttu-id="120d5-108">Lorsque vous utilisez le fournisseur ADO pour exécuter une requête, le jeu de résultats retourne uniquement les premiers 1000 objets.</span><span class="sxs-lookup"><span data-stu-id="120d5-108">When using the ADO provider to perform a query, the result set will only return the first 1000 objects.</span></span> <span data-ttu-id="120d5-109">Pour cette raison, il est important d’utiliser une requête paginée afin de pouvoir récupérer tous les objets du jeu de résultats, tant que le service d’annuaire n’a pas été défini pour limiter le nombre d’éléments dans un jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="120d5-109">For this reason, it is important to use a paged query so that you can retrieve all of the objects in the result set, as long as the directory service has not been set to limit the number of items in a result set.</span></span> <span data-ttu-id="120d5-110">Les jeux de retours contiendront le nombre d’éléments que vous spécifiez dans la taille de la page, et les jeux paginés continueront à être retournés jusqu’à ce que tous les éléments du jeu de résultats aient été retournés.</span><span class="sxs-lookup"><span data-stu-id="120d5-110">Return sets will contain the number of items that you specify in the page size, and paged sets will continue to be returned until all items in the result set have been returned.</span></span>


```VB
' Create the connection and command object.
Set oConnection1 = CreateObject("ADODB.Connection")
Set oCommand1 = CreateObject("ADODB.Command")
' Open the connection.
oConnection1.Provider = "ADsDSOObject"  ' This is the ADSI OLE-DB provider name
oConnection1.Open "Active Directory Provider"
' Create a command object for this connection.
Set oCommand1.ActiveConnection = oConnection1

' Compose a search string.
oCommand1.CommandText = "select name,telephoneNumber " & _
"from 'LDAP://DC=Fabrikam,DC=com'" & _
"WHERE objectCategory='Person'" & _
"AND objectClass='user'" & _
"AND title='Program Manager'" & _
"AND department=101"

' Execute the query.
Set rs = oCommand1.Execute
'--------------------------------------
' Navigate the record set
'--------------------------------------
While Not rs.EOF
    Debug.Print rs.Fields("Name") & " , " & rs.Fields("telephoneNumber")
    rs.MoveNext
Wend
```



<span data-ttu-id="120d5-111">Pour effectuer une recherche ADSI dans Visual Basic ou dans un environnement de script, trois composants ADO sont requis : **connexion**, **commande** et **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="120d5-111">To perform an ADSI search in Visual Basic or a scripting environment, three ADO components are required: **Connection**, **Command**, and **Recordset**.</span></span> <span data-ttu-id="120d5-112">L’objet de **connexion** vous permet de spécifier le nom du fournisseur, les autres informations d’identification, le cas échéant, ainsi que d’autres indicateurs.</span><span class="sxs-lookup"><span data-stu-id="120d5-112">The **Connection** object enables you to specify the provider name, alternate credentials, if applicable, and other flags.</span></span> <span data-ttu-id="120d5-113">L’objet **Command** vous permet de spécifier des préférences de recherche et la chaîne de requête.</span><span class="sxs-lookup"><span data-stu-id="120d5-113">The **Command** object enables you to specify search preferences and the query string.</span></span> <span data-ttu-id="120d5-114">Vous devez associer l’objet de **connexion** à un objet de **commande** avant l’exécution de la requête.</span><span class="sxs-lookup"><span data-stu-id="120d5-114">You must associate the **Connection** object to a **Command** object before the execution of the query.</span></span> <span data-ttu-id="120d5-115">Enfin, l’objet **Recordset** est utilisé pour itérer le jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="120d5-115">Finally, the **Recordset** object is used to iterate the result set.</span></span>

<span data-ttu-id="120d5-116">ADSI prend en charge deux types de chaînes de requête ou de dialectes.</span><span class="sxs-lookup"><span data-stu-id="120d5-116">ADSI supports two types of query strings or dialects.</span></span> <span data-ttu-id="120d5-117">L’exemple de code précédent utilise le dialecte SQL.</span><span class="sxs-lookup"><span data-stu-id="120d5-117">The preceding code example uses the SQL dialect.</span></span> <span data-ttu-id="120d5-118">Vous pouvez également utiliser le dialecte LDAP.</span><span class="sxs-lookup"><span data-stu-id="120d5-118">You can also use the LDAP dialect.</span></span> <span data-ttu-id="120d5-119">La chaîne de requête de dialecte LDAP est basée sur la [norme rfc 2254](https://www.ietf.org/rfc/rfc2254.txt) (une RFC est un document de demande de commentaires, qui est la base du développement de normes LDAP).</span><span class="sxs-lookup"><span data-stu-id="120d5-119">The LDAP dialect query string is based on [RFC 2254](https://www.ietf.org/rfc/rfc2254.txt) (an RFC is a Request For Comments document, which is the basis for developing LDAP standards).</span></span> <span data-ttu-id="120d5-120">L’exemple précédent peut être traduit dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="120d5-120">The preceding example can be translated to the following code example.</span></span>


```VB
oCommand1.CommandText = "<LDAP://DC=fabrikam,DC=COM>;" & _
"(&(objectCategory=Person)" & _
"(objectClass=user)" & _
"(title=ProgramManager)" & _
"(department=101));" & _
"name,telephoneNumber;subTree"
```



<span data-ttu-id="120d5-121">Pourquoi le mot « sous-arbre » se trouve-t-il à la fin de la chaîne ?</span><span class="sxs-lookup"><span data-stu-id="120d5-121">Why is the word "subtree" at the end of the string?</span></span> <span data-ttu-id="120d5-122">Dans le monde de l’annuaire, vous pouvez spécifier l’étendue de la recherche.</span><span class="sxs-lookup"><span data-stu-id="120d5-122">In the directory world, you can specify the scope of search.</span></span> <span data-ttu-id="120d5-123">Les choix sont les suivants : « base », « onelevel » et « sous-arborescence ».</span><span class="sxs-lookup"><span data-stu-id="120d5-123">The choices are: "base", "onelevel", and "subtree".</span></span> <span data-ttu-id="120d5-124">« base » est utilisé pour lire l’objet lui-même ; « onelevel » fait référence aux enfants immédiats, similaires à la commande **dir** . « sous-arborescence » permet d’effectuer des recherches sur plusieurs niveaux (comme **dir/s**).</span><span class="sxs-lookup"><span data-stu-id="120d5-124">"base" is used to read the object itself; "onelevel" refers to the immediate children, similar to the **dir** command; "subtree" is used to search deep or down multiple levels (similar to **dir /s**).</span></span>

<span data-ttu-id="120d5-125">Avec le dialecte SQL, vous pouvez spécifier la portée dans la propriété Command, comme dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="120d5-125">With the SQL dialect, you can specify scope in the command property, such as in the following code example.</span></span>


```VB
oCommand1.Properties("SearchScope") = ADS_SCOPE_ONELEVEL
```



<span data-ttu-id="120d5-126">Si l’étendue n’est pas spécifiée, par défaut, elle utilise une recherche de sous-arborescence.</span><span class="sxs-lookup"><span data-stu-id="120d5-126">If scope is not specified, by default it uses a subtree search.</span></span>

> [!Note]  
> <span data-ttu-id="120d5-127">Si vous utilisez C++, vous pouvez utiliser l’interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) à partir d’ADSI.</span><span class="sxs-lookup"><span data-stu-id="120d5-127">If you use C++, you can use the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface from ADSI.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="120d5-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="120d5-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="120d5-129">Réorganisation</span><span class="sxs-lookup"><span data-stu-id="120d5-129">Reorganization</span></span>](reorganization.md)
</dt> </dl>

 

 




