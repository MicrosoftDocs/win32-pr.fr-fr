---
title: création d’une jointure hétérogène entre SQL Server & Active Directory
description: Tous les employés de Fabrikam Corporation sont revus tous les six mois.
ms.assetid: 16f605ae-7f6c-4429-a379-47686618b15d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8620706db56124b83c8cd8151c067a548d5a73d557fa6523ed82167647450b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117840289"
---
# <a name="creating-a-heterogeneous-join-between-sql-server--active-directory"></a>création d’une jointure hétérogène entre SQL Server & Active Directory

Tous les employés de Fabrikam Corporation sont revus tous les six mois. Les évaluations sont stockées dans la base de données des ressources humaines dans SQL Server. Pour créer un affichage de ces données, Joe worden, administrateur d’entreprise, doit d’abord créer une table de vérification des performances des employés.

dans l’analyseur de requêtes SQL, Joe crée une table appelée EMP \_ REVIEW qui contient trois colonnes pour contenir le nom de l’employé, la date de la révision et l’évaluation que l’employé a reçue.


```sql
CREATE TABLE EMP_REVIEW
(
userName varChar(40),
reviewDate datetime,
rating decimal 
)
```



Joe peut ensuite insérer quelques enregistrements.


```sql
INSERT EMP_REVIEW VALUES('Julie Adam', '2/15/1999', 4 )
INSERT EMP_REVIEW VALUES('Julie Bankert', '7/15/1999', 5 )
INSERT EMP_REVIEW VALUES('Chris Gray', '2/15/1999', 3 )
INSERT EMP_REVIEW VALUES('Chris Gray', '7/15/1999', 4 )
```



Joe peut désormais joindre les objets utilisateur Active Directory à la table SQL Server.

Dans cet exemple, l’instruction [Select](https://msdn.microsoft.com/library/Aa259187.aspx) contient la liste des données qui seront obtenues à partir du service d’annuaire et SQL Server. L’instruction [from](https://msdn.microsoft.com/library/Aa258869.aspx) contient le nom du serveur d’annuaire lié dans lequel ces informations seront obtenues, dans le cas présent, viewADUsers. L’instruction [Where](https://msdn.microsoft.com/library/Aa260674.aspx) fournit les conditions de recherche. dans cet exemple, il recherche par le nom dans le service d’annuaire, qui est défini sur le nom d’utilisateur SQL entré dans la tâche précédente.


```sql
SELECT ADsPath, userName, title, ReviewDate, Rating 
FROM EMP_REVIEW, viewADUsers
WHERE userName = Name
```



la commande précédente obtient le résultat de SQL Server et Active Directory. AdsPath et title proviennent de Active Directory, tandis que userName, ReviewDate et Rating proviennent de la table SQL. Il peut même créer une autre vue pour cette jointure.


```sql
CREATE VIEW reviewReport
AS
SELECT ADsPath, userName, title, ReviewDate, Rating 
FROM EMP_REVIEW, viewADUsers
WHERE userName = Name
GO
SELECT * FROM reviewReport
```



 

 




