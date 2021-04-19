---
description: Il existe plusieurs façons d’utiliser Windows Search pour interroger l’index. Cette rubrique décrit les approches de la syntaxe de requête avancée (AQS) et des méthodes basées sur les langage SQL (SQL).
ms.assetid: 544f03b3-cdf8-4550-a6da-e4a3bfc44744
title: Utilisation des approches SQL et AQS pour interroger l’index
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4641bea0e6109182b5896aa1f0f981695fd91b81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517456"
---
# <a name="using-sql-and-aqs-approaches-to-query-the-index"></a><span data-ttu-id="86cc2-104">Utilisation des approches SQL et AQS pour interroger l’index</span><span class="sxs-lookup"><span data-stu-id="86cc2-104">Using SQL and AQS Approaches to Query the Index</span></span>

<span data-ttu-id="86cc2-105">Il existe plusieurs façons d’utiliser Windows Search pour interroger l’index.</span><span class="sxs-lookup"><span data-stu-id="86cc2-105">There are several ways to use Windows Search to query the index.</span></span> <span data-ttu-id="86cc2-106">Cette rubrique décrit les approches de la syntaxe de requête avancée (AQS) et des méthodes basées sur les langage SQL (SQL).</span><span class="sxs-lookup"><span data-stu-id="86cc2-106">This topic outlines Advanced Query Syntax (AQS) and Structured Query Language (SQL) based approaches.</span></span>

<span data-ttu-id="86cc2-107">Cette rubrique est organisée comme suit :</span><span class="sxs-lookup"><span data-stu-id="86cc2-107">This topic is organized as follows:</span></span>

- [<span data-ttu-id="86cc2-108">Requêtes basées sur SQL</span><span class="sxs-lookup"><span data-stu-id="86cc2-108">SQL Based Queries</span></span>](#sql-based-queries)
  - [<span data-ttu-id="86cc2-109">Utilisation de OLE DB</span><span class="sxs-lookup"><span data-stu-id="86cc2-109">Using OLE DB</span></span>](#using-ole-db)
  - [<span data-ttu-id="86cc2-110">Utilisation d’ADO et de ADO.NET</span><span class="sxs-lookup"><span data-stu-id="86cc2-110">Using ADO and ADO.NET</span></span>](#using-ado-and-adonet)
  - [<span data-ttu-id="86cc2-111">Utilisation de SQL dans des requêtes locales et distantes</span><span class="sxs-lookup"><span data-stu-id="86cc2-111">Using SQL in Local and Remote Queries</span></span>](#using-sql-in-local-and-remote-queries)
- [<span data-ttu-id="86cc2-112">Requêtes basées sur AQS</span><span class="sxs-lookup"><span data-stu-id="86cc2-112">AQS Based Queries</span></span>](#aqs-based-queries)
  - [<span data-ttu-id="86cc2-113">Utilisation de ISearchQueryHelper</span><span class="sxs-lookup"><span data-stu-id="86cc2-113">Using ISearchQueryHelper</span></span>](#using-isearchqueryhelper)
  - [<span data-ttu-id="86cc2-114">Utilisation du protocole search-ms</span><span class="sxs-lookup"><span data-stu-id="86cc2-114">Using the search-ms Protocol</span></span>](#using-the-search-ms-protocol)
- [<span data-ttu-id="86cc2-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="86cc2-115">Related topics</span></span>](#related-topics)

## <a name="sql-based-queries"></a><span data-ttu-id="86cc2-116">Requêtes basées sur SQL</span><span class="sxs-lookup"><span data-stu-id="86cc2-116">SQL Based Queries</span></span>

<span data-ttu-id="86cc2-117">SQL est un langage de texte qui définit des requêtes.</span><span class="sxs-lookup"><span data-stu-id="86cc2-117">SQL is a text language that defines queries.</span></span> <span data-ttu-id="86cc2-118">SQL est commun entre de nombreuses technologies de base de données.</span><span class="sxs-lookup"><span data-stu-id="86cc2-118">SQL is common across many different database technologies.</span></span> <span data-ttu-id="86cc2-119">Windows Search utilise SQL, en implémente un sous-ensemble et l’étend en ajoutant des éléments au langage.</span><span class="sxs-lookup"><span data-stu-id="86cc2-119">Windows Search uses SQL, implements a subset of it, and extends it by adding elements to the language.</span></span> <span data-ttu-id="86cc2-120">Le SQL de recherche Windows utilisé par Windows Search étend les parties de la syntaxe de requête de base de données SQL-92 et SQL-99 standard pour améliorer son utilité avec les recherches textuelles.</span><span class="sxs-lookup"><span data-stu-id="86cc2-120">The Windows Search SQL used by Windows Search extends portions of the standard SQL-92 and SQL-99 database query syntax to enhance its usefulness with text-based searches.</span></span> <span data-ttu-id="86cc2-121">Toutes les fonctionnalités de Windows Search SQL sont compatibles avec Windows Search sur Windows XP et Windows Server 2003, et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="86cc2-121">All features of Windows Search SQL are compatible with Windows Search on Windows XP and Windows Server 2003, and later.</span></span>

<span data-ttu-id="86cc2-122">Pour plus d’informations sur l’utilisation de la syntaxe SQL de Windows Search, consultez [interrogation de l’index avec la syntaxe SQL de Windows Search](-search-sql-windowssearch-entry.md) et [vue d’ensemble de la syntaxe SQL de Windows Search](-search-sql-ovwofsearchquery.md).</span><span class="sxs-lookup"><span data-stu-id="86cc2-122">For more information about using Windows Search SQL syntax, see [Querying the Index with Windows Search SQL Syntax](-search-sql-windowssearch-entry.md) and [Overview of Windows Search SQL Syntax](-search-sql-ovwofsearchquery.md).</span></span>

<span data-ttu-id="86cc2-123">Les approches suivantes pour l’interrogation de l’index sont basées sur SQL.</span><span class="sxs-lookup"><span data-stu-id="86cc2-123">The following approaches for querying the index are SQL based.</span></span>

### <a name="using-ole-db"></a><span data-ttu-id="86cc2-124">Utilisation de OLE DB</span><span class="sxs-lookup"><span data-stu-id="86cc2-124">Using OLE DB</span></span>

<span data-ttu-id="86cc2-125">La base de données de liaison et d’incorporation d’objets (OLE DB) est une API COM (Component Object Model) qui vous permet d’accéder uniformément à différents types de magasins de données, y compris des bases de données non relationnelles telles que des feuilles de calcul.</span><span class="sxs-lookup"><span data-stu-id="86cc2-125">The Object Linking and Embedding Database (OLE DB) is a Component Object Model (COM) API that enables you to access different types of data stores uniformly, including non-relational databases like spreadsheets.</span></span> <span data-ttu-id="86cc2-126">OLE DB sépare le magasin de données de l’application qui y accède via un ensemble d’abstractions incluant la source de données Shell, la session, la commande et les ensembles de lignes.</span><span class="sxs-lookup"><span data-stu-id="86cc2-126">OLE DB separates the data store from the application accessing it through a set of abstractions that include the Shell data source, session, command, and rowsets.</span></span> <span data-ttu-id="86cc2-127">Un fournisseur de OLE DB est un composant logiciel qui implémente l’interface OLE DB pour fournir des données aux applications à partir d’un magasin de données particulier.</span><span class="sxs-lookup"><span data-stu-id="86cc2-127">An OLE DB provider is a software component that implements the OLE DB interface to provide data to applications from a particular data store.</span></span>

<span data-ttu-id="86cc2-128">Vous pouvez accéder au fournisseur de OLE DB de recherche Windows par programme à l’aide des objets OleDbConnection et OleDbSession en C et à l' \# aide de la prise en charge OLE DB intégrée à Active Template Library (ATL) en C++ (via atlclidb. h).</span><span class="sxs-lookup"><span data-stu-id="86cc2-128">You can access the Windows Search OLE DB provider programmatically by using the OleDbConnection and OleDbSession objects in C\# and by using the OLE DB support built into Active Template Library (ATL) in C++ (via atlclidb.h).</span></span> <span data-ttu-id="86cc2-129">La seule propriété qui doit être définie est la chaîne du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="86cc2-129">The only property that has to be set is the provider string.</span></span>

<span data-ttu-id="86cc2-130">Vous pouvez utiliser la chaîne suivante :</span><span class="sxs-lookup"><span data-stu-id="86cc2-130">You can use the following string:</span></span>

`provider=Search.CollatorDSO;EXTENDED PROPERTIES="Application=Windows"`

<span data-ttu-id="86cc2-131">Vous pouvez également récupérer la chaîne de connexion en appelant [**ISearchQueryHelper :: obtient \_ ConnectionString**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_connectionstring).</span><span class="sxs-lookup"><span data-stu-id="86cc2-131">Alternatively, you can get the connection string by calling [**ISearchQueryHelper::get\_ConnectionString**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_connectionstring).</span></span> <span data-ttu-id="86cc2-132">Pour obtenir un exemple, consultez Utilisation de [ISearchQueryHelper](#using-isearchqueryhelper) .</span><span class="sxs-lookup"><span data-stu-id="86cc2-132">See Using [ISearchQueryHelper](#using-isearchqueryhelper) for an example.</span></span>

> [!Note]  
> <span data-ttu-id="86cc2-133">Le fournisseur de OLE DB de recherche Windows est en lecture seule et prend en charge les instructions SELECT et GROUP ON.</span><span class="sxs-lookup"><span data-stu-id="86cc2-133">The Windows Search OLE DB provider is read-only, and support SELECT and GROUP ON statements.</span></span> <span data-ttu-id="86cc2-134">Les instructions INSERT et DELETE ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="86cc2-134">INSERT and DELETE statements are not supported.</span></span>

```cpp
#include <atldbcli.h>
CDataSource cDataSource;
hr = cDataSource.OpenFromInitializationString(L"provider=Search.CollatorDSO.1;EXTENDED PROPERTIES=\"Application=Windows\"");

if (SUCCEEDED(hr))
{
    CSession cSession;
    hr = cSession.Open(cDataSource);

    if (SUCCEEDED(hr))
    {
        CCommand<CDynamicAccessor, CRowset> cCommand;
        hr = cCommand.Open(cSession, pszSQL);

        if (SUCCEEDED(hr))
        {
            for (hr = cCommand.MoveFirst(); S_OK == hr; hr = cCommand.MoveNext())
            {
                for (DBORDINAL i = 1; i <= cCommand.GetColumnCount(); i++)
                {
                    PCWSTR pszName = cCommand.GetColumnName(i);
                    // do something with the column here
                }
            }
            cCommand.Close();
        }
    }
}
```

<span data-ttu-id="86cc2-135">Pour plus d’informations sur la OLE DB, consultez [OLE DB vue d’ensemble](https://msdn.microsoft.com/library/5d8sd9we(VS.71).aspx)de la programmation.</span><span class="sxs-lookup"><span data-stu-id="86cc2-135">For more information on OLE DB, see [OLE DB Programming Overview](https://msdn.microsoft.com/library/5d8sd9we(VS.71).aspx).</span></span> <span data-ttu-id="86cc2-136">Pour plus d’informations sur le Fournisseur de données .NET Framework pour OLE DB, consultez la documentation de l' [espace de noms System. Data. OleDb](/dotnet/api/system.data.oledb?view=dotnet-plat-ext-3.1) .</span><span class="sxs-lookup"><span data-stu-id="86cc2-136">For information on the .NET Framework Data Provider for OLE DB, see the [System.Data.OleDb Namespace](/dotnet/api/system.data.oledb?view=dotnet-plat-ext-3.1) documentation.</span></span>

### <a name="using-ado-and-adonet"></a><span data-ttu-id="86cc2-137">Utilisation d’ADO et de ADO.NET</span><span class="sxs-lookup"><span data-stu-id="86cc2-137">Using ADO and ADO.NET</span></span>

<span data-ttu-id="86cc2-138">Microsoft ActiveX Data Objects (ADO) et ADO.NET vous permettent d’écrire des applications clientes pour accéder et manipuler les données d’un serveur de base de données par le biais d’un fournisseur.</span><span class="sxs-lookup"><span data-stu-id="86cc2-138">Microsoft ActiveX Data Objects (ADO) and ADO.NET enable you to write client applications to access and manipulate data in a database server through a provider.</span></span> <span data-ttu-id="86cc2-139">La recherche Windows est une technologie en lecture seule : vous pouvez récupérer des données à l’aide de la recherche sur le bureau, mais vous ne pouvez pas modifier les données à l’aide de la recherche Windows.</span><span class="sxs-lookup"><span data-stu-id="86cc2-139">Windows Search is a read-only technology: you can retrieve data using Desktop Search but you can't change data using Windows Search.</span></span> <span data-ttu-id="86cc2-140">Toutefois, vous pouvez passer les résultats d’une recherche à une technologie susceptible de modifier les données.</span><span class="sxs-lookup"><span data-stu-id="86cc2-140">You can, however, pass the results of a search over to a technology that can change data.</span></span>

<span data-ttu-id="86cc2-141">Les exemples de code suivants illustrent l’ouverture d’une connexion à la source de données, la création et l’ouverture d’un jeu d’enregistrements avec une instruction [Windows Search SQL](-search-sql-ovwofsearchquery.md) SELECT et l’obtention des URL des cinq fichiers les plus volumineux de l’index.</span><span class="sxs-lookup"><span data-stu-id="86cc2-141">The following code examples demonstrate how to open a connection to the data source, create and open a RecordSet with a [Windows Search SQL](-search-sql-ovwofsearchquery.md) SELECT statement, and get the URLs of the five largest files from the index.</span></span>

> [!Note]  
> <span data-ttu-id="86cc2-142">Pour plus d’informations sur la façon d’obtenir la chaîne de connexion, consultez [interrogation de l’index avec ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md)et [ISearchQueryHelper :: obtenir la \_ chaîne de connexion](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_connectionstring).</span><span class="sxs-lookup"><span data-stu-id="86cc2-142">For information on how to obtain the connection string, see [Querying the Index with ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md), and [ISearchQueryHelper::get\_Connection String](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_connectionstring).</span></span>

#### <a name="ado-and-vbscript"></a><span data-ttu-id="86cc2-143">ADO et VBScript</span><span class="sxs-lookup"><span data-stu-id="86cc2-143">ADO and VBScript</span></span>

```VB
'To run this snippet, save it to a file and run it using cscript.exe from a command line.
'Running the .vbs file with Windows Script Host may cause dialog boxes to open for each item returned from the index.

On Error Resume Next

Set objConnection = CreateObject("ADODB.Connection")
Set objRecordSet = CreateObject("ADODB.Recordset")

objConnection.Open "Provider=Search.CollatorDSO;Extended Properties='Application=Windows';"

objRecordSet.Open "SELECT Top 5 System.ItemPathDisplay FROM SYSTEMINDEX WHERE scope='file:' ORDER BY System.Size DESC", objConnection

objRecordSet.MoveFirst
Do Until objRecordset.EOF
    Wscript.Echo objRecordset.Fields.Item("System.ItemPathDisplay")
    objRecordset.MoveNext
Loop
```

#### <a name="ado-and-c"></a><span data-ttu-id="86cc2-144">ADO et C++</span><span class="sxs-lookup"><span data-stu-id="86cc2-144">ADO and C++</span></span>

```cpp
#import "msado15.dll" rename_namespace("ADO") rename("EOF", "EndOfFile") implementation_only

ADO::_ConnectionPtr connection = NULL;
HRESULT hr = connection.CreateInstance(__uuidof(ADO::Connection));
if (SUCCEEDED(hr))
{
    ADO::_RecordsetPtr recordset = NULL;
    hr = recordset.CreateInstance(__uuidof(ADO::Recordset));
    if (SUCCEEDED(hr))
    {
        connection->CursorLocation = ADO::adUseClient;
        hr = connection->Open(L"Provider=Search.CollatorDSO;Extended Properties='Application=Windows';",
            L"", L"", ADO::adConnectUnspecified);
        if (SUCCEEDED(hr))
        {
            hr = recordset->Open("SELECT Top 5 System.ItemPathDisplay FROM SYSTEMINDEX WHERE scope='file:' ORDER BY System.Size DESC",
            connection.GetInterfacePtr(), ADO::adOpenForwardOnly, ADO::adLockReadOnly, ADO::adCmdText);
            if (SUCCEEDED(hr))
            {
                while (!recordset->EndOfFile)
                {
                    _variant_t var;
                    var = recordset->Fields->GetItem(L"System.ItemPathDisplay")->GetValue();
                    std::cout << static_cast<char *>(_bstr_t(var.bstrVal)) << std::endl;
                    recordset->MoveNext();
                };
                recordset->Close();
            }
            connection->Close();
        }
    }
}

```

#### <a name="ado-and-visualbasic"></a><span data-ttu-id="86cc2-145">ADO et VisualBasic</span><span class="sxs-lookup"><span data-stu-id="86cc2-145">ADO and VisualBasic</span></span>

<span data-ttu-id="86cc2-146">Ajoutez d’abord une référence à ADODB dans votre projet</span><span class="sxs-lookup"><span data-stu-id="86cc2-146">First add a reference to ADODB in your project</span></span>

```VB
Dim con As ADODB.Connection
Dim rst As ADODB.Recordset

con = New ADODB.Connection
rst = New ADODB.Recordset

Dim sConString As String
Dim sSQLString As String

sConString = "Provider=Search.CollatorDSO;Extended Properties='Application=Windows';"
con.Open(sConString)

sSQLString = "SELECT Top 5 System.ItemPathDisplay FROM SYSTEMINDEX
                WHERE scope='file:'
                ORDER BY System.Size DESC"

rst = con.Execute(sSQLString)

Do Until (rst.EOF)
    Print(1, rst("System.ItemPathDisplay").Value)
    rst.MoveNext
Loop

rst.Close
rst = Nothing

con.Close
con = Nothing
```

#### <a name="adonet-and-c"></a><span data-ttu-id="86cc2-147">ADO.NET et C\#</span><span class="sxs-lookup"><span data-stu-id="86cc2-147">ADO.NET and C\#</span></span>

```csharp
string query = @"SELECT Top 5 System.ItemPathDisplay FROM SYSTEMINDEX
                WHERE scope='file:'
                ORDER BY System.Size DESC";

using (OleDbConnection objConnection =
    new OleDbConnection
    ("Provider=Search.CollatorDSO.1;Extended?Properties='Application=Windows';"))
{
    objConnection.Open();
    OleDbCommand cmd = new OleDbCommand(query, objConnection);
    using (OleDbDataReader rdr = cmd.ExecuteReader())
    {
        for (int i = 0; i < rdr.FieldCount; i++)
        {
            Console.Write(rdr.GetName(i));
            Console.Write('\t');
        }
        while (rdr.Read())
        {
            Console.WriteLine();
            for (int i = 0; i < rdr.FieldCount; i++)
            {
                Console.Write(rdr[i]);
                Console.Write('\t');
            }
        }
        Console.ReadKey();
    }
}
```

### <a name="using-sql-in-local-and-remote-queries"></a><span data-ttu-id="86cc2-148">Utilisation de SQL dans des requêtes locales et distantes</span><span class="sxs-lookup"><span data-stu-id="86cc2-148">Using SQL in Local and Remote Queries</span></span>

<span data-ttu-id="86cc2-149">Vous pouvez exécuter vos requêtes localement ou à distance.</span><span class="sxs-lookup"><span data-stu-id="86cc2-149">You can execute your queries either locally or remotely.</span></span> <span data-ttu-id="86cc2-150">Une requête locale utilisant la [clause from](-search-sql-from.md) est présentée dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="86cc2-150">A local query using the [FROM clause](-search-sql-from.md) is shown in the following example.</span></span> <span data-ttu-id="86cc2-151">Une requête locale interroge le catalogue SystemIndex local uniquement.</span><span class="sxs-lookup"><span data-stu-id="86cc2-151">A local query queries the local SystemIndex catalog only.</span></span>

```sql
FROM SystemIndex
```

<span data-ttu-id="86cc2-152">Une requête distante à l’aide de la [clause from](-search-sql-from.md) est présentée dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="86cc2-152">A remote query using the [FROM clause](-search-sql-from.md) is shown in the following example.</span></span> <span data-ttu-id="86cc2-153">L’ajout de NomOrdinateur transforme l’exemple précédent en une requête distante.</span><span class="sxs-lookup"><span data-stu-id="86cc2-153">Adding ComputerName transforms the previous example into a remote query.</span></span>

```sql
FROM [<ComputerName>.]SystemIndex
```

<span data-ttu-id="86cc2-154">Par défaut, Windows XP et Windows Server 2003 n’ont pas installé Windows Search.</span><span class="sxs-lookup"><span data-stu-id="86cc2-154">By default, Windows XP and Windows Server 2003 do not have Windows Search installed.</span></span> <span data-ttu-id="86cc2-155">Seul Windows Search 4 (WS4) fournit une prise en charge des requêtes distantes.</span><span class="sxs-lookup"><span data-stu-id="86cc2-155">Only Windows Search 4 (WS4) provides remote query support.</span></span> <span data-ttu-id="86cc2-156">Les versions précédentes de Windows Desktop Search (WDS), telles que 3,01 et antérieures, ne prennent pas en charge l’interrogation à distance.</span><span class="sxs-lookup"><span data-stu-id="86cc2-156">Previous versions of Windows Desktop Search (WDS), such as 3.01 and earlier, do not support remote querying.</span></span> <span data-ttu-id="86cc2-157">Avec l’Explorateur Windows, vous pouvez interroger l’index local d’un ordinateur distant pour les éléments du système de fichiers (éléments gérés par le protocole « fichier : »).</span><span class="sxs-lookup"><span data-stu-id="86cc2-157">With Windows Explorer you can query the local index of a remote computer for file system items (items handled by the "file:" protocol).</span></span>

<span data-ttu-id="86cc2-158">Pour récupérer un élément à l’aide d’une requête distante, l’élément doit remplir les conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="86cc2-158">To retrieve an item by remote query, the item must meet the following requirements:</span></span>

- <span data-ttu-id="86cc2-159">Être accessible via le chemin d’accès UNC (Universal Naming Convention).</span><span class="sxs-lookup"><span data-stu-id="86cc2-159">Be accessible via Universal Naming Convention (UNC) path.</span></span>
- <span data-ttu-id="86cc2-160">Existent sur l’ordinateur distant auquel le client a accès.</span><span class="sxs-lookup"><span data-stu-id="86cc2-160">Exist on the remote computer to which the client has access.</span></span>
- <span data-ttu-id="86cc2-161">A sa sécurité définie pour autoriser le client à avoir un accès en lecture.</span><span class="sxs-lookup"><span data-stu-id="86cc2-161">Have its security set to allow the client to have Read access.</span></span>

<span data-ttu-id="86cc2-162">L’Explorateur Windows possède des fonctionnalités permettant de partager des éléments, y compris un partage « public » ( \\ \\ ordinateur \\ public \\ ...) dans le **Centre réseau et partage**, et un partage « utilisateurs » ( \\ \\ \\ utilisateurs \\ de l’ordinateur...) pour les éléments partagés via l’Assistant partage.</span><span class="sxs-lookup"><span data-stu-id="86cc2-162">Windows Explorer has features for sharing items including a "Public" share (\\\\Machine\\Public\\...) in the **Network and Sharing Center**, and a "Users" share (\\\\Machine\\Users\\...) for items shared through the Sharing Wizard.</span></span> <span data-ttu-id="86cc2-163">Une fois que vous avez partagé le ou les dossiers, vous pouvez interroger l’index local en spécifiant le nom d’ordinateur de l’ordinateur distant dans la clause FROM et un chemin d’accès UNC sur l’ordinateur distant dans la clause SCOPE, comme indiqué dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="86cc2-163">After you share the folder(s), you can query the local index by specifying the remote computer's machine name in the FROM clause, and a UNC path on the remote machine in the SCOPE clause, as shown in the following example:</span></span>

```sql
SELECT System.ItemName FROM MachineName.SystemIndex WHERE SCOPE='file://MachineName/<path>'
```

## <a name="aqs-based-queries"></a><span data-ttu-id="86cc2-164">Requêtes basées sur AQS</span><span class="sxs-lookup"><span data-stu-id="86cc2-164">AQS Based Queries</span></span>

<span data-ttu-id="86cc2-165">AQS est la syntaxe de requête par défaut utilisée par Windows Search pour interroger l’index et affiner et limiter les paramètres de recherche.</span><span class="sxs-lookup"><span data-stu-id="86cc2-165">AQS is the default query syntax used by Windows Search to query the index and to refine and narrow search parameters.</span></span> <span data-ttu-id="86cc2-166">Bien que AQS soit principalement utilisé par l’utilisateur, il peut être utilisé par les développeurs pour créer des requêtes par programmation.</span><span class="sxs-lookup"><span data-stu-id="86cc2-166">While AQS is primarily user facing, it can be used by developers to build queries programmatically.</span></span> <span data-ttu-id="86cc2-167">Dans Windows 7, la AQS canonique a été introduite et doit être utilisée dans Windows 7 et versions ultérieures pour générer des requêtes AQS par programmation.</span><span class="sxs-lookup"><span data-stu-id="86cc2-167">In Windows 7 canonical AQS was introduced, and must be used in Windows 7 and later, to programmatically generate AQS queries.</span></span> <span data-ttu-id="86cc2-168">Pour plus d’informations sur AQS, consultez Utilisation de la [syntaxe de requête avancée par programmation](-search-3x-advancedquerysyntax.md).</span><span class="sxs-lookup"><span data-stu-id="86cc2-168">For detailed information on AQS, see [Using Advanced Query Syntax Programmatically](-search-3x-advancedquerysyntax.md).</span></span>

<span data-ttu-id="86cc2-169">Les approches suivantes pour l’interrogation de l’index sont basées sur AQS.</span><span class="sxs-lookup"><span data-stu-id="86cc2-169">The following approaches for querying the index are AQS based.</span></span>

### <a name="using-isearchqueryhelper"></a><span data-ttu-id="86cc2-170">Utilisation de ISearchQueryHelper</span><span class="sxs-lookup"><span data-stu-id="86cc2-170">Using ISearchQueryHelper</span></span>

<span data-ttu-id="86cc2-171">Vous pouvez développer une classe de composant ou d’assistance pour interroger l’index à l’aide de l’interface [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) , ce qui vous permet de tirer parti de certaines fonctionnalités du système et de simplifier l’utilisation de la recherche Windows.</span><span class="sxs-lookup"><span data-stu-id="86cc2-171">You can develop a component or helper class to query the index by using the [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) interface, which enables you to take advantage of some features of the system and simplify your use of Windows Search.</span></span> <span data-ttu-id="86cc2-172">Cette interface vous aide à :</span><span class="sxs-lookup"><span data-stu-id="86cc2-172">This interface helps you:</span></span>

- <span data-ttu-id="86cc2-173">Obtenez une chaîne de connexion OLE DB pour vous connecter à la base de données de recherche Windows.</span><span class="sxs-lookup"><span data-stu-id="86cc2-173">Obtain an OLE DB connection string to connect to the Windows Search database.</span></span>
- <span data-ttu-id="86cc2-174">Convertir les requêtes utilisateur de AQS en SQL de recherche Windows.</span><span class="sxs-lookup"><span data-stu-id="86cc2-174">Convert user queries from AQS to Windows Search SQL.</span></span>

<span data-ttu-id="86cc2-175">Cette interface est implémentée en tant que classe d’assistance à [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) et est obtenue en appelant [**ISearchCatalogManager :: GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper), comme indiqué dans l’exemple C++ suivant.</span><span class="sxs-lookup"><span data-stu-id="86cc2-175">This interface is implemented as a helper class to [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) and is obtained by calling [**ISearchCatalogManager::GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper), as shown in the following C++ example.</span></span>

```cpp
HRESULT GetQueryHelper(ISearchQueryHelper **ppQueryHelper)
{
    *ppQueryHelper = NULL;

    // Create an instance of the search manager

    ISearchManager *pSearchManager;
    HRESULT hr = CoCreateInstance(__uuidof(CSearchManager), NULL, CLSCTX_LOCAL_SERVER, IID_PPV_ARGS(&pSearchManager));
    if (SUCCEEDED(hr))
    {
        // Get the catalog manager from the search manager
        ISearchCatalogManager *pSearchCatalogManager;
        hr = pSearchManager->GetCatalog(L"SystemIndex", &pSearchCatalogManager);
        if (SUCCEEDED(hr))
        {
            // Get the query helper from the catalog manager
            hr = pSearchCatalogManager->GetQueryHelper(ppQueryHelper);
            pSearchCatalogManager->Release();
        }
        pSearchManager->Release();
    }

    return hr;
}
```

<span data-ttu-id="86cc2-176">Pour implémenter l’interface [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) , consultez [utilisation de l’interface ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md) et la rubrique de référence [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) .</span><span class="sxs-lookup"><span data-stu-id="86cc2-176">To implement the [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) interface, see [Using the ISearchQueryHelper Interface](-search-3x-wds-qryidx-searchqueryhelper.md) and the [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) reference topic.</span></span>

> [!Note]  
> <span data-ttu-id="86cc2-177">Compatibilité héritée de Microsoft Windows Desktop Search (WDS) 2x : sur les ordinateurs exécutant Windows XP et Windows Server 2003 et versions ultérieures, [**ISearchDesktop**](/previous-versions//aa965729(v=vs.85)) est déconseillé.</span><span class="sxs-lookup"><span data-stu-id="86cc2-177">Legacy Microsoft Windows Desktop Search (WDS) 2x compatibility: On computers running Windows XP and Windows Server 2003 and later, [**ISearchDesktop**](/previous-versions//aa965729(v=vs.85)) is deprecated.</span></span> <span data-ttu-id="86cc2-178">Au lieu de cela, les développeurs doivent utiliser [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) pour obtenir une chaîne de connexion, analyser la requête de l’utilisateur dans SQL, puis interroger OLE DB.</span><span class="sxs-lookup"><span data-stu-id="86cc2-178">Instead, developers should use [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) to get a connection string, parse the user's query into SQL, and then query through OLE DB.</span></span>

### <a name="using-the-search-ms-protocol"></a><span data-ttu-id="86cc2-179">Utilisation du protocole search-ms</span><span class="sxs-lookup"><span data-stu-id="86cc2-179">Using the search-ms Protocol</span></span>

<span data-ttu-id="86cc2-180">La **recherche-** [protocole d’application](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85)) MS est une convention pour le démarrage d’une application, comme l’Explorateur Windows, pour interroger l’index de recherche Windows.</span><span class="sxs-lookup"><span data-stu-id="86cc2-180">The **search-ms** [application protocol](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85)) is a convention for starting an application, like Windows Explorer, to query the Windows Search index.</span></span> <span data-ttu-id="86cc2-181">Il permet de générer des requêtes avec des arguments de valeur de paramètre, notamment des arguments de propriété, des recherches précédemment enregistrées, une syntaxe de requête avancée (AQS), une syntaxe de requête naturelle (NQS) et des identificateurs de code de langue (LCID) pour l’indexeur et la requête elle-même.</span><span class="sxs-lookup"><span data-stu-id="86cc2-181">It enables queries to be built with parameter-value arguments, including property arguments, previously saved searches, Advanced Query Syntax (AQS), Natural Query Syntax (NQS), and language code identifiers (LCIDs) for both the indexer and the query itself.</span></span>

<span data-ttu-id="86cc2-182">Pour plus d’informations sur la syntaxe de protocole search-ms, consultez [interrogation de l’index avec le protocole search-ms](-search-3x-wds-qryidx-searchms.md).</span><span class="sxs-lookup"><span data-stu-id="86cc2-182">For detailed information on the search-ms protocol syntax, see [Querying the Index with the search-ms Protocol](-search-3x-wds-qryidx-searchms.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="86cc2-183">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="86cc2-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86cc2-184">Interrogation de l’index programmatiquement</span><span class="sxs-lookup"><span data-stu-id="86cc2-184">Querying the Index Programmatically</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="86cc2-185">Interrogation de l’index avec ISearchQueryHelper</span><span class="sxs-lookup"><span data-stu-id="86cc2-185">Querying the Index with ISearchQueryHelper</span></span>](-search-3x-wds-qryidx-searchqueryhelper.md)
</dt> <dt>

[<span data-ttu-id="86cc2-186">Interrogation de l’index avec le protocole search-ms</span><span class="sxs-lookup"><span data-stu-id="86cc2-186">Querying the Index with the search-ms Protocol</span></span>](-search-3x-wds-qryidx-searchms.md)
</dt> <dt>

[<span data-ttu-id="86cc2-187">Interrogation de l’index avec la syntaxe SQL de Windows Search</span><span class="sxs-lookup"><span data-stu-id="86cc2-187">Querying the Index with Windows Search SQL Syntax</span></span>](-search-sql-windowssearch-entry.md)
</dt> <dt>

[<span data-ttu-id="86cc2-188">Utilisation de la syntaxe de requête avancée par programmation</span><span class="sxs-lookup"><span data-stu-id="86cc2-188">Using Advanced Query Syntax Programmatically</span></span>](-search-3x-advancedquerysyntax.md)
</dt> </dl>
