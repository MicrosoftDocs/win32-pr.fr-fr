---
title: Requête distribuée
description: Étant donné qu’ADSI est un fournisseur de OLE DB, il peut participer à une requête distribuée introduite dans Microsoft SQL Server 7,0.
ms.assetid: 0a93ec2e-397a-47f7-b00c-f0f9aaa06de6
ms.tgt_platform: multiple
keywords:
- requêtes ADSI, requête distribuée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8675f0a5ba9faa6ece78783eb4f61f17aafabc8
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "106511474"
---
# <a name="distributed-query"></a><span data-ttu-id="94f32-104">Requête distribuée</span><span class="sxs-lookup"><span data-stu-id="94f32-104">Distributed Query</span></span>

<span data-ttu-id="94f32-105">Étant donné qu’ADSI est un fournisseur de OLE DB, il peut participer à une requête distribuée introduite dans Microsoft SQL Server 7,0.</span><span class="sxs-lookup"><span data-stu-id="94f32-105">Because ADSI is an OLE DB Provider, it can participate in Distributed Query introduced in Microsoft SQL Server 7.0.</span></span> <span data-ttu-id="94f32-106">Les scénarios possibles sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="94f32-106">The following are possible scenarios:</span></span>

-   <span data-ttu-id="94f32-107">Jointure d’objets Active Directory avec des données SQL Server.</span><span class="sxs-lookup"><span data-stu-id="94f32-107">Joining Active Directory objects with SQL Server data.</span></span>
-   <span data-ttu-id="94f32-108">Mise à jour des données SQL à partir d’objets Active Directory.</span><span class="sxs-lookup"><span data-stu-id="94f32-108">Updating SQL data from Active Directory objects.</span></span>
-   <span data-ttu-id="94f32-109">Création de jointures à trois ou quatre voies avec d’autres fournisseurs de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="94f32-109">Creating three-way or four-way joins with other OLE DB Providers.</span></span> <span data-ttu-id="94f32-110">Par exemple, Index Server, SQL Server et Active Directory.</span><span class="sxs-lookup"><span data-stu-id="94f32-110">For example, Index Server, SQL Server, and Active Directory.</span></span>

<span data-ttu-id="94f32-111">Le fournisseur OLE DB prend en charge deux dialectes de commande, LDAP et SQL, pour accéder au service d’annuaire et retourner des résultats sous forme de tableau qui peut être interrogé avec SQL Server requêtes distribuées.</span><span class="sxs-lookup"><span data-stu-id="94f32-111">The OLE DB Provider supports two command dialects, LDAP and SQL, to access the directory service and return results in a tabular form that can be queried with SQL Server distributed queries.</span></span>

<span data-ttu-id="94f32-112">**Pour démarrer l’analyseur de requêtes SQL**</span><span class="sxs-lookup"><span data-stu-id="94f32-112">**To start the SQL Query Analyzer**</span></span>

1.  <span data-ttu-id="94f32-113">Tout d’abord, ouvrez l' [Analyseur de requêtes SQL](https://msdn.microsoft.com/library/Aa216983.aspx) sur le SQL Server lié au service d’annuaire (consultez Création d’un serveur lié).</span><span class="sxs-lookup"><span data-stu-id="94f32-113">First, open the [SQL Query Analyzer](https://msdn.microsoft.com/library/Aa216983.aspx) on the SQL Server that is linked to the directory service (see Creating a Linked Server).</span></span>
2.  <span data-ttu-id="94f32-114">Exécuter l' **Analyseur de requêtes SQL** ( \| programmes de démarrage \| Microsoft SQL Server 7,0)</span><span class="sxs-lookup"><span data-stu-id="94f32-114">Run the **SQL Query Analyzer** (Start \| Programs \| Microsoft SQL Server 7.0)</span></span>
3.  <span data-ttu-id="94f32-115">Connectez-vous à l’ordinateur SQL Server.</span><span class="sxs-lookup"><span data-stu-id="94f32-115">Log on to the SQL Server computer.</span></span>
4.  <span data-ttu-id="94f32-116">Entrez la requête SQL dans le volet de l’éditeur de la fenêtre de requête.</span><span class="sxs-lookup"><span data-stu-id="94f32-116">Enter the SQL Query into the Editor pane of the query window.</span></span>
5.  <span data-ttu-id="94f32-117">Exécutez la requête en appuyant sur F5.</span><span class="sxs-lookup"><span data-stu-id="94f32-117">Execute the query by pressing F5.</span></span>

<span data-ttu-id="94f32-118">Les sections suivantes fournissent plus de détails :</span><span class="sxs-lookup"><span data-stu-id="94f32-118">The following sections provide more detail:</span></span>

-   [<span data-ttu-id="94f32-119">Création d’un serveur lié</span><span class="sxs-lookup"><span data-stu-id="94f32-119">Creating a Linked Server</span></span>](#creating-a-linked-server)
-   [<span data-ttu-id="94f32-120">Création d’une connexion authentifiée SQL Server</span><span class="sxs-lookup"><span data-stu-id="94f32-120">Creating a SQL Server Authenticated Login</span></span>](#creating-a-sql-server-authenticated-login)
-   [<span data-ttu-id="94f32-121">Interrogation du service d'annuaire</span><span class="sxs-lookup"><span data-stu-id="94f32-121">Querying the Directory Service</span></span>](#querying-the-directory-service)

## <a name="creating-a-linked-server"></a><span data-ttu-id="94f32-122">Création d’un serveur lié</span><span class="sxs-lookup"><span data-stu-id="94f32-122">Creating a Linked Server</span></span>

<span data-ttu-id="94f32-123">Pour configurer une jointure distribuée sur un service d’annuaire Windows 2000 Server, créez un serveur lié.</span><span class="sxs-lookup"><span data-stu-id="94f32-123">To set up a distributed join on a Windows 2000 Server directory service, create a linked server.</span></span> <span data-ttu-id="94f32-124">Pour ce faire, configurez le mappage ADSI à l’aide de la procédure stockée système [SP \_ addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) .</span><span class="sxs-lookup"><span data-stu-id="94f32-124">To do this, set up ADSI mapping by using the [sp\_addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) System Stored Procedure.</span></span> <span data-ttu-id="94f32-125">Cette procédure lie un nom à un nom de fournisseur OLE DB.</span><span class="sxs-lookup"><span data-stu-id="94f32-125">This procedure links a name to an OLE DB Provider name.</span></span>

<span data-ttu-id="94f32-126">Dans l’exemple suivant, Notez qu’il existe plusieurs arguments utilisés avec la procédure stockée système [SP \_ addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) :</span><span class="sxs-lookup"><span data-stu-id="94f32-126">In the following example, note that there are several arguments used with the [sp\_addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) System Stored Procedure:</span></span>

-   <span data-ttu-id="94f32-127">« ADSI » est l’argument de **serveur** et sera le nom de ce serveur lié.</span><span class="sxs-lookup"><span data-stu-id="94f32-127">"ADSI" is the **server** argument and will be the name of this linked server.</span></span>
-   <span data-ttu-id="94f32-128">« Active Directory Services 2,5 » est l’argument **srvproduct** , qui est le nom de la source de données OLE DB que vous ajoutez en tant que serveur lié.</span><span class="sxs-lookup"><span data-stu-id="94f32-128">"Active Directory Services 2.5" is the **srvproduct** argument, which is the name of the OLE DB data source that you are adding as a linked server.</span></span>
-   <span data-ttu-id="94f32-129">« ADSDSOObject » est l’argument du **\_ nom du fournisseur** .</span><span class="sxs-lookup"><span data-stu-id="94f32-129">"ADSDSOObject" is the **provider\_name** argument.</span></span>
-   <span data-ttu-id="94f32-130">« adsdatasource » est l’argument de **\_ source de données** , qui est le nom de la source de données tel qu’il est interprété par le fournisseur OLE DB.</span><span class="sxs-lookup"><span data-stu-id="94f32-130">"adsdatasource" is the **data\_source** argument, which is the name of the data source as interpreted by the OLE DB Provider.</span></span>

<span data-ttu-id="94f32-131">La commande [Exec](https://msdn.microsoft.com/library/Aa258848.aspx) est utilisée pour exécuter des procédures stockées système.</span><span class="sxs-lookup"><span data-stu-id="94f32-131">The [EXEC](https://msdn.microsoft.com/library/Aa258848.aspx) command is used to execute System Stored Procedures.</span></span>


```sql
EXEC sp_addlinkedserver 'ADSI', 'Active Directory Services 2.5', 
'ADSDSOObject', 'adsdatasource'
GO
```



<span data-ttu-id="94f32-132">Pour les connexions authentifiées par Windows, l’auto-mappage est suffisant pour accéder à l’annuaire avec SQL Server délégation de sécurité.</span><span class="sxs-lookup"><span data-stu-id="94f32-132">For Windows-authenticated logins, the self-mapping is sufficient to access the directory with SQL Server Security Delegation.</span></span> <span data-ttu-id="94f32-133">Étant donné que le mappage automatique est créé par défaut pour les serveurs liés créés via [SP \_ addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx), aucun autre mappage de connexion n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="94f32-133">Because the self-mapping is created by default for linked servers created through [sp\_addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx), no other login mapping is necessary.</span></span>

<span data-ttu-id="94f32-134">Pour les connexions SQL Server – authentifiées, vous pouvez configurer des connexions et des mots de passe appropriés pour la connexion au service d’annuaire à l’aide de la procédure stockée système [SP \_ addlinkedsrvlogin](https://msdn.microsoft.com/library/Aa259581.aspx) .</span><span class="sxs-lookup"><span data-stu-id="94f32-134">For SQL Server–authenticated logins, you can configure suitable logins and passwords for connecting to the directory service by using the [sp\_addlinkedsrvlogin](https://msdn.microsoft.com/library/Aa259581.aspx) System Stored Procedure.</span></span>

> [!Note]  
> <span data-ttu-id="94f32-135">Lorsque c'est possible, utilisez l'authentification Windows.</span><span class="sxs-lookup"><span data-stu-id="94f32-135">When possible, use Windows Authentication.</span></span>

 

## <a name="creating-a-sql-server-authenticated-login"></a><span data-ttu-id="94f32-136">Création d’une connexion authentifiée SQL Server</span><span class="sxs-lookup"><span data-stu-id="94f32-136">Creating a SQL Server Authenticated Login</span></span>

<span data-ttu-id="94f32-137">Si vous préférez utiliser une connexion SQL Server-authentifié plutôt que l’authentification Windows, ajoutez une connexion au serveur lié (voir la section précédente).</span><span class="sxs-lookup"><span data-stu-id="94f32-137">If you prefer to use a SQL Server–authenticated login rather than Windows Authentication, add a login to the linked server (see the previous section).</span></span> <span data-ttu-id="94f32-138">Pour ce faire, utilisez la procédure stockée système [SP \_ addlinkedsrvlogin](https://msdn.microsoft.com/library/Aa259581.aspx) .</span><span class="sxs-lookup"><span data-stu-id="94f32-138">To do this, use the [sp\_addlinkedsrvlogin](https://msdn.microsoft.com/library/Aa259581.aspx) System Stored Procedure.</span></span>

<span data-ttu-id="94f32-139">Dans l’exemple suivant, plusieurs arguments sont utilisés avec la procédure stockée système [SP \_ addlinkedsrvlogin](https://msdn.microsoft.com/library/Aa259581.aspx) :</span><span class="sxs-lookup"><span data-stu-id="94f32-139">In the following example, there are several arguments that are used with the [sp\_addlinkedsrvlogin](https://msdn.microsoft.com/library/Aa259581.aspx) System Stored Procedure:</span></span>

-   <span data-ttu-id="94f32-140">« ADSI » est l’argument **rmtsvrname** , qui est le nom du serveur lié créé dans l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="94f32-140">"ADSI" is the **rmtsvrname** argument, which is the name of the linked server created in the previous example.</span></span>
-   <span data-ttu-id="94f32-141">« Fabrikam \\ Administrator » est l’argument **LocalLogin** , qui est la connexion sur le serveur local et peut être la connexion SQL Server ou un utilisateur Windows NT.</span><span class="sxs-lookup"><span data-stu-id="94f32-141">"Fabrikam\\Administrator" is the **locallogin** argument, which is the login on the local server and can be the SQL Server login or a Windows NT user.</span></span>
-   <span data-ttu-id="94f32-142">"CN = administrateur, OU = Sales, DC = activeds, DC = fabrikam, DC = com" est l’argument **rmtuser** , qui est le nom d’utilisateur que vous utilisez pour vous connecter, car **useself** a la **valeur false**.</span><span class="sxs-lookup"><span data-stu-id="94f32-142">"CN=Administrator,OU=Sales,DC=activeds,DC=Fabrikam,DC=com" is the **rmtuser** argument, which is the user name that you use to connect because **useself** is **false**.</span></span>
-   <span data-ttu-id="94f32-143">« secret \* \* 2000 » est le **rmtpassword**, qui est le mot de passe associé à **rmtuser**</span><span class="sxs-lookup"><span data-stu-id="94f32-143">"secret\*\*2000" is the **rmtpassword**, which is the password associated to **rmtuser**</span></span>

<span data-ttu-id="94f32-144">La commande [Exec](https://msdn.microsoft.com/library/Aa258848.aspx) est utilisée pour exécuter des procédures stockées système.</span><span class="sxs-lookup"><span data-stu-id="94f32-144">The [EXEC](https://msdn.microsoft.com/library/Aa258848.aspx) command is used to execute System Stored Procedures.</span></span>


```sql
EXEC sp_addlinkedsrvlogin 'ADSI', false, 'Fabrikam\Administrator', 
'CN=Administrator,OU=Sales,DC=activeds,DC=Fabrikam,DC=com', 'secret**2000'
```



## <a name="querying-the-directory-service"></a><span data-ttu-id="94f32-145">Interrogation du service d'annuaire</span><span class="sxs-lookup"><span data-stu-id="94f32-145">Querying the Directory Service</span></span>

<span data-ttu-id="94f32-146">Une fois que vous avez créé un serveur lié, utilisez une instruction [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) pour envoyer une requête au service d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="94f32-146">After you have created a linked server, use an [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) statement to send a query to the Directory Service.</span></span> <span data-ttu-id="94f32-147">La requête SQL suivante crée une table virtuelle pour stocker les résultats de votre requête à l’aide de l’instruction [Create View](https://msdn.microsoft.com/library/Aa258253.aspx) .</span><span class="sxs-lookup"><span data-stu-id="94f32-147">The following SQL query creates a virtual table to hold your query results by using the [CREATE VIEW](https://msdn.microsoft.com/library/Aa258253.aspx) statement.</span></span> <span data-ttu-id="94f32-148">La vue créée est nommée « viewADContacts ».</span><span class="sxs-lookup"><span data-stu-id="94f32-148">The view that is created is named "viewADContacts".</span></span>

<span data-ttu-id="94f32-149">La première instruction [Select](https://msdn.microsoft.com/library/Aa259187.aspx) définit les informations qui sont interrogées à partir du service d’annuaire et les mappe à une colonne de la table.</span><span class="sxs-lookup"><span data-stu-id="94f32-149">The first [SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) statement defines the information that is being queried from the directory service and maps it to a column in the table.</span></span> <span data-ttu-id="94f32-150">Les informations entourées de crochets indiquent les données qui sont placées dans la table virtuelle.</span><span class="sxs-lookup"><span data-stu-id="94f32-150">Information surrounded by brackets indicates the data that is put into the virtual table.</span></span> <span data-ttu-id="94f32-151">Les informations qui ne sont pas entre parenthèses indiquent les données récupérées à partir du service d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="94f32-151">The information that is not in brackets indicates the data that is retrieved from the directory service.</span></span> <span data-ttu-id="94f32-152">Notez que les informations récupérées à partir du service d’annuaire doivent être référencées par leur nom complet LDAP.</span><span class="sxs-lookup"><span data-stu-id="94f32-152">Notice that the information that is being retrieved from the directory service must be referenced by its LDAP display name.</span></span>

<span data-ttu-id="94f32-153">L’instruction suivante est l’instruction [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) .</span><span class="sxs-lookup"><span data-stu-id="94f32-153">The next statement is the [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) statement.</span></span> <span data-ttu-id="94f32-154">Cette instruction a deux arguments : ADSI, qui est le nom du serveur lié que vous avez créé et une instruction de requête.</span><span class="sxs-lookup"><span data-stu-id="94f32-154">This statement has two arguments: ADSI, which is the name of the linked server that you created, and a query statement.</span></span> <span data-ttu-id="94f32-155">L’instruction de requête contient les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="94f32-155">The query statement contains the following items:</span></span>

-   <span data-ttu-id="94f32-156">L’instruction [Select](https://msdn.microsoft.com/library/Aa259187.aspx) contient la liste des données qui seront obtenues à partir du service d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="94f32-156">The [SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) statement contains the list of data that will be obtained from the directory service.</span></span> <span data-ttu-id="94f32-157">Vous devrez utiliser le nom d’affichage LDAP pour indiquer les données que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="94f32-157">You will need to use the LDAP display name to indicate which data you are searching for.</span></span>
-   <span data-ttu-id="94f32-158">L’instruction [from](https://msdn.microsoft.com/library/Aa258869.aspx) contient le nom du serveur d’annuaire lié à partir duquel ces informations seront obtenues.</span><span class="sxs-lookup"><span data-stu-id="94f32-158">The [FROM](https://msdn.microsoft.com/library/Aa258869.aspx) statement contains the name of the linked directory server where this information will be obtained from.</span></span>
-   <span data-ttu-id="94f32-159">L’instruction [Where](https://msdn.microsoft.com/library/Aa260674.aspx) fournit les conditions de recherche.</span><span class="sxs-lookup"><span data-stu-id="94f32-159">The [WHERE](https://msdn.microsoft.com/library/Aa260674.aspx) statement provides the search conditions.</span></span> <span data-ttu-id="94f32-160">Dans cet exemple, il recherche des contacts.</span><span class="sxs-lookup"><span data-stu-id="94f32-160">In this example, it is searching for contacts.</span></span>

<span data-ttu-id="94f32-161">La dernière instruction [Select](https://msdn.microsoft.com/library/Aa259187.aspx) est utilisée pour récupérer les résultats de la vue à afficher.</span><span class="sxs-lookup"><span data-stu-id="94f32-161">The final [SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) statement is used to pick up results from the view to display.</span></span>


```sql
CREATE VIEW viewADContacts
AS
SELECT  [Name], sn [Last Name], street [Street], l [City], st [State]
FROM OPENQUERY( ADSI, 
     'SELECT name, sn, street, l, st
      FROM 'LDAP:// OU=Sales,DC=activeds,DC=Fabrikam,DC=Com'
      WHERE objectCategory='Person' AND 
      objectClass = 'contact'')
GO
SELECT * FROM viewADContacts
```



 

 




