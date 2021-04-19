---
title: Rechercher à l’aide d’ActiveX Data Objects (ADO)
description: Le modèle ADO (ActiveX Data Object) se compose d’objets listés dans le tableau suivant.
ms.assetid: 27298f53-a652-49f2-a6e6-d92c7c6022af
ms.tgt_platform: multiple
keywords:
- ActiveX Data Objects ADSI, recherche avec ADO
- Recherche avec ActiveX Data Objects ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9e73f630892169c7086daf9bb1e7b6c13bfdf0a
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "106513556"
---
# <a name="searching-with-activex-data-objects-ado"></a><span data-ttu-id="c9f6e-105">Rechercher à l’aide d’ActiveX Data Objects (ADO)</span><span class="sxs-lookup"><span data-stu-id="c9f6e-105">Searching with ActiveX Data Objects (ADO)</span></span>

<span data-ttu-id="c9f6e-106">Le modèle ADO (ActiveX Data Object) se compose d’objets listés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-106">The ActiveX Data Object (ADO) model consists of objects listed in the following table.</span></span>



| <span data-ttu-id="c9f6e-107">Object</span><span class="sxs-lookup"><span data-stu-id="c9f6e-107">Object</span></span>         | <span data-ttu-id="c9f6e-108">Description</span><span class="sxs-lookup"><span data-stu-id="c9f6e-108">Description</span></span>                                                                                                                        |
|----------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9f6e-109">**Connection**</span><span class="sxs-lookup"><span data-stu-id="c9f6e-109">**Connection**</span></span> | <span data-ttu-id="c9f6e-110">Connexion ouverte à une source de données OLE DB telle que ADSI.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-110">An open connection to an OLE DB data source such as ADSI.</span></span>                                                                          |
| <span data-ttu-id="c9f6e-111">**Commande**</span><span class="sxs-lookup"><span data-stu-id="c9f6e-111">**Command**</span></span>    | <span data-ttu-id="c9f6e-112">Définit une commande spécifique à exécuter sur la source de données.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-112">Defines a specific command to run against the data source.</span></span>                                                                         |
| <span data-ttu-id="c9f6e-113">**Paramètre**</span><span class="sxs-lookup"><span data-stu-id="c9f6e-113">**Parameter**</span></span>  | <span data-ttu-id="c9f6e-114">Collection facultative pour tous les paramètres à fournir à l’objet de commande.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-114">An optional collection for any parameters to provide to the command object.</span></span>                                                        |
| <span data-ttu-id="c9f6e-115">**RecordSet**</span><span class="sxs-lookup"><span data-stu-id="c9f6e-115">**RecordSet**</span></span>  | <span data-ttu-id="c9f6e-116">Ensemble d’enregistrements d’une table, d’un objet de commande ou d’une syntaxe SQL.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-116">A set of records from a table, command object, or SQL syntax.</span></span> <span data-ttu-id="c9f6e-117">Un jeu d’enregistrements peut être créé sans objet de connexion sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-117">A recordset can be created without any underlying connection object.</span></span> |
| <span data-ttu-id="c9f6e-118">**Champ**</span><span class="sxs-lookup"><span data-stu-id="c9f6e-118">**Field**</span></span>      | <span data-ttu-id="c9f6e-119">Une seule colonne de données dans un jeu d’enregistrements.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-119">A single column of data in a recordset.</span></span>                                                                                            |
| <span data-ttu-id="c9f6e-120">**Propriété**</span><span class="sxs-lookup"><span data-stu-id="c9f6e-120">**Property**</span></span>   | <span data-ttu-id="c9f6e-121">Collection de valeurs fournies par le fournisseur pour ADO.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-121">A collection of values supplied by the provider for ADO.</span></span>                                                                           |
| <span data-ttu-id="c9f6e-122">**Error**</span><span class="sxs-lookup"><span data-stu-id="c9f6e-122">**Error**</span></span>      | <span data-ttu-id="c9f6e-123">Contient des données sur les erreurs d’accès aux données.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-123">Contains data about data access errors.</span></span> <span data-ttu-id="c9f6e-124">Actualisation lorsqu’une erreur se produit en une seule opération.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-124">Refreshed when an error occurs in a single operation.</span></span>                                      |



 

<span data-ttu-id="c9f6e-125">Pour qu’ADO communique avec ADSI, il doit y avoir au moins deux objets ADO : **Connection** et **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-125">For ADO to communicate with ADSI, there must be, at least, two ADO objects: **Connection** and **RecordSet**.</span></span> <span data-ttu-id="c9f6e-126">Ces objets ADO servent à authentifier les utilisateurs et à énumérer les résultats, respectivement.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-126">These ADO objects serve to authenticate users and enumerate results, respectively.</span></span> <span data-ttu-id="c9f6e-127">En règle générale, vous allez également utiliser un objet de **commande** pour maintenir une connexion active, spécifier des paramètres de requête, tels que la taille de page et l’étendue de recherche, et exécuter une requête.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-127">Typically, you will also use a **Command** object to maintain an active connection, specify query parameters, such as page size and search scope, and perform a query.</span></span> <span data-ttu-id="c9f6e-128">Pour plus d’informations sur la syntaxe de filtre de recherche, consultez [syntaxe de filtre de recherche](search-filter-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="c9f6e-128">For more information about the search filter syntax, see [Search Filter Syntax](search-filter-syntax.md).</span></span>

<span data-ttu-id="c9f6e-129">L’objet de **connexion** charge le fournisseur OLE DB et valide les informations d’identification de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-129">The **Connection** object loads the OLE DB provider, and validates user credentials.</span></span> <span data-ttu-id="c9f6e-130">Dans Visual Basic, appelez la fonction **CreateObject** avec «ADODB. Connexion» pour créer une instance d’un objet de **connexion** , puis définissez la propriété **Provider** de l’objet de **connexion** sur « ADSDSOObject ».</span><span class="sxs-lookup"><span data-stu-id="c9f6e-130">In Visual Basic, call the **CreateObject** function with "ADODB.Connection" to create an instance of a **Connection** object, and then set the **Provider** property of the **Connection** object to "ADsDSOObject".</span></span> <span data-ttu-id="c9f6e-131">ADODB. Connection» est le ProgID de l’objet **Connection** et « ADSDSOObject » est le nom du fournisseur OLE DB dans ADSI.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-131">"ADODB.Connection" is the ProgID of the **Connection** object and "ADsDSOObject" is the name of the OLE DB provider in ADSI.</span></span> <span data-ttu-id="c9f6e-132">Si aucune information d’identification n’est spécifiée, les informations d’identification de l’utilisateur actuellement connecté sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-132">If no credentials are specified, the credentials of the currently logged on user are used.</span></span>

<span data-ttu-id="c9f6e-133">L’exemple de code suivant montre comment créer une instance d’un objet de **connexion** .</span><span class="sxs-lookup"><span data-stu-id="c9f6e-133">The following code example shows how to create an instance of a **Connection** object.</span></span>


```VB
Set con = CreateObject("ADODB.Connection")
con.Provider = "ADsDSOObject"
```



<span data-ttu-id="c9f6e-134">L’exemple de code suivant montre comment créer une instance d’un objet de **connexion** .</span><span class="sxs-lookup"><span data-stu-id="c9f6e-134">The following code example shows how to create an instance of a **Connection** object.</span></span>


```VB
<%
Set con = Server.CreateObject("ADODB.Connection")
con.Provider = "ADsDSOObject"
%>
```



<span data-ttu-id="c9f6e-135">L’exemple de code suivant montre comment créer une instance d’un objet de **connexion** .</span><span class="sxs-lookup"><span data-stu-id="c9f6e-135">The following code example shows how to create an instance of a **Connection** object.</span></span> <span data-ttu-id="c9f6e-136">N’oubliez pas que vous devez inclure la bibliothèque de types ADO (msadoXX.dll) comme l’une des références dans le projet Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-136">Be aware that you must include the ADO type library (msadoXX.dll) as one of the references in the Visual Basic project.</span></span>


```VB
Dim Con As New Connection
con.Provider = "ADsDSOObject"
```



<span data-ttu-id="c9f6e-137">Spécifiez les données d’authentification de l’utilisateur en définissant les propriétés de l’objet de **connexion** .</span><span class="sxs-lookup"><span data-stu-id="c9f6e-137">Specify user authentication data by setting the properties of the **Connection** object.</span></span> <span data-ttu-id="c9f6e-138">Le tableau suivant répertorie les propriétés d’authentification utilisateur prises en charge par ADSI.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-138">The following table lists ADSI-supported user-authentication properties.</span></span>



| <span data-ttu-id="c9f6e-139">Propriété</span><span class="sxs-lookup"><span data-stu-id="c9f6e-139">Property</span></span>           | <span data-ttu-id="c9f6e-140">Description</span><span class="sxs-lookup"><span data-stu-id="c9f6e-140">Description</span></span>                                                                                                                                                                                                                                                                                                                                    |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9f6e-141">« ID utilisateur »</span><span class="sxs-lookup"><span data-stu-id="c9f6e-141">"User ID"</span></span>          | <span data-ttu-id="c9f6e-142">Chaîne qui identifie l’utilisateur dont le contexte de sécurité est utilisé lors de l’exécution de la recherche.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-142">A string that identifies the user whose security context is used when performing the search.</span></span> <span data-ttu-id="c9f6e-143">Pour plus d’informations sur le format de la chaîne de nom d’utilisateur, consultez [**IADsOpenDSObject :: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject).</span><span class="sxs-lookup"><span data-stu-id="c9f6e-143">For more information about the format of the user name string, see [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject).</span></span> <span data-ttu-id="c9f6e-144">S’il n’est pas spécifié, la valeur par défaut est l’utilisateur connecté, ou l’utilisateur représenté par le processus appelant.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-144">If not specified, the default is the logged on user, or the user impersonated by the calling process.</span></span> |
| <span data-ttu-id="c9f6e-145">« Mot de passe »</span><span class="sxs-lookup"><span data-stu-id="c9f6e-145">"Password"</span></span>         | <span data-ttu-id="c9f6e-146">Chaîne qui spécifie le mot de passe de l’utilisateur identifié par « ID d’utilisateur ».</span><span class="sxs-lookup"><span data-stu-id="c9f6e-146">A string that specifies the password of the user identified by "User ID".</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="c9f6e-147">« Chiffrer le mot de passe »</span><span class="sxs-lookup"><span data-stu-id="c9f6e-147">"Encrypt Password"</span></span> | <span data-ttu-id="c9f6e-148">Valeur booléenne qui spécifie si le mot de passe est chiffré.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-148">A Boolean value that specifies whether the password is encrypted.</span></span> <span data-ttu-id="c9f6e-149">La valeur par défaut est **false**.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-149">The default is **false**.</span></span>                                                                                                                                                                                                                                                    |
| <span data-ttu-id="c9f6e-150">« Indicateur ADSI »</span><span class="sxs-lookup"><span data-stu-id="c9f6e-150">"ADSI Flag"</span></span>        | <span data-ttu-id="c9f6e-151">Ensemble d’indicateurs de l’énumération [**\_ d' \_ énumération d’authentification ADS**](/windows/win32/api/iads/ne-iads-ads_authentication_enum) qui spécifient les options d’authentification de liaison.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-151">A set of flags from the [**ADS\_AUTHENTICATION\_ENUM**](/windows/win32/api/iads/ne-iads-ads_authentication_enum) enumeration that specify the binding authentication options.</span></span> <span data-ttu-id="c9f6e-152">La valeur par défaut est zéro.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-152">The default is zero.</span></span>                                                                                                                                                                         |



 

<span data-ttu-id="c9f6e-153">L’exemple de code suivant montre comment les propriétés sont définies avant la création de l’objet de **commande** .</span><span class="sxs-lookup"><span data-stu-id="c9f6e-153">The following code example shows how the properties are set before creating the **Command** object.</span></span>


```VB
Set oConnect = CreateObject("ADODB.Connection")
oConnect.Provider = "ADsDSOObject"
oConnect.Properties("User ID") = stUser
oConnect.Properties("Password") = stPass
oConnect.Properties("Encrypt Password") = True
oConnect.Open "DS Query", stUser, stPass
```



<span data-ttu-id="c9f6e-154">Le deuxième objet ADO est l’objet **Command** .</span><span class="sxs-lookup"><span data-stu-id="c9f6e-154">The second ADO object is the **Command** object.</span></span> <span data-ttu-id="c9f6e-155">L’identificateur de programme (ProgID) de l’objet **Command** est « ADODB. Command ».</span><span class="sxs-lookup"><span data-stu-id="c9f6e-155">The ProgID of the **Command** object is "ADODB.Command".</span></span> <span data-ttu-id="c9f6e-156">Cet objet vous permet d’émettre des instructions de requête et d’autres commandes à ADSI à l’aide de la connexion active.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-156">This object enables you to issue query statements and other commands to ADSI using the active connection.</span></span> <span data-ttu-id="c9f6e-157">L’objet **Command** utilise sa propriété **ActiveConnection** pour maintenir une connexion active.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-157">The **Command** object uses its **ActiveConnection** property to maintain an active connection.</span></span> <span data-ttu-id="c9f6e-158">Elle gère également la propriété **CommandText** pour contenir des instructions de requête émises par un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-158">It also maintains the **CommandText** property to hold query statements issued by a user.</span></span> <span data-ttu-id="c9f6e-159">Les instructions de requête sont exprimées dans le dialecte [SQL](sql-dialect.md) ou le [dialecte LDAP](ldap-dialect.md).</span><span class="sxs-lookup"><span data-stu-id="c9f6e-159">The query statements are expressed in either the [SQL dialect](sql-dialect.md) or the [LDAP dialect](ldap-dialect.md).</span></span>

<span data-ttu-id="c9f6e-160">Les exemples de code suivants montrent comment créer un objet de **commande** .</span><span class="sxs-lookup"><span data-stu-id="c9f6e-160">The following code examples show how to create a **Command** object.</span></span>


```VB
Set command = CreateObject("ADODB.Command")
Set command.ActiveConnection = oConnect
command.CommandText = 
"SELECT AdsPath, cn FROM 'LDAP://DC=Fabrikam,DC=com' WHERE objectClass = '*'"
```



<span data-ttu-id="c9f6e-161">Dans l’exemple de code suivant, incluez la bibliothèque de types ADO (msadoXX.dll) comme l’une des références.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-161">In the following code example, include ADO type library (msadoXX.dll) as one of the references.</span></span>


```VB
Dim command As New Command
Set command.ActiveConnection = oConnect
command.CommandText = "<LDAP://DC=Fabrikam,DC=com>;(objectClass=*);AdsPath, cn; subTree"
```



<span data-ttu-id="c9f6e-162">Les options de recherche pour l’objet de **commande** sont spécifiées en définissant la propriété **Properties** .</span><span class="sxs-lookup"><span data-stu-id="c9f6e-162">Search options for the **Command** object are specified by setting the **Properties** property.</span></span> <span data-ttu-id="c9f6e-163">Le tableau suivant répertorie les propriétés nommées acceptables pour les **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-163">The following table lists acceptable named properties for **Properties**.</span></span>



| <span data-ttu-id="c9f6e-164">Propriété nommée</span><span class="sxs-lookup"><span data-stu-id="c9f6e-164">Named property</span></span>      | <span data-ttu-id="c9f6e-165">Description</span><span class="sxs-lookup"><span data-stu-id="c9f6e-165">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9f6e-166">Synchrone</span><span class="sxs-lookup"><span data-stu-id="c9f6e-166">"Asynchronous"</span></span>      | <span data-ttu-id="c9f6e-167">Valeur booléenne qui spécifie si la recherche est synchrone ou asynchrone.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-167">A Boolean value that specifies whether the search is synchronous or asynchronous.</span></span> <span data-ttu-id="c9f6e-168">La valeur par défaut est false (synchrone).</span><span class="sxs-lookup"><span data-stu-id="c9f6e-168">The default is False (synchronous).</span></span> <span data-ttu-id="c9f6e-169">Une recherche synchrone bloque jusqu’à ce que le serveur retourne l’intégralité du résultat, ou pour une recherche paginée, la page entière.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-169">A synchronous search blocks until the server returns the entire result, or for a paged search, the entire page.</span></span> <span data-ttu-id="c9f6e-170">Une recherche asynchrone se bloque jusqu’à ce qu’une ligne des résultats de la recherche soit disponible ou jusqu’à ce que l’heure spécifiée par la propriété « Timeout » soit écoulée.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-170">An asynchronous search blocks until one row of the search results is available, or until the time specified by the "Timeout" property elapses.</span></span>                           |
| <span data-ttu-id="c9f6e-171">« Résultats du cache »</span><span class="sxs-lookup"><span data-stu-id="c9f6e-171">"Cache results"</span></span>     | <span data-ttu-id="c9f6e-172">Valeur booléenne qui spécifie si le résultat doit être mis en cache côté client.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-172">A Boolean value that specifies whether the result should be cached on the client side.</span></span> <span data-ttu-id="c9f6e-173">La valeur par défaut est **true**. L’interface ADSI met en cache le jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-173">The default is **true**; ADSI caches the result set.</span></span> <span data-ttu-id="c9f6e-174">La désactivation de cette option peut être souhaitable pour les jeux de résultats volumineux.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-174">Turning off this option may be desirable for large result sets.</span></span>                                                                                                                                                                                                    |
| <span data-ttu-id="c9f6e-175">« Débusquer les références »</span><span class="sxs-lookup"><span data-stu-id="c9f6e-175">"Chase referrals"</span></span>   | <span data-ttu-id="c9f6e-176">Valeur de l' [**\_ \_ \_ énumération de références Chase ADS**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) qui spécifie la manière dont la recherche repère les références.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-176">A value from the [**ADS\_CHASE\_REFERRALS\_ENUM**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) that specifies how the search chases referrals.</span></span> <span data-ttu-id="c9f6e-177">La valeur par défaut est les références de la **\_ Chase ADS \_ \_ jamais**. Pour plus d’informations sur cette propriété, consultez [références](/windows/desktop/AD/referrals).</span><span class="sxs-lookup"><span data-stu-id="c9f6e-177">The default is **ADS\_CHASE\_REFERRALS\_NEVER**.For more information about this property, see [Referrals](/windows/desktop/AD/referrals).</span></span><br/>                                                                                                                                           |
| <span data-ttu-id="c9f6e-178">« Noms de colonnes uniquement »</span><span class="sxs-lookup"><span data-stu-id="c9f6e-178">"Column Names Only"</span></span> | <span data-ttu-id="c9f6e-179">Valeur booléenne qui indique que la recherche doit récupérer uniquement le nom des attributs auxquels des valeurs ont été assignées.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-179">A Boolean value that indicates that the search should retrieve only the name of attributes to which values have been assigned.</span></span> <span data-ttu-id="c9f6e-180">La valeur par défaut est **false**.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-180">The default is **false**.</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="c9f6e-181">« Alias de Deref »</span><span class="sxs-lookup"><span data-stu-id="c9f6e-181">"Deref Aliases"</span></span>     | <span data-ttu-id="c9f6e-182">Valeur booléenne qui spécifie si les alias des objets trouvés sont résolus.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-182">A Boolean value that specifies whether aliases of found objects are resolved.</span></span> <span data-ttu-id="c9f6e-183">La valeur par défaut est **false**.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-183">The default is **false**.</span></span>                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="c9f6e-184">« Taille de la page »</span><span class="sxs-lookup"><span data-stu-id="c9f6e-184">"Page size"</span></span>         | <span data-ttu-id="c9f6e-185">Valeur entière qui active la pagination et spécifie le nombre maximal d’objets à retourner dans un jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-185">An integer value that turns on paging and specifies the maximum number of objects to return in a results set.</span></span> <span data-ttu-id="c9f6e-186">La valeur par défaut est aucune taille de page.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-186">The default is no page size.</span></span> <span data-ttu-id="c9f6e-187">Pour plus d’informations, consultez [récupération de jeux de résultats volumineux](retrieving-large-results-sets.md).</span><span class="sxs-lookup"><span data-stu-id="c9f6e-187">For more information, see [Retrieving Large Results Sets](retrieving-large-results-sets.md).</span></span>                                                                                                                                                                       |
| <span data-ttu-id="c9f6e-188">SearchScope</span><span class="sxs-lookup"><span data-stu-id="c9f6e-188">"SearchScope"</span></span>       | <span data-ttu-id="c9f6e-189">Valeur de l’énumération [**\_ SCOPEENUM ADS**](/windows/win32/api/iads/ne-iads-ads_scopeenum) qui spécifie la zone de recherche.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-189">A value from the [**ADS\_SCOPEENUM**](/windows/win32/api/iads/ne-iads-ads_scopeenum) enumeration that specifies the search scope.</span></span> <span data-ttu-id="c9f6e-190">La valeur par défaut est la **\_ sous- \_ arborescence étendue ADS**.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-190">The default is **ADS\_SCOPE\_SUBTREE**.</span></span>                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="c9f6e-191">« Limite de taille »</span><span class="sxs-lookup"><span data-stu-id="c9f6e-191">"Size Limit"</span></span>        | <span data-ttu-id="c9f6e-192">Valeur entière qui spécifie la limite de taille pour la recherche.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-192">An integer value that specifies the size limit for the search.</span></span> <span data-ttu-id="c9f6e-193">Par Active Directory, la limite de taille spécifie le nombre maximal d’objets retournés.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-193">For Active Directory, the size limit specifies the maximum number of returned objects.</span></span> <span data-ttu-id="c9f6e-194">Le serveur arrête la recherche lorsque la limite de taille est atteinte et retourne les résultats accumulés.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-194">The server stops searching when the size limit is reached and returns the results accumulated.</span></span> <span data-ttu-id="c9f6e-195">La valeur par défaut est aucune limite.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-195">The default is no limit.</span></span>                                                                                                                                  |
| <span data-ttu-id="c9f6e-196">« Trier sur »</span><span class="sxs-lookup"><span data-stu-id="c9f6e-196">"Sort on"</span></span>           | <span data-ttu-id="c9f6e-197">Chaîne qui spécifie une liste d’attributs séparés par des virgules à utiliser comme clés de tri.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-197">A string that specifies a comma-separated list of attributes to use as sort keys.</span></span> <span data-ttu-id="c9f6e-198">Cette propriété fonctionne uniquement pour les serveurs d’annuaire qui prennent en charge le contrôle LDAP pour le tri côté serveur.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-198">This property works only for directory servers that support the LDAP control for server-side sorting.</span></span> <span data-ttu-id="c9f6e-199">Active Directory prend en charge le contrôle de tri, mais il peut avoir un impact sur les performances du serveur, en particulier si le jeu de résultats est volumineux.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-199">Active Directory supports the sort control, but it can impact server performance, particularly if the results set is large.</span></span> <span data-ttu-id="c9f6e-200">N’oubliez pas que Active Directory ne prend en charge qu’une seule clé de tri.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-200">Be aware that Active Directory supports only a single sort key.</span></span> <span data-ttu-id="c9f6e-201">La valeur par défaut est aucun tri.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-201">The default is no sorting.</span></span> |
| <span data-ttu-id="c9f6e-202">« Limite de temps »</span><span class="sxs-lookup"><span data-stu-id="c9f6e-202">"Time Limit"</span></span>        | <span data-ttu-id="c9f6e-203">Valeur entière qui spécifie la limite de temps, en secondes, pour la recherche.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-203">An integer value that specifies the time limit, in seconds, for the search.</span></span> <span data-ttu-id="c9f6e-204">Lorsque la limite de temps est atteinte, le serveur arrête la recherche et retourne les résultats accumulés.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-204">When the time limit is reached, the server stops searching and returns the results accumulated.</span></span> <span data-ttu-id="c9f6e-205">La valeur par défaut est aucune limite de durée.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-205">The default is no time limit.</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="c9f6e-206">Expiré</span><span class="sxs-lookup"><span data-stu-id="c9f6e-206">"Timeout"</span></span>           | <span data-ttu-id="c9f6e-207">Valeur entière qui spécifie la valeur du délai d’attente côté client, en secondes.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-207">An integer value that specifies the client-side timeout value, in seconds.</span></span> <span data-ttu-id="c9f6e-208">Cette valeur indique l’heure à laquelle le client attend les résultats du serveur avant d’arrêter la recherche.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-208">This value indicates the time the client waits for results from the server before stopping the search.</span></span> <span data-ttu-id="c9f6e-209">La valeur par défaut est aucun délai d’attente.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-209">The default is no time-out.</span></span>                                                                                                                                                                                                  |



 

<span data-ttu-id="c9f6e-210">L’exemple de code suivant montre comment définir des options de recherche.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-210">The following code example shows how to set search options.</span></span>


```VB
Const ADS_SCOPE_ONELEVEL = 1
Const ADS_CHASE_REFERRALS_EXTERNAL = &H40

Dim Com As New Command
 
Com.Properties("Page Size") = 999
Com.Properties("Timeout") = 30     ' Seconds
Com.Properties("searchscope") = ADS_SCOPE_ONELEVEL
Com.Properties("Chase referrals") = ADS_CHASE_REFERRALS_EXTERNAL
Com.Properties("Cache Results") = False     ' Do not cache the result set.
```



<span data-ttu-id="c9f6e-211">Le troisième objet ADO est **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-211">The third ADO object is **RecordSet**.</span></span> <span data-ttu-id="c9f6e-212">Vous obtenez cet objet lorsque vous appelez la méthode **Execute** sur un objet **Command** .</span><span class="sxs-lookup"><span data-stu-id="c9f6e-212">You obtain this object when you invoke the **Execute** method on a **Command** object.</span></span> <span data-ttu-id="c9f6e-213">La fonction principale de l’objet **Recordset** consiste à énumérer le jeu de résultats et à obtenir les données.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-213">The primary function of the **RecordSet** object is to enumerate the result set and obtain the data.</span></span> <span data-ttu-id="c9f6e-214">Le jeu de résultats peut contenir des valeurs pour les attributs qui ont une ou plusieurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-214">The result set can contain values for attributes that have both single or multiple values.</span></span> <span data-ttu-id="c9f6e-215">L’obtention d’un attribut à valeur unique est simple, similaire à l’obtention de la valeur de colonne dans la base de données relationnelle, par exemple :</span><span class="sxs-lookup"><span data-stu-id="c9f6e-215">Getting a single-valued attribute is simple, similar to getting the column value in the relational database, for example:</span></span>


```VB
Fields('name').Value
```



<span data-ttu-id="c9f6e-216">Toutefois, l’obtention d’un attribut avec plusieurs valeurs est plus complexe.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-216">Getting an attribute with multiple values, however, is more challenging.</span></span> <span data-ttu-id="c9f6e-217">Dans ce cas, le **champ. Value** est un tableau et vous devez vérifier les limites inférieure et supérieure du tableau, comme indiqué dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-217">In this case, the **Field.Value** is an array and you must check the lower and upper bound of the array, as shown in the following code example.</span></span>


```VB
Set rs = Com.Execute
 
For i = 0 To rs.Fields.Count - 1
    Debug.Print rs.Fields(i).Name, rs.Fields(i).Type
Next i
 
'--------------------------
' Navigate the record set.
'--------------------------
rs.MoveFirst
lstResult.Clear      ' Clear the user interface.
While Not rs.EOF
For i = 0 To rs.Fields.Count - 1
    ' For Multi Value attribute
    If rs.Fields(i).Type = adVariant And Not (IsNull(rs.Fields(i).Value)) Then
        Debug.Print rs.Fields(i).Name, " = "
        For j = LBound(rs.Fields(i).Value) To UBound(rs.Fields(i).Value)
            Debug.Print rs.Fields(i).Value(j), " # "
            lstResult.AddItem rs.Fields(i).Value(j)
        Next j
    Else
        ' For Single Value attribute.
         Debug.Print rs.Fields(i).Name, " = ", rs.Fields(i).Value
         lstResult.AddItem rs.Fields(i).Value
    End If
Next i
rs.MoveNext
Wend
```



<span data-ttu-id="c9f6e-218">L’exemple de code suivant désactive les comptes d’utilisateur sur un serveur LDAP.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-218">The following code example disables the user accounts on an LDAP server.</span></span>


```VB
Dim X as IADs
Dim con As New Connection, rs As New Recordset
Dim MyUser As IADsUser
 
con.Provider = "ADsDSOObject"
con.Open "Active Directory Provider", "CN=Test,CN=Users,DC=Fabrikam,DC=COM,O=INTERNET", "Password"
Set rs = con.Execute("<LDAP://MyMachine/DC=MyDomain,DC=Fabrikam,DC=com>;(objectClass=User);ADsPath;onelevel")
 
While Not rs.EOF
    ' Bind to the object to make changes 
    ' to it because ADO is currently read-only.
    MyUser = GetObject(rs.Fields(0).Value)
    MyUser.AccountDisabled = True
    MyUser.SetInfo
    rs.MoveNext
Wend
```



<span data-ttu-id="c9f6e-219">Pour plus d’informations sur le modèle objet ADO, consultez [Microsoft ActiveX Data Objects](/sql/ado/microsoft-activex-data-objects-ado?view=sql-server-ver15).</span><span class="sxs-lookup"><span data-stu-id="c9f6e-219">For more information about the ADO object model, see [Microsoft ActiveX Data Objects](/sql/ado/microsoft-activex-data-objects-ado?view=sql-server-ver15).</span></span>

 

