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
# <a name="using-sql-and-aqs-approaches-to-query-the-index"></a>Utilisation des approches SQL et AQS pour interroger l’index

Il existe plusieurs façons d’utiliser Windows Search pour interroger l’index. Cette rubrique décrit les approches de la syntaxe de requête avancée (AQS) et des méthodes basées sur les langage SQL (SQL).

Cette rubrique est organisée comme suit :

- [Requêtes basées sur SQL](#sql-based-queries)
  - [Utilisation de OLE DB](#using-ole-db)
  - [Utilisation d’ADO et de ADO.NET](#using-ado-and-adonet)
  - [Utilisation de SQL dans des requêtes locales et distantes](#using-sql-in-local-and-remote-queries)
- [Requêtes basées sur AQS](#aqs-based-queries)
  - [Utilisation de ISearchQueryHelper](#using-isearchqueryhelper)
  - [Utilisation du protocole search-ms](#using-the-search-ms-protocol)
- [Rubriques connexes](#related-topics)

## <a name="sql-based-queries"></a>Requêtes basées sur SQL

SQL est un langage de texte qui définit des requêtes. SQL est commun entre de nombreuses technologies de base de données. Windows Search utilise SQL, en implémente un sous-ensemble et l’étend en ajoutant des éléments au langage. Le SQL de recherche Windows utilisé par Windows Search étend les parties de la syntaxe de requête de base de données SQL-92 et SQL-99 standard pour améliorer son utilité avec les recherches textuelles. Toutes les fonctionnalités de Windows Search SQL sont compatibles avec Windows Search sur Windows XP et Windows Server 2003, et versions ultérieures.

Pour plus d’informations sur l’utilisation de la syntaxe SQL de Windows Search, consultez [interrogation de l’index avec la syntaxe SQL de Windows Search](-search-sql-windowssearch-entry.md) et [vue d’ensemble de la syntaxe SQL de Windows Search](-search-sql-ovwofsearchquery.md).

Les approches suivantes pour l’interrogation de l’index sont basées sur SQL.

### <a name="using-ole-db"></a>Utilisation de OLE DB

La base de données de liaison et d’incorporation d’objets (OLE DB) est une API COM (Component Object Model) qui vous permet d’accéder uniformément à différents types de magasins de données, y compris des bases de données non relationnelles telles que des feuilles de calcul. OLE DB sépare le magasin de données de l’application qui y accède via un ensemble d’abstractions incluant la source de données Shell, la session, la commande et les ensembles de lignes. Un fournisseur de OLE DB est un composant logiciel qui implémente l’interface OLE DB pour fournir des données aux applications à partir d’un magasin de données particulier.

Vous pouvez accéder au fournisseur de OLE DB de recherche Windows par programme à l’aide des objets OleDbConnection et OleDbSession en C et à l' \# aide de la prise en charge OLE DB intégrée à Active Template Library (ATL) en C++ (via atlclidb. h). La seule propriété qui doit être définie est la chaîne du fournisseur.

Vous pouvez utiliser la chaîne suivante :

`provider=Search.CollatorDSO;EXTENDED PROPERTIES="Application=Windows"`

Vous pouvez également récupérer la chaîne de connexion en appelant [**ISearchQueryHelper :: obtient \_ ConnectionString**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_connectionstring). Pour obtenir un exemple, consultez Utilisation de [ISearchQueryHelper](#using-isearchqueryhelper) .

> [!Note]  
> Le fournisseur de OLE DB de recherche Windows est en lecture seule et prend en charge les instructions SELECT et GROUP ON. Les instructions INSERT et DELETE ne sont pas prises en charge.

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

Pour plus d’informations sur la OLE DB, consultez [OLE DB vue d’ensemble](https://msdn.microsoft.com/library/5d8sd9we(VS.71).aspx)de la programmation. Pour plus d’informations sur le Fournisseur de données .NET Framework pour OLE DB, consultez la documentation de l' [espace de noms System. Data. OleDb](/dotnet/api/system.data.oledb?view=dotnet-plat-ext-3.1) .

### <a name="using-ado-and-adonet"></a>Utilisation d’ADO et de ADO.NET

Microsoft ActiveX Data Objects (ADO) et ADO.NET vous permettent d’écrire des applications clientes pour accéder et manipuler les données d’un serveur de base de données par le biais d’un fournisseur. La recherche Windows est une technologie en lecture seule : vous pouvez récupérer des données à l’aide de la recherche sur le bureau, mais vous ne pouvez pas modifier les données à l’aide de la recherche Windows. Toutefois, vous pouvez passer les résultats d’une recherche à une technologie susceptible de modifier les données.

Les exemples de code suivants illustrent l’ouverture d’une connexion à la source de données, la création et l’ouverture d’un jeu d’enregistrements avec une instruction [Windows Search SQL](-search-sql-ovwofsearchquery.md) SELECT et l’obtention des URL des cinq fichiers les plus volumineux de l’index.

> [!Note]  
> Pour plus d’informations sur la façon d’obtenir la chaîne de connexion, consultez [interrogation de l’index avec ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md)et [ISearchQueryHelper :: obtenir la \_ chaîne de connexion](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_connectionstring).

#### <a name="ado-and-vbscript"></a>ADO et VBScript

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

#### <a name="ado-and-c"></a>ADO et C++

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

#### <a name="ado-and-visualbasic"></a>ADO et VisualBasic

Ajoutez d’abord une référence à ADODB dans votre projet

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

#### <a name="adonet-and-c"></a>ADO.NET et C\#

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

### <a name="using-sql-in-local-and-remote-queries"></a>Utilisation de SQL dans des requêtes locales et distantes

Vous pouvez exécuter vos requêtes localement ou à distance. Une requête locale utilisant la [clause from](-search-sql-from.md) est présentée dans l’exemple suivant. Une requête locale interroge le catalogue SystemIndex local uniquement.

```sql
FROM SystemIndex
```

Une requête distante à l’aide de la [clause from](-search-sql-from.md) est présentée dans l’exemple suivant. L’ajout de NomOrdinateur transforme l’exemple précédent en une requête distante.

```sql
FROM [<ComputerName>.]SystemIndex
```

Par défaut, Windows XP et Windows Server 2003 n’ont pas installé Windows Search. Seul Windows Search 4 (WS4) fournit une prise en charge des requêtes distantes. Les versions précédentes de Windows Desktop Search (WDS), telles que 3,01 et antérieures, ne prennent pas en charge l’interrogation à distance. Avec l’Explorateur Windows, vous pouvez interroger l’index local d’un ordinateur distant pour les éléments du système de fichiers (éléments gérés par le protocole « fichier : »).

Pour récupérer un élément à l’aide d’une requête distante, l’élément doit remplir les conditions suivantes :

- Être accessible via le chemin d’accès UNC (Universal Naming Convention).
- Existent sur l’ordinateur distant auquel le client a accès.
- A sa sécurité définie pour autoriser le client à avoir un accès en lecture.

L’Explorateur Windows possède des fonctionnalités permettant de partager des éléments, y compris un partage « public » ( \\ \\ ordinateur \\ public \\ ...) dans le **Centre réseau et partage**, et un partage « utilisateurs » ( \\ \\ \\ utilisateurs \\ de l’ordinateur...) pour les éléments partagés via l’Assistant partage. Une fois que vous avez partagé le ou les dossiers, vous pouvez interroger l’index local en spécifiant le nom d’ordinateur de l’ordinateur distant dans la clause FROM et un chemin d’accès UNC sur l’ordinateur distant dans la clause SCOPE, comme indiqué dans l’exemple suivant :

```sql
SELECT System.ItemName FROM MachineName.SystemIndex WHERE SCOPE='file://MachineName/<path>'
```

## <a name="aqs-based-queries"></a>Requêtes basées sur AQS

AQS est la syntaxe de requête par défaut utilisée par Windows Search pour interroger l’index et affiner et limiter les paramètres de recherche. Bien que AQS soit principalement utilisé par l’utilisateur, il peut être utilisé par les développeurs pour créer des requêtes par programmation. Dans Windows 7, la AQS canonique a été introduite et doit être utilisée dans Windows 7 et versions ultérieures pour générer des requêtes AQS par programmation. Pour plus d’informations sur AQS, consultez Utilisation de la [syntaxe de requête avancée par programmation](-search-3x-advancedquerysyntax.md).

Les approches suivantes pour l’interrogation de l’index sont basées sur AQS.

### <a name="using-isearchqueryhelper"></a>Utilisation de ISearchQueryHelper

Vous pouvez développer une classe de composant ou d’assistance pour interroger l’index à l’aide de l’interface [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) , ce qui vous permet de tirer parti de certaines fonctionnalités du système et de simplifier l’utilisation de la recherche Windows. Cette interface vous aide à :

- Obtenez une chaîne de connexion OLE DB pour vous connecter à la base de données de recherche Windows.
- Convertir les requêtes utilisateur de AQS en SQL de recherche Windows.

Cette interface est implémentée en tant que classe d’assistance à [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) et est obtenue en appelant [**ISearchCatalogManager :: GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper), comme indiqué dans l’exemple C++ suivant.

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

Pour implémenter l’interface [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) , consultez [utilisation de l’interface ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md) et la rubrique de référence [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) .

> [!Note]  
> Compatibilité héritée de Microsoft Windows Desktop Search (WDS) 2x : sur les ordinateurs exécutant Windows XP et Windows Server 2003 et versions ultérieures, [**ISearchDesktop**](/previous-versions//aa965729(v=vs.85)) est déconseillé. Au lieu de cela, les développeurs doivent utiliser [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) pour obtenir une chaîne de connexion, analyser la requête de l’utilisateur dans SQL, puis interroger OLE DB.

### <a name="using-the-search-ms-protocol"></a>Utilisation du protocole search-ms

La **recherche-** [protocole d’application](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85)) MS est une convention pour le démarrage d’une application, comme l’Explorateur Windows, pour interroger l’index de recherche Windows. Il permet de générer des requêtes avec des arguments de valeur de paramètre, notamment des arguments de propriété, des recherches précédemment enregistrées, une syntaxe de requête avancée (AQS), une syntaxe de requête naturelle (NQS) et des identificateurs de code de langue (LCID) pour l’indexeur et la requête elle-même.

Pour plus d’informations sur la syntaxe de protocole search-ms, consultez [interrogation de l’index avec le protocole search-ms](-search-3x-wds-qryidx-searchms.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Interrogation de l’index programmatiquement](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[Interrogation de l’index avec ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md)
</dt> <dt>

[Interrogation de l’index avec le protocole search-ms](-search-3x-wds-qryidx-searchms.md)
</dt> <dt>

[Interrogation de l’index avec la syntaxe SQL de Windows Search](-search-sql-windowssearch-entry.md)
</dt> <dt>

[Utilisation de la syntaxe de requête avancée par programmation](-search-3x-advancedquerysyntax.md)
</dt> </dl>
