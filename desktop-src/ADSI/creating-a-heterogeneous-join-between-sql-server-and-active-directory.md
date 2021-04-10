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
# <a name="creating-a-heterogeneous-join-between-sql-server--active-directory"></a><span data-ttu-id="646a3-103">Création d’une jointure hétérogène entre SQL Server & Active Directory</span><span class="sxs-lookup"><span data-stu-id="646a3-103">Creating a Heterogeneous Join between SQL Server & Active Directory</span></span>

<span data-ttu-id="646a3-104">Tous les employés de Fabrikam Corporation sont revus tous les six mois.</span><span class="sxs-lookup"><span data-stu-id="646a3-104">All employees at the Fabrikam corporation are reviewed every six months.</span></span> <span data-ttu-id="646a3-105">Les évaluations sont stockées dans la base de données des ressources humaines dans SQL Server.</span><span class="sxs-lookup"><span data-stu-id="646a3-105">Review ratings are stored in the Human Resource database in SQL Server.</span></span> <span data-ttu-id="646a3-106">Pour créer un affichage de ces données, Joe worden, administrateur d’entreprise, doit d’abord créer une table de vérification des performances des employés.</span><span class="sxs-lookup"><span data-stu-id="646a3-106">To create a view of this data, Joe Worden, the enterprise administrator, must first create an employee performance review table.</span></span>

<span data-ttu-id="646a3-107">Dans l’analyseur de requêtes SQL, Joe va créer une table appelée EMP \_ Review qui contiendra trois colonnes pour contenir le nom de l’employé, la date de la révision et l’évaluation que l’employé a reçue.</span><span class="sxs-lookup"><span data-stu-id="646a3-107">In the SQL Query Analyzer, Joe is going to create a table called EMP\_REVIEW that will contain three columns to hold the name of the employee, the date of the review, and the rating that the employee received.</span></span>


```sql
CREATE TABLE EMP_REVIEW
(
userName varChar(40),
reviewDate datetime,
rating decimal 
)
```



<span data-ttu-id="646a3-108">Joe peut ensuite insérer quelques enregistrements.</span><span class="sxs-lookup"><span data-stu-id="646a3-108">Joe can then insert a few records.</span></span>


```sql
INSERT EMP_REVIEW VALUES('Julie Adam', '2/15/1999', 4 )
INSERT EMP_REVIEW VALUES('Julie Bankert', '7/15/1999', 5 )
INSERT EMP_REVIEW VALUES('Chris Gray', '2/15/1999', 3 )
INSERT EMP_REVIEW VALUES('Chris Gray', '7/15/1999', 4 )
```



<span data-ttu-id="646a3-109">Joe peut désormais joindre les objets utilisateur Active Directory à la table SQL Server.</span><span class="sxs-lookup"><span data-stu-id="646a3-109">Now Joe can join the Active Directory user objects to the SQL Server table.</span></span>

<span data-ttu-id="646a3-110">Dans cet exemple, l’instruction [Select](https://msdn.microsoft.com/library/Aa259187.aspx) contient la liste des données qui seront obtenues à partir du service d’annuaire et SQL Server.</span><span class="sxs-lookup"><span data-stu-id="646a3-110">In this example, the [SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) statement contains the list of data that will be obtained from the directory service and SQL Server.</span></span> <span data-ttu-id="646a3-111">L’instruction [from](https://msdn.microsoft.com/library/Aa258869.aspx) contient le nom du serveur d’annuaire lié dans lequel ces informations seront obtenues, dans le cas présent, viewADUsers.</span><span class="sxs-lookup"><span data-stu-id="646a3-111">The [FROM](https://msdn.microsoft.com/library/Aa258869.aspx) statement contains the name of the linked directory server where this information will be obtained from, in this case, viewADUsers.</span></span> <span data-ttu-id="646a3-112">L’instruction [Where](https://msdn.microsoft.com/library/Aa260674.aspx) fournit les conditions de recherche.</span><span class="sxs-lookup"><span data-stu-id="646a3-112">The [WHERE](https://msdn.microsoft.com/library/Aa260674.aspx) statement provides the search conditions.</span></span> <span data-ttu-id="646a3-113">Dans cet exemple, il recherche par le nom dans le service d’annuaire, qui est défini sur le nom d’utilisateur SQL entré dans la tâche précédente.</span><span class="sxs-lookup"><span data-stu-id="646a3-113">In this example, it is searching by the name in the directory service, which is set to the SQL userName entered in the previous task.</span></span>


```sql
SELECT ADsPath, userName, title, ReviewDate, Rating 
FROM EMP_REVIEW, viewADUsers
WHERE userName = Name
```



<span data-ttu-id="646a3-114">La commande précédente obtient le résultat de SQL Server et Active Directory.</span><span class="sxs-lookup"><span data-stu-id="646a3-114">The previous command gets the result from both SQL Server and Active Directory.</span></span> <span data-ttu-id="646a3-115">AdsPath et title proviennent de Active Directory, tandis que userName, ReviewDate et Rating proviennent de la table SQL.</span><span class="sxs-lookup"><span data-stu-id="646a3-115">AdsPath and title are from Active Directory, whereas userName, ReviewDate, and Rating are from the SQL table.</span></span> <span data-ttu-id="646a3-116">Il peut même créer une autre vue pour cette jointure.</span><span class="sxs-lookup"><span data-stu-id="646a3-116">He can even create another view for this join.</span></span>


```sql
CREATE VIEW reviewReport
AS
SELECT ADsPath, userName, title, ReviewDate, Rating 
FROM EMP_REVIEW, viewADUsers
WHERE userName = Name
GO
SELECT * FROM reviewReport
```



 

 




