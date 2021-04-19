---
title: Jointure de données hétérogènes
description: Les organisations classiques stockent les données dans plusieurs bases de données hétérogènes. Les données des ressources humaines peuvent être stockées dans SQL Server, tandis que les données de gestion des comptes sont stockées dans l’annuaire. D’autres données peuvent être stockées dans des formats propriétaires.
ms.assetid: 45281b42-5cb2-42f9-9c7c-f3e3174b0f9d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e1099028bc85dc6492eade0315b7308b4c6aaa9
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314612"
---
# <a name="joining-heterogeneous-data"></a><span data-ttu-id="2348c-105">Jointure de données hétérogènes</span><span class="sxs-lookup"><span data-stu-id="2348c-105">Joining Heterogeneous Data</span></span>

<span data-ttu-id="2348c-106">Les organisations classiques stockent les données dans plusieurs bases de données hétérogènes.</span><span class="sxs-lookup"><span data-stu-id="2348c-106">Typical organizations store data in multiple heterogeneous databases.</span></span> <span data-ttu-id="2348c-107">Les données des ressources humaines peuvent être stockées dans SQL Server, tandis que les données de gestion des comptes sont stockées dans l’annuaire.</span><span class="sxs-lookup"><span data-stu-id="2348c-107">Human Resources data may be stored in SQL Server, while account management data is stored in the directory.</span></span> <span data-ttu-id="2348c-108">D’autres données peuvent être stockées dans des formats propriétaires.</span><span class="sxs-lookup"><span data-stu-id="2348c-108">Other data may be stored in proprietary formats.</span></span>

<span data-ttu-id="2348c-109">Avec, SQL Server 7,0, ADSI et le fournisseur OLE DB, il est possible de joindre des données de Active Directory à des données dans SQL Server et de créer une vue des données jointes.</span><span class="sxs-lookup"><span data-stu-id="2348c-109">With, SQL Server 7.0, ADSI, and the OLE DB Provider, it is possible to join data from Active Directory to data in SQL Server and create a view of the joined data.</span></span>

<span data-ttu-id="2348c-110">**Pour joindre des données Active Directory à des données SQL Server**</span><span class="sxs-lookup"><span data-stu-id="2348c-110">**To join Active Directory Data with SQL Server Data**</span></span>

1.  <span data-ttu-id="2348c-111">Exécuter l' **Analyseur de requêtes SQL** ( \| programmes de démarrage \| Microsoft SQL Server 7,0)</span><span class="sxs-lookup"><span data-stu-id="2348c-111">Run the **SQL Query Analyzer** (Start \| Programs \| Microsoft SQL Server 7.0)</span></span>
2.  <span data-ttu-id="2348c-112">Connectez-vous à l’ordinateur SQL Server.</span><span class="sxs-lookup"><span data-stu-id="2348c-112">Log on to the SQL Server computer.</span></span>
3.  <span data-ttu-id="2348c-113">Exécutez la ligne suivante (en la mettant en surbrillance et en appuyant sur CTRL + E) :</span><span class="sxs-lookup"><span data-stu-id="2348c-113">Execute the following line (by highlighting it and pressing CTRL+E):</span></span>

    ```sql
    EXEC sp_addlinkedserver 'ADSI', 'Active Directory Service Interfaces', 
    'ADSDSOObject', 'adsdatasource'
    GO
    ```

    

    <span data-ttu-id="2348c-114">Dans cette ligne, les arguments de la procédure stockée système [SP \_ addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="2348c-114">In this line, the arguments for the [sp\_addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) System Stored Procedure are as follows:</span></span>

    -   <span data-ttu-id="2348c-115">« ADSI » est l’argument de **serveur** , qui est le nom de ce serveur lié.</span><span class="sxs-lookup"><span data-stu-id="2348c-115">" ADSI" is the **server** argument, which will be the name of this linked server.</span></span>
    -   <span data-ttu-id="2348c-116">« Active Directory Services » est l’argument **srvproduct** , qui est le nom de la source de données OLE DB que vous ajoutez en tant que serveur lié.</span><span class="sxs-lookup"><span data-stu-id="2348c-116">"Active Directory Services" is the **srvproduct** argument, which is the name of the OLE DB data source that you are adding as a linked server.</span></span>
    -   <span data-ttu-id="2348c-117">« ADSDSOObject » est l’argument du **\_ nom du fournisseur** et indique que vous utilisez le fournisseur de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="2348c-117">"ADSDSOObject" is the **provider\_name** argument and indicates you are using the OLE DB Provider.</span></span>
    -   <span data-ttu-id="2348c-118">« adsdatasource » est l' **\_ argument de source de données**, qui est le nom de la source de données tel qu’il est interprété par le fournisseur OLE DB.</span><span class="sxs-lookup"><span data-stu-id="2348c-118">"adsdatasource" is the **data\_source argument**, which is the name of the data source as interpreted by the OLE DB Provider.</span></span>

    <span data-ttu-id="2348c-119">Vous pouvez maintenant utiliser le serveur lié pour accéder à Active Directory à partir de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="2348c-119">You can now use the linked server to access Active Directory from SQL Server.</span></span>

4.  <span data-ttu-id="2348c-120">L’exemple suivant exécute une requête à l’aide de l’instruction [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) .</span><span class="sxs-lookup"><span data-stu-id="2348c-120">The next example performs a query using the [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) statement.</span></span> <span data-ttu-id="2348c-121">Cette instruction a deux arguments : ADSI, qui est le nom du serveur lié que vous venez de créer et une instruction de requête.</span><span class="sxs-lookup"><span data-stu-id="2348c-121">This statement has two arguments: ADSI, which is the name of the linked server that you just created, and a query statement.</span></span> <span data-ttu-id="2348c-122">L’instruction de requête contient les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="2348c-122">The query statement contains the following items:</span></span>

    -   <span data-ttu-id="2348c-123">L’instruction [Select](https://msdn.microsoft.com/library/Aa259187.aspx) contient la liste des données qui seront obtenues à partir du service d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="2348c-123">The [SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) statement contains the list of data that will be obtained from the directory service.</span></span> <span data-ttu-id="2348c-124">Vous devrez utiliser le nom d’affichage LDAP pour indiquer les données que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="2348c-124">You will need to use the LDAP display name to indicate which data you are searching for.</span></span>
    -   <span data-ttu-id="2348c-125">L’instruction [from](https://msdn.microsoft.com/library/Aa258869.aspx) contient le nom du serveur d’annuaire lié à partir duquel ces informations seront obtenues.</span><span class="sxs-lookup"><span data-stu-id="2348c-125">The [FROM](https://msdn.microsoft.com/library/Aa258869.aspx) statement contains the name of the linked directory server where this information will be obtained from.</span></span>
    -   <span data-ttu-id="2348c-126">L’instruction [Where](https://msdn.microsoft.com/library/Aa260674.aspx) fournit les conditions de recherche.</span><span class="sxs-lookup"><span data-stu-id="2348c-126">The [WHERE](https://msdn.microsoft.com/library/Aa260674.aspx) statement provides the search conditions.</span></span> <span data-ttu-id="2348c-127">Dans cet exemple, il recherche des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="2348c-127">In this example, it is searching for users.</span></span>

    <span data-ttu-id="2348c-128">Tapez et exécutez :</span><span class="sxs-lookup"><span data-stu-id="2348c-128">Type and execute:</span></span>

    ```sql
    SELECT * FROM OPENQUERY( ADSI, 
        'SELECT name, adsPath 
         FROM 'LDAP://DC=Fabrikam,DC=com' 
         WHERE objectCategory = 'Person' AND objectClass= 'user'')
    ```

    

    <span data-ttu-id="2348c-129">Vous pouvez également utiliser le [dialecte ADSI LDAP](ldap-dialect.md).</span><span class="sxs-lookup"><span data-stu-id="2348c-129">You can also use the ADSI [LDAP dialect](ldap-dialect.md).</span></span> <span data-ttu-id="2348c-130">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="2348c-130">For example:</span></span>

    ```sql
    SELECT * FROM OPENQUERY(ADSI,
        '<LDAP://DC=Fabrikam,DC=COM>;(&(objectCategory=Person)(objectClass=user));name, adspath;subtree')
    ```

    

    <span data-ttu-id="2348c-131">Dans l’exemple précédent, la requête LDAP se compose de quatre parties :</span><span class="sxs-lookup"><span data-stu-id="2348c-131">In the previous example, the LDAP query has four parts:</span></span>

    -   <span data-ttu-id="2348c-132">" \<LDAP://DC=Fabrikam,DC=COM> " est le nom unique du serveur d’annuaire à rechercher.</span><span class="sxs-lookup"><span data-stu-id="2348c-132">"\<LDAP://DC=Fabrikam,DC=COM>" is the distinguished name of the directory server to search.</span></span>
    -   <span data-ttu-id="2348c-133">« (& (objectCategory = person) (objectClass = user)) » est le filtre de recherche LDAP (voir la [syntaxe du filtre de recherche](search-filter-syntax.md)).</span><span class="sxs-lookup"><span data-stu-id="2348c-133">"(&(objectCategory=Person)(objectClass=user))" is the LDAP search filter (see [Search Filter Syntax](search-filter-syntax.md)).</span></span>
    -   <span data-ttu-id="2348c-134">« Name, ADsPath » sont les noms (à l’aide du format de nom complet LDAP) des attributs à récupérer.</span><span class="sxs-lookup"><span data-stu-id="2348c-134">"name, adspath" are the names (using the LDAP display name format) of the attributes to retrieve.</span></span>
    -   <span data-ttu-id="2348c-135">« sous-arborescence » indique l' [étendue](scope-of-query.md) de la recherche.</span><span class="sxs-lookup"><span data-stu-id="2348c-135">"subtree" indicates the [scope](scope-of-query.md) of the search.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2348c-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2348c-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2348c-137">Création et exécution d’une vue</span><span class="sxs-lookup"><span data-stu-id="2348c-137">Creating and Executing a View</span></span>](creating-and-executing-a-view.md)
</dt> </dl>

 

 




