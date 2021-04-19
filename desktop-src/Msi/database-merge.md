---
description: La méthode Merge de l’objet Database fusionne la base de données de référence avec la base de données de base.
ms.assetid: 777060cf-c672-49d5-a1a8-8674fdc4bde4
title: Database. Merge, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.Merge
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 0a1d93ba6a9a4dc0304daba11c5868b77ece43b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525513"
---
# <a name="databasemerge-method"></a><span data-ttu-id="88320-103">Database. Merge, méthode</span><span class="sxs-lookup"><span data-stu-id="88320-103">Database.Merge method</span></span>

<span data-ttu-id="88320-104">La méthode **Merge** de l’objet [**Database**](database-object.md) fusionne la base de données de référence avec la base de données de base.</span><span class="sxs-lookup"><span data-stu-id="88320-104">The **Merge** method of the [**Database**](database-object.md) object merges the reference database with the base database.</span></span>

## <a name="syntax"></a><span data-ttu-id="88320-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="88320-105">Syntax</span></span>


```JScript
Database.Merge(
  reference,
  errorTable
)
```



## <a name="parameters"></a><span data-ttu-id="88320-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="88320-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88320-107">*reference*</span><span class="sxs-lookup"><span data-stu-id="88320-107">*reference*</span></span> 
</dt> <dd>

<span data-ttu-id="88320-108">Objet [**de base de données**](database-object.md) requis à fusionner dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="88320-108">The required [**Database**](database-object.md) object to be merged into the database.</span></span>

</dd> <dt>

<span data-ttu-id="88320-109">*errorTable*</span><span class="sxs-lookup"><span data-stu-id="88320-109">*errorTable*</span></span> 
</dt> <dd>

<span data-ttu-id="88320-110">Nom facultatif d’une table qui contient les noms des tables contenant les conflits de fusion, le nombre de lignes en conflit dans la table et une référence à la table avec le conflit de fusion.</span><span class="sxs-lookup"><span data-stu-id="88320-110">An optional name of a table to contain the names of the tables containing merge conflicts, the number of conflicting rows within the table, and a reference to the table with the merge conflict.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88320-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="88320-111">Return value</span></span>

<span data-ttu-id="88320-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="88320-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="88320-113">Notes</span><span class="sxs-lookup"><span data-stu-id="88320-113">Remarks</span></span>

<span data-ttu-id="88320-114">La fonction [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) et la méthode **Merge** de l’objet [**Database**](database-object.md) ne peuvent pas être utilisées pour fusionner un module inclus dans un package d’installation.</span><span class="sxs-lookup"><span data-stu-id="88320-114">The [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) function and the **Merge** method of the [**Database**](database-object.md) object cannot be used to merge a module included within an installation package.</span></span> <span data-ttu-id="88320-115">Ils ne doivent pas être utilisés pour fusionner des [modules de fusion](merge-modules.md) dans un package de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="88320-115">They should not be used to merge [Merge Modules](merge-modules.md) into a Windows Installer package.</span></span> <span data-ttu-id="88320-116">Pour inclure un module de fusion dans un package d’installation, les auteurs des packages d’installation doivent suivre les instructions décrites dans la rubrique [application de modules de fusion](applying-merge-modules.md) .</span><span class="sxs-lookup"><span data-stu-id="88320-116">To include a merge module in an installation package, authors of installation packages should follow the guidelines that are described in the [Applying Merge Modules](applying-merge-modules.md) topic.</span></span>

<span data-ttu-id="88320-117">La méthode **Merge** ne copie pas les [fichiers CAB](cabinet-files.md) incorporés ni les [transformations incorporées](embedded-transforms.md) de la base de données de référence dans la base de données cible.</span><span class="sxs-lookup"><span data-stu-id="88320-117">The **Merge** method does not copy over embedded [cabinet files](cabinet-files.md) or [embedded transforms](embedded-transforms.md) from the reference database into the target database.</span></span> <span data-ttu-id="88320-118">Les flux de données incorporés qui sont répertoriés dans la table [binaire](binary-table.md) ou [icône](icon-table.md) sont copiés de la base de données de référence vers la base de données cible.</span><span class="sxs-lookup"><span data-stu-id="88320-118">Embedded data streams that are listed in the [Binary Table](binary-table.md) or [Icon Table](icon-table.md) are copied from the reference database to the target database.</span></span> <span data-ttu-id="88320-119">Les stockages incorporés dans la base de données de référence ne sont pas copiés dans la base de données cible.</span><span class="sxs-lookup"><span data-stu-id="88320-119">Storages embedded in the reference database are not copied to the target database.</span></span>

<span data-ttu-id="88320-120">Si aucune table n’est fournie, le message d’erreur général indique le nombre de tables contenant des conflits de fusion.</span><span class="sxs-lookup"><span data-stu-id="88320-120">If no table is provided, the general error message provides the number of tables containing merge conflicts.</span></span> <span data-ttu-id="88320-121">Une table peut être transmise, mais toutes les autres colonnes doivent avoir la valeur null, car l’opération de mise à jour de la [table d’erreurs](error-table.md) échoue si une colonne n’accepte pas la valeur null.</span><span class="sxs-lookup"><span data-stu-id="88320-121">Any table can be passed in, but all other columns must be nullable because the operation to update the [Error Table](error-table.md) fails if a column is not nullable.</span></span> <span data-ttu-id="88320-122">Une table nouvellement créée peut également être transmise, car la méthode **Merge** crée automatiquement les colonnes qu’elle utilise si des conflits de fusion sont détectés.</span><span class="sxs-lookup"><span data-stu-id="88320-122">A newly created table can be passed in as well because the **Merge** method automatically creates the columns it uses if merge conflicts are found.</span></span> <span data-ttu-id="88320-123">Deux colonnes sont utilisées pour présenter les conflits de fusion.</span><span class="sxs-lookup"><span data-stu-id="88320-123">Two columns are used to present merge conflicts.</span></span> <span data-ttu-id="88320-124">La première colonne est le nom de la table et la colonne de clé primaire.</span><span class="sxs-lookup"><span data-stu-id="88320-124">The first column is the table name and the primary key column.</span></span> <span data-ttu-id="88320-125">La deuxième colonne est le nombre de lignes de cette table qui ont des échecs de fusion.</span><span class="sxs-lookup"><span data-stu-id="88320-125">The second column is the number of rows of that table that have merge failures.</span></span>

<span data-ttu-id="88320-126">Si des tables portant le même nom dans les deux bases de données ne correspondent pas au nombre de clés primaires, aux types de colonnes, au nombre de colonnes ou aux noms de colonnes, la méthode de **fusion** échoue et publie un message d’erreur indiquant ce qui s’est produit.</span><span class="sxs-lookup"><span data-stu-id="88320-126">If tables of the same name in both databases do not match in the number of primary keys, the column types, the number of columns, or the column names, the **Merge** method fails and posts an error message stating what occurred.</span></span>

<span data-ttu-id="88320-127">Pour que la table d’erreurs reste, le gestionnaire d’erreurs doit valider la base de données à laquelle la table d’erreurs appartient.</span><span class="sxs-lookup"><span data-stu-id="88320-127">For the Error table to remain, the error handler must commit the database to which the Error table belongs.</span></span> <span data-ttu-id="88320-128">Toutefois, cette validation doit être effectuée après l’utilisation de la troisième colonne pour obtenir les références aux tables où des conflits de fusion se sont produits.</span><span class="sxs-lookup"><span data-stu-id="88320-128">However, this commit should be done after using the third column to obtain the references to those tables where merge conflicts occurred.</span></span>

<span data-ttu-id="88320-129">Si la méthode échoue, vous pouvez obtenir des informations d’erreur étendues à l’aide de la méthode [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="88320-129">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="88320-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="88320-130">Requirements</span></span>



| <span data-ttu-id="88320-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="88320-131">Requirement</span></span> | <span data-ttu-id="88320-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="88320-132">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88320-133">Version</span><span class="sxs-lookup"><span data-stu-id="88320-133">Version</span></span><br/> | <span data-ttu-id="88320-134">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="88320-134">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="88320-135">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="88320-135">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="88320-136">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="88320-136">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="88320-137">DLL</span><span class="sxs-lookup"><span data-stu-id="88320-137">DLL</span></span><br/>     | <dl> <span data-ttu-id="88320-138"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88320-138"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="88320-139">IID</span><span class="sxs-lookup"><span data-stu-id="88320-139">IID</span></span><br/>     | <span data-ttu-id="88320-140">IID \_ IDatabase est défini en tant que 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="88320-140">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



 

 




