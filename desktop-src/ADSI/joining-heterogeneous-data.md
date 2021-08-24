---
title: Jointure de données hétérogènes
description: Les organisations classiques stockent les données dans plusieurs bases de données hétérogènes. les données des ressources humaines peuvent être stockées dans SQL Server, tandis que les données de gestion des comptes sont stockées dans l’annuaire. D’autres données peuvent être stockées dans des formats propriétaires.
ms.assetid: 45281b42-5cb2-42f9-9c7c-f3e3174b0f9d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 409ac4e82d735f5099bb8846a59683075007c3fbdf56600bc5ae01e6863ffa2a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119656999"
---
# <a name="joining-heterogeneous-data"></a>Jointure de données hétérogènes

Les organisations classiques stockent les données dans plusieurs bases de données hétérogènes. les données des ressources humaines peuvent être stockées dans SQL Server, tandis que les données de gestion des comptes sont stockées dans l’annuaire. D’autres données peuvent être stockées dans des formats propriétaires.

avec, SQL Server 7,0, ADSI et le fournisseur OLE DB, il est possible de joindre des données de Active Directory à des données dans SQL Server et de créer une vue des données jointes.

**pour joindre des données Active Directory à des données SQL Server**

1.  exécuter l' **analyseur de requêtes SQL** (démarrer les \| programmes \| Microsoft SQL Server 7,0)
2.  connectez-vous à l’ordinateur SQL Server.
3.  Exécutez la ligne suivante (en la mettant en surbrillance et en appuyant sur CTRL + E) :

    ```sql
    EXEC sp_addlinkedserver 'ADSI', 'Active Directory Service Interfaces', 
    'ADSDSOObject', 'adsdatasource'
    GO
    ```

    

    Dans cette ligne, les arguments de la procédure stockée système [SP \_ addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) sont les suivants :

    -   « ADSI » est l’argument de **serveur** , qui est le nom de ce serveur lié.
    -   « Active Directory Services » est l’argument **srvproduct** , qui est le nom de la source de données OLE DB que vous ajoutez en tant que serveur lié.
    -   « ADSDSOObject » est l’argument du **\_ nom du fournisseur** et indique que vous utilisez le fournisseur de OLE DB.
    -   « adsdatasource » est l' **\_ argument de source de données**, qui est le nom de la source de données tel qu’il est interprété par le fournisseur OLE DB.

    Vous pouvez maintenant utiliser le serveur lié pour accéder à Active Directory à partir de SQL Server.

4.  L’exemple suivant exécute une requête à l’aide de l’instruction [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) . Cette instruction a deux arguments : ADSI, qui est le nom du serveur lié que vous venez de créer et une instruction de requête. L’instruction de requête contient les éléments suivants :

    -   L’instruction [Select](https://msdn.microsoft.com/library/Aa259187.aspx) contient la liste des données qui seront obtenues à partir du service d’annuaire. Vous devrez utiliser le nom d’affichage LDAP pour indiquer les données que vous recherchez.
    -   L’instruction [from](https://msdn.microsoft.com/library/Aa258869.aspx) contient le nom du serveur d’annuaire lié à partir duquel ces informations seront obtenues.
    -   L’instruction [Where](https://msdn.microsoft.com/library/Aa260674.aspx) fournit les conditions de recherche. Dans cet exemple, il recherche des utilisateurs.

    Tapez et exécutez :

    ```sql
    SELECT * FROM OPENQUERY( ADSI, 
        'SELECT name, adsPath 
         FROM 'LDAP://DC=Fabrikam,DC=com' 
         WHERE objectCategory = 'Person' AND objectClass= 'user'')
    ```

    

    Vous pouvez également utiliser le [dialecte ADSI LDAP](ldap-dialect.md). Par exemple :

    ```sql
    SELECT * FROM OPENQUERY(ADSI,
        '<LDAP://DC=Fabrikam,DC=COM>;(&(objectCategory=Person)(objectClass=user));name, adspath;subtree')
    ```

    

    Dans l’exemple précédent, la requête LDAP se compose de quatre parties :

    -   " \<LDAP://DC=Fabrikam,DC=COM> " est le nom unique du serveur d’annuaire à rechercher.
    -   « (& (objectCategory = person) (objectClass = user)) » est le filtre de recherche LDAP (voir la [syntaxe du filtre de recherche](search-filter-syntax.md)).
    -   « Name, ADsPath » sont les noms (à l’aide du format de nom complet LDAP) des attributs à récupérer.
    -   « sous-arborescence » indique l' [étendue](scope-of-query.md) de la recherche.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création et exécution d’une vue](creating-and-executing-a-view.md)
</dt> </dl>

 

 




