---
description: les données binaires ne peuvent pas être insérées directement dans une table à l’aide des requêtes INSERT into ou UPDATE SQL.
ms.assetid: cc055de8-eaba-48eb-a982-4d584ac7a881
title: Ajout de données binaires à une table à l’aide de SQL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 005b7de98fa62ae6e79378831802b8a5a9c95b1d0f3d33dd353fd5403ad600ca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996949"
---
# <a name="adding-binary-data-to-a-table-using-sql"></a>Ajout de données binaires à une table à l’aide de SQL

les données binaires ne peuvent pas être insérées directement dans une table à l’aide des requêtes INSERT into ou UPDATE SQL. Pour ajouter des données binaires à une table, vous devez d’abord utiliser le marqueur de paramètre ( ?) dans la requête en tant qu’espace réservé pour la valeur binaire. L’exécution de la requête doit inclure un enregistrement qui contient les données binaires dans l’un de ses champs.

Un marqueur est une référence de paramètre à une valeur fournie par un enregistrement envoyé avec la requête. elle est représentée dans l’instruction SQL par un point d’interrogation ( ?).

L’exemple de code suivant ajoute des données binaires à une table.


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



L’exemple de script suivant ajoute des données binaires à une table.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des requêtes](working-with-queries.md)
</dt> <dt>

[Syntaxe SQL](sql-syntax.md)
</dt> <dt>

[exemples de requêtes de base de données utilisant des SQL et des scripts](examples-of-database-queries-using-sql-and-script.md)
</dt> </dl>

 

 



