---
title: Requête distribuée
description: étant donné qu’ADSI est un fournisseur de OLE DB, il peut participer à une requête distribuée introduite dans Microsoft SQL Server 7,0.
ms.assetid: 0a93ec2e-397a-47f7-b00c-f0f9aaa06de6
ms.tgt_platform: multiple
keywords:
- requêtes ADSI, requête distribuée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b46ab174565d8a02ae9058792aa36ef7c3379453e0ba0f861cddf150abf662c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118428700"
---
# <a name="distributed-query"></a>Requête distribuée

étant donné qu’ADSI est un fournisseur de OLE DB, il peut participer à une requête distribuée introduite dans Microsoft SQL Server 7,0. Les scénarios possibles sont les suivants :

-   jointure d’objets Active Directory avec des données SQL Server.
-   mise à jour des données SQL à partir d’objets Active Directory.
-   Création de jointures à trois ou quatre voies avec d’autres fournisseurs de OLE DB. par exemple, Index Server, SQL Server et Active Directory.

le fournisseur OLE DB prend en charge deux dialectes de commande, LDAP et SQL, pour accéder au service d’annuaire et retourner des résultats sous forme de tableau qui peut être interrogé avec SQL Server requêtes distribuées.

**pour démarrer l’analyseur de requêtes SQL**

1.  tout d’abord, ouvrez l' [analyseur de requêtes SQL](https://msdn.microsoft.com/library/Aa216983.aspx) sur le SQL Server qui est lié au service d’annuaire (consultez création d’un serveur lié).
2.  exécuter l' **analyseur de requêtes SQL** (démarrer les \| programmes \| Microsoft SQL Server 7,0)
3.  connectez-vous à l’ordinateur SQL Server.
4.  entrez la requête SQL dans le volet de l’éditeur de la fenêtre de requête.
5.  Exécutez la requête en appuyant sur F5.

Les sections suivantes fournissent plus de détails :

-   [Création d’un serveur lié](#creating-a-linked-server)
-   [création d’une connexion authentifiée SQL Server](#creating-a-sql-server-authenticated-login)
-   [Interrogation du service d'annuaire](#querying-the-directory-service)

## <a name="creating-a-linked-server"></a>Création d’un serveur lié

pour configurer une jointure distribuée sur un service d’annuaire Windows 2000 server, créez un serveur lié. Pour ce faire, configurez le mappage ADSI à l’aide de la procédure stockée système [SP \_ addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) . Cette procédure lie un nom à un nom de fournisseur OLE DB.

Dans l’exemple suivant, Notez qu’il existe plusieurs arguments utilisés avec la procédure stockée système [SP \_ addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) :

-   « ADSI » est l’argument de **serveur** et sera le nom de ce serveur lié.
-   « Active Directory Services 2,5 » est l’argument **srvproduct** , qui est le nom de la source de données OLE DB que vous ajoutez en tant que serveur lié.
-   « ADSDSOObject » est l’argument du **\_ nom du fournisseur** .
-   « adsdatasource » est l’argument de **\_ source de données** , qui est le nom de la source de données tel qu’il est interprété par le fournisseur OLE DB.

La commande [Exec](https://msdn.microsoft.com/library/Aa258848.aspx) est utilisée pour exécuter des procédures stockées système.


```sql
EXEC sp_addlinkedserver 'ADSI', 'Active Directory Services 2.5', 
'ADSDSOObject', 'adsdatasource'
GO
```



pour les connexions authentifiées par Windows, l’auto-mappage suffit pour accéder à l’annuaire avec SQL Server délégation de sécurité. Étant donné que le mappage automatique est créé par défaut pour les serveurs liés créés via [SP \_ addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx), aucun autre mappage de connexion n’est nécessaire.

pour les connexions SQL Server – authentifiées, vous pouvez configurer des connexions et des mots de passe appropriés pour la connexion au service d’annuaire à l’aide de la procédure stockée système [sp \_ addlinkedsrvlogin](https://msdn.microsoft.com/library/Aa259581.aspx) .

> [!Note]  
> Lorsque c'est possible, utilisez l'authentification Windows.

 

## <a name="creating-a-sql-server-authenticated-login"></a>création d’une connexion authentifiée SQL Server

si vous préférez utiliser une connexion SQL Server-authentifié plutôt que Windows l’authentification, ajoutez une connexion au serveur lié (voir la section précédente). Pour ce faire, utilisez la procédure stockée système [SP \_ addlinkedsrvlogin](https://msdn.microsoft.com/library/Aa259581.aspx) .

Dans l’exemple suivant, plusieurs arguments sont utilisés avec la procédure stockée système [SP \_ addlinkedsrvlogin](https://msdn.microsoft.com/library/Aa259581.aspx) :

-   « ADSI » est l’argument **rmtsvrname** , qui est le nom du serveur lié créé dans l’exemple précédent.
-   « Fabrikam \\ Administrator » est l’argument **locallogin** , qui est la connexion sur le serveur local et peut être la connexion SQL Server ou un utilisateur Windows NT.
-   "CN = administrateur, OU = Sales, DC = activeds, DC = fabrikam, DC = com" est l’argument **rmtuser** , qui est le nom d’utilisateur que vous utilisez pour vous connecter, car **useself** a la **valeur false**.
-   « secret \* \* 2000 » est le **rmtpassword**, qui est le mot de passe associé à **rmtuser**

La commande [Exec](https://msdn.microsoft.com/library/Aa258848.aspx) est utilisée pour exécuter des procédures stockées système.


```sql
EXEC sp_addlinkedsrvlogin 'ADSI', false, 'Fabrikam\Administrator', 
'CN=Administrator,OU=Sales,DC=activeds,DC=Fabrikam,DC=com', 'secret**2000'
```



## <a name="querying-the-directory-service"></a>Interrogation du service d'annuaire

Une fois que vous avez créé un serveur lié, utilisez une instruction [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) pour envoyer une requête au service d’annuaire. la requête SQL suivante crée une table virtuelle pour stocker les résultats de votre requête à l’aide de l’instruction [create VIEW](https://msdn.microsoft.com/library/Aa258253.aspx) . La vue créée est nommée « viewADContacts ».

La première instruction [Select](https://msdn.microsoft.com/library/Aa259187.aspx) définit les informations qui sont interrogées à partir du service d’annuaire et les mappe à une colonne de la table. Les informations entourées de crochets indiquent les données qui sont placées dans la table virtuelle. Les informations qui ne sont pas entre parenthèses indiquent les données récupérées à partir du service d’annuaire. Notez que les informations récupérées à partir du service d’annuaire doivent être référencées par leur nom complet LDAP.

L’instruction suivante est l’instruction [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) . Cette instruction a deux arguments : ADSI, qui est le nom du serveur lié que vous avez créé et une instruction de requête. L’instruction de requête contient les éléments suivants :

-   L’instruction [Select](https://msdn.microsoft.com/library/Aa259187.aspx) contient la liste des données qui seront obtenues à partir du service d’annuaire. Vous devrez utiliser le nom d’affichage LDAP pour indiquer les données que vous recherchez.
-   L’instruction [from](https://msdn.microsoft.com/library/Aa258869.aspx) contient le nom du serveur d’annuaire lié à partir duquel ces informations seront obtenues.
-   L’instruction [Where](https://msdn.microsoft.com/library/Aa260674.aspx) fournit les conditions de recherche. Dans cet exemple, il recherche des contacts.

La dernière instruction [Select](https://msdn.microsoft.com/library/Aa259187.aspx) est utilisée pour récupérer les résultats de la vue à afficher.


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



 

 




