---
description: 'En savoir plus sur : fonction JetCreateTableColumnIndex3'
title: JetCreateTableColumnIndex3 fonction)
TOCTitle: JetCreateTableColumnIndex3 Function
ms:assetid: c1a1b091-b4a6-4cdc-a0ea-af21c1462449
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294079(v=EXCHG.10)
ms:contentKeyID: 32765694
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateTableColumnIndex3
- JetCreateTableColumnIndex3W
- JetCreateTableColumnIndex3A
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bf1d6aed3178f5593826097f8c5d6b01bd8c72d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106543750"
---
# <a name="jetcreatetablecolumnindex3-function"></a><span data-ttu-id="5e3cb-103">JetCreateTableColumnIndex3 fonction)</span><span class="sxs-lookup"><span data-stu-id="5e3cb-103">JetCreateTableColumnIndex3 Function</span></span>


<span data-ttu-id="5e3cb-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="5e3cb-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreatetablecolumnindex3-function"></a><span data-ttu-id="5e3cb-105">JetCreateTableColumnIndex3 fonction)</span><span class="sxs-lookup"><span data-stu-id="5e3cb-105">JetCreateTableColumnIndex3 Function</span></span>

<span data-ttu-id="5e3cb-106">La fonction **JetCreateTableColumnIndex3** crée une table dans une base de données ESE avec un ensemble initial d’index et un ensemble initial de colonnes à partir d’un tableau de structures [JET_TABLECREATE3](./jet-tablecreate3-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="5e3cb-106">The **JetCreateTableColumnIndex3** function creates a table in an ESE database with an initial set of indexes and an initial set of columns from an array of [JET_TABLECREATE3](./jet-tablecreate3-structure.md) structures.</span></span> <span data-ttu-id="5e3cb-107">La structure [JET_TABLECREATE3](./jet-tablecreate3-structure.md) permet de spécifier une fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-107">The [JET_TABLECREATE3](./jet-tablecreate3-structure.md) structure allows a callback function to be specified.</span></span>

<span data-ttu-id="5e3cb-108">**Windows 7 :** **JetCreateTableColumnIndex3** est introduit dans le système d’exploitation Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-108">**Windows 7:** **JetCreateTableColumnIndex3** is introduced in the Windows 7 operating system.</span></span>

```cpp
    JET_ERR JET_API JetCreateTableColumnIndex3(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in_out      JET_TABLECREATE3* ptablecreate
    );
```

### <a name="parameters"></a><span data-ttu-id="5e3cb-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5e3cb-109">Parameters</span></span>

<span data-ttu-id="5e3cb-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="5e3cb-110">*sesid*</span></span>

<span data-ttu-id="5e3cb-111">Contexte de la session de base de données à utiliser pour l’appel d’API.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-111">The database session context to use for the API call.</span></span>

<span data-ttu-id="5e3cb-112">*dbid*</span><span class="sxs-lookup"><span data-stu-id="5e3cb-112">*dbid*</span></span>

<span data-ttu-id="5e3cb-113">Identificateur de base de données à utiliser pour l’appel d’API.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-113">The database identifier to use for the API call.</span></span>

<span data-ttu-id="5e3cb-114">*ptablecreate*</span><span class="sxs-lookup"><span data-stu-id="5e3cb-114">*ptablecreate*</span></span>

<span data-ttu-id="5e3cb-115">Pointeur vers une structure [JET_TABLECREATE3](./jet-tablecreate3-structure.md) qui définit la table à créer.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-115">A pointer to a [JET_TABLECREATE3](./jet-tablecreate3-structure.md) structure that defines the table to be created.</span></span> <span data-ttu-id="5e3cb-116">Pour plus d’informations, consultez [JET_TABLECREATE3](./jet-tablecreate3-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="5e3cb-116">See [JET_TABLECREATE3](./jet-tablecreate3-structure.md) for more details.</span></span>

### <a name="return-value"></a><span data-ttu-id="5e3cb-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5e3cb-117">Return Value</span></span>

<span data-ttu-id="5e3cb-118">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-118">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="5e3cb-119">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="5e3cb-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5e3cb-120">Code de retour</span><span class="sxs-lookup"><span data-stu-id="5e3cb-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="5e3cb-121">Description</span><span class="sxs-lookup"><span data-stu-id="5e3cb-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5e3cb-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="5e3cb-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="5e3cb-123">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e3cb-124">JET_errCallbackNotResolved</span><span class="sxs-lookup"><span data-stu-id="5e3cb-124">JET_errCallbackNotResolved</span></span></p></td>
<td><p><span data-ttu-id="5e3cb-125">La fonction de rappel n’a pas pu être résolue.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-125">The callback function could not be resolved.</span></span> <span data-ttu-id="5e3cb-126">La DLL n’a peut-être pas été trouvée, ou la fonction dans la DLL n’a peut-être pas été trouvée.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-126">The DLL might not have been found, or the function in the DLL might not have been found.</span></span> <span data-ttu-id="5e3cb-127">Une fois la journalisation suffisante activée, le journal des événements fournit plus de détails.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-127">With sufficient logging enabled, the event log will provide more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e3cb-128">JET_errCannotIndex</span><span class="sxs-lookup"><span data-stu-id="5e3cb-128">JET_errCannotIndex</span></span></p></td>
<td><p><span data-ttu-id="5e3cb-129">Une tentative d’indexation sur une colonne de dépôt/mise à jour ou SLV (Notez que les colonnes SLV sont dépréciées) a été tentée.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-129">An attempt was made to index over an escrow-update or SLV column (note that SLV columns are deprecated).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e3cb-130">JET_errCannotNestDDL</span><span class="sxs-lookup"><span data-stu-id="5e3cb-130">JET_errCannotNestDDL</span></span></p></td>
<td><p><span data-ttu-id="5e3cb-131">Si ptablecreate- &gt; Grbit spécifie JET_bitTableCreateTemplateTable, mais ptablecreate- &gt; szTemplateTableName a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-131">If ptablecreate-&gt;grbit specifies JET_bitTableCreateTemplateTable, but ptablecreate-&gt;szTemplateTableName is set to NULL.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e3cb-132">JET_errColumnDuplicate</span><span class="sxs-lookup"><span data-stu-id="5e3cb-132">JET_errColumnDuplicate</span></span></p></td>
<td><p><span data-ttu-id="5e3cb-133">Une colonne existe déjà.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-133">A column already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e3cb-134">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="5e3cb-134">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="5e3cb-135">Une tentative d’indexation sur une colonne inexistante a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-135">An attempt was made to index over a non-existent column.</span></span> <span data-ttu-id="5e3cb-136">Toute tentative d’indexation conditionnelle sur une colonne inexistante peut également générer cette erreur.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-136">Attempting to conditionally index over a non-existent column can also produce this error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e3cb-137">JET_errColumnRedundant</span><span class="sxs-lookup"><span data-stu-id="5e3cb-137">JET_errColumnRedundant</span></span></p></td>
<td><p><span data-ttu-id="5e3cb-138">Une tentative d’ajout d’une colonne redondante a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-138">An attempt was made to add a redundant column.</span></span> <span data-ttu-id="5e3cb-139">Il ne doit y avoir qu’une seule colonne AutoIncrement et pas plus d’une colonne version par table.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-139">There should be no more than one autoincrement column, and no more than one version column per table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e3cb-140">JET_errDensityInvalid</span><span class="sxs-lookup"><span data-stu-id="5e3cb-140">JET_errDensityInvalid</span></span></p></td>
<td><p><span data-ttu-id="5e3cb-141">Cette erreur est retournée si le membre <strong>ulDensity</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> est défini sur un nombre inférieur à 20 ou supérieur à 100.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-141">This error will be returned if the <strong>ulDensity</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is set to a number less than 20 or more than 100.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e3cb-142">JET_errDDLNotInheritable</span><span class="sxs-lookup"><span data-stu-id="5e3cb-142">JET_errDDLNotInheritable</span></span></p></td>
<td><p><span data-ttu-id="5e3cb-143">Signifie que la table nommée dans le membre <strong>szTemplateTableName</strong> de la structure <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> n’a pas été marquée comme table de modèle (autrement dit, cette table n’avait pas de JET_bitTableCreateTemplateTable définie).</span><span class="sxs-lookup"><span data-stu-id="5e3cb-143">Signifies that the table named in the <strong>szTemplateTableName</strong> member of the <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> structure was not marked as a template table (that is, that table did not have JET_bitTableCreateTemplateTable set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e3cb-144">JET_errIndexDuplicate</span><span class="sxs-lookup"><span data-stu-id="5e3cb-144">JET_errIndexDuplicate</span></span></p></td>
<td><p><span data-ttu-id="5e3cb-145">Une tentative de définition de deux index identiques a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-145">An attempt to define two identical indexes was made.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e3cb-146">JET_errIndexHasPrimary</span><span class="sxs-lookup"><span data-stu-id="5e3cb-146">JET_errIndexHasPrimary</span></span></p></td>
<td><p><span data-ttu-id="5e3cb-147">Une tentative a été effectuée pour spécifier plusieurs index primaires pour une table.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-147">An attempt was made to specify more than one primary index for a table.</span></span> <span data-ttu-id="5e3cb-148">Une table doit avoir un seul index primaire.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-148">A table must have exactly one primary index.</span></span> <span data-ttu-id="5e3cb-149">Si aucun index primaire n’est spécifié, le moteur de base de données en crée un en toute transparence.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-149">If no primary index is specified, the database engine will transparently create one.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e3cb-150">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="5e3cb-150">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="5e3cb-151">Une définition d’index non valide a été spécifiée.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-151">An invalid index definition was specified.</span></span> <span data-ttu-id="5e3cb-152">Voici quelques-unes des raisons possibles de la réception de cette erreur :</span><span class="sxs-lookup"><span data-stu-id="5e3cb-152">The following are some of the possible reasons for receiving this error:</span></span></p>
<ul>
<li><p><span data-ttu-id="5e3cb-153">Un index principal est conditionnel (autrement dit, le membre <strong>Grbit</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> a JET_bitIndexPrimary jeu et le membre <strong>cConditionalColumn</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> est supérieur à zéro).</span><span class="sxs-lookup"><span data-stu-id="5e3cb-153">A primary index is conditional (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has JET_bitIndexPrimary set, and <strong>cConditionalColumn</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is greater than zero).</span></span></p></li>
<li><p><span data-ttu-id="5e3cb-154">Windows Server 2003 et versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-154">Windows Server 2003 and later versions of Windows.</span></span> <span data-ttu-id="5e3cb-155">La tentative de création d’un index de tuple avec des limites de tuple, mais sans passer le membre <strong>ptuplelimits</strong> dans la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> (autrement dit, le membre <strong>Grbit</strong> de la structure JET_INDEXCREATE2 a JET_bitIndexTupleLimits défini, mais le pointeur <strong>ptuplelimits</strong> a la valeur null).</span><span class="sxs-lookup"><span data-stu-id="5e3cb-155">Attempting to create a tuple index with tuple limits, but without passing the <strong>ptuplelimits</strong> member in the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure (that is, the <strong>grbit</strong> member of the JET_INDEXCREATE2 structure has JET_bitIndexTupleLimits set, but the <strong>ptuplelimits</strong> pointer is NULL).</span></span></p></li>
<li><p><span data-ttu-id="5e3cb-156">Passage d’une définition de clé non valide dans le membre <strong>szKey</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="5e3cb-156">Passing in an invalid key definition in the <strong>szKey</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure.</span></span> <span data-ttu-id="5e3cb-157">Pour plus d’informations sur les définitions valides, consultez <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="5e3cb-157">See <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> for a discussion of valid definitions.</span></span></p></li>
<li><p><span data-ttu-id="5e3cb-158">La définition du membre <strong>cbVarSegMac</strong> dans <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> est supérieure à JET_cbPrimaryKeyMost (pour un index principal) ou supérieure à JET_cbSecondaryKeyMost (pour un index secondaire).</span><span class="sxs-lookup"><span data-stu-id="5e3cb-158">Setting the <strong>cbVarSegMac</strong> member in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> to be greater than JET_cbPrimaryKeyMost (for a primary index) or greater than JET_cbSecondaryKeyMost (for a secondary index).</span></span></p></li>
<li><p><span data-ttu-id="5e3cb-159">Passage d’une combinaison non valide pour un index Unicode défini par l’utilisateur (un qui a le bit JET_bitIndexUnicode défini dans le membre <strong>Grbit</strong> de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>).</span><span class="sxs-lookup"><span data-stu-id="5e3cb-159">Passing an invalid combination for a user-defined Unicode index (one that has the JET_bitIndexUnicode bit set in the <strong>grbit</strong> member of <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>).</span></span> <span data-ttu-id="5e3cb-160">Certaines causes courantes incluent le membre <strong>pidxunicode</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> a la valeur null, ou le LCID spécifié dans la structure <strong>pidxunicode</strong> n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-160">Some common causes include the <strong>pidxunicode</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is NULL, or the LCID specified in the <strong>pidxunicode</strong> structure is invalid.</span></span></p></li>
<li><p><span data-ttu-id="5e3cb-161">Spécification d’une colonne à valeurs multiples pour un index primaire.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-161">Specifying a multi-valued column for a primary index.</span></span></p></li>
<li><p><span data-ttu-id="5e3cb-162">Tentative d’indexation d’un trop grand nombre de colonnes conditionnelles.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-162">Trying to index too many conditional columns.</span></span> <span data-ttu-id="5e3cb-163">Le membre <strong>cConditionalColumn</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ne doit pas être supérieur à JET_ccolKeyMost.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-163">The <strong>cConditionalColumn</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not be greater than JET_ccolKeyMost.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e3cb-164">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="5e3cb-164">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="5e3cb-165">Windows XP et versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-165">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="5e3cb-166">Une structure de <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> a été spécifiée et ses limites ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-166">A <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure was specified, and its limits are not supported.</span></span> <span data-ttu-id="5e3cb-167">Consultez la section Notes de la structure <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</span><span class="sxs-lookup"><span data-stu-id="5e3cb-167">See the remarks section of the <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e3cb-168">JET_errIndexTuplesNonUniqueOnly</span><span class="sxs-lookup"><span data-stu-id="5e3cb-168">JET_errIndexTuplesNonUniqueOnly</span></span></p></td>
<td><p><span data-ttu-id="5e3cb-169">Windows XP et versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-169">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="5e3cb-170">Un index de tuple ne peut pas être unique (autrement dit, le membre <em>Grbit</em> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ne doit pas avoir JET_bitIndexPrimary et JET_bitIndexUnique défini).</span><span class="sxs-lookup"><span data-stu-id="5e3cb-170">A tuple index cannot be unique (that is, the <em>grbit</em> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexUnique set).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e3cb-171">JET_errIndexTuplesOneColumnOnly</span><span class="sxs-lookup"><span data-stu-id="5e3cb-171">JET_errIndexTuplesOneColumnOnly</span></span></p></td>
<td><p><span data-ttu-id="5e3cb-172">Windows XP et versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-172">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="5e3cb-173">Un index de tuple ne peut être que sur une seule colonne (autrement dit, si le membre <strong>Grbit</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> a JET_bitIndexTuples jeu et que le membre <strong>szKey</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> spécifie plusieurs colonnes).</span><span class="sxs-lookup"><span data-stu-id="5e3cb-173">A tuple index can only be over a single column (that is, if the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has JET_bitIndexTuples set, and the <strong>szKey</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure specifies more than one column).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e3cb-174">JET_errIndexTuplesSecondaryIndexOnly</span><span class="sxs-lookup"><span data-stu-id="5e3cb-174">JET_errIndexTuplesSecondaryIndexOnly</span></span></p></td>
<td><p><span data-ttu-id="5e3cb-175">Windows XP et versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-175">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="5e3cb-176">Un index de tuple ne peut pas être un index primaire (autrement dit, le membre <strong>Grbit</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ne doit pas avoir JET_bitIndexPrimary et JET_bitIndexTuples défini).</span><span class="sxs-lookup"><span data-stu-id="5e3cb-176">A tuple index cannot be a primary index (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexTuples set).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e3cb-177">JET_errIndexTuplesTextColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="5e3cb-177">JET_errIndexTuplesTextColumnsOnly</span></span></p></td>
<td><p><span data-ttu-id="5e3cb-178">Windows XP et versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-178">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="5e3cb-179">Un index de tuple ne peut être que sur une colonne de type texte ou Unicode.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-179">A tuple index can only be on a text or Unicode column.</span></span> <span data-ttu-id="5e3cb-180">Toute tentative d’index d’autres colonnes (telles que des colonnes binaires) entraîne JET_errIndexTuplesTextColumnsOnly.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-180">An attempt to index other columns (such as binary columns) will result in JET_errIndexTuplesTextColumnsOnly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e3cb-181">JET_errIndexTuplesVarSegMacNotAllowed</span><span class="sxs-lookup"><span data-stu-id="5e3cb-181">JET_errIndexTuplesVarSegMacNotAllowed</span></span></p></td>
<td><p><span data-ttu-id="5e3cb-182">Windows XP et versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-182">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="5e3cb-183">Un index de tuple n’autorise pas la définition du membre <strong>cbVarSegMac</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="5e3cb-183">A tuple index does not allow the <strong>cbVarSegMac</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure to be set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e3cb-184">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="5e3cb-184">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="5e3cb-185">Une tentative de création d’un index sans informations de version a été effectuée dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-185">An attempt was made to create an index without version information while in a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e3cb-186">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="5e3cb-186">JET_errInvalidCodePage</span></span></p></td>
<td><p><span data-ttu-id="5e3cb-187">Le membre <strong>CP</strong> de la structure <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> n’a pas été défini sur une page de codes valide.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-187">The <strong>cp</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure was not set to a valid code page.</span></span> <span data-ttu-id="5e3cb-188">Les seules valeurs valides pour les colonnes de texte sont l’anglais (1252) et Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="5e3cb-188">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="5e3cb-189">La valeur 0 signifie que la valeur par défaut sera utilisée (anglais, 1252).</span><span class="sxs-lookup"><span data-stu-id="5e3cb-189">A value of 0 means the default will be used (English, 1252).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e3cb-190">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="5e3cb-190">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="5e3cb-191">Le membre <strong>coltyp</strong> de la structure <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> n’a pas été défini sur un type de colonne valide.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-191">The <strong>coltyp</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure was not set to a valid column type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e3cb-192">JET_errInvalidCreateIndex</span><span class="sxs-lookup"><span data-stu-id="5e3cb-192">JET_errInvalidCreateIndex</span></span></p></td>
<td><p><span data-ttu-id="5e3cb-193">Voici les raisons pour lesquelles cette erreur peut se produire :</span><span class="sxs-lookup"><span data-stu-id="5e3cb-193">The following are some reasons why this error may occur:</span></span></p>
<ul>
<li><p><span data-ttu-id="5e3cb-194">Le membre <strong>rgindexcreate</strong> de la structure <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-194">The <strong>rgindexcreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was set to NULL.</span></span></p></li>
<li><p><span data-ttu-id="5e3cb-195">Le membre <strong>rgcolumncreate</strong> de la structure <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-195">The <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was set to NULL.</span></span></p></li>
<li><p><span data-ttu-id="5e3cb-196">Le membre <strong>cbStruct</strong> d’une structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> n’a pas été défini sur une valeur valide.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-196">The <strong>cbStruct</strong> member of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure was not set to a valid value.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e3cb-197">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="5e3cb-197">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="5e3cb-198">Une combinaison de membres <strong>Grbit</strong> non valide a été spécifiée dans <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a>.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-198">An invalid combination of <strong>grbit</strong> members was specified in <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a>.</span></span></p>
<p><span data-ttu-id="5e3cb-199">La définition de l’index n’est pas valide, car le membre <strong>Grbit</strong> contient des valeurs incohérentes.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-199">The index definition is invalid because the <strong>grbit</strong> member contains inconsistent values.</span></span> <span data-ttu-id="5e3cb-200">Voici quelques raisons possibles :</span><span class="sxs-lookup"><span data-stu-id="5e3cb-200">The following are some possible reasons:</span></span></p>
<ul>
<li><p><span data-ttu-id="5e3cb-201">Un index primaire a un bit ignore spécifié (autrement dit, JET_bitIndexPrimary a été passé avec JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull ou JET_bitIndexIgnoreFirstNull).</span><span class="sxs-lookup"><span data-stu-id="5e3cb-201">A primary index had an ignore bit specified (that is, JET_bitIndexPrimary was passed with JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull, or JET_bitIndexIgnoreFirstNull).</span></span></p></li>
<li><p><span data-ttu-id="5e3cb-202">Un index vide n’ignore pas les membres NULL (autrement dit, le membre <strong>Grbit</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> n’a JET_bitIndexEmpty défini, mais n’a pas de JET_bitIndexIgnoreAnyNull défini).</span><span class="sxs-lookup"><span data-stu-id="5e3cb-202">An empty index does not ignore any NULL members (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has JET_bitIndexEmpty set, but does not have JET_bitIndexIgnoreAnyNull set).</span></span></p></li>
<li><p><span data-ttu-id="5e3cb-203">Passage d’une structure <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> avec un membre <strong>Grbit</strong> non valide.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-203">Passing in a <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> structure with an invalid <strong>grbit</strong> member.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e3cb-204">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="5e3cb-204">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="5e3cb-205">Un ID de paramètres régionaux (LCID) non valide a été transmis (par le biais du membre <strong>LCID</strong> de la structure <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> qui est référencée par le membre <strong>pidxunicode</strong> dans la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ou par le champ <strong>LCID</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ).</span><span class="sxs-lookup"><span data-stu-id="5e3cb-205">An invalid Locale ID (LCID) was passed in (either through the <strong>lcid</strong> member of the <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> structure which is pointed to by the <strong>pidxunicode</strong> member in the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure, or through the <strong>lcid</strong> field of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e3cb-206">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="5e3cb-206">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="5e3cb-207">Un paramètre non valide a été spécifié.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-207">An invalid parameter was given.</span></span> <span data-ttu-id="5e3cb-208">Voici quelques raisons possibles :</span><span class="sxs-lookup"><span data-stu-id="5e3cb-208">The following are some possible reasons:</span></span></p>
<ul>
<li><p><span data-ttu-id="5e3cb-209">Le membre <strong>rgcolumncreate</strong> de la structure <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-209">The <strong>rgcolumncreate</strong> member of the <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> structure is NULL.</span></span></p></li>
<li><p><span data-ttu-id="5e3cb-210">Le membre <strong>cbStruct</strong> de l’une des structures <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> données dans le membre <strong>rgcolumncreate</strong> de la structure <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> n’a pas la valeur sizeof (JET_COLUMNCREATE).</span><span class="sxs-lookup"><span data-stu-id="5e3cb-210">The <strong>cbStruct</strong> member of one of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structures given in the <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was not set to sizeof( JET_COLUMNCREATE ).</span></span></p></li>
<li><p><span data-ttu-id="5e3cb-211">Le membre <strong>cbKey</strong> d’une structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> a la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-211">The <strong>cbKey</strong> member of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is set to zero.</span></span></p></li>
<li><p><span data-ttu-id="5e3cb-212">Le membre <strong>cbStruct</strong> d’une structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> n’a pas la valeur sizeof (JET_INDEXCREATE2).</span><span class="sxs-lookup"><span data-stu-id="5e3cb-212">The <strong>cbStruct</strong> member of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is not set to sizeof( JET_INDEXCREATE2 ).</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e3cb-213">JET_errRecordTooBig</span><span class="sxs-lookup"><span data-stu-id="5e3cb-213">JET_errRecordTooBig</span></span></p></td>
<td><p><span data-ttu-id="5e3cb-214">L’enregistrement est trop volumineux.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-214">The record is too big.</span></span> <span data-ttu-id="5e3cb-215">La somme du membre <strong>cbMax</strong> de la structure <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> pour toutes les colonnes fixes ne doit pas dépasser une certaine valeur.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-215">The sum of the <strong>cbMax</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure for all fixed columns must not exceed a certain value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e3cb-216">JET_errTableDuplicate</span><span class="sxs-lookup"><span data-stu-id="5e3cb-216">JET_errTableDuplicate</span></span></p></td>
<td><p><span data-ttu-id="5e3cb-217">La table existe déjà.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-217">The table already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e3cb-218">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="5e3cb-218">JET_errTooManyColumns</span></span></p></td>
<td><p><span data-ttu-id="5e3cb-219">Une tentative d’ajout d’un trop grand nombre de colonnes à la table a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-219">An attempt was made to add too many columns to the table.</span></span> <span data-ttu-id="5e3cb-220">Une table ne peut pas comporter plus de JET_ccolFixedMost colonnes fixes, ni plus de JET_ccolVarMost colonnes de longueur variable, ni plus de JET_ccolTaggedMost colonnes avec balises.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-220">A table can have no more than JET_ccolFixedMost fixed columns, no more than JET_ccolVarMost variable-length columns, and no more than JET_ccolTaggedMost tagged columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e3cb-221">JET_errUnicodeTranslationFail</span><span class="sxs-lookup"><span data-stu-id="5e3cb-221">JET_errUnicodeTranslationFail</span></span></p></td>
<td><p><span data-ttu-id="5e3cb-222">Une erreur s’est produite lors de la normalisation d’une colonne Unicode.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-222">An error occurred attempting to normalize a Unicode column.</span></span> <span data-ttu-id="5e3cb-223">Cela peut être dû à un manque de ressources système.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-223">This can be caused by running out of system resources.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e3cb-224">JET_errSpaceHintsInvalid</span><span class="sxs-lookup"><span data-stu-id="5e3cb-224">JET_errSpaceHintsInvalid</span></span></p></td>
<td><p><span data-ttu-id="5e3cb-225">Un élément de la structure d’indicateurs d’espace JET n’est pas correct ou n’est pas exploitable.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-225">An element of the JET space hints structure was not correct or actionable.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="5e3cb-226">Notes</span><span class="sxs-lookup"><span data-stu-id="5e3cb-226">Remarks</span></span>

<span data-ttu-id="5e3cb-227">Le nom **JetCreateTableColumnIndex3** provient de l’ordre de création des objets : il crée d’abord une table, des colonnes, puis enfin des index.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-227">The name **JetCreateTableColumnIndex3** comes from the order of creation of the objects: It first creates a table, columns, and then finally indexes.</span></span> <span data-ttu-id="5e3cb-228">**JetCreateTableColumnIndex3** crée une table avec un ensemble initial de colonnes et d’index.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-228">**JetCreateTableColumnIndex3** creates a table with an initial set of columns and indexes.</span></span> <span data-ttu-id="5e3cb-229">Des colonnes et des index supplémentaires peuvent être ajoutés et supprimés dynamiquement avec [JetAddColumn](./jetaddcolumn-function.md), [JetDeleteColumn](./jetdeletecolumn-function.md), [JetDeleteColumn2](./jetdeletecolumn2-function.md), [JetCreateIndex](./jetcreateindex-function.md), [JetCreateIndex2](./jetcreateindex2-function.md), [JetCreateIndex3](./jetcreateindex3-function.md)et [JetDeleteIndex](./jetdeleteindex-function.md).</span><span class="sxs-lookup"><span data-stu-id="5e3cb-229">Additional columns and indexes can be added and removed dynamically with [JetAddColumn](./jetaddcolumn-function.md), [JetDeleteColumn](./jetdeletecolumn-function.md), [JetDeleteColumn2](./jetdeletecolumn2-function.md), [JetCreateIndex](./jetcreateindex-function.md), [JetCreateIndex2](./jetcreateindex2-function.md), [JetCreateIndex3](./jetcreateindex3-function.md), and [JetDeleteIndex](./jetdeleteindex-function.md).</span></span>

<span data-ttu-id="5e3cb-230">Comme [JetOpenTable](./jetopentable-function.md), lorsque l’application est effectuée à l’aide de l' *TableID* retourné, elle doit généralement être fermée avec [JetCloseTable](./jetclosetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="5e3cb-230">Like [JetOpenTable](./jetopentable-function.md), when the application is done using the returned *tableid*, it should usually be closed with [JetCloseTable](./jetclosetable-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="5e3cb-231">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5e3cb-231">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5e3cb-232"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="5e3cb-232"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="5e3cb-233">Nécessite Windows Vista ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-233">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e3cb-234"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="5e3cb-234"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="5e3cb-235">Requiert Windows Server 2008 ou Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-235">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e3cb-236"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="5e3cb-236"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="5e3cb-237">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-237">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e3cb-238"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="5e3cb-238"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="5e3cb-239">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-239">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e3cb-240"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="5e3cb-240"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="5e3cb-241">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="5e3cb-241">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e3cb-242"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="5e3cb-242"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="5e3cb-243">Implémenté en tant que <strong>JetCreateTableColumnIndex3W</strong> (Unicode) et <strong>JetCreateTableColumnIndex3A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="5e3cb-243">Implemented as <strong>JetCreateTableColumnIndex3W</strong> (Unicode) and <strong>JetCreateTableColumnIndex3A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="5e3cb-244">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5e3cb-244">See Also</span></span>

[<span data-ttu-id="5e3cb-245">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="5e3cb-245">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="5e3cb-246">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="5e3cb-246">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="5e3cb-247">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="5e3cb-247">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="5e3cb-248">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="5e3cb-248">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="5e3cb-249">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="5e3cb-249">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="5e3cb-250">JET_INDEXCREATE2</span><span class="sxs-lookup"><span data-stu-id="5e3cb-250">JET_INDEXCREATE2</span></span>](./jet-indexcreate2-structure.md)  
[<span data-ttu-id="5e3cb-251">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="5e3cb-251">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="5e3cb-252">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="5e3cb-252">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="5e3cb-253">JET_TABLECREATE2</span><span class="sxs-lookup"><span data-stu-id="5e3cb-253">JET_TABLECREATE2</span></span>](./jet-tablecreate2-structure.md)  
[<span data-ttu-id="5e3cb-254">JET_TABLECREATE3</span><span class="sxs-lookup"><span data-stu-id="5e3cb-254">JET_TABLECREATE3</span></span>](./jet-tablecreate3-structure.md)  
[<span data-ttu-id="5e3cb-255">JET_TUPLELIMITS</span><span class="sxs-lookup"><span data-stu-id="5e3cb-255">JET_TUPLELIMITS</span></span>](./jet-tuplelimits-structure.md)  
[<span data-ttu-id="5e3cb-256">JetAddColumn</span><span class="sxs-lookup"><span data-stu-id="5e3cb-256">JetAddColumn</span></span>](./jetaddcolumn-function.md)  
[<span data-ttu-id="5e3cb-257">JetCreateIndex</span><span class="sxs-lookup"><span data-stu-id="5e3cb-257">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="5e3cb-258">JetCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="5e3cb-258">JetCreateIndex2</span></span>](./jetcreateindex2-function.md)  
[<span data-ttu-id="5e3cb-259">JetCreateIndex3</span><span class="sxs-lookup"><span data-stu-id="5e3cb-259">JetCreateIndex3</span></span>](./jetcreateindex3-function.md)  
[<span data-ttu-id="5e3cb-260">JetCreateTable</span><span class="sxs-lookup"><span data-stu-id="5e3cb-260">JetCreateTable</span></span>](./jetcreatetable-function.md)  
[<span data-ttu-id="5e3cb-261">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="5e3cb-261">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="5e3cb-262">JetDeleteColumn</span><span class="sxs-lookup"><span data-stu-id="5e3cb-262">JetDeleteColumn</span></span>](./jetdeletecolumn-function.md)  
[<span data-ttu-id="5e3cb-263">JetDeleteColumn2</span><span class="sxs-lookup"><span data-stu-id="5e3cb-263">JetDeleteColumn2</span></span>](./jetdeletecolumn2-function.md)
