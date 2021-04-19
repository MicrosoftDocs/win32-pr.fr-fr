---
description: 'En savoir plus sur : fonction JetCreateTableColumnIndex4W'
title: JetCreateTableColumnIndex4W fonction)
TOCTitle: JetCreateTableColumnIndex4W Function
ms:assetid: 5a74b397-dfb4-4a1d-807b-284329239bc3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835042(v=EXCHG.10)
ms:contentKeyID: 49894664
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetCreateTableColumnIndex4W
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 26ebdb8cf62123febe2d44b5a638c285c180062c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524716"
---
# <a name="jetcreatetablecolumnindex4w-function"></a><span data-ttu-id="3e94f-103">JetCreateTableColumnIndex4W fonction)</span><span class="sxs-lookup"><span data-stu-id="3e94f-103">JetCreateTableColumnIndex4W Function</span></span>


<span data-ttu-id="3e94f-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="3e94f-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="3e94f-105">La fonction **JetCreateTableColumnIndex4W** crée une table dans un moteur ESE (Extensible Storage Engine) (base de données avec un ensemble initial d’index et un ensemble initial de colonnes à partir d’un tableau de structures [JET_TABLECREATE3](./jet-tablecreate3-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="3e94f-105">The **JetCreateTableColumnIndex4W** function creates a table in an Extensible Storage Engine (ESE( database with an initial set of indexes and an initial set of columns from an array of [JET_TABLECREATE3](./jet-tablecreate3-structure.md) structures.</span></span> <span data-ttu-id="3e94f-106">La structure [JET_TABLECREATE3](./jet-tablecreate3-structure.md) permet de spécifier une fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="3e94f-106">The [JET_TABLECREATE3](./jet-tablecreate3-structure.md) structure allows a callback function to be specified.</span></span>

<span data-ttu-id="3e94f-107">La fonction **JetCreateTableColumnIndex4W** a été introduite dans le système d’exploitation Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3e94f-107">The **JetCreateTableColumnIndex4W** function was introduced in the Windows 8 operating system.</span></span>

``` c++
JET_ERR JET_API JetCreateTableColumnIndex4W(
  __in          JET_SESID sesid,
  __in          JET_DBID dbid,
  __in_out      JET_TABLECREATE3* ptablecreate
);
```

### <a name="parameters"></a><span data-ttu-id="3e94f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3e94f-108">Parameters</span></span>

<span data-ttu-id="3e94f-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="3e94f-109">*sesid*</span></span>

<span data-ttu-id="3e94f-110">Contexte de la session de base de données à utiliser pour l’appel d’API.</span><span class="sxs-lookup"><span data-stu-id="3e94f-110">The database session context to use for the API call.</span></span>

<span data-ttu-id="3e94f-111">*dbid*</span><span class="sxs-lookup"><span data-stu-id="3e94f-111">*dbid*</span></span>

<span data-ttu-id="3e94f-112">Identificateur de base de données à utiliser pour l’appel d’API.</span><span class="sxs-lookup"><span data-stu-id="3e94f-112">The database identifier to use for the API call.</span></span>

<span data-ttu-id="3e94f-113">*ptablecreate*</span><span class="sxs-lookup"><span data-stu-id="3e94f-113">*ptablecreate*</span></span>

<span data-ttu-id="3e94f-114">Pointeur vers une structure [JET_TABLECREATE3](./jet-tablecreate3-structure.md) qui définit la table à créer.</span><span class="sxs-lookup"><span data-stu-id="3e94f-114">A pointer to a [JET_TABLECREATE3](./jet-tablecreate3-structure.md) structure that defines the table to be created.</span></span> <span data-ttu-id="3e94f-115">Pour plus d’informations, consultez [JET_TABLECREATE3](./jet-tablecreate3-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="3e94f-115">See [JET_TABLECREATE3](./jet-tablecreate3-structure.md) for more details.</span></span>

### <a name="return-value"></a><span data-ttu-id="3e94f-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3e94f-116">Return value</span></span>

<span data-ttu-id="3e94f-117">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour énumérés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="3e94f-117">This function returns the [JET_ERR](./jet-err.md) datatype with one of the return codes listed in the following table.</span></span> <span data-ttu-id="3e94f-118">Pour plus d’informations sur les erreurs ESE (Extensible Storage enginge) possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="3e94f-118">For more information about the possible Extensible Storage Enginge (ESE) errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3e94f-119">Code de retour</span><span class="sxs-lookup"><span data-stu-id="3e94f-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="3e94f-120">Description</span><span class="sxs-lookup"><span data-stu-id="3e94f-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3e94f-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="3e94f-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="3e94f-122">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="3e94f-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3e94f-123">JET_errCallbackNotResolved</span><span class="sxs-lookup"><span data-stu-id="3e94f-123">JET_errCallbackNotResolved</span></span></p></td>
<td><p><span data-ttu-id="3e94f-124">La fonction de rappel n’a pas pu être résolue.</span><span class="sxs-lookup"><span data-stu-id="3e94f-124">The callback function could not be resolved.</span></span> <span data-ttu-id="3e94f-125">La DLL n’a peut-être pas été trouvée, ou la fonction dans la DLL n’a peut-être pas été trouvée.</span><span class="sxs-lookup"><span data-stu-id="3e94f-125">The DLL might not have been found, or the function in the DLL might not have been found.</span></span> <span data-ttu-id="3e94f-126">Une fois la journalisation suffisante activée, le journal des événements fournit plus de détails.</span><span class="sxs-lookup"><span data-stu-id="3e94f-126">With sufficient logging enabled, the event log will provide more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3e94f-127">JET_errCannotIndex</span><span class="sxs-lookup"><span data-stu-id="3e94f-127">JET_errCannotIndex</span></span></p></td>
<td><p><span data-ttu-id="3e94f-128">Une tentative d’indexation sur une colonne de dépôt/mise à jour ou SLV (Notez que les colonnes SLV sont dépréciées) a été tentée.</span><span class="sxs-lookup"><span data-stu-id="3e94f-128">An attempt was made to index over an escrow-update or SLV column (note that SLV columns are deprecated).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3e94f-129">JET_errCannotNestDDL</span><span class="sxs-lookup"><span data-stu-id="3e94f-129">JET_errCannotNestDDL</span></span></p></td>
<td><p><span data-ttu-id="3e94f-130">Retournée si le paramètre <em>ptablecreate- &gt; Grbit</em> spécifie la valeur JET_bitTableCreateTemplateTable, mais que le paramètre <em>ptablecreate- &gt; szTemplateTableName</em> est défini sur null.</span><span class="sxs-lookup"><span data-stu-id="3e94f-130">Returned if the <em>ptablecreate-&gt;grbit</em> parameter specifies the JET_bitTableCreateTemplateTable value, but the <em>ptablecreate-&gt;szTemplateTableName</em> parameter is set to null.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3e94f-131">JET_errColumnDuplicate</span><span class="sxs-lookup"><span data-stu-id="3e94f-131">JET_errColumnDuplicate</span></span></p></td>
<td><p><span data-ttu-id="3e94f-132">Une colonne existe déjà.</span><span class="sxs-lookup"><span data-stu-id="3e94f-132">A column already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3e94f-133">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="3e94f-133">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="3e94f-134">Une tentative d’indexation sur une colonne inexistante a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="3e94f-134">An attempt was made to index over a nonexistent column.</span></span> <span data-ttu-id="3e94f-135">Une tentative d’index conditionnel sur une colonne inexistante peut également générer cette erreur.</span><span class="sxs-lookup"><span data-stu-id="3e94f-135">An attempt to conditionally index over a nonexistent column can also produce this error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3e94f-136">JET_errColumnRedundant</span><span class="sxs-lookup"><span data-stu-id="3e94f-136">JET_errColumnRedundant</span></span></p></td>
<td><p><span data-ttu-id="3e94f-137">Une tentative d’ajout d’une colonne redondante a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="3e94f-137">An attempt was made to add a redundant column.</span></span> <span data-ttu-id="3e94f-138">Il ne doit exister qu’une seule colonne AutoIncrement, et une seule colonne de version doit exister par table.</span><span class="sxs-lookup"><span data-stu-id="3e94f-138">No more than one autoincrement column should exist, and no more than one version column should exist per table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3e94f-139">JET_errDensityInvalid</span><span class="sxs-lookup"><span data-stu-id="3e94f-139">JET_errDensityInvalid</span></span></p></td>
<td><p><span data-ttu-id="3e94f-140">Cette erreur est retournée si le membre <strong>ulDensity</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> est défini sur un nombre inférieur à 20 ou supérieur à 100.</span><span class="sxs-lookup"><span data-stu-id="3e94f-140">This error will be returned if the <strong>ulDensity</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is set to a number less than 20 or more than 100.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3e94f-141">JET_errDDLNotInheritable</span><span class="sxs-lookup"><span data-stu-id="3e94f-141">JET_errDDLNotInheritable</span></span></p></td>
<td><p><span data-ttu-id="3e94f-142">Signifie que la table nommée dans le membre <strong>szTemplateTableName</strong> de la structure <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> n’a pas été marquée comme table de modèle (autrement dit, cette table n’a pas la valeur de paramètre JET_bitTableCreateTemplateTable définie).</span><span class="sxs-lookup"><span data-stu-id="3e94f-142">Signifies that the table named in the <strong>szTemplateTableName</strong> member of the <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> structure was not marked as a template table (that is, that table did not have the JET_bitTableCreateTemplateTable parameter value set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3e94f-143">JET_errIndexDuplicate</span><span class="sxs-lookup"><span data-stu-id="3e94f-143">JET_errIndexDuplicate</span></span></p></td>
<td><p><span data-ttu-id="3e94f-144">Une tentative de définition de deux index identiques a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="3e94f-144">An attempt to define two identical indexes was made.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3e94f-145">JET_errIndexHasPrimary</span><span class="sxs-lookup"><span data-stu-id="3e94f-145">JET_errIndexHasPrimary</span></span></p></td>
<td><p><span data-ttu-id="3e94f-146">Une tentative a été effectuée pour spécifier plusieurs index primaires pour une table.</span><span class="sxs-lookup"><span data-stu-id="3e94f-146">An attempt was made to specify more than one primary index for a table.</span></span> <span data-ttu-id="3e94f-147">Une table doit avoir un seul index primaire.</span><span class="sxs-lookup"><span data-stu-id="3e94f-147">A table must have exactly one primary index.</span></span> <span data-ttu-id="3e94f-148">Si aucun index primaire n’est spécifié, le moteur de base de données en crée un en toute transparence.</span><span class="sxs-lookup"><span data-stu-id="3e94f-148">If no primary index is specified, the database engine will transparently create one.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3e94f-149">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="3e94f-149">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="3e94f-150">Une définition d’index non valide a été spécifiée.</span><span class="sxs-lookup"><span data-stu-id="3e94f-150">An invalid index definition was specified.</span></span> <span data-ttu-id="3e94f-151">Voici quelques-unes des raisons possibles de cette erreur :</span><span class="sxs-lookup"><span data-stu-id="3e94f-151">The following are some of the possible reasons for this error:</span></span></p>
<ul>
<li><p><span data-ttu-id="3e94f-152">Un index principal est conditionnel (autrement dit, le membre <strong>Grbit</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> a la valeur JET_bitIndexPrimary définie et le membre <strong>cConditionalColumn</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> est supérieur à zéro).</span><span class="sxs-lookup"><span data-stu-id="3e94f-152">A primary index is conditional (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has the JET_bitIndexPrimary value set, and the <strong>cConditionalColumn</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is greater than zero).</span></span></p></li>
<li><p><span data-ttu-id="3e94f-153">S’applique aux versions du système d’exploitation Windows Server à partir de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="3e94f-153">Applies to versions of the Windows Server operating system starting with Windows Server 2003.</span></span> <span data-ttu-id="3e94f-154">Une tentative de création d’un index de tuple avec des limites de tuple, mais sans passer le membre <strong>ptuplelimits</strong> dans la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> (autrement dit, le membre <strong>Grbit</strong> de la structure <strong>JET_INDEXCREATE2</strong> a JET_bitIndexTupleLimits valeur définie, mais le pointeur <strong>ptuplelimits</strong> est null).</span><span class="sxs-lookup"><span data-stu-id="3e94f-154">An attempt to create a tuple index with tuple limits, but without passing the <strong>ptuplelimits</strong> member in the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure (that is, the <strong>grbit</strong> member of the <strong>JET_INDEXCREATE2</strong> structure has JET_bitIndexTupleLimits value set, but the <strong>ptuplelimits</strong> pointer is null).</span></span></p></li>
<li><p><span data-ttu-id="3e94f-155">Passage d’une définition de clé non valide dans le membre <strong>szKey</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="3e94f-155">Passing in an invalid key definition in the <strong>szKey</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure.</span></span> <span data-ttu-id="3e94f-156">Pour plus d’informations sur les définitions valides, consultez <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>.</span><span class="sxs-lookup"><span data-stu-id="3e94f-156">For information about valid definitions, see <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>.</span></span></p></li>
<li><p><span data-ttu-id="3e94f-157">La définition du membre <strong>cbVarSegMac</strong> dans <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> est supérieure à la valeur JET_cbPrimaryKeyMost (pour un index principal) ou supérieure à la valeur JET_cbSecondaryKeyMost (pour un index secondaire).</span><span class="sxs-lookup"><span data-stu-id="3e94f-157">Setting the <strong>cbVarSegMac</strong> member in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> to be greater than the JET_cbPrimaryKeyMost value (for a primary index) or greater than the JET_cbSecondaryKeyMost value (for a secondary index).</span></span></p></li>
<li><p><span data-ttu-id="3e94f-158">Passage d’une combinaison non valide pour un index Unicode défini par l’utilisateur (un qui a le bit de valeur JET_bitIndexUnicode défini dans le membre <strong>Grbit</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ).</span><span class="sxs-lookup"><span data-stu-id="3e94f-158">Passing an invalid combination for a user-defined Unicode index (one that has the JET_bitIndexUnicode value bit set in the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure).</span></span> <span data-ttu-id="3e94f-159">Certaines causes courantes incluent le membre <strong>pidxunicode</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> a la valeur null, ou le LCID spécifié dans la structure <strong>pidxunicode</strong> n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="3e94f-159">Some common causes include the <strong>pidxunicode</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is null, or the LCID specified in the <strong>pidxunicode</strong> structure is invalid.</span></span></p></li>
<li><p><span data-ttu-id="3e94f-160">Spécification d’une colonne à valeurs multiples pour un index primaire.</span><span class="sxs-lookup"><span data-stu-id="3e94f-160">Specifying a multivalued column for a primary index.</span></span></p></li>
<li><p><span data-ttu-id="3e94f-161">Tentative d’indexation d’un trop grand nombre de colonnes conditionnelles.</span><span class="sxs-lookup"><span data-stu-id="3e94f-161">Trying to index too many conditional columns.</span></span> <span data-ttu-id="3e94f-162">Le membre <strong>cConditionalColumn</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ne doit pas être supérieur à <strong>JET_ccolKeyMost</strong>.</span><span class="sxs-lookup"><span data-stu-id="3e94f-162">The <strong>cConditionalColumn</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not be greater than <strong>JET_ccolKeyMost</strong>.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3e94f-163">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="3e94f-163">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="3e94f-164">S’applique aux versions de Windows à partir de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3e94f-164">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="3e94f-165">Une structure de <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> a été spécifiée et ses limites ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="3e94f-165">A <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure was specified, and its limits are not supported.</span></span> <span data-ttu-id="3e94f-166">Pour plus d’informations, consultez la section Notes de la structure <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</span><span class="sxs-lookup"><span data-stu-id="3e94f-166">For more information, see the remarks section of the <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3e94f-167">JET_errIndexTuplesNonUniqueOnly</span><span class="sxs-lookup"><span data-stu-id="3e94f-167">JET_errIndexTuplesNonUniqueOnly</span></span></p></td>
<td><p><span data-ttu-id="3e94f-168">S’applique aux versions de Windows à partir de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3e94f-168">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="3e94f-169">Un index de tuple ne peut pas être unique (autrement dit, le membre <em>Grbit</em> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ne doit pas avoir les valeurs JET_bitIndexPrimary et JET_bitIndexUnique définies).</span><span class="sxs-lookup"><span data-stu-id="3e94f-169">A tuple index cannot be unique (that is, the <em>grbit</em> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexUnique values set).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3e94f-170">JET_errIndexTuplesOneColumnOnly</span><span class="sxs-lookup"><span data-stu-id="3e94f-170">JET_errIndexTuplesOneColumnOnly</span></span></p></td>
<td><p><span data-ttu-id="3e94f-171">S’applique aux versions de Windows à partir de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3e94f-171">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="3e94f-172">Un index de tuple ne peut être que sur une seule colonne (autrement dit, si le membre <strong>Grbit</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> a JET_bitIndexTuples valeur définie et que le membre <strong>szKey</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> spécifie plusieurs colonnes).</span><span class="sxs-lookup"><span data-stu-id="3e94f-172">A tuple index can only be over a single column (that is, if the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has JET_bitIndexTuples value set, and the <strong>szKey</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure specifies more than one column).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3e94f-173">JET_errIndexTuplesSecondaryIndexOnly</span><span class="sxs-lookup"><span data-stu-id="3e94f-173">JET_errIndexTuplesSecondaryIndexOnly</span></span></p></td>
<td><p><span data-ttu-id="3e94f-174">S’applique aux versions de Windows à partir de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3e94f-174">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="3e94f-175">Un index de tuple ne peut pas être un index primaire (autrement dit, le membre <strong>Grbit</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ne doit pas avoir JET_bitIndexPrimary et JET_bitIndexTuples défini).</span><span class="sxs-lookup"><span data-stu-id="3e94f-175">A tuple index cannot be a primary index (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexTuples set).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3e94f-176">JET_errIndexTuplesTextColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="3e94f-176">JET_errIndexTuplesTextColumnsOnly</span></span></p></td>
<td><p><span data-ttu-id="3e94f-177">S’applique aux versions de Windows à partir de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3e94f-177">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="3e94f-178">Un index de tuple ne peut être que sur une colonne de type texte ou Unicode.</span><span class="sxs-lookup"><span data-stu-id="3e94f-178">A tuple index can only be on a text or Unicode column.</span></span> <span data-ttu-id="3e94f-179">Si vous tentez d’indexer d’autres colonnes (telles que des colonnes binaires), vous obtiendrez un code de réponse JET_errIndexTuplesTextColumnsOnly.</span><span class="sxs-lookup"><span data-stu-id="3e94f-179">An attempt to index other columns (such as binary columns) will result in a JET_errIndexTuplesTextColumnsOnly response code.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3e94f-180">JET_errIndexTuplesVarSegMacNotAllowed</span><span class="sxs-lookup"><span data-stu-id="3e94f-180">JET_errIndexTuplesVarSegMacNotAllowed</span></span></p></td>
<td><p><span data-ttu-id="3e94f-181">S’applique aux versions de Windows à partir de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3e94f-181">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="3e94f-182">Un index de tuple n’autorise pas la définition du membre <strong>cbVarSegMac</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="3e94f-182">A tuple index does not allow the <strong>cbVarSegMac</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure to be set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3e94f-183">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="3e94f-183">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="3e94f-184">Une tentative de création d’un index sans informations de version a été effectuée dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="3e94f-184">An attempt was made to create an index without version information while in a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3e94f-185">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="3e94f-185">JET_errInvalidCodePage</span></span></p></td>
<td><p><span data-ttu-id="3e94f-186">Le membre <strong>CP</strong> de la structure <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> n’a pas été défini sur une page de codes valide.</span><span class="sxs-lookup"><span data-stu-id="3e94f-186">The <strong>cp</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure was not set to a valid code page.</span></span> <span data-ttu-id="3e94f-187">Les seules valeurs valides pour les colonnes de texte sont l’anglais (1252) et Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="3e94f-187">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="3e94f-188">La valeur 0 signifie que la valeur par défaut sera utilisée (anglais, 1252).</span><span class="sxs-lookup"><span data-stu-id="3e94f-188">A value of 0 means the default will be used (English, 1252).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3e94f-189">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="3e94f-189">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="3e94f-190">Le membre <strong>coltyp</strong> de la structure <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> n’a pas été défini sur un type de colonne valide.</span><span class="sxs-lookup"><span data-stu-id="3e94f-190">The <strong>coltyp</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure was not set to a valid column type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3e94f-191">JET_errInvalidCreateIndex</span><span class="sxs-lookup"><span data-stu-id="3e94f-191">JET_errInvalidCreateIndex</span></span></p></td>
<td><p><span data-ttu-id="3e94f-192">Voici les raisons pour lesquelles cette erreur peut se produire :</span><span class="sxs-lookup"><span data-stu-id="3e94f-192">The following are some reasons why this error may occur:</span></span></p>
<ul>
<li><p><span data-ttu-id="3e94f-193">Le membre <strong>rgindexcreate</strong> de la structure <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="3e94f-193">The <strong>rgindexcreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was set to null.</span></span></p></li>
<li><p><span data-ttu-id="3e94f-194">Le membre <strong>rgcolumncreate</strong> de la structure <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="3e94f-194">The <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was set to null.</span></span></p></li>
<li><p><span data-ttu-id="3e94f-195">Le membre <strong>cbStruct</strong> d’une structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> n’a pas été défini sur une valeur valide.</span><span class="sxs-lookup"><span data-stu-id="3e94f-195">The <strong>cbStruct</strong> member of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure was not set to a valid value.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3e94f-196">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="3e94f-196">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="3e94f-197">Une combinaison de membres <strong>Grbit</strong> non valide a été spécifiée dans la structure <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> .</span><span class="sxs-lookup"><span data-stu-id="3e94f-197">An invalid combination of <strong>grbit</strong> members was specified in the <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> structure.</span></span></p>
<p><span data-ttu-id="3e94f-198">La définition de l’index n’est pas valide, car le membre <strong>Grbit</strong> contient des valeurs incohérentes.</span><span class="sxs-lookup"><span data-stu-id="3e94f-198">The index definition is invalid because the <strong>grbit</strong> member contains inconsistent values.</span></span> <span data-ttu-id="3e94f-199">Voici quelques raisons possibles :</span><span class="sxs-lookup"><span data-stu-id="3e94f-199">The following are some possible reasons:</span></span></p>
<ul>
<li><p><span data-ttu-id="3e94f-200">Un index primaire a un bit ignore spécifié (autrement dit, JET_bitIndexPrimary valeur a été passée avec les valeurs JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull ou JET_bitIndexIgnoreFirstNull).</span><span class="sxs-lookup"><span data-stu-id="3e94f-200">A primary index had an ignore bit specified (that is, JET_bitIndexPrimary value was passed with the JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull, or JET_bitIndexIgnoreFirstNull values).</span></span></p></li>
<li><p><span data-ttu-id="3e94f-201">Un index vide n’ignore aucun membre null (autrement dit, le membre <strong>Grbit</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> a la valeur JET_bitIndexEmpty définie, mais aucune valeur JET_bitIndexIgnoreAnyNull n’est définie).</span><span class="sxs-lookup"><span data-stu-id="3e94f-201">An empty index does not ignore any null members (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has the JET_bitIndexEmpty value set, but does not have JET_bitIndexIgnoreAnyNull value set).</span></span></p></li>
<li><p><span data-ttu-id="3e94f-202">Passage d’une structure <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> avec un membre <strong>Grbit</strong> non valide.</span><span class="sxs-lookup"><span data-stu-id="3e94f-202">Passing in a <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> structure with an invalid <strong>grbit</strong> member.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3e94f-203">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="3e94f-203">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="3e94f-204">Un ID de paramètres régionaux (LCID) non valide a été passé (par le biais du membre <strong>LCID</strong> de la structure <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> dans laquelle le membre <strong>pidxunicode</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> pointe, ou via le champ <strong>LCID</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ).</span><span class="sxs-lookup"><span data-stu-id="3e94f-204">An invalid Locale ID (LCID) was passed in (either through the <strong>lcid</strong> member of the <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> structure that the <strong>pidxunicode</strong> member in the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure points to, or through the <strong>lcid</strong> field of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3e94f-205">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="3e94f-205">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="3e94f-206">Un paramètre non valide a été spécifié.</span><span class="sxs-lookup"><span data-stu-id="3e94f-206">An invalid parameter was given.</span></span> <span data-ttu-id="3e94f-207">Voici quelques raisons possibles :</span><span class="sxs-lookup"><span data-stu-id="3e94f-207">The following are some possible reasons:</span></span></p>
<ul>
<li><p><span data-ttu-id="3e94f-208">Le membre <strong>rgcolumncreate</strong> de la structure <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="3e94f-208">The <strong>rgcolumncreate</strong> member of the <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> structure is null.</span></span></p></li>
<li><p><span data-ttu-id="3e94f-209">Le membre <strong>cbStruct</strong> de l’une des structures <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> données dans le membre <strong>rgcolumncreate</strong> de la structure <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> n’a pas la valeur sizeof (JET_COLUMNCREATE).</span><span class="sxs-lookup"><span data-stu-id="3e94f-209">The <strong>cbStruct</strong> member of one of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structures given in the <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was not set to sizeof( JET_COLUMNCREATE ).</span></span></p></li>
<li><p><span data-ttu-id="3e94f-210">Le membre <strong>cbKey</strong> d’une structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> a la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="3e94f-210">The <strong>cbKey</strong> member of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is set to zero.</span></span></p></li>
<li><p><span data-ttu-id="3e94f-211">Le membre <strong>cbStruct</strong> d’une structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> n’a pas la valeur sizeof (JET_INDEXCREATE2).</span><span class="sxs-lookup"><span data-stu-id="3e94f-211">The <strong>cbStruct</strong> member of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is not set to sizeof( JET_INDEXCREATE2 ).</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3e94f-212">JET_errRecordTooBig</span><span class="sxs-lookup"><span data-stu-id="3e94f-212">JET_errRecordTooBig</span></span></p></td>
<td><p><span data-ttu-id="3e94f-213">L’enregistrement est trop volumineux.</span><span class="sxs-lookup"><span data-stu-id="3e94f-213">The record is too big.</span></span> <span data-ttu-id="3e94f-214">La somme du membre <strong>cbMax</strong> de la structure <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> pour toutes les colonnes fixes ne doit pas dépasser une certaine valeur.</span><span class="sxs-lookup"><span data-stu-id="3e94f-214">The sum of the <strong>cbMax</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure for all fixed columns must not exceed a certain value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3e94f-215">JET_errTableDuplicate</span><span class="sxs-lookup"><span data-stu-id="3e94f-215">JET_errTableDuplicate</span></span></p></td>
<td><p><span data-ttu-id="3e94f-216">La table existe déjà.</span><span class="sxs-lookup"><span data-stu-id="3e94f-216">The table already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3e94f-217">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="3e94f-217">JET_errTooManyColumns</span></span></p></td>
<td><p><span data-ttu-id="3e94f-218">Une tentative d’ajout d’un trop grand nombre de colonnes à la table a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="3e94f-218">An attempt was made to add too many columns to the table.</span></span> <span data-ttu-id="3e94f-219">Une table ne peut pas comporter plus de <strong>JET_ccolFixedMost</strong> colonnes fixes, ni plus de <strong>JET_ccolVarMost</strong> colonnes de longueur variable, ni plus de <strong>JET_ccolTaggedMost</strong> colonnes avec balises.</span><span class="sxs-lookup"><span data-stu-id="3e94f-219">A table can have no more than <strong>JET_ccolFixedMost</strong> fixed columns, no more than <strong>JET_ccolVarMost</strong> variable-length columns, and no more than <strong>JET_ccolTaggedMost</strong> tagged columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3e94f-220">JET_errUnicodeTranslationFail</span><span class="sxs-lookup"><span data-stu-id="3e94f-220">JET_errUnicodeTranslationFail</span></span></p></td>
<td><p><span data-ttu-id="3e94f-221">Une erreur s’est produite lors d’une tentative de normalisation d’une colonne Unicode.</span><span class="sxs-lookup"><span data-stu-id="3e94f-221">An error occurred when an attempt was made to normalize a Unicode column.</span></span> <span data-ttu-id="3e94f-222">Cela peut être dû à un manque de ressources système.</span><span class="sxs-lookup"><span data-stu-id="3e94f-222">This can be caused by running out of system resources.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3e94f-223">JET_errSpaceHintsInvalid</span><span class="sxs-lookup"><span data-stu-id="3e94f-223">JET_errSpaceHintsInvalid</span></span></p></td>
<td><p><span data-ttu-id="3e94f-224">Un élément de la structure d’indicateurs d’espace JET n’est pas correct ou n’est pas exploitable.</span><span class="sxs-lookup"><span data-stu-id="3e94f-224">An element of the JET space hints structure was not correct or actionable.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="3e94f-225">Notes</span><span class="sxs-lookup"><span data-stu-id="3e94f-225">Remarks</span></span>

<span data-ttu-id="3e94f-226">La fonction **JetCreateTableColumnIndex4W** crée une table avec un ensemble initial de colonnes et d’index.</span><span class="sxs-lookup"><span data-stu-id="3e94f-226">The **JetCreateTableColumnIndex4W** function creates a table with an initial set of columns and indexes.</span></span> <span data-ttu-id="3e94f-227">Des colonnes et des index supplémentaires peuvent être ajoutés et supprimés dynamiquement au moyen des fonctions [JetAddColumn](./jetaddcolumn-function.md), [JetDeleteColumn](./jetdeletecolumn-function.md), [JetDeleteColumn2](./jetdeletecolumn2-function.md), [JetCreateIndex](./jetcreateindex-function.md), [JetCreateIndex2](./jetcreateindex2-function.md), [JetCreateIndex3](./jetcreateindex3-function.md), [JetCreateIndex4W](./jetcreateindex4w-function.md)et [JetDeleteIndex](./jetdeleteindex-function.md) .</span><span class="sxs-lookup"><span data-stu-id="3e94f-227">Additional columns and indexes can be added and removed dynamically by means of the [JetAddColumn](./jetaddcolumn-function.md), [JetDeleteColumn](./jetdeletecolumn-function.md), [JetDeleteColumn2](./jetdeletecolumn2-function.md), [JetCreateIndex](./jetcreateindex-function.md), [JetCreateIndex2](./jetcreateindex2-function.md), [JetCreateIndex3](./jetcreateindex3-function.md), [JetCreateIndex4W](./jetcreateindex4w-function.md), and [JetDeleteIndex](./jetdeleteindex-function.md) functions.</span></span>

<span data-ttu-id="3e94f-228">Comme avec la fonction [JetOpenTable](./jetopentable-function.md) , lorsque l’application est effectuée à l’aide de l' *TableID* retourné, la fonction [JetCloseTable](./jetclosetable-function.md) doit fermer l’application.</span><span class="sxs-lookup"><span data-stu-id="3e94f-228">As with the [JetOpenTable](./jetopentable-function.md) function, when the application is done using the returned *tableid*, the [JetCloseTable](./jetclosetable-function.md) function should close the application.</span></span>

#### <a name="requirements"></a><span data-ttu-id="3e94f-229">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3e94f-229">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3e94f-230"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="3e94f-230"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="3e94f-231">Requiert Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3e94f-231">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3e94f-232"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="3e94f-232"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="3e94f-233">Requiert Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="3e94f-233">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3e94f-234"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="3e94f-234"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="3e94f-235">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="3e94f-235">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3e94f-236"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="3e94f-236"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="3e94f-237">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="3e94f-237">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3e94f-238"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="3e94f-238"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="3e94f-239">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="3e94f-239">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="3e94f-240">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e94f-240">See also</span></span>

[<span data-ttu-id="3e94f-241">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="3e94f-241">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="3e94f-242">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="3e94f-242">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="3e94f-243">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="3e94f-243">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="3e94f-244">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="3e94f-244">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="3e94f-245">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="3e94f-245">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="3e94f-246">JET_INDEXCREATE2</span><span class="sxs-lookup"><span data-stu-id="3e94f-246">JET_INDEXCREATE2</span></span>](./jet-indexcreate2-structure.md)  
[<span data-ttu-id="3e94f-247">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="3e94f-247">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="3e94f-248">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="3e94f-248">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="3e94f-249">JET_TABLECREATE2</span><span class="sxs-lookup"><span data-stu-id="3e94f-249">JET_TABLECREATE2</span></span>](./jet-tablecreate2-structure.md)  
[<span data-ttu-id="3e94f-250">JET_TABLECREATE3</span><span class="sxs-lookup"><span data-stu-id="3e94f-250">JET_TABLECREATE3</span></span>](./jet-tablecreate3-structure.md)  
[<span data-ttu-id="3e94f-251">JET_TUPLELIMITS</span><span class="sxs-lookup"><span data-stu-id="3e94f-251">JET_TUPLELIMITS</span></span>](./jet-tuplelimits-structure.md)  
[<span data-ttu-id="3e94f-252">JetAddColumn</span><span class="sxs-lookup"><span data-stu-id="3e94f-252">JetAddColumn</span></span>](./jetaddcolumn-function.md)  
[<span data-ttu-id="3e94f-253">JetCreateIndex</span><span class="sxs-lookup"><span data-stu-id="3e94f-253">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="3e94f-254">JetCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="3e94f-254">JetCreateIndex2</span></span>](./jetcreateindex2-function.md)  
[<span data-ttu-id="3e94f-255">JetCreateIndex3</span><span class="sxs-lookup"><span data-stu-id="3e94f-255">JetCreateIndex3</span></span>](./jetcreateindex3-function.md)  
[<span data-ttu-id="3e94f-256">JetCreateTable</span><span class="sxs-lookup"><span data-stu-id="3e94f-256">JetCreateTable</span></span>](./jetcreatetable-function.md)  
[<span data-ttu-id="3e94f-257">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="3e94f-257">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="3e94f-258">JetDeleteColumn</span><span class="sxs-lookup"><span data-stu-id="3e94f-258">JetDeleteColumn</span></span>](./jetdeletecolumn-function.md)  
[<span data-ttu-id="3e94f-259">JetDeleteColumn2</span><span class="sxs-lookup"><span data-stu-id="3e94f-259">JetDeleteColumn2</span></span>](./jetdeletecolumn2-function.md)
