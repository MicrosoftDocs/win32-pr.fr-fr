---
title: Création d’une jointure hétérogène entre SQL Server & Active Directory
description: Tous les employés de Fabrikam Corporation sont revus tous les six mois.
ms.assetid: 16f605ae-7f6c-4429-a379-47686618b15d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93e4e6b7f3bfd9c853d9ff262365d49c1f3a8d5c
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "103940705"
---
# <a name="creating-a-heterogeneous-join-between-sql-server--active-directory"></a>Création d’une jointure hétérogène entre SQL Server & Active Directory

Tous les employés de Fabrikam Corporation sont revus tous les six mois. Les évaluations sont stockées dans la base de données des ressources humaines dans SQL Server. Pour créer un affichage de ces données, Joe worden, administrateur d’entreprise, doit d’abord créer une table de vérification des performances des employés.

Dans l’analyseur de requêtes SQL, Joe va créer une table appelée EMP \_ Review qui contiendra trois colonnes pour contenir le nom de l’employé, la date de la révision et l’évaluation que l’employé a reçue.


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

Dans cet exemple, l’instruction [Select](https://msdn.microsoft.com/library/Aa259187.aspx) contient la liste des données qui seront obtenues à partir du service d’annuaire et SQL Server. L’instruction [from](https://msdn.microsoft.com/library/Aa258869.aspx) contient le nom du serveur d’annuaire lié dans lequel ces informations seront obtenues, dans le cas présent, viewADUsers. L’instruction [Where](https://msdn.microsoft.com/library/Aa260674.aspx) fournit les conditions de recherche. Dans cet exemple, il recherche par le nom dans le service d’annuaire, qui est défini sur le nom d’utilisateur SQL entré dans la tâche précédente.


```sql
SELECT ADsPath, userName, title, ReviewDate, Rating 
FROM EMP_REVIEW, viewADUsers
WHERE userName = Name
```



La commande précédente obtient le résultat de SQL Server et Active Directory. AdsPath et title proviennent de Active Directory, tandis que userName, ReviewDate et Rating proviennent de la table SQL. Il peut même créer une autre vue pour cette jointure.


```sql
CREATE VIEW reviewReport
AS
SELECT ADsPath, userName, title, ReviewDate, Rating 
FROM EMP_REVIEW, viewADUsers
WHERE userName = Name
GO
SELECT * FROM reviewReport
```



 

 




