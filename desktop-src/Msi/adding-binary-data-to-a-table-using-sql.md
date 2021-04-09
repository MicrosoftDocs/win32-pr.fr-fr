---
description: Les données binaires ne peuvent pas être insérées directement dans une table à l’aide de l’instruction INSERT INTO ou UPDATE SQL.
ms.assetid: cc055de8-eaba-48eb-a982-4d584ac7a881
title: Ajout de données binaires à une table à l’aide de SQL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 491bfe57354b4faf9f7c385bc4e14c64ad366f1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864525"
---
# <a name="adding-binary-data-to-a-table-using-sql"></a><span data-ttu-id="80865-103">Ajout de données binaires à une table à l’aide de SQL</span><span class="sxs-lookup"><span data-stu-id="80865-103">Adding Binary Data to a Table Using SQL</span></span>

<span data-ttu-id="80865-104">Les données binaires ne peuvent pas être insérées directement dans une table à l’aide de l’instruction INSERT INTO ou UPDATE SQL.</span><span class="sxs-lookup"><span data-stu-id="80865-104">Binary data cannot be inserted into a table directly using the INSERT INTO or UPDATE SQL queries.</span></span> <span data-ttu-id="80865-105">Pour ajouter des données binaires à une table, vous devez d’abord utiliser le marqueur de paramètre ( ?) dans la requête en tant qu’espace réservé pour la valeur binaire.</span><span class="sxs-lookup"><span data-stu-id="80865-105">In order to add binary data to a table, you must first use the parameter marker (?) in the query as a placeholder for the binary value.</span></span> <span data-ttu-id="80865-106">L’exécution de la requête doit inclure un enregistrement qui contient les données binaires dans l’un de ses champs.</span><span class="sxs-lookup"><span data-stu-id="80865-106">The execution of the query should include a record that contains the binary data in one of its fields.</span></span>

<span data-ttu-id="80865-107">Un marqueur est une référence de paramètre à une valeur fournie par un enregistrement envoyé avec la requête.</span><span class="sxs-lookup"><span data-stu-id="80865-107">A marker is a parameter reference to a value supplied by a record submitted with the query.</span></span> <span data-ttu-id="80865-108">Elle est représentée dans l’instruction SQL par un point d’interrogation ( ?).</span><span class="sxs-lookup"><span data-stu-id="80865-108">It is represented in the SQL statement by a question mark (?).</span></span>

<span data-ttu-id="80865-109">L’exemple de code suivant ajoute des données binaires à une table.</span><span class="sxs-lookup"><span data-stu-id="80865-109">The following sample code adds binary data to a table.</span></span>


```C++
#include <windows.h>
#include <Msiquery.h>
#include <tchar.h>
#pragma comment(lib, "msi.lib")


int main()  
{ 

PMSIHANDLE hDatabase = 0;
PMSIHANDLE hView = 0;
PMSIHANDLE hRec = 0;

if (ERROR_SUCCESS == MsiOpenDatabase(_T("c:\\temp\\testdb.msi"), MSIDBOPEN_TRANSACT, &hDatabase))
{
    //
    // Open view on Binary table so that we can add a new row, must use '?' to represent Binary data
    //

    if (ERROR_SUCCESS == MsiDatabaseOpenView(hDatabase, _T("INSERT INTO `Binary` (`Name`, `Data`) VALUES ('NewBlob', ?)"), &hView))
    {

        //
        // Create record with binary data in 1st field (must match up with '?' in query)
        //

        hRec = MsiCreateRecord(1);
        if (ERROR_SUCCESS == MsiRecordSetStream(hRec, 1, _T("c:\\temp\\data.bin")))
        {

            //
            // Execute view with record containing binary data value; commit database to save changes
            //

            if (ERROR_SUCCESS == MsiViewExecute(hView, hRec)
              && ERROR_SUCCESS == MsiViewClose(hView)
              && ERROR_SUCCESS == MsiDatabaseCommit(hDatabase))
            {
                //
                // New binary data successfully committed to the database
                //
            }
        }
    }
}

return 0;  
}
```



<span data-ttu-id="80865-110">L’exemple de script suivant ajoute des données binaires à une table.</span><span class="sxs-lookup"><span data-stu-id="80865-110">The following sample script adds binary data to a table.</span></span>


```VB
Dim Installer
Dim Database
Dim View
Dim Record

Set Installer = CreateObject("WindowsInstaller.Installer")

Set Record = Installer.CreateRecord(1)
Record.SetStream 1, "c:\temp\data.bin"

Set Database = Installer.OpenDatabase("c:\temp\testdb.msi", msiOpenDatabaseModeTransact)
Set View = Database.OpenView("INSERT INTO `Binary` (`Name`, `Data`) VALUES ('NewBlob', ?)")
View.Execute Record
Database.Commit ' save changes
```



## <a name="related-topics"></a><span data-ttu-id="80865-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="80865-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80865-112">Utilisation des requêtes</span><span class="sxs-lookup"><span data-stu-id="80865-112">Working with Queries</span></span>](working-with-queries.md)
</dt> <dt>

[<span data-ttu-id="80865-113">Syntaxe SQL</span><span class="sxs-lookup"><span data-stu-id="80865-113">SQL Syntax</span></span>](sql-syntax.md)
</dt> <dt>

[<span data-ttu-id="80865-114">Exemples de requêtes de base de données utilisant SQL et script</span><span class="sxs-lookup"><span data-stu-id="80865-114">Examples of Database Queries Using SQL and Script</span></span>](examples-of-database-queries-using-sql-and-script.md)
</dt> </dl>

 

 



