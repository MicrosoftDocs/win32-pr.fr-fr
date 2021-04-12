---
description: 'En savoir plus sur : fonction JetCreateIndex3'
title: Fonction JetCreateIndex3
TOCTitle: JetCreateIndex3 Function
ms:assetid: bc9b940e-65c6-49d6-ad32-74434527d29f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294075(v=EXCHG.10)
ms:contentKeyID: 32765690
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateIndex3A
- JetCreateIndex3
- JetCreateIndex3W
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c4f3331a903d4885499ff6c2cd2cad0d8b8534a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319762"
---
# <a name="jetcreateindex3-function"></a><span data-ttu-id="46855-103">Fonction JetCreateIndex3</span><span class="sxs-lookup"><span data-stu-id="46855-103">JetCreateIndex3 Function</span></span>


<span data-ttu-id="46855-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="46855-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreateindex3-function"></a><span data-ttu-id="46855-105">Fonction JetCreateIndex3</span><span class="sxs-lookup"><span data-stu-id="46855-105">JetCreateIndex3 Function</span></span>

<span data-ttu-id="46855-106">La fonction **JetCreateIndex3** crée des index sur les données d’une base de données ESE, qui peut être utilisée pour localiser rapidement des données spécifiques.</span><span class="sxs-lookup"><span data-stu-id="46855-106">The **JetCreateIndex3** function creates indexes over data in an ESE database, which can be used to locate specific data quickly.</span></span>

<span data-ttu-id="46855-107">**Windows 7 : JetCreateIndex3** est introduit dans le système d’exploitation Windows 7.</span><span class="sxs-lookup"><span data-stu-id="46855-107">**Windows 7:  JetCreateIndex3** is introduced in the Windows 7 operating system.</span></span>

```cpp
    JET_ERR JET_API JetCreateIndex3(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_INDEXCREATE2* pindexcreate,
      __in          unsigned long cIndexCreate
    );
```

### <a name="parameters"></a><span data-ttu-id="46855-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="46855-108">Parameters</span></span>

<span data-ttu-id="46855-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="46855-109">*sesid*</span></span>

<span data-ttu-id="46855-110">Contexte de la session de base de données à utiliser pour l’appel d’API.</span><span class="sxs-lookup"><span data-stu-id="46855-110">The database session context to use for the API call.</span></span>

<span data-ttu-id="46855-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="46855-111">*tableid*</span></span>

<span data-ttu-id="46855-112">Table sur laquelle l’index sera créé.</span><span class="sxs-lookup"><span data-stu-id="46855-112">The table on which the index will be created.</span></span>

<span data-ttu-id="46855-113">*pindexcreate*</span><span class="sxs-lookup"><span data-stu-id="46855-113">*pindexcreate*</span></span>

<span data-ttu-id="46855-114">Tableau de structures [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) , qui définissent chacune un index à créer.</span><span class="sxs-lookup"><span data-stu-id="46855-114">An array of [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) structures, each of which defines an index to be created.</span></span>

<span data-ttu-id="46855-115">*cIndexCreate*</span><span class="sxs-lookup"><span data-stu-id="46855-115">*cIndexCreate*</span></span>

<span data-ttu-id="46855-116">Nombre d’éléments dans le tableau *pindexcreate* .</span><span class="sxs-lookup"><span data-stu-id="46855-116">The number of elements in the *pindexcreate* array.</span></span>

### <a name="return-value"></a><span data-ttu-id="46855-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="46855-117">Return Value</span></span>

<span data-ttu-id="46855-118">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="46855-118">This function returns the [JET_ERR](./jet-err.md) data type with one of the following return codes.</span></span> <span data-ttu-id="46855-119">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="46855-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="46855-120">Code de retour</span><span class="sxs-lookup"><span data-stu-id="46855-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="46855-121">Description</span><span class="sxs-lookup"><span data-stu-id="46855-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="46855-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="46855-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="46855-123">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="46855-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46855-124">JET_errCannotIndex</span><span class="sxs-lookup"><span data-stu-id="46855-124">JET_errCannotIndex</span></span></p></td>
<td><p><span data-ttu-id="46855-125">Une tentative d’indexation sur une colonne de dépôt/mise à jour ou SLV (Notez que les colonnes SLV sont dépréciées) a été tentée.</span><span class="sxs-lookup"><span data-stu-id="46855-125">An attempt was made to index over an escrow-update or SLV column (note that SLV columns are deprecated).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46855-126">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="46855-126">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="46855-127">Une tentative d’indexation sur une colonne inexistante a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="46855-127">An attempt was made to index over a non-existent column.</span></span> <span data-ttu-id="46855-128">Toute tentative d’indexation conditionnelle sur une colonne inexistante peut également générer cette erreur.</span><span class="sxs-lookup"><span data-stu-id="46855-128">Attempting to conditionally index over a non-existent column can also produce this error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46855-129">JET_errDensityInvalid</span><span class="sxs-lookup"><span data-stu-id="46855-129">JET_errDensityInvalid</span></span></p></td>
<td><p><span data-ttu-id="46855-130">Cette erreur est retournée si le membre <strong>ulDensity</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> est défini sur un nombre inférieur à 20 ou supérieur à 100.</span><span class="sxs-lookup"><span data-stu-id="46855-130">This error will be returned if the <strong>ulDensity</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is set to a number less than 20 or greater than 100.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46855-131">JET_errIndexDuplicate</span><span class="sxs-lookup"><span data-stu-id="46855-131">JET_errIndexDuplicate</span></span></p></td>
<td><p><span data-ttu-id="46855-132">Une tentative de définition de deux index identiques a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="46855-132">An attempt to define two identical indexes was made.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46855-133">JET_errIndexHasPrimary</span><span class="sxs-lookup"><span data-stu-id="46855-133">JET_errIndexHasPrimary</span></span></p></td>
<td><p><span data-ttu-id="46855-134">Une tentative a été effectuée pour spécifier plusieurs index primaires pour une table.</span><span class="sxs-lookup"><span data-stu-id="46855-134">An attempt was made to specify more than one primary index for a table.</span></span> <span data-ttu-id="46855-135">Une table doit avoir un seul index primaire.</span><span class="sxs-lookup"><span data-stu-id="46855-135">A table must have exactly one primary index.</span></span> <span data-ttu-id="46855-136">Si aucun index primaire n’est spécifié, le moteur de base de données en crée un en toute transparence.</span><span class="sxs-lookup"><span data-stu-id="46855-136">If no primary index is specified, the database engine will transparently create one.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46855-137">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="46855-137">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="46855-138">Une définition d’index non valide a été spécifiée.</span><span class="sxs-lookup"><span data-stu-id="46855-138">An invalid index definition was specified.</span></span> <span data-ttu-id="46855-139">Voici quelques raisons possibles pour la réception de cette erreur :</span><span class="sxs-lookup"><span data-stu-id="46855-139">The following are some possible reasons for receiving this error:</span></span></p>
<ul>
<li><p><span data-ttu-id="46855-140">Un index principal est conditionnel (le membre<strong>Grbit</strong> de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> a JET_bitIndexPrimary défini et le membre <strong>cConditionalColumn</strong> de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> est supérieur à zéro).</span><span class="sxs-lookup"><span data-stu-id="46855-140">A primary index is conditional (<strong>grbit</strong> member of <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> has JET_bitIndexPrimary set, and the <strong>cConditionalColumn</strong> member of <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> is greater than zero).</span></span></p></li>
<li><p><span data-ttu-id="46855-141">Windows Server 2003 et versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="46855-141">Windows Server 2003 and later versions of Windows.</span></span> <span data-ttu-id="46855-142">Tentative de création d’un index de tuple avec des limites de tuple, mais sans passer d’informations dans le membre <strong>ptuplelimits</strong> de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> (autrement dit, <em>Grbit</em> a JET_bitIndexTupleLimits défini, mais le pointeur <strong>ptuplelimits</strong> est null).</span><span class="sxs-lookup"><span data-stu-id="46855-142">Attempting to create a tuple index with tuple limits, but without passing information in the <strong>ptuplelimits</strong> member in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> (that is, <em>grbit</em> has JET_bitIndexTupleLimits set, but the <strong>ptuplelimits</strong> pointer is NULL).</span></span></p></li>
<li><p><span data-ttu-id="46855-143">Passage d’une définition de clé non valide dans le membre <strong>szKey</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="46855-143">Passing in an invalid key definition in the <strong>szKey</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure.</span></span> <span data-ttu-id="46855-144">Pour plus d’informations sur les définitions valides, consultez <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="46855-144">See <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> for a discussion of valid definitions.</span></span></p></li>
<li><p><span data-ttu-id="46855-145">La définition du membre <strong>cbVarSegMac</strong> dans <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> est supérieure à JET_cbPrimaryKeyMost (pour un index principal) ou supérieure à JET_cbSecondaryKeyMost (pour un index secondaire).</span><span class="sxs-lookup"><span data-stu-id="46855-145">Setting the <strong>cbVarSegMac</strong> member in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> to be greater than JET_cbPrimaryKeyMost (for a primary index) or greater than JET_cbSecondaryKeyMost (for a secondary index).</span></span></p></li>
<li><p><span data-ttu-id="46855-146">Passage d’une combinaison non valide pour un index Unicode défini par l’utilisateur (un qui a le bit JET_bitIndexUnicode défini dans le membre <strong>Grbit</strong> de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>).</span><span class="sxs-lookup"><span data-stu-id="46855-146">Passing an invalid combination for a user-defined Unicode index (one which has the JET_bitIndexUnicode bit set in the <strong>grbit</strong> member of <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>).</span></span> <span data-ttu-id="46855-147">Certaines causes courantes peuvent être que le champ pidxunicode de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> a la valeur null ou que le LCID spécifié dans la structure pidxunicode n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="46855-147">Some common causes may be that the pidxunicode field of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is NULL, or the LCID specified in the pidxunicode structure is invalid.</span></span></p></li>
<li><p><span data-ttu-id="46855-148">Spécification d’une colonne à valeurs multiples pour un index primaire.</span><span class="sxs-lookup"><span data-stu-id="46855-148">Specifying a multi-valued column for a primary index.</span></span></p></li>
<li><p><span data-ttu-id="46855-149">Tentative d’indexation d’un trop grand nombre de colonnes conditionnelles.</span><span class="sxs-lookup"><span data-stu-id="46855-149">Trying to index too many conditional columns.</span></span> <span data-ttu-id="46855-150">Le membre <strong>cConditionalColumn</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ne doit pas être supérieur à JET_ccolKeyMost.</span><span class="sxs-lookup"><span data-stu-id="46855-150">The <strong>cConditionalColumn</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not be greater than JET_ccolKeyMost.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46855-151">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="46855-151">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="46855-152">Windows XP et versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="46855-152">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="46855-153">Une structure de <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> a été spécifiée et ses limites ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="46855-153">A <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure was specified, and its limits are not supported.</span></span> <span data-ttu-id="46855-154">Consultez la section Notes de la structure <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</span><span class="sxs-lookup"><span data-stu-id="46855-154">See the remarks section of the <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46855-155">JET_errIndexTuplesNonUniqueOnly</span><span class="sxs-lookup"><span data-stu-id="46855-155">JET_errIndexTuplesNonUniqueOnly</span></span></p></td>
<td><p><span data-ttu-id="46855-156">Windows XP et versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="46855-156">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="46855-157">Un index de tuple ne peut pas être unique (<em>Grbit</em> ne doit pas avoir à la fois JET_bitIndexTuples et JET_bitIndexUnique défini).</span><span class="sxs-lookup"><span data-stu-id="46855-157">A tuple index cannot be unique (<em>grbit</em> must not have both JET_bitIndexTuples and JET_bitIndexUnique set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46855-158">JET_errIndexTuplesOneColumnOnly</span><span class="sxs-lookup"><span data-stu-id="46855-158">JET_errIndexTuplesOneColumnOnly</span></span></p></td>
<td><p><span data-ttu-id="46855-159">Windows XP et versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="46855-159">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="46855-160">Un index de tuple ne peut être que sur une seule colonne (autrement dit, le membre <strong>Grbit</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> a JET_bitIndexTuples jeu et le membre <strong>szKey</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> spécifie plusieurs colonnes).</span><span class="sxs-lookup"><span data-stu-id="46855-160">A tuple index can only be over a single column (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has JET_bitIndexTuples set, and the <strong>szKey</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure specifies more than one column).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46855-161">JET_errIndexTuplesSecondaryIndexOnly</span><span class="sxs-lookup"><span data-stu-id="46855-161">JET_errIndexTuplesSecondaryIndexOnly</span></span></p></td>
<td><p><span data-ttu-id="46855-162">Windows XP et versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="46855-162">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="46855-163">Un index de tuple ne peut pas être un index primaire (autrement dit, le membre <strong>Grbit</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ne doit pas avoir JET_bitIndexPrimary et JET_bitIndexTuples défini).</span><span class="sxs-lookup"><span data-stu-id="46855-163">A tuple index cannot be a primary index (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexTuples set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46855-164">JET_errIndexTuplesTextColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="46855-164">JET_errIndexTuplesTextColumnsOnly</span></span></p></td>
<td><p><span data-ttu-id="46855-165">Windows XP et versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="46855-165">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="46855-166">Un index de tuple ne peut être que sur une colonne de type texte ou Unicode.</span><span class="sxs-lookup"><span data-stu-id="46855-166">A tuple index can only be on a text or Unicode column.</span></span> <span data-ttu-id="46855-167">Si vous tentez d’indexer d’autres colonnes (par exemple, des colonnes binaires), JET_errIndexTuplesTextColumnsOnly.</span><span class="sxs-lookup"><span data-stu-id="46855-167">An attempt to index other columns (for example, binary columns) will result in JET_errIndexTuplesTextColumnsOnly.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46855-168">JET_errIndexTuplesVarSegMacNotAllowed</span><span class="sxs-lookup"><span data-stu-id="46855-168">JET_errIndexTuplesVarSegMacNotAllowed</span></span></p></td>
<td><p><span data-ttu-id="46855-169">Windows XP et versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="46855-169">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="46855-170">Un index de tuple n’autorise pas la définition du membre <strong>cbVarSegMac</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="46855-170">A tuple index does not allow the <strong>cbVarSegMac</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure to be set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46855-171">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="46855-171">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="46855-172">Une tentative de création d’un index sans informations de version a été effectuée dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="46855-172">An attempt was made to create an index without version information while in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46855-173">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="46855-173">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="46855-174">La définition de l’index n’est pas valide, car le membre <strong>Grbit</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> contient des valeurs incohérentes.</span><span class="sxs-lookup"><span data-stu-id="46855-174">The index definition is invalid because the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure contains inconsistent values.</span></span> <span data-ttu-id="46855-175">Voici quelques raisons possibles :</span><span class="sxs-lookup"><span data-stu-id="46855-175">The following are some possible reasons:</span></span></p>
<ul>
<li><p><span data-ttu-id="46855-176">Un index principal avait un bit ignore spécifié (JET_bitIndexPrimary a été passé avec l’un des JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull ou JET_bitIndexIgnoreFirstNull).</span><span class="sxs-lookup"><span data-stu-id="46855-176">A primary index had an ignore bit specified (JET_bitIndexPrimary was passed with one of JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull, or JET_bitIndexIgnoreFirstNull).</span></span></p></li>
<li><p><span data-ttu-id="46855-177">Un index vide n’ignore aucun champ NULL (autrement dit, le membre <strong>Grbit</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> n’a JET_bitIndexEmpty défini, mais n’a pas de JET_bitIndexIgnoreAnyNull défini).</span><span class="sxs-lookup"><span data-stu-id="46855-177">An empty index does not ignore any NULL fields (that is, <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has JET_bitIndexEmpty set, but does not have JET_bitIndexIgnoreAnyNull set).</span></span></p></li>
<li><p><span data-ttu-id="46855-178">Passage d’une structure <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> avec un membre <strong>Grbit</strong> non valide.</span><span class="sxs-lookup"><span data-stu-id="46855-178">Passing in a <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> structure with an invalid <strong>grbit</strong> member.</span></span> <span data-ttu-id="46855-179">Consultez <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>.</span><span class="sxs-lookup"><span data-stu-id="46855-179">See <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>.</span></span></p></li>
</ul>
<p><span data-ttu-id="46855-180">Lors de la création de plusieurs index à la fois (autrement dit, si le paramètre <em>cIndexCreate</em> est supérieur à un), aucun des index ne peut contenir l’un des bits suivants :</span><span class="sxs-lookup"><span data-stu-id="46855-180">When creating several indexes at once (that is, if the <em>cIndexCreate</em> parameter is greater than one), none of the indexes may contain any of the following bits:</span></span></p>
<ul>
<li><p><span data-ttu-id="46855-181">JET_bitIndexPrimary</span><span class="sxs-lookup"><span data-stu-id="46855-181">JET_bitIndexPrimary</span></span></p></li>
<li><p><span data-ttu-id="46855-182">JET_bitIndexUnversioned</span><span class="sxs-lookup"><span data-stu-id="46855-182">JET_bitIndexUnversioned</span></span></p></li>
<li><p><span data-ttu-id="46855-183">JET_bitIndexEmpty</span><span class="sxs-lookup"><span data-stu-id="46855-183">JET_bitIndexEmpty</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46855-184">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="46855-184">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="46855-185">Un ID de paramètres régionaux (LCID) non valide a été passé (par le biais du membre <strong>LCID</strong> dans la structure <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> , que le membre <strong>pidxunicode</strong> dans la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> contient un pointeur vers ou via le membre <strong>LCID</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ).</span><span class="sxs-lookup"><span data-stu-id="46855-185">An invalid Locale ID (LCID) was passed in (either through the <strong>lcid</strong> member in the <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> structure, which the <strong>pidxunicode</strong> member in the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure contains a pointer to, or through the <strong>lcid</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46855-186">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="46855-186">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="46855-187">Un nom d’index non valide a été spécifié.</span><span class="sxs-lookup"><span data-stu-id="46855-187">An invalid index name was specified.</span></span> <span data-ttu-id="46855-188">Pour plus d’informations, consultez <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="46855-188">See <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> for more details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46855-189">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="46855-189">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="46855-190">Un paramètre non valide a été passé dans l’API.</span><span class="sxs-lookup"><span data-stu-id="46855-190">An invalid parameter was passed into the API.</span></span> <span data-ttu-id="46855-191">Voici quelques raisons pour lesquelles cette erreur peut être retournée :</span><span class="sxs-lookup"><span data-stu-id="46855-191">The following are some reasons why this error may be returned:</span></span></p>
<ul>
<li><p><span data-ttu-id="46855-192">Le champ <strong>cbKey</strong> d’une structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> a la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="46855-192">The <strong>cbKey</strong> field of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is set to zero.</span></span></p></li>
<li><p><span data-ttu-id="46855-193">Le membre <strong>cbStruct</strong> d’une structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> n’a pas la valeur sizeof ( <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ).</span><span class="sxs-lookup"><span data-stu-id="46855-193">The <strong>cbStruct</strong> member of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is not set to sizeof( <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ).</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46855-194">JET_errUnicodeTranslationFail</span><span class="sxs-lookup"><span data-stu-id="46855-194">JET_errUnicodeTranslationFail</span></span></p></td>
<td><p><span data-ttu-id="46855-195">Une erreur s’est produite lors de la normalisation d’une colonne Unicode.</span><span class="sxs-lookup"><span data-stu-id="46855-195">An error occurred while trying to normalize a Unicode column.</span></span> <span data-ttu-id="46855-196">Cela peut être dû à un manque de ressources système.</span><span class="sxs-lookup"><span data-stu-id="46855-196">This can be caused by running out of system resources.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46855-197">JET_errSpaceHintsInvalid</span><span class="sxs-lookup"><span data-stu-id="46855-197">JET_errSpaceHintsInvalid</span></span></p></td>
<td><p><span data-ttu-id="46855-198">Un élément de la structure d’indicateurs d’espace JET n’est pas correct ou n’est pas exploitable.</span><span class="sxs-lookup"><span data-stu-id="46855-198">An element of the JET space hints structure was not correct or actionable.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="46855-199">Notes</span><span class="sxs-lookup"><span data-stu-id="46855-199">Remarks</span></span>

<span data-ttu-id="46855-200">La valeur de retour est JET_errSuccess en cas d’achèvement réussi de tous les index spécifiés.</span><span class="sxs-lookup"><span data-stu-id="46855-200">The return value is JET_errSuccess on successful completion of all indexes specified.</span></span>

<span data-ttu-id="46855-201">**JetCreateIndex3** itère au sein des index donnés dans **pindexcreate**, et s’abandonne parfois lors du premier échec.</span><span class="sxs-lookup"><span data-stu-id="46855-201">**JetCreateIndex3** iterates through the indexes given in **pindexcreate**, and will sometimes abort on the first failure.</span></span> <span data-ttu-id="46855-202">Les index qui suivent le premier index avec une erreur n’ont peut-être pas été tentés, même si le membre **Err** de la structure [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) contient des JET_errSuccess.</span><span class="sxs-lookup"><span data-stu-id="46855-202">Any indexes after the first index with an error may not have been attempted, even though the **err** member of the [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) structure contains JET_errSuccess.</span></span>

#### <a name="requirements"></a><span data-ttu-id="46855-203">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="46855-203">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="46855-204"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="46855-204"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="46855-205">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="46855-205">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46855-206"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="46855-206"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="46855-207">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="46855-207">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46855-208"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="46855-208"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="46855-209">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="46855-209">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46855-210"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="46855-210"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="46855-211">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="46855-211">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46855-212"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="46855-212"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="46855-213">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="46855-213">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46855-214"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="46855-214"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="46855-215">Implémenté en tant que <strong>JetCreateIndex3W</strong> (Unicode) et <strong>JetCreateIndex3A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="46855-215">Implemented as <strong>JetCreateIndex3W</strong> (Unicode) and <strong>JetCreateIndex3A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="46855-216">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="46855-216">See Also</span></span>

[<span data-ttu-id="46855-217">JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="46855-217">JET_CONDITIONALCOLUMN</span></span>](./jet-conditionalcolumn-structure.md)  
[<span data-ttu-id="46855-218">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="46855-218">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="46855-219">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="46855-219">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="46855-220">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="46855-220">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="46855-221">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="46855-221">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="46855-222">JET_INDEXCREATE2</span><span class="sxs-lookup"><span data-stu-id="46855-222">JET_INDEXCREATE2</span></span>](./jet-indexcreate2-structure.md)  
[<span data-ttu-id="46855-223">JetCreateIndex</span><span class="sxs-lookup"><span data-stu-id="46855-223">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="46855-224">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="46855-224">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="46855-225">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="46855-225">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)  
[<span data-ttu-id="46855-226">JET_SPACEHINTS</span><span class="sxs-lookup"><span data-stu-id="46855-226">JET_SPACEHINTS</span></span>](./jet-spacehints-structure.md)
