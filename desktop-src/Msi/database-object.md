---
description: L’objet de base de données accède à une base de données du programme d’installation.
ms.assetid: 97765884-3e1c-486a-932c-6430b113fac8
title: Objet de base de données
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5b47e4678d9475abe90c4b55d6adb514314dcc0e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537895"
---
# <a name="database-object"></a><span data-ttu-id="92157-103">Objet de base de données</span><span class="sxs-lookup"><span data-stu-id="92157-103">Database object</span></span>

<span data-ttu-id="92157-104">L’objet **de base de données** accède à une base de données du programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="92157-104">The **Database** object accesses an installer database.</span></span>

<span data-ttu-id="92157-105">L’objet **de base de données** est libéré lorsqu’il est retiré de l’étendue ou lorsque la variable objet associée est définie sur null.</span><span class="sxs-lookup"><span data-stu-id="92157-105">The **Database** object is released when it is either taken out of scope or when the object variable associated with it is set to null.</span></span> <span data-ttu-id="92157-106">La méthode de [**validation**](database-commit.md) doit être appelée avant que l’objet **de base de données** ne soit libéré pour écrire toutes les modifications persistantes.</span><span class="sxs-lookup"><span data-stu-id="92157-106">The [**Commit**](database-commit.md) method must be called before the **Database** object is released to write out all persistent changes.</span></span> <span data-ttu-id="92157-107">Si la méthode de **validation** n’est pas appelée, le programme d’installation effectue une restauration implicite lors de la destruction de l’objet.</span><span class="sxs-lookup"><span data-stu-id="92157-107">If the **Commit** method is not called, the installer performs an implicit rollback upon object destruction.</span></span>

<span data-ttu-id="92157-108">Le client peut utiliser la procédure suivante pour l’accès aux données.</span><span class="sxs-lookup"><span data-stu-id="92157-108">The client can use the following procedure for data access.</span></span>

<span data-ttu-id="92157-109">**Pour interroger l’API de séquencement**</span><span class="sxs-lookup"><span data-stu-id="92157-109">**To Query API Sequencing**</span></span>

1.  <span data-ttu-id="92157-110">Obtenez un objet **de base de données** en appelant l’objet [**OpenDatabase**](installer-opendatabase.md) ou le [**programme d’installation**](installer-object.md) .</span><span class="sxs-lookup"><span data-stu-id="92157-110">Obtain a **Database** object by calling the [**OpenDatabase**](installer-opendatabase.md) or the [**Installer**](installer-object.md) object.</span></span>
2.  <span data-ttu-id="92157-111">Lancez une requête à l’aide d’une chaîne SQL en appelant la méthode [**OpenView**](database-openview.md) de l’objet **de base de données** .</span><span class="sxs-lookup"><span data-stu-id="92157-111">Initiate a query using a SQL string by calling the [**OpenView**](database-openview.md) method of the **Database** object.</span></span>
3.  <span data-ttu-id="92157-112">Définissez les paramètres de requête dans un objet [**enregistrement**](record-object.md) et exécutez la requête de base de données en appelant la méthode [**Execute**](view-execute.md) de l’objet [**View**](view-object.md) .</span><span class="sxs-lookup"><span data-stu-id="92157-112">Set query parameters in a [**Record**](record-object.md) object and execute the database query by calling the [**Execute**](view-execute.md) method of the [**View**](view-object.md) object.</span></span> <span data-ttu-id="92157-113">Cela génère un résultat qui peut être extrait ou mis à jour.</span><span class="sxs-lookup"><span data-stu-id="92157-113">This produces a result that can be fetched or updated.</span></span>
4.  <span data-ttu-id="92157-114">Appelez la méthode [**Fetch**](view-fetch.md) de l’objet [**View**](view-object.md) à plusieurs reprises pour retourner des objets [**Record**](record-object.md) .</span><span class="sxs-lookup"><span data-stu-id="92157-114">Call the [**Fetch**](view-fetch.md) method of the [**View**](view-object.md) object repeatedly to return [**Record**](record-object.md) objects.</span></span>
5.  <span data-ttu-id="92157-115">Met à jour les lignes de base de données d’un objet [**Record**](record-object.md) obtenu par la méthode [**Fetch**](view-fetch.md) à l’aide de la méthode [**Modify**](view-modify.md) de l’objet [**View**](view-object.md) .</span><span class="sxs-lookup"><span data-stu-id="92157-115">Update database rows of a [**Record**](record-object.md) object obtained by the [**Fetch**](view-fetch.md) method using the [**Modify**](view-modify.md) method of the [**View**](view-object.md) object.</span></span>
6.  <span data-ttu-id="92157-116">Libérez la requête et tous les enregistrements non récupérés en appelant la méthode [**Close**](view-close.md) de l’objet [**View**](view-object.md) .</span><span class="sxs-lookup"><span data-stu-id="92157-116">Release the query and any unfetched records by calling the [**Close**](view-close.md) method of the [**View**](view-object.md) object.</span></span>
7.  <span data-ttu-id="92157-117">Conservez toutes les mises à jour de base de données en appelant la méthode [**Commit**](database-commit.md) de l’objet **Database** .</span><span class="sxs-lookup"><span data-stu-id="92157-117">Persist any database updates by calling the [**Commit**](database-commit.md) method of the **Database** object.</span></span>

## <a name="members"></a><span data-ttu-id="92157-118">Membres</span><span class="sxs-lookup"><span data-stu-id="92157-118">Members</span></span>

<span data-ttu-id="92157-119">L’objet **de base de données** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="92157-119">The **Database** object has these types of members:</span></span>

-   [<span data-ttu-id="92157-120">Méthodes</span><span class="sxs-lookup"><span data-stu-id="92157-120">Methods</span></span>](#methods)
-   [<span data-ttu-id="92157-121">Propriétés</span><span class="sxs-lookup"><span data-stu-id="92157-121">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="92157-122">Méthodes</span><span class="sxs-lookup"><span data-stu-id="92157-122">Methods</span></span>

<span data-ttu-id="92157-123">L’objet **de base de données** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="92157-123">The **Database** object has these methods.</span></span>



| <span data-ttu-id="92157-124">Méthode</span><span class="sxs-lookup"><span data-stu-id="92157-124">Method</span></span>                                                                    | <span data-ttu-id="92157-125">Description</span><span class="sxs-lookup"><span data-stu-id="92157-125">Description</span></span>                                                                                                                                                               |
|:--------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="92157-126">**ApplyTransform**</span><span class="sxs-lookup"><span data-stu-id="92157-126">**ApplyTransform**</span></span>](database-applytransform.md)                         | <span data-ttu-id="92157-127">Applique la transformation à cette base de données.</span><span class="sxs-lookup"><span data-stu-id="92157-127">Applies the transform to this database.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="92157-128">**Commit**</span><span class="sxs-lookup"><span data-stu-id="92157-128">**Commit**</span></span>](database-commit.md)                                         | <span data-ttu-id="92157-129">Finalise la forme persistante de la base de données.</span><span class="sxs-lookup"><span data-stu-id="92157-129">Finalizes the persistent form of the database.</span></span><br/>                                                                                                                 |
| [<span data-ttu-id="92157-130">**CreateTransformSummaryInfo**</span><span class="sxs-lookup"><span data-stu-id="92157-130">**CreateTransformSummaryInfo**</span></span>](database-createtransformsummaryinfo.md) | <span data-ttu-id="92157-131">Crée et remplit le flux d’informations de synthèse d’un fichier de transformation existant.</span><span class="sxs-lookup"><span data-stu-id="92157-131">Creates and populates the summary information stream of an existing transform file.</span></span><br/>                                                                            |
| [<span data-ttu-id="92157-132">**EnableUIPreview**</span><span class="sxs-lookup"><span data-stu-id="92157-132">**EnableUIPreview**</span></span>](database-enableuipreview.md)                       | <span data-ttu-id="92157-133">Facilite la création de boîtes de dialogue et de panneaux en fournissant la prise en charge nécessaire pour afficher les boîtes de dialogue de l’interface utilisateur stockées dans la base de données du programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="92157-133">Facilitates the authoring of dialog boxes and billboards by providing the support needed to view user interface dialog boxes stored in the installer database.</span></span><br/> |
| [<span data-ttu-id="92157-134">**Exporter**</span><span class="sxs-lookup"><span data-stu-id="92157-134">**Export**</span></span>](database-export.md)                                         | <span data-ttu-id="92157-135">Copie la structure et les données d’une table spécifiée dans un fichier d’archive de texte.</span><span class="sxs-lookup"><span data-stu-id="92157-135">Copies the structure and data from a specified table to a text archive file.</span></span><br/>                                                                                   |
| [<span data-ttu-id="92157-136">**GenerateTransform**</span><span class="sxs-lookup"><span data-stu-id="92157-136">**GenerateTransform**</span></span>](database-generatetransform.md)                   | <span data-ttu-id="92157-137">Crée une transformation.</span><span class="sxs-lookup"><span data-stu-id="92157-137">Creates a transform.</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="92157-138">**Importer**</span><span class="sxs-lookup"><span data-stu-id="92157-138">**Import**</span></span>](database-import.md)                                         | <span data-ttu-id="92157-139">Importe une table de base de données à partir d’un fichier d’archive de texte.</span><span class="sxs-lookup"><span data-stu-id="92157-139">Imports a database table from a text archive file.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="92157-140">**Fusion**</span><span class="sxs-lookup"><span data-stu-id="92157-140">**Merge**</span></span>](database-merge.md)                                           | <span data-ttu-id="92157-141">Fusionne la base de données de référence avec la base de données de base.</span><span class="sxs-lookup"><span data-stu-id="92157-141">Merges the reference database with the base database.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="92157-142">**OpenView**</span><span class="sxs-lookup"><span data-stu-id="92157-142">**OpenView**</span></span>](database-openview.md)                                     | <span data-ttu-id="92157-143">Retourne un objet de [**vue**](view-object.md) représentant la requête spécifiée par une chaîne SQL.</span><span class="sxs-lookup"><span data-stu-id="92157-143">Returns a [**View**](view-object.md) object representing the query specified by a SQL string.</span></span><br/>                                                                 |



 

### <a name="properties"></a><span data-ttu-id="92157-144">Propriétés</span><span class="sxs-lookup"><span data-stu-id="92157-144">Properties</span></span>

<span data-ttu-id="92157-145">L’objet **de base de données** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="92157-145">The **Database** object has these properties.</span></span>



| <span data-ttu-id="92157-146">Propriété</span><span class="sxs-lookup"><span data-stu-id="92157-146">Property</span></span>                                                                               | <span data-ttu-id="92157-147">Description</span><span class="sxs-lookup"><span data-stu-id="92157-147">Description</span></span>                                                                                                                                                      |
|:---------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="92157-148">**DatabaseState**</span><span class="sxs-lookup"><span data-stu-id="92157-148">**DatabaseState**</span></span>](database-databasestate.md)<br/>                             | <span data-ttu-id="92157-149">Retourne l’état de persistance de la base de données.</span><span class="sxs-lookup"><span data-stu-id="92157-149">Returns the persistence state of the database.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="92157-150">**PrimaryKeys**</span><span class="sxs-lookup"><span data-stu-id="92157-150">**PrimaryKeys**</span></span>](database-primarykeys.md)<br/>                                 | <span data-ttu-id="92157-151">Retourne un objet [**Record**](record-object.md) contenant le nom de la table et les noms des colonnes (qui composent les clés primaires).</span><span class="sxs-lookup"><span data-stu-id="92157-151">Returns a [**Record**](record-object.md) object containing the table name and the column names (comprising the primary keys).</span></span><br/>                        |
| [<span data-ttu-id="92157-152">**SummaryInformation (objet de base de données)**</span><span class="sxs-lookup"><span data-stu-id="92157-152">**SummaryInformation (Database Object)**</span></span>](database-summaryinformation.md)<br/> | <span data-ttu-id="92157-153">Retourne un objet [**SummaryInfo**](summaryinfo-object.md) qui peut être utilisé pour examiner, mettre à jour et ajouter des propriétés au flux d’informations de synthèse.</span><span class="sxs-lookup"><span data-stu-id="92157-153">Returns a [**SummaryInfo**](summaryinfo-object.md) object that can be used to examine, update, and add properties to the summary information stream.</span></span><br/> |
| [<span data-ttu-id="92157-154">**TablePersistent**</span><span class="sxs-lookup"><span data-stu-id="92157-154">**TablePersistent**</span></span>](database-tablepersistent.md)<br/>                         | <span data-ttu-id="92157-155">Retourne l’état de persistance de la table.</span><span class="sxs-lookup"><span data-stu-id="92157-155">Returns the persistence state of the table.</span></span><br/>                                                                                                           |



 

## <a name="requirements"></a><span data-ttu-id="92157-156">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="92157-156">Requirements</span></span>



| <span data-ttu-id="92157-157">Condition requise</span><span class="sxs-lookup"><span data-stu-id="92157-157">Requirement</span></span> | <span data-ttu-id="92157-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="92157-158">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92157-159">Version</span><span class="sxs-lookup"><span data-stu-id="92157-159">Version</span></span><br/> | <span data-ttu-id="92157-160">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="92157-160">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="92157-161">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="92157-161">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="92157-162">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="92157-162">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="92157-163">DLL</span><span class="sxs-lookup"><span data-stu-id="92157-163">DLL</span></span><br/>     | <dl> <span data-ttu-id="92157-164"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92157-164"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="92157-165">IID</span><span class="sxs-lookup"><span data-stu-id="92157-165">IID</span></span><br/>     | <span data-ttu-id="92157-166">IID \_ IDatabase est défini en tant que 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="92157-166">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="92157-167">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="92157-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92157-168">Exemples de scripts Windows Installer</span><span class="sxs-lookup"><span data-stu-id="92157-168">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




