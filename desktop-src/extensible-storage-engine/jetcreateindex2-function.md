---
description: 'En savoir plus sur : fonction JetCreateIndex2'
title: Fonction JetCreateIndex2
TOCTitle: JetCreateIndex2 Function
ms:assetid: 8810eaed-40cb-4561-aafc-9a9bbdb0d05b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269324(v=EXCHG.10)
ms:contentKeyID: 32765614
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateIndex2W
- JetCreateIndex2A
- JetCreateIndex2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 42c1eb8fa1bb7fa880cf7286a1ec472ddc7ba7fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545005"
---
# <a name="jetcreateindex2-function"></a><span data-ttu-id="1ea7d-103">Fonction JetCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="1ea7d-103">JetCreateIndex2 Function</span></span>


<span data-ttu-id="1ea7d-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="1ea7d-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreateindex2-function"></a><span data-ttu-id="1ea7d-105">Fonction JetCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="1ea7d-105">JetCreateIndex2 Function</span></span>

<span data-ttu-id="1ea7d-106">La fonction **JetCreateIndex2** crée des index sur les données d’une base de données ESE, qui peut être utilisée pour localiser rapidement des données spécifiques.</span><span class="sxs-lookup"><span data-stu-id="1ea7d-106">The **JetCreateIndex2** function creates indexes over data in an ESE database, which can be used to locate specific data quickly.</span></span>

```cpp
    JET_ERR JET_API JetCreateIndex2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_INDEXCREATE* pindexcreate,
      __in          unsigned long cIndexCreate
    );
```

### <a name="parameters"></a><span data-ttu-id="1ea7d-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1ea7d-107">Parameters</span></span>

<span data-ttu-id="1ea7d-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="1ea7d-108">*sesid*</span></span>

<span data-ttu-id="1ea7d-109">Contexte de la session de base de données à utiliser pour l’appel d’API.</span><span class="sxs-lookup"><span data-stu-id="1ea7d-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="1ea7d-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="1ea7d-110">*tableid*</span></span>

<span data-ttu-id="1ea7d-111">Table sur laquelle l’index sera créé.</span><span class="sxs-lookup"><span data-stu-id="1ea7d-111">The table on which the index will be created.</span></span>

<span data-ttu-id="1ea7d-112">*pindexcreate*</span><span class="sxs-lookup"><span data-stu-id="1ea7d-112">*pindexcreate*</span></span>

<span data-ttu-id="1ea7d-113">Tableau de structures [JET_INDEXCREATE](./jet-indexcreate-structure.md) , qui définissent chacune un index à créer.</span><span class="sxs-lookup"><span data-stu-id="1ea7d-113">An array of [JET_INDEXCREATE](./jet-indexcreate-structure.md) structures, each of which defines an index to be created.</span></span>

<span data-ttu-id="1ea7d-114">*cIndexCreate*</span><span class="sxs-lookup"><span data-stu-id="1ea7d-114">*cIndexCreate*</span></span>

<span data-ttu-id="1ea7d-115">Nombre d’éléments dans le tableau *pindexcreate* .</span><span class="sxs-lookup"><span data-stu-id="1ea7d-115">The number of elements in the *pindexcreate* array.</span></span>

### <a name="return-value"></a><span data-ttu-id="1ea7d-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1ea7d-116">Return Value</span></span>

<span data-ttu-id="1ea7d-117">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="1ea7d-117">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="1ea7d-118">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="1ea7d-118">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1ea7d-119">Code de retour</span><span class="sxs-lookup"><span data-stu-id="1ea7d-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="1ea7d-120">Description</span><span class="sxs-lookup"><span data-stu-id="1ea7d-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1ea7d-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="1ea7d-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="1ea7d-122">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="1ea7d-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ea7d-123">JET_errCannotIndex</span><span class="sxs-lookup"><span data-stu-id="1ea7d-123">JET_errCannotIndex</span></span></p></td>
<td><p><span data-ttu-id="1ea7d-124">Une tentative d’indexation sur une colonne de dépôt/mise à jour ou SLV (Notez que les colonnes SLV sont dépréciées) a été tentée.</span><span class="sxs-lookup"><span data-stu-id="1ea7d-124">An attempt was made to index over an escrow-update or SLV column (note that SLV columns are deprecated).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ea7d-125">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="1ea7d-125">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="1ea7d-126">Une tentative d’indexation sur une colonne inexistante a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="1ea7d-126">An attempt was made to index over a non-existent column.</span></span> <span data-ttu-id="1ea7d-127">Toute tentative d’indexation conditionnelle sur une colonne inexistante peut également générer cette erreur.</span><span class="sxs-lookup"><span data-stu-id="1ea7d-127">Attempting to conditionally index over a non-existent column can also produce this error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ea7d-128">JET_errDensityInvalid</span><span class="sxs-lookup"><span data-stu-id="1ea7d-128">JET_errDensityInvalid</span></span></p></td>
<td><p><span data-ttu-id="1ea7d-129">Cette erreur est retournée si le membre <strong>ulDensity</strong> de la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> est défini sur un nombre inférieur à 20 ou supérieur à 100.</span><span class="sxs-lookup"><span data-stu-id="1ea7d-129">This error will be returned if the <strong>ulDensity</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is set to a number less than 20 or more than 100.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ea7d-130">JET_errIndexDuplicate</span><span class="sxs-lookup"><span data-stu-id="1ea7d-130">JET_errIndexDuplicate</span></span></p></td>
<td><p><span data-ttu-id="1ea7d-131">Une tentative de définition de deux index identiques a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="1ea7d-131">An attempt to define two identical indexes was made.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ea7d-132">JET_errIndexHasPrimary</span><span class="sxs-lookup"><span data-stu-id="1ea7d-132">JET_errIndexHasPrimary</span></span></p></td>
<td><p><span data-ttu-id="1ea7d-133">Une tentative a été effectuée pour spécifier plusieurs index primaires pour une table.</span><span class="sxs-lookup"><span data-stu-id="1ea7d-133">An attempt was made to specify more than one primary index for a table.</span></span> <span data-ttu-id="1ea7d-134">Une table doit avoir un seul index primaire.</span><span class="sxs-lookup"><span data-stu-id="1ea7d-134">A table must have exactly one primary index.</span></span> <span data-ttu-id="1ea7d-135">Si aucun index primaire n’est spécifié, le moteur de base de données en crée un en toute transparence.</span><span class="sxs-lookup"><span data-stu-id="1ea7d-135">If no primary index is specified, the database engine will transparently create one.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ea7d-136">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="1ea7d-136">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="1ea7d-137">Une définition d’index non valide a été spécifiée.</span><span class="sxs-lookup"><span data-stu-id="1ea7d-137">An invalid index definition was specified.</span></span> <span data-ttu-id="1ea7d-138">Voici quelques-unes des raisons possibles de la réception de cette erreur :</span><span class="sxs-lookup"><span data-stu-id="1ea7d-138">Some of the possible reasons for receiving this error are:</span></span></p>
<ul>
<li><p><span data-ttu-id="1ea7d-139">Un index principal est conditionnel (le membre<strong>Grbit</strong> de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> a JET_bitIndexPrimary défini et le membre <strong>cConditionalColumn</strong> de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> est supérieur à zéro).</span><span class="sxs-lookup"><span data-stu-id="1ea7d-139">A primary index is conditional (<strong>grbit</strong> member of <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> has JET_bitIndexPrimary set, and the <strong>cConditionalColumn</strong> member of <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> is greater than zero).</span></span></p></li>
<li><p><span data-ttu-id="1ea7d-140">Windows Server 2003 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="1ea7d-140">Windows Server 2003 and later.</span></span> <span data-ttu-id="1ea7d-141">Tentative de création d’un index de tuple avec des limites de tuple, mais sans passer d’informations dans le membre <strong>ptuplelimits</strong> de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> (autrement dit, <em>Grbit</em> a JET_bitIndexTupleLimits défini, mais le pointeur <strong>ptuplelimits</strong> est null).</span><span class="sxs-lookup"><span data-stu-id="1ea7d-141">Attempting to create a tuple index with tuple limits, but without passing information in the <strong>ptuplelimits</strong> member in <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> (that is, <em>grbit</em> has JET_bitIndexTupleLimits set, but the <strong>ptuplelimits</strong> pointer is NULL).</span></span></p></li>
<li><p><span data-ttu-id="1ea7d-142">Passage d’une définition de clé non valide dans le membre <strong>szKey</strong> de la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="1ea7d-142">Passing in an invalid key definition in the <strong>szKey</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure.</span></span> <span data-ttu-id="1ea7d-143">Pour plus d’informations sur les définitions valides, consultez <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="1ea7d-143">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for a discussion of valid definitions.</span></span></p></li>
<li><p><span data-ttu-id="1ea7d-144">La définition du membre <strong>cbVarSegMac</strong> dans <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> est supérieure à JET_cbPrimaryKeyMost (pour un index principal) ou supérieure à JET_cbSecondaryKeyMost (pour un index secondaire).</span><span class="sxs-lookup"><span data-stu-id="1ea7d-144">Setting the <strong>cbVarSegMac</strong> member in <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> to be greater than JET_cbPrimaryKeyMost (for a primary index) or greater than JET_cbSecondaryKeyMost (for a secondary index).</span></span></p></li>
<li><p><span data-ttu-id="1ea7d-145">Passage d’une combinaison non valide pour un index Unicode défini par l’utilisateur (un qui a le bit JET_bitIndexUnicode défini dans le membre <strong>Grbit</strong> de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>).</span><span class="sxs-lookup"><span data-stu-id="1ea7d-145">Passing an invalid combination for a user-defined Unicode index (one which has the JET_bitIndexUnicode bit set in the <strong>grbit</strong> member of <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>).</span></span> <span data-ttu-id="1ea7d-146">Certaines causes courantes peuvent être que le champ pidxunicode de la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> a la valeur null ou que le LCID spécifié dans la structure pidxunicode n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="1ea7d-146">Some common causes may be that the pidxunicode field of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is NULL, or the LCID specified in the pidxunicode structure is invalid.</span></span></p></li>
<li><p><span data-ttu-id="1ea7d-147">Spécification d’une colonne à valeurs multiples pour un index primaire.</span><span class="sxs-lookup"><span data-stu-id="1ea7d-147">Specifying a multi-valued column for a primary index.</span></span></p></li>
<li><p><span data-ttu-id="1ea7d-148">Tentative d’indexation d’un trop grand nombre de colonnes conditionnelles.</span><span class="sxs-lookup"><span data-stu-id="1ea7d-148">Trying to index too many conditional columns.</span></span> <span data-ttu-id="1ea7d-149">Le membre <strong>cConditionalColumn</strong> de la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ne doit pas être supérieur à JET_ccolKeyMost.</span><span class="sxs-lookup"><span data-stu-id="1ea7d-149">The <strong>cConditionalColumn</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure must not be greater than JET_ccolKeyMost.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ea7d-150">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="1ea7d-150">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="1ea7d-151">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="1ea7d-151">Windows XP and later.</span></span> <span data-ttu-id="1ea7d-152">Une structure de <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> a été spécifiée et ses limites ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="1ea7d-152">A <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure was specified, and its limits are not supported.</span></span> <span data-ttu-id="1ea7d-153">Consultez la section Notes de la structure <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</span><span class="sxs-lookup"><span data-stu-id="1ea7d-153">See the remarks section of the <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ea7d-154">JET_errIndexTuplesNonUniqueOnly</span><span class="sxs-lookup"><span data-stu-id="1ea7d-154">JET_errIndexTuplesNonUniqueOnly</span></span></p></td>
<td><p><span data-ttu-id="1ea7d-155">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="1ea7d-155">Windows XP and later.</span></span> <span data-ttu-id="1ea7d-156">Un index de tuple ne peut pas être unique (<em>Grbit</em> ne doit pas avoir à la fois JET_bitIndexTuples et JET_bitIndexUnique défini).</span><span class="sxs-lookup"><span data-stu-id="1ea7d-156">A tuple index cannot be unique (<em>grbit</em> must not have both JET_bitIndexTuples and JET_bitIndexUnique set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ea7d-157">JET_errIndexTuplesOneColumnOnly</span><span class="sxs-lookup"><span data-stu-id="1ea7d-157">JET_errIndexTuplesOneColumnOnly</span></span></p></td>
<td><p><span data-ttu-id="1ea7d-158">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="1ea7d-158">Windows XP and later.</span></span> <span data-ttu-id="1ea7d-159">Un index de tuple ne peut être que sur une seule colonne (autrement dit, le membre <strong>Grbit</strong> de la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> a JET_bitIndexTuples jeu et le membre <strong>szKey</strong> de la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> spécifie plusieurs colonnes).</span><span class="sxs-lookup"><span data-stu-id="1ea7d-159">A tuple index can only be over a single column (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexTuples set, and the <strong>szKey</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure specifies more than one column).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ea7d-160">JET_errIndexTuplesSecondaryIndexOnly</span><span class="sxs-lookup"><span data-stu-id="1ea7d-160">JET_errIndexTuplesSecondaryIndexOnly</span></span></p></td>
<td><p><span data-ttu-id="1ea7d-161">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="1ea7d-161">Windows XP and later.</span></span> <span data-ttu-id="1ea7d-162">Un index de tuple ne peut pas être un index primaire (autrement dit, le membre <strong>Grbit</strong> de la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ne doit pas avoir JET_bitIndexPrimary et JET_bitIndexTuples défini).</span><span class="sxs-lookup"><span data-stu-id="1ea7d-162">A tuple index cannot be a primary index (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexTuples set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ea7d-163">JET_errIndexTuplesTextColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="1ea7d-163">JET_errIndexTuplesTextColumnsOnly</span></span></p></td>
<td><p><span data-ttu-id="1ea7d-164">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="1ea7d-164">Windows XP and later.</span></span> <span data-ttu-id="1ea7d-165">Un index de tuple ne peut être que sur une colonne de type texte ou Unicode.</span><span class="sxs-lookup"><span data-stu-id="1ea7d-165">A tuple index can only be on a text or Unicode column.</span></span> <span data-ttu-id="1ea7d-166">Si vous tentez d’indexer d’autres colonnes (par exemple, des colonnes binaires), JET_errIndexTuplesTextColumnsOnly.</span><span class="sxs-lookup"><span data-stu-id="1ea7d-166">An attempt to index other columns (for example, binary columns) will result in JET_errIndexTuplesTextColumnsOnly.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ea7d-167">JET_errIndexTuplesVarSegMacNotAllowed</span><span class="sxs-lookup"><span data-stu-id="1ea7d-167">JET_errIndexTuplesVarSegMacNotAllowed</span></span></p></td>
<td><p><span data-ttu-id="1ea7d-168">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="1ea7d-168">Windows XP and later.</span></span> <span data-ttu-id="1ea7d-169">Un index de tuple n’autorise pas la définition du membre <strong>cbVarSegMac</strong> de la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="1ea7d-169">A tuple index does not allow the <strong>cbVarSegMac</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure to be set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ea7d-170">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="1ea7d-170">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="1ea7d-171">Une tentative de création d’un index sans informations de version a été effectuée dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="1ea7d-171">An attempt was made to create an index without version information while in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ea7d-172">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="1ea7d-172">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="1ea7d-173">La définition de l’index n’est pas valide, car le membre <strong>Grbit</strong> de la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> contient des valeurs incohérentes.</span><span class="sxs-lookup"><span data-stu-id="1ea7d-173">The index definition is invalid because the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure contains inconsistent values.</span></span> <span data-ttu-id="1ea7d-174">Voici quelques raisons possibles :</span><span class="sxs-lookup"><span data-stu-id="1ea7d-174">Some possible reasons are:</span></span></p>
<ul>
<li><p><span data-ttu-id="1ea7d-175">Un index principal avait un bit ignore spécifié (JET_bitIndexPrimary a été passé avec l’un des JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull ou JET_bitIndexIgnoreFirstNull).</span><span class="sxs-lookup"><span data-stu-id="1ea7d-175">A primary index had an ignore bit specified (JET_bitIndexPrimary was passed with one of JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull, or JET_bitIndexIgnoreFirstNull).</span></span></p></li>
<li><p><span data-ttu-id="1ea7d-176">Un index vide n’ignore aucun champ NULL (autrement dit, le membre <strong>Grbit</strong> de la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> n’a JET_bitIndexEmpty défini, mais n’a pas de JET_bitIndexIgnoreAnyNull défini).</span><span class="sxs-lookup"><span data-stu-id="1ea7d-176">An empty index does not ignore any NULL fields (that is, <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexEmpty set, but does not have JET_bitIndexIgnoreAnyNull set).</span></span></p></li>
<li><p><span data-ttu-id="1ea7d-177">Passage d’une structure <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> avec un membre <strong>Grbit</strong> non valide.</span><span class="sxs-lookup"><span data-stu-id="1ea7d-177">Passing in a <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> structure with an invalid <strong>grbit</strong> member.</span></span> <span data-ttu-id="1ea7d-178">Consultez <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>.</span><span class="sxs-lookup"><span data-stu-id="1ea7d-178">See <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>.</span></span></p></li>
</ul>
<p><span data-ttu-id="1ea7d-179">Lors de la création de plusieurs index à la fois (autrement dit, si le paramètre <em>cIndexCreate</em> est supérieur à un), aucun des index ne peut contenir l’un des bits suivants :</span><span class="sxs-lookup"><span data-stu-id="1ea7d-179">When creating several indexes at once (that is, if the <em>cIndexCreate</em> parameter is greater than one), none of the indexes may contain any of the following bits:</span></span></p>
<ul>
<li><p><span data-ttu-id="1ea7d-180">JET_bitIndexPrimary</span><span class="sxs-lookup"><span data-stu-id="1ea7d-180">JET_bitIndexPrimary</span></span></p></li>
<li><p><span data-ttu-id="1ea7d-181">JET_bitIndexUnversioned</span><span class="sxs-lookup"><span data-stu-id="1ea7d-181">JET_bitIndexUnversioned</span></span></p></li>
<li><p><span data-ttu-id="1ea7d-182">JET_bitIndexEmpty</span><span class="sxs-lookup"><span data-stu-id="1ea7d-182">JET_bitIndexEmpty</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ea7d-183">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="1ea7d-183">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="1ea7d-184">Un ID de paramètres régionaux (LCID) non valide a été passé (par le biais du membre <strong>LCID</strong> dans la structure <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> , que le membre <strong>pidxunicode</strong> dans la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> contient un pointeur vers ou via le membre <strong>LCID</strong> de la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ).</span><span class="sxs-lookup"><span data-stu-id="1ea7d-184">An invalid Locale ID (LCID) was passed in (either through the <strong>lcid</strong> member in the <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> structure, which the <strong>pidxunicode</strong> member in the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure contains a pointer to, or through the <strong>lcid</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ea7d-185">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="1ea7d-185">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="1ea7d-186">Un nom d’index non valide a été spécifié.</span><span class="sxs-lookup"><span data-stu-id="1ea7d-186">An invalid index name was specified.</span></span> <span data-ttu-id="1ea7d-187">Pour plus d’informations, consultez <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="1ea7d-187">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for more details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ea7d-188">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="1ea7d-188">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="1ea7d-189">Un paramètre non valide a été passé dans l’API.</span><span class="sxs-lookup"><span data-stu-id="1ea7d-189">An invalid parameter was passed into the API.</span></span> <span data-ttu-id="1ea7d-190">Voici quelques-unes des raisons pour lesquelles cette erreur peut être retournée :</span><span class="sxs-lookup"><span data-stu-id="1ea7d-190">Some of the reasons this error may be returned are:</span></span></p>
<ul>
<li><p><span data-ttu-id="1ea7d-191">Le champ <strong>cbKey</strong> d’une structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> a la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="1ea7d-191">The <strong>cbKey</strong> field of a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is set to zero.</span></span></p></li>
<li><p><span data-ttu-id="1ea7d-192">Le membre <strong>cbStruct</strong> d’une structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> n’a pas la valeur sizeof (<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ).</span><span class="sxs-lookup"><span data-stu-id="1ea7d-192">The <strong>cbStruct</strong> member of a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is not set to sizeof(<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ).</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ea7d-193">JET_errUnicodeTranslationFail</span><span class="sxs-lookup"><span data-stu-id="1ea7d-193">JET_errUnicodeTranslationFail</span></span></p></td>
<td><p><span data-ttu-id="1ea7d-194">Une erreur s’est produite lors de la normalisation d’une colonne Unicode.</span><span class="sxs-lookup"><span data-stu-id="1ea7d-194">An error occurred attempting to normalize a Unicode column.</span></span> <span data-ttu-id="1ea7d-195">Cela peut être dû à un manque de ressources système.</span><span class="sxs-lookup"><span data-stu-id="1ea7d-195">This can be caused by running out of system resources.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="1ea7d-196">Notes</span><span class="sxs-lookup"><span data-stu-id="1ea7d-196">Remarks</span></span>

<span data-ttu-id="1ea7d-197">La valeur de retour est JET_errSuccess en cas d’achèvement réussi de tous les index spécifiés.</span><span class="sxs-lookup"><span data-stu-id="1ea7d-197">The return value is JET_errSuccess on successful completion of all indexes specified.</span></span>

<span data-ttu-id="1ea7d-198">**JetCreateIndex2** itère au sein des index donnés dans **pindexcreate**, et s’abandonne parfois lors du premier échec.</span><span class="sxs-lookup"><span data-stu-id="1ea7d-198">**JetCreateIndex2** iterates through the indexes given in **pindexcreate**, and will sometimes abort on the first failure.</span></span> <span data-ttu-id="1ea7d-199">Les index qui suivent le premier index avec une erreur n’ont peut-être pas été tentés, même si le membre **Err** de la structure [JET_INDEXCREATE](./jet-indexcreate-structure.md) contient des JET_errSuccess.</span><span class="sxs-lookup"><span data-stu-id="1ea7d-199">Any indexes after the first index with an error may not have been attempted, even though the **err** member of the [JET_INDEXCREATE](./jet-indexcreate-structure.md) structure contains JET_errSuccess.</span></span>

#### <a name="requirements"></a><span data-ttu-id="1ea7d-200">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1ea7d-200">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1ea7d-201"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="1ea7d-201"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="1ea7d-202">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="1ea7d-202">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ea7d-203"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="1ea7d-203"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="1ea7d-204">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="1ea7d-204">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ea7d-205"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="1ea7d-205"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="1ea7d-206">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="1ea7d-206">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ea7d-207"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="1ea7d-207"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="1ea7d-208">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="1ea7d-208">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ea7d-209"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="1ea7d-209"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="1ea7d-210">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="1ea7d-210">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ea7d-211"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="1ea7d-211"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="1ea7d-212">Implémenté en tant que <strong>JetCreateIndex2W</strong> (Unicode) et <strong>JetCreateIndex2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="1ea7d-212">Implemented as <strong>JetCreateIndex2W</strong> (Unicode) and <strong>JetCreateIndex2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="1ea7d-213">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ea7d-213">See Also</span></span>

[<span data-ttu-id="1ea7d-214">JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="1ea7d-214">JET_CONDITIONALCOLUMN</span></span>](./jet-conditionalcolumn-structure.md)  
[<span data-ttu-id="1ea7d-215">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="1ea7d-215">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="1ea7d-216">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="1ea7d-216">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="1ea7d-217">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="1ea7d-217">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="1ea7d-218">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="1ea7d-218">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="1ea7d-219">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="1ea7d-219">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="1ea7d-220">JetCreateIndex</span><span class="sxs-lookup"><span data-stu-id="1ea7d-220">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="1ea7d-221">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="1ea7d-221">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="1ea7d-222">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="1ea7d-222">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)
