---
description: L’objet View représente un jeu de résultats obtenu lors du traitement d’une requête à l’aide de la méthode OpenView de l’objet Database.
ms.assetid: d9d6583a-1cf3-4c33-a851-83e862e2338e
title: Afficher l’objet
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: c26cfa3c4873913d70fca63537f1d25532648a42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528560"
---
# <a name="view-object"></a><span data-ttu-id="55513-103">Afficher l’objet</span><span class="sxs-lookup"><span data-stu-id="55513-103">View object</span></span>

<span data-ttu-id="55513-104">L’objet **View** représente un jeu de résultats obtenu lors du traitement d’une requête à l’aide de la méthode [**OpenView**](database-openview.md) de l’objet [**Database**](database-object.md) .</span><span class="sxs-lookup"><span data-stu-id="55513-104">The **View** object represents a result set obtained when processing a query using the [**OpenView**](database-openview.md) method of the [**Database**](database-object.md) object.</span></span> <span data-ttu-id="55513-105">Avant de pouvoir transférer des données, la requête doit être exécutée à l’aide de la méthode [**Execute**](view-execute.md) , en lui transmettant tous les paramètres remplaçables désignés dans la chaîne de requête SQL.</span><span class="sxs-lookup"><span data-stu-id="55513-105">Before any data can be transferred, the query must be executed using the [**Execute**](view-execute.md) method, passing to it all replaceable parameters designated within the SQL query string.</span></span> <span data-ttu-id="55513-106">La requête peut être exécutée à nouveau, avec des paramètres différents, si nécessaire, mais uniquement après avoir libéré le jeu de résultats en extrayant tous les enregistrements ou en appelant la méthode [**Close**](view-close.md) .</span><span class="sxs-lookup"><span data-stu-id="55513-106">The query may be executed again, with different parameters if needed, but only after freeing the result set either by fetching all the records or by calling the [**Close**](view-close.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="55513-107">Membres</span><span class="sxs-lookup"><span data-stu-id="55513-107">Members</span></span>

<span data-ttu-id="55513-108">L’objet de **vue** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="55513-108">The **View** object has these types of members:</span></span>

-   [<span data-ttu-id="55513-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="55513-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="55513-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="55513-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="55513-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="55513-111">Methods</span></span>

<span data-ttu-id="55513-112">L’objet de **vue** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="55513-112">The **View** object has these methods.</span></span>



| <span data-ttu-id="55513-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="55513-113">Method</span></span>                            | <span data-ttu-id="55513-114">Description</span><span class="sxs-lookup"><span data-stu-id="55513-114">Description</span></span>                                                                                                                                                                     |
|:----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="55513-115">**Fermer**</span><span class="sxs-lookup"><span data-stu-id="55513-115">**Close**</span></span>](view-close.md)       | <span data-ttu-id="55513-116">Met fin à l’exécution de la requête et libère les ressources de la base de données.</span><span class="sxs-lookup"><span data-stu-id="55513-116">Terminates query execution and releases database resources.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="55513-117">**Execute**</span><span class="sxs-lookup"><span data-stu-id="55513-117">**Execute**</span></span>](view-execute.md)   | <span data-ttu-id="55513-118">Utilise le jeton de point d’interrogation pour représenter les paramètres dans une requête SQL.</span><span class="sxs-lookup"><span data-stu-id="55513-118">Uses the question mark token to represent parameters in a SQL query.</span></span> <span data-ttu-id="55513-119">Les valeurs de ces paramètres sont transmises en tant que champs correspondants d’un enregistrement de paramètre.</span><span class="sxs-lookup"><span data-stu-id="55513-119">The values of these parameters are passed in as the corresponding fields of a parameter record.</span></span><br/> |
| [<span data-ttu-id="55513-120">**Collecté**</span><span class="sxs-lookup"><span data-stu-id="55513-120">**Fetch**</span></span>](view-fetch.md)       | <span data-ttu-id="55513-121">Retourne un objet [**Record**](record-object.md) contenant les données de la colonne demandée si davantage de lignes sont disponibles dans le jeu de résultats, sinon retourne la valeur null.</span><span class="sxs-lookup"><span data-stu-id="55513-121">Returns a [**Record**](record-object.md) object containing the requested column data if more rows are available in the result set, otherwise, it returns null.</span></span><br/>      |
| [<span data-ttu-id="55513-122">**GetError**</span><span class="sxs-lookup"><span data-stu-id="55513-122">**GetError**</span></span>](view-geterror.md) | <span data-ttu-id="55513-123">Retourne l’erreur de validation et le nom de la colonne pour laquelle l’erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="55513-123">Returns the Validation error and column name for which the error occurred.</span></span><br/>                                                                                           |
| [<span data-ttu-id="55513-124">**Modifier**</span><span class="sxs-lookup"><span data-stu-id="55513-124">**Modify**</span></span>](view-modify.md)     | <span data-ttu-id="55513-125">Modifie une ligne de base de données avec un objet [**enregistrement**](record-object.md) modifié obtenu à l’aide de la méthode [**Fetch**](view-fetch.md) .</span><span class="sxs-lookup"><span data-stu-id="55513-125">Modifies a database row with a modified [**Record**](record-object.md) object obtained by the [**Fetch**](view-fetch.md) method.</span></span><br/>                                   |



 

### <a name="properties"></a><span data-ttu-id="55513-126">Propriétés</span><span class="sxs-lookup"><span data-stu-id="55513-126">Properties</span></span>

<span data-ttu-id="55513-127">L’objet de **vue** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="55513-127">The **View** object has these properties.</span></span>



| <span data-ttu-id="55513-128">Propriété</span><span class="sxs-lookup"><span data-stu-id="55513-128">Property</span></span>                                         | <span data-ttu-id="55513-129">Description</span><span class="sxs-lookup"><span data-stu-id="55513-129">Description</span></span>                                                                                                                           |
|:-------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="55513-130">**ColumnInfo**</span><span class="sxs-lookup"><span data-stu-id="55513-130">**ColumnInfo**</span></span>](view-columninfo.md)<br/> | <span data-ttu-id="55513-131">Retourne un objet [**Record**](record-object.md) contenant les informations demandées sur chaque colonne du jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="55513-131">Returns a [**Record**](record-object.md) object containing the requested information about each column in the result set.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="55513-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="55513-132">Requirements</span></span>



| <span data-ttu-id="55513-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="55513-133">Requirement</span></span> | <span data-ttu-id="55513-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="55513-134">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55513-135">Version</span><span class="sxs-lookup"><span data-stu-id="55513-135">Version</span></span><br/> | <span data-ttu-id="55513-136">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="55513-136">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="55513-137">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="55513-137">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="55513-138">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="55513-138">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="55513-139">DLL</span><span class="sxs-lookup"><span data-stu-id="55513-139">DLL</span></span><br/>     | <dl> <span data-ttu-id="55513-140"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55513-140"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="55513-141">IID</span><span class="sxs-lookup"><span data-stu-id="55513-141">IID</span></span><br/>     | <span data-ttu-id="55513-142">L’IID \_ IView est défini en tant que 000C109C-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="55513-142">IID\_IView is defined as 000C109C-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



## <a name="see-also"></a><span data-ttu-id="55513-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="55513-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55513-144">Exemples de scripts Windows Installer</span><span class="sxs-lookup"><span data-stu-id="55513-144">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




