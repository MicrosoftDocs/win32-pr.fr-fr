---
description: 'En savoir plus sur : fonction JetCreateTableColumnIndex2'
title: JetCreateTableColumnIndex2 fonction)
TOCTitle: JetCreateTableColumnIndex2 Function
ms:assetid: ad9caaf3-8cd2-453f-894d-8ac438c50b73
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294057(v=EXCHG.10)
ms:contentKeyID: 32765672
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateTableColumnIndex2W
- JetCreateTableColumnIndex2
- JetCreateTableColumnIndex2A
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 51a1789fe050ddd62990f6561ddeb01363d69f6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042833"
---
# <a name="jetcreatetablecolumnindex2-function"></a><span data-ttu-id="bc295-103">JetCreateTableColumnIndex2 fonction)</span><span class="sxs-lookup"><span data-stu-id="bc295-103">JetCreateTableColumnIndex2 Function</span></span>


<span data-ttu-id="bc295-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="bc295-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreatetablecolumnindex2-function"></a><span data-ttu-id="bc295-105">JetCreateTableColumnIndex2 fonction)</span><span class="sxs-lookup"><span data-stu-id="bc295-105">JetCreateTableColumnIndex2 Function</span></span>

<span data-ttu-id="bc295-106">La fonction **JetCreateTableColumnIndex2** crée une table dans une base de données ESE avec un ensemble initial d’index et un ensemble initial de colonnes à partir d’un tableau de structures [JET_TABLECREATE2](./jet-tablecreate2-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="bc295-106">The **JetCreateTableColumnIndex2** function creates a table in an ESE database with an initial set of indexes and an initial set of columns from an array of [JET_TABLECREATE2](./jet-tablecreate2-structure.md) structures.</span></span> <span data-ttu-id="bc295-107">La structure [JET_TABLECREATE2](./jet-tablecreate2-structure.md) permet de spécifier une fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="bc295-107">The [JET_TABLECREATE2](./jet-tablecreate2-structure.md) structure allows a callback function to be specified.</span></span>

<span data-ttu-id="bc295-108">**Windows XP : JetCreateTableColumnIndex2** est introduit dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bc295-108">**Windows XP:  JetCreateTableColumnIndex2** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetCreateTableColumnIndex2(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in_out      JET_TABLECREATE2* ptablecreate
    );
```

### <a name="parameters"></a><span data-ttu-id="bc295-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bc295-109">Parameters</span></span>

<span data-ttu-id="bc295-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="bc295-110">*sesid*</span></span>

<span data-ttu-id="bc295-111">Contexte de la session de base de données à utiliser pour l’appel d’API.</span><span class="sxs-lookup"><span data-stu-id="bc295-111">The database session context to use for the API call.</span></span>

<span data-ttu-id="bc295-112">*dbid*</span><span class="sxs-lookup"><span data-stu-id="bc295-112">*dbid*</span></span>

<span data-ttu-id="bc295-113">Identificateur de base de données à utiliser pour l’appel d’API.</span><span class="sxs-lookup"><span data-stu-id="bc295-113">The database identifier to use for the API call.</span></span>

<span data-ttu-id="bc295-114">*ptablecreate*</span><span class="sxs-lookup"><span data-stu-id="bc295-114">*ptablecreate*</span></span>

<span data-ttu-id="bc295-115">Pointeur vers une structure [JET_TABLECREATE2](./jet-tablecreate2-structure.md) qui définit la table à créer.</span><span class="sxs-lookup"><span data-stu-id="bc295-115">A pointer to a [JET_TABLECREATE2](./jet-tablecreate2-structure.md) structure which defines the table to be created.</span></span> <span data-ttu-id="bc295-116">Pour plus d’informations, consultez [JET_TABLECREATE2](./jet-tablecreate2-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="bc295-116">See [JET_TABLECREATE2](./jet-tablecreate2-structure.md) for more details.</span></span>

### <a name="return-value"></a><span data-ttu-id="bc295-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="bc295-117">Return Value</span></span>

<span data-ttu-id="bc295-118">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="bc295-118">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="bc295-119">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="bc295-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bc295-120">Code de retour</span><span class="sxs-lookup"><span data-stu-id="bc295-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="bc295-121">Description</span><span class="sxs-lookup"><span data-stu-id="bc295-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bc295-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="bc295-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="bc295-123">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="bc295-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc295-124">JET_errCallbackNotResolved</span><span class="sxs-lookup"><span data-stu-id="bc295-124">JET_errCallbackNotResolved</span></span></p></td>
<td><p><span data-ttu-id="bc295-125">La fonction de rappel n’a pas pu être résolue.</span><span class="sxs-lookup"><span data-stu-id="bc295-125">The callback function could not be resolved.</span></span> <span data-ttu-id="bc295-126">La DLL n’a peut-être pas été trouvée, ou la fonction dans la DLL n’a peut-être pas été trouvée.</span><span class="sxs-lookup"><span data-stu-id="bc295-126">The DLL might not have been found, or the function in the DLL might not have been found.</span></span> <span data-ttu-id="bc295-127">Une fois la journalisation suffisante activée, le journal des événements fournit plus de détails.</span><span class="sxs-lookup"><span data-stu-id="bc295-127">With sufficient logging enabled, the event log will provide more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc295-128">JET_errCannotIndex</span><span class="sxs-lookup"><span data-stu-id="bc295-128">JET_errCannotIndex</span></span></p></td>
<td><p><span data-ttu-id="bc295-129">Une tentative d’indexation sur une colonne de dépôt/mise à jour ou SLV (Notez que les colonnes SLV sont dépréciées) a été tentée.</span><span class="sxs-lookup"><span data-stu-id="bc295-129">An attempt was made to index over an escrow-update or SLV column (note that SLV columns are deprecated).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc295-130">JET_errCannotNestDDL</span><span class="sxs-lookup"><span data-stu-id="bc295-130">JET_errCannotNestDDL</span></span></p></td>
<td><p><span data-ttu-id="bc295-131">Si ptablecreate- &gt; Grbit spécifie JET_bitTableCreateTemplateTable, mais ptablecreate- &gt; szTemplateTableName a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="bc295-131">If ptablecreate-&gt;grbit specifies JET_bitTableCreateTemplateTable, but ptablecreate-&gt;szTemplateTableName is set to NULL.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc295-132">JET_errColumnDuplicate</span><span class="sxs-lookup"><span data-stu-id="bc295-132">JET_errColumnDuplicate</span></span></p></td>
<td><p><span data-ttu-id="bc295-133">Une colonne existe déjà.</span><span class="sxs-lookup"><span data-stu-id="bc295-133">A column already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc295-134">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="bc295-134">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="bc295-135">Une tentative d’indexation sur une colonne inexistante a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="bc295-135">An attempt was made to index over a non-existent column.</span></span> <span data-ttu-id="bc295-136">Toute tentative d’indexation conditionnelle sur une colonne inexistante peut également générer cette erreur.</span><span class="sxs-lookup"><span data-stu-id="bc295-136">Attempting to conditionally index over a non-existent column can also produce this error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc295-137">JET_errColumnRedundant</span><span class="sxs-lookup"><span data-stu-id="bc295-137">JET_errColumnRedundant</span></span></p></td>
<td><p><span data-ttu-id="bc295-138">Une tentative d’ajout d’une colonne redondante a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="bc295-138">An attempt was made to add a redundant column.</span></span> <span data-ttu-id="bc295-139">Il ne doit y avoir qu’une seule colonne AutoIncrement et pas plus d’une colonne version par table.</span><span class="sxs-lookup"><span data-stu-id="bc295-139">There should be no more than one autoincrement column, and no more than one version column per table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc295-140">JET_errDensityInvalid</span><span class="sxs-lookup"><span data-stu-id="bc295-140">JET_errDensityInvalid</span></span></p></td>
<td><p><span data-ttu-id="bc295-141">Cette erreur est retournée si le membre <strong>ulDensity</strong> de la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> est défini sur un nombre inférieur à 20 ou supérieur à 100.</span><span class="sxs-lookup"><span data-stu-id="bc295-141">This error will be returned if the <strong>ulDensity</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is set to a number less than 20 or more than 100.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc295-142">JET_errDDLNotInheritable</span><span class="sxs-lookup"><span data-stu-id="bc295-142">JET_errDDLNotInheritable</span></span></p></td>
<td><p><span data-ttu-id="bc295-143">Signifie que la table nommée dans le membre <strong>szTemplateTableName</strong> de la structure <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> n’était pas marquée comme table de modèle (autrement dit, cette table n’avait pas de JET_bitTableCreateTemplateTable définie).</span><span class="sxs-lookup"><span data-stu-id="bc295-143">Signifies that the table named in the <strong>szTemplateTableName</strong> member of the <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> structure was not a marked as a template table (that is, that table did not have JET_bitTableCreateTemplateTable set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc295-144">JET_errIndexDuplicate</span><span class="sxs-lookup"><span data-stu-id="bc295-144">JET_errIndexDuplicate</span></span></p></td>
<td><p><span data-ttu-id="bc295-145">Une tentative de définition de deux index identiques a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="bc295-145">An attempt to define two identical indexes was made.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc295-146">JET_errIndexHasPrimary</span><span class="sxs-lookup"><span data-stu-id="bc295-146">JET_errIndexHasPrimary</span></span></p></td>
<td><p><span data-ttu-id="bc295-147">Une tentative a été effectuée pour spécifier plusieurs index primaires pour une table.</span><span class="sxs-lookup"><span data-stu-id="bc295-147">An attempt was made to specify more than one primary index for a table.</span></span> <span data-ttu-id="bc295-148">Une table doit avoir un seul index primaire.</span><span class="sxs-lookup"><span data-stu-id="bc295-148">A table must have exactly one primary index.</span></span> <span data-ttu-id="bc295-149">Si aucun index primaire n’est spécifié, le moteur de base de données en crée un en toute transparence.</span><span class="sxs-lookup"><span data-stu-id="bc295-149">If no primary index is specified, the database engine will transparently create one.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc295-150">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="bc295-150">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="bc295-151">Une définition d’index non valide a été spécifiée.</span><span class="sxs-lookup"><span data-stu-id="bc295-151">An invalid index definition was specified.</span></span> <span data-ttu-id="bc295-152">Voici quelques-unes des raisons possibles de la réception de cette erreur :</span><span class="sxs-lookup"><span data-stu-id="bc295-152">Some of the possible reasons for receiving this error are:</span></span></p>
<ul>
<li><p><span data-ttu-id="bc295-153">Un index principal est conditionnel (autrement dit, le membre <strong>Grbit</strong> de la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> a JET_bitIndexPrimary jeu et le membre <strong>cConditionalColumn</strong> de la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> est supérieur à zéro).</span><span class="sxs-lookup"><span data-stu-id="bc295-153">A primary index is conditional (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexPrimary set, and <strong>cConditionalColumn</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is greater than zero).</span></span></p></li>
<li><p><span data-ttu-id="bc295-154">Windows Server 2003 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="bc295-154">Windows Server 2003 and later.</span></span> <span data-ttu-id="bc295-155">La tentative de création d’un index de tuple avec des limites de tuple, mais sans passer le membre <strong>ptuplelimits</strong> dans la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> (autrement dit, le membre <strong>Grbit</strong> de la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> a JET_bitIndexTupleLimits défini, mais le pointeur <strong>ptuplelimits</strong> a la valeur null).</span><span class="sxs-lookup"><span data-stu-id="bc295-155">Attempting to create a tuple index with tuple limits, but without passing the <strong>ptuplelimits</strong> member in the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexTupleLimits set, but the <strong>ptuplelimits</strong> pointer is NULL).</span></span></p></li>
<li><p><span data-ttu-id="bc295-156">Passage d’une définition de clé non valide dans le membre <strong>szKey</strong> de la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="bc295-156">Passing in an invalid key definition in the <strong>szKey</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure.</span></span> <span data-ttu-id="bc295-157">Pour plus d’informations sur les définitions valides, consultez <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="bc295-157">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for a discussion of valid definitions.</span></span></p></li>
<li><p><span data-ttu-id="bc295-158">La définition du membre <strong>cbVarSegMac</strong> dans <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> est supérieure à JET_cbPrimaryKeyMost (pour un index principal) ou supérieure à JET_cbSecondaryKeyMost (pour un index secondaire).</span><span class="sxs-lookup"><span data-stu-id="bc295-158">Setting the <strong>cbVarSegMac</strong> member in <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> to be greater than JET_cbPrimaryKeyMost (for a primary index) or greater than JET_cbSecondaryKeyMost (for a secondary index).</span></span></p></li>
<li><p><span data-ttu-id="bc295-159">Passage d’une combinaison non valide pour un index Unicode défini par l’utilisateur (un qui a le bit JET_bitIndexUnicode défini dans le membre <strong>Grbit</strong> de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>).</span><span class="sxs-lookup"><span data-stu-id="bc295-159">Passing an invalid combination for a user-defined Unicode index (one which has the JET_bitIndexUnicode bit set in the <strong>grbit</strong> member of <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>).</span></span> <span data-ttu-id="bc295-160">Certaines causes courantes incluent le membre <strong>pidxunicode</strong> de la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> a la valeur null, ou le LCID spécifié dans la structure <strong>pidxunicode</strong> n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="bc295-160">Some common causes include the <strong>pidxunicode</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is NULL, or the LCID specified in the <strong>pidxunicode</strong> structure is invalid.</span></span></p></li>
<li><p><span data-ttu-id="bc295-161">Spécification d’une colonne à valeurs multiples pour un index primaire.</span><span class="sxs-lookup"><span data-stu-id="bc295-161">Specifying a multi-valued column for a primary index.</span></span></p></li>
<li><p><span data-ttu-id="bc295-162">Tentative d’indexation d’un trop grand nombre de colonnes conditionnelles.</span><span class="sxs-lookup"><span data-stu-id="bc295-162">Trying to index too many conditional columns.</span></span> <span data-ttu-id="bc295-163">Le membre <strong>cConditionalColumn</strong> de la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ne doit pas être supérieur à JET_ccolKeyMost.</span><span class="sxs-lookup"><span data-stu-id="bc295-163">The <strong>cConditionalColumn</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure must not be greater than JET_ccolKeyMost.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc295-164">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="bc295-164">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="bc295-165">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="bc295-165">Windows XP and later.</span></span> <span data-ttu-id="bc295-166">Une structure de <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> a été spécifiée et ses limites ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="bc295-166">A <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure was specified, and its limits are not supported.</span></span> <span data-ttu-id="bc295-167">Consultez la section Notes de la structure <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</span><span class="sxs-lookup"><span data-stu-id="bc295-167">See the remarks section of the <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc295-168">JET_errIndexTuplesNonUniqueOnly</span><span class="sxs-lookup"><span data-stu-id="bc295-168">JET_errIndexTuplesNonUniqueOnly</span></span></p></td>
<td><p><span data-ttu-id="bc295-169">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="bc295-169">Windows XP and later.</span></span> <span data-ttu-id="bc295-170">Un index de tuple ne peut pas être unique (autrement dit, le membre <em>Grbit</em> de la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ne doit pas avoir JET_bitIndexPrimary et JET_bitIndexUnique défini).</span><span class="sxs-lookup"><span data-stu-id="bc295-170">A tuple index cannot be unique (that is, the <em>grbit</em> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexUnique set).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc295-171">JET_errIndexTuplesOneColumnOnly</span><span class="sxs-lookup"><span data-stu-id="bc295-171">JET_errIndexTuplesOneColumnOnly</span></span></p></td>
<td><p><span data-ttu-id="bc295-172">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="bc295-172">Windows XP and later.</span></span> <span data-ttu-id="bc295-173">Un index de tuple ne peut être que sur une seule colonne (autrement dit, si le membre <strong>Grbit</strong> de la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> a JET_bitIndexTuples jeu et que le membre <strong>szKey</strong> de la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> spécifie plusieurs colonnes).</span><span class="sxs-lookup"><span data-stu-id="bc295-173">A tuple index can only be over a single column (that is, if the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexTuples set, and the <strong>szKey</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure specifies more than one column).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc295-174">JET_errIndexTuplesSecondaryIndexOnly</span><span class="sxs-lookup"><span data-stu-id="bc295-174">JET_errIndexTuplesSecondaryIndexOnly</span></span></p></td>
<td><p><span data-ttu-id="bc295-175">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="bc295-175">Windows XP and later.</span></span> <span data-ttu-id="bc295-176">Un index de tuple ne peut pas être un index primaire (autrement dit, le membre <strong>Grbit</strong> de la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ne doit pas avoir JET_bitIndexPrimary et JET_bitIndexTuples défini).</span><span class="sxs-lookup"><span data-stu-id="bc295-176">A tuple index cannot be a primary index (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexTuples set).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc295-177">JET_errIndexTuplesTextColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="bc295-177">JET_errIndexTuplesTextColumnsOnly</span></span></p></td>
<td><p><span data-ttu-id="bc295-178">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="bc295-178">Windows XP and later.</span></span> <span data-ttu-id="bc295-179">Un index de tuple ne peut être que sur une colonne de type texte ou Unicode.</span><span class="sxs-lookup"><span data-stu-id="bc295-179">A tuple index can only be on a text or Unicode column.</span></span> <span data-ttu-id="bc295-180">Toute tentative d’index d’autres colonnes (telles que des colonnes binaires) entraîne JET_errIndexTuplesTextColumnsOnly.</span><span class="sxs-lookup"><span data-stu-id="bc295-180">An attempt to index other columns (such as binary columns) will result in JET_errIndexTuplesTextColumnsOnly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc295-181">JET_errIndexTuplesVarSegMacNotAllowed</span><span class="sxs-lookup"><span data-stu-id="bc295-181">JET_errIndexTuplesVarSegMacNotAllowed</span></span></p></td>
<td><p><span data-ttu-id="bc295-182">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="bc295-182">Windows XP and later.</span></span> <span data-ttu-id="bc295-183">Un index de tuple n’autorise pas la définition du membre <strong>cbVarSegMac</strong> de la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="bc295-183">A tuple index does not allow the <strong>cbVarSegMac</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure to be set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc295-184">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="bc295-184">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="bc295-185">Une tentative de création d’un index sans informations de version a été effectuée dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="bc295-185">An attempt was made to create an index without version information while in a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc295-186">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="bc295-186">JET_errInvalidCodePage</span></span></p></td>
<td><p><span data-ttu-id="bc295-187">Le membre <strong>CP</strong> de la structure <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> n’a pas été défini sur une page de codes valide.</span><span class="sxs-lookup"><span data-stu-id="bc295-187">The <strong>cp</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure was not set to a valid code page.</span></span> <span data-ttu-id="bc295-188">Les seules valeurs valides pour les colonnes de texte sont l’anglais (1252) et Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="bc295-188">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="bc295-189">La valeur 0 signifie que la valeur par défaut sera utilisée (anglais, 1252).</span><span class="sxs-lookup"><span data-stu-id="bc295-189">A value of 0 means the default will be used (English, 1252).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc295-190">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="bc295-190">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="bc295-191">Le membre <strong>coltyp</strong> de la structure <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> n’a pas été défini sur un type de colonne valide.</span><span class="sxs-lookup"><span data-stu-id="bc295-191">The <strong>coltyp</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure was not set to a valid column type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc295-192">JET_errInvalidCreateIndex</span><span class="sxs-lookup"><span data-stu-id="bc295-192">JET_errInvalidCreateIndex</span></span></p></td>
<td><p><span data-ttu-id="bc295-193">Cette erreur peut se produire pour les raisons suivantes :</span><span class="sxs-lookup"><span data-stu-id="bc295-193">Some of the reasons this error may occur:</span></span></p>
<ul>
<li><p><span data-ttu-id="bc295-194">Le membre <strong>rgindexcreate</strong> de la structure <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="bc295-194">The <strong>rgindexcreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was set to NULL.</span></span></p></li>
<li><p><span data-ttu-id="bc295-195">Le membre <strong>rgcolumncreate</strong> de la structure <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="bc295-195">The <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was set to NULL.</span></span></p></li>
<li><p><span data-ttu-id="bc295-196">Le membre <strong>cbStruct</strong> d’une structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> n’a pas été défini sur une valeur valide.</span><span class="sxs-lookup"><span data-stu-id="bc295-196">The <strong>cbStruct</strong> member of a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure was not set to a valid value.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc295-197">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="bc295-197">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="bc295-198">Une combinaison de membres <strong>Grbit</strong> non valide a été spécifiée dans <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> ou <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>.</span><span class="sxs-lookup"><span data-stu-id="bc295-198">An invalid combination of <strong>grbit</strong> members was specified in <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>.</span></span></p>
<p><span data-ttu-id="bc295-199">La définition de l’index n’est pas valide, car le membre <strong>Grbit</strong> contient des valeurs incohérentes.</span><span class="sxs-lookup"><span data-stu-id="bc295-199">The index definition is invalid because the <strong>grbit</strong> member contains inconsistent values.</span></span> <span data-ttu-id="bc295-200">Voici quelques raisons possibles :</span><span class="sxs-lookup"><span data-stu-id="bc295-200">Some possible reasons are:</span></span></p>
<ul>
<li><p><span data-ttu-id="bc295-201">Un index primaire a un bit ignore spécifié (autrement dit, JET_bitIndexPrimary a été passé avec JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull ou JET_bitIndexIgnoreFirstNull).</span><span class="sxs-lookup"><span data-stu-id="bc295-201">A primary index had an ignore bit specified (that is, JET_bitIndexPrimary was passed with JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull, or JET_bitIndexIgnoreFirstNull).</span></span></p></li>
<li><p><span data-ttu-id="bc295-202">Un index vide n’ignore pas les membres NULL (autrement dit, le membre <strong>Grbit</strong> de la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> n’a JET_bitIndexEmpty défini, mais n’a pas de JET_bitIndexIgnoreAnyNull défini).</span><span class="sxs-lookup"><span data-stu-id="bc295-202">An empty index does not ignore any NULL members (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexEmpty set, but does not have JET_bitIndexIgnoreAnyNull set).</span></span></p></li>
<li><p><span data-ttu-id="bc295-203">Passage d’une structure <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> avec un membre <strong>Grbit</strong> non valide.</span><span class="sxs-lookup"><span data-stu-id="bc295-203">Passing in a <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> structure with an invalid <strong>grbit</strong> member.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc295-204">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="bc295-204">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="bc295-205">Un ID de paramètres régionaux (LCID) non valide a été transmis (par le biais du membre <strong>LCID</strong> de la structure <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> qui est référencée par le membre <strong>pidxunicode</strong> dans la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ou par le champ <strong>LCID</strong> de la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ).</span><span class="sxs-lookup"><span data-stu-id="bc295-205">An invalid Locale ID (LCID) was passed in (either through the <strong>lcid</strong> member of the <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> structure which is pointed to by the <strong>pidxunicode</strong> member in the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure, or through the <strong>lcid</strong> field of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc295-206">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="bc295-206">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="bc295-207">Un paramètre non valide a été spécifié.</span><span class="sxs-lookup"><span data-stu-id="bc295-207">An invalid parameter was given.</span></span> <span data-ttu-id="bc295-208">Voici quelques raisons possibles :</span><span class="sxs-lookup"><span data-stu-id="bc295-208">Some possible reasons are:</span></span></p>
<ul>
<li><p><span data-ttu-id="bc295-209">Le membre <strong>rgcolumncreate</strong> de la structure <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="bc295-209">The <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure is NULL.</span></span></p></li>
<li><p><span data-ttu-id="bc295-210">Le membre <strong>cbStruct</strong> de l’une des structures <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> données dans le membre <strong>rgcolumncreate</strong> de la structure <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> n’a pas la valeur sizeof (JET_COLUMNCREATE).</span><span class="sxs-lookup"><span data-stu-id="bc295-210">The <strong>cbStruct</strong> member of one of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structures given in the <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was not set to sizeof( JET_COLUMNCREATE ).</span></span></p></li>
<li><p><span data-ttu-id="bc295-211">Le membre <strong>cbKey</strong> d’une structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> a la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="bc295-211">The <strong>cbKey</strong> member of a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is set to zero.</span></span></p></li>
<li><p><span data-ttu-id="bc295-212">Le membre <strong>cbStruct</strong> d’une structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> n’a pas la valeur sizeof (JET_INDEXCREATE).</span><span class="sxs-lookup"><span data-stu-id="bc295-212">The <strong>cbStruct</strong> member of a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is not set to sizeof( JET_INDEXCREATE ).</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc295-213">JET_errRecordTooBig</span><span class="sxs-lookup"><span data-stu-id="bc295-213">JET_errRecordTooBig</span></span></p></td>
<td><p><span data-ttu-id="bc295-214">L’enregistrement est trop volumineux.</span><span class="sxs-lookup"><span data-stu-id="bc295-214">The record is too big.</span></span> <span data-ttu-id="bc295-215">La somme du membre <strong>cbMax</strong> de la structure <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> pour toutes les colonnes fixes ne doit pas dépasser une certaine valeur.</span><span class="sxs-lookup"><span data-stu-id="bc295-215">The sum of the <strong>cbMax</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure for all fixed columns must not exceed a certain value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc295-216">JET_errTableDuplicate</span><span class="sxs-lookup"><span data-stu-id="bc295-216">JET_errTableDuplicate</span></span></p></td>
<td><p><span data-ttu-id="bc295-217">La table existe déjà.</span><span class="sxs-lookup"><span data-stu-id="bc295-217">The table already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc295-218">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="bc295-218">JET_errTooManyColumns</span></span></p></td>
<td><p><span data-ttu-id="bc295-219">Une tentative d’ajout d’un trop grand nombre de colonnes à la table a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="bc295-219">An attempt was made to add too many columns to the table.</span></span> <span data-ttu-id="bc295-220">Une table ne peut pas comporter plus de JET_ccolFixedMost colonnes fixes, ni plus de JET_ccolVarMost colonnes de longueur variable, ni plus de JET_ccolTaggedMost colonnes avec balises.</span><span class="sxs-lookup"><span data-stu-id="bc295-220">A table can have no more than JET_ccolFixedMost fixed columns, no more than JET_ccolVarMost variable-length columns, and no more than JET_ccolTaggedMost tagged columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc295-221">JET_errUnicodeTranslationFail</span><span class="sxs-lookup"><span data-stu-id="bc295-221">JET_errUnicodeTranslationFail</span></span></p></td>
<td><p><span data-ttu-id="bc295-222">Une erreur s’est produite lors de la normalisation d’une colonne Unicode.</span><span class="sxs-lookup"><span data-stu-id="bc295-222">An error occurred attempting to normalize a Unicode column.</span></span> <span data-ttu-id="bc295-223">Cela peut être dû à un manque de ressources système.</span><span class="sxs-lookup"><span data-stu-id="bc295-223">This can be caused by running out of system resources.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="bc295-224">Notes</span><span class="sxs-lookup"><span data-stu-id="bc295-224">Remarks</span></span>

<span data-ttu-id="bc295-225">Le nom **JetCreateTableColumnIndex2** provient de l’ordre de création des objets : il crée d’abord une table, des colonnes, puis enfin des index.</span><span class="sxs-lookup"><span data-stu-id="bc295-225">The name **JetCreateTableColumnIndex2** comes from the order of creation of the objects: It first creates a table, columns, and then finally indexes.</span></span> <span data-ttu-id="bc295-226">**JetCreateTableColumnIndex2** crée une table avec un ensemble initial de colonnes et d’index.</span><span class="sxs-lookup"><span data-stu-id="bc295-226">**JetCreateTableColumnIndex2** creates a table with an initial set of columns and indexes.</span></span> <span data-ttu-id="bc295-227">Des colonnes et des index supplémentaires peuvent être ajoutés et supprimés dynamiquement avec [JetAddColumn](./jetaddcolumn-function.md), [JetDeleteColumn](./jetdeletecolumn-function.md), [JetDeleteColumn2](./jetdeletecolumn2-function.md), [JetCreateIndex](./jetcreateindex-function.md), [JetCreateIndex2](./jetcreateindex2-function.md)et [JetDeleteIndex](./jetdeleteindex-function.md).</span><span class="sxs-lookup"><span data-stu-id="bc295-227">Additional columns and indexes can be added and removed dynamically with [JetAddColumn](./jetaddcolumn-function.md), [JetDeleteColumn](./jetdeletecolumn-function.md), [JetDeleteColumn2](./jetdeletecolumn2-function.md), [JetCreateIndex](./jetcreateindex-function.md), [JetCreateIndex2](./jetcreateindex2-function.md), and [JetDeleteIndex](./jetdeleteindex-function.md).</span></span>

<span data-ttu-id="bc295-228">Comme [JetOpenTable](./jetopentable-function.md), lorsque l’application est effectuée à l’aide de l' *TableID* retourné, elle doit généralement être fermée avec [JetCloseTable](./jetclosetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="bc295-228">Like [JetOpenTable](./jetopentable-function.md), when the application is done using the returned *tableid*, it should usually be closed with [JetCloseTable](./jetclosetable-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="bc295-229">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bc295-229">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bc295-230"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="bc295-230"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="bc295-231">Nécessite Windows Vista ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bc295-231">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc295-232"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="bc295-232"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="bc295-233">Requiert Windows Server 2008 ou Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="bc295-233">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc295-234"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="bc295-234"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="bc295-235">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="bc295-235">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc295-236"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="bc295-236"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="bc295-237">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="bc295-237">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc295-238"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="bc295-238"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="bc295-239">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="bc295-239">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc295-240"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="bc295-240"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="bc295-241">Implémenté en tant que <strong>JetCreateTableColumnIndex2W</strong> (Unicode) et <strong>JetCreateTableColumnIndex2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="bc295-241">Implemented as <strong>JetCreateTableColumnIndex2W</strong> (Unicode) and <strong>JetCreateTableColumnIndex2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="bc295-242">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bc295-242">See Also</span></span>

[<span data-ttu-id="bc295-243">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="bc295-243">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="bc295-244">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="bc295-244">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="bc295-245">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="bc295-245">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="bc295-246">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="bc295-246">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="bc295-247">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="bc295-247">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="bc295-248">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="bc295-248">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="bc295-249">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="bc295-249">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="bc295-250">JET_TABLECREATE</span><span class="sxs-lookup"><span data-stu-id="bc295-250">JET_TABLECREATE</span></span>](./jet-tablecreate-structure.md)  
[<span data-ttu-id="bc295-251">JET_TABLECREATE2</span><span class="sxs-lookup"><span data-stu-id="bc295-251">JET_TABLECREATE2</span></span>](./jet-tablecreate2-structure.md)  
[<span data-ttu-id="bc295-252">JET_TUPLELIMITS</span><span class="sxs-lookup"><span data-stu-id="bc295-252">JET_TUPLELIMITS</span></span>](./jet-tuplelimits-structure.md)  
[<span data-ttu-id="bc295-253">JetAddColumn</span><span class="sxs-lookup"><span data-stu-id="bc295-253">JetAddColumn</span></span>](./jetaddcolumn-function.md)  
[<span data-ttu-id="bc295-254">JetCreateIndex</span><span class="sxs-lookup"><span data-stu-id="bc295-254">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="bc295-255">JetCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="bc295-255">JetCreateIndex2</span></span>](./jetcreateindex2-function.md)  
[<span data-ttu-id="bc295-256">JetCreateTable</span><span class="sxs-lookup"><span data-stu-id="bc295-256">JetCreateTable</span></span>](./jetcreatetable-function.md)  
[<span data-ttu-id="bc295-257">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="bc295-257">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="bc295-258">JetDeleteColumn</span><span class="sxs-lookup"><span data-stu-id="bc295-258">JetDeleteColumn</span></span>](./jetdeletecolumn-function.md)  
[<span data-ttu-id="bc295-259">JetDeleteColumn2</span><span class="sxs-lookup"><span data-stu-id="bc295-259">JetDeleteColumn2</span></span>](./jetdeletecolumn2-function.md)
