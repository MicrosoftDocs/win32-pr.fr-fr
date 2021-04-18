---
description: 'En savoir plus sur : fonction JetCreateIndex4W'
title: Fonction JetCreateIndex4W
TOCTitle: JetCreateIndex4W Function
ms:assetid: 968745a2-66ce-4c7f-ab5b-43282adc5313
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835044(v=EXCHG.10)
ms:contentKeyID: 49894666
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetCreateIndex4W
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9a4c7671cbe361b6214552f4c611cd1706c0e48d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520059"
---
# <a name="jetcreateindex4w-function"></a><span data-ttu-id="b1489-103">Fonction JetCreateIndex4W</span><span class="sxs-lookup"><span data-stu-id="b1489-103">JetCreateIndex4W Function</span></span>


<span data-ttu-id="b1489-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="b1489-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="b1489-105">La fonction **JetCreateIndex4W** crée des index sur des données dans une base de données ESE (Extensible Storage Engine), qui peut être utilisée pour localiser rapidement des données spécifiques.</span><span class="sxs-lookup"><span data-stu-id="b1489-105">The **JetCreateIndex4W** function creates indexes over data in an Extensible Storage Engine (ESE) database, which can be used to locate specific data quickly.</span></span>

<span data-ttu-id="b1489-106">La fonction **JetCreateIndex4W** a été introduite dans le système d’exploitation Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b1489-106">The **JetCreateIndex4W** function was introduced in the Windows 8 operating system.</span></span>

``` c++
JET_ERR JET_API JetCreateIndex4W(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          JET_INDEXCREATE2* pindexcreate,
  __in          unsigned long cIndexCreate
);
```

### <a name="parameters"></a><span data-ttu-id="b1489-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b1489-107">Parameters</span></span>

<span data-ttu-id="b1489-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="b1489-108">*sesid*</span></span>

<span data-ttu-id="b1489-109">Contexte de la session de base de données à utiliser pour l’appel d’API.</span><span class="sxs-lookup"><span data-stu-id="b1489-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="b1489-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="b1489-110">*tableid*</span></span>

<span data-ttu-id="b1489-111">Table sur laquelle l’index sera créé.</span><span class="sxs-lookup"><span data-stu-id="b1489-111">The table on which the index will be created.</span></span>

<span data-ttu-id="b1489-112">*pindexcreate*</span><span class="sxs-lookup"><span data-stu-id="b1489-112">*pindexcreate*</span></span>

<span data-ttu-id="b1489-113">Tableau de structures [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) , qui définissent chacune un index à créer.</span><span class="sxs-lookup"><span data-stu-id="b1489-113">An array of [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) structures, each of which defines an index to be created.</span></span>

<span data-ttu-id="b1489-114">*cIndexCreate*</span><span class="sxs-lookup"><span data-stu-id="b1489-114">*cIndexCreate*</span></span>

<span data-ttu-id="b1489-115">Nombre d’éléments dans le tableau *pindexcreate* .</span><span class="sxs-lookup"><span data-stu-id="b1489-115">The number of elements in the *pindexcreate* array.</span></span>

### <a name="return-value"></a><span data-ttu-id="b1489-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b1489-116">Return value</span></span>

<span data-ttu-id="b1489-117">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour énumérés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="b1489-117">This function returns the [JET_ERR](./jet-err.md) data type with one of the return codes listed in the following table.</span></span> <span data-ttu-id="b1489-118">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="b1489-118">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b1489-119">Code de retour</span><span class="sxs-lookup"><span data-stu-id="b1489-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="b1489-120">Description</span><span class="sxs-lookup"><span data-stu-id="b1489-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b1489-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="b1489-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="b1489-122">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="b1489-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1489-123">JET_errCannotIndex</span><span class="sxs-lookup"><span data-stu-id="b1489-123">JET_errCannotIndex</span></span></p></td>
<td><p><span data-ttu-id="b1489-124">Une tentative d’indexation sur une colonne de dépôt/mise à jour ou SLV (Notez que les colonnes SLV sont dépréciées) a été tentée.</span><span class="sxs-lookup"><span data-stu-id="b1489-124">An attempt was made to index over an escrow-update or SLV column (note that SLV columns are deprecated).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1489-125">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="b1489-125">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="b1489-126">Une tentative d’indexation sur une colonne inexistante a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="b1489-126">An attempt was made to index over a nonexistent column.</span></span> <span data-ttu-id="b1489-127">Une tentative d’index conditionnel sur une colonne inexistante peut également générer cette erreur.</span><span class="sxs-lookup"><span data-stu-id="b1489-127">An attempt to conditionally index over a nonexistent column can also produce this error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1489-128">JET_errDensityInvalid</span><span class="sxs-lookup"><span data-stu-id="b1489-128">JET_errDensityInvalid</span></span></p></td>
<td><p><span data-ttu-id="b1489-129">Cette erreur est retournée si le membre <strong>ulDensity</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> est défini sur un nombre inférieur à 20 ou supérieur à 100.</span><span class="sxs-lookup"><span data-stu-id="b1489-129">This error will be returned if the <strong>ulDensity</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is set to a number less than 20 or greater than 100.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1489-130">JET_errIndexDuplicate</span><span class="sxs-lookup"><span data-stu-id="b1489-130">JET_errIndexDuplicate</span></span></p></td>
<td><p><span data-ttu-id="b1489-131">Une tentative de définition de deux index identiques a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="b1489-131">An attempt to define two identical indexes was made.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1489-132">JET_errIndexHasPrimary</span><span class="sxs-lookup"><span data-stu-id="b1489-132">JET_errIndexHasPrimary</span></span></p></td>
<td><p><span data-ttu-id="b1489-133">Une tentative a été effectuée pour spécifier plusieurs index primaires pour une table.</span><span class="sxs-lookup"><span data-stu-id="b1489-133">An attempt was made to specify more than one primary index for a table.</span></span> <span data-ttu-id="b1489-134">Une table doit avoir un seul index primaire.</span><span class="sxs-lookup"><span data-stu-id="b1489-134">A table must have exactly one primary index.</span></span> <span data-ttu-id="b1489-135">Si aucun index primaire n’est spécifié, le moteur de base de données en crée un en toute transparence.</span><span class="sxs-lookup"><span data-stu-id="b1489-135">If no primary index is specified, the database engine will transparently create one.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1489-136">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="b1489-136">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="b1489-137">Une définition d’index non valide a été spécifiée.</span><span class="sxs-lookup"><span data-stu-id="b1489-137">An invalid index definition was specified.</span></span> <span data-ttu-id="b1489-138">Voici quelques raisons possibles pour cette erreur :</span><span class="sxs-lookup"><span data-stu-id="b1489-138">The following are some possible reasons for this error:</span></span></p>
<ul>
<li><p><span data-ttu-id="b1489-139">Un index principal est conditionnel (le membre<strong>Grbit</strong> de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> a <strong>JET_bitIndexPrimary</strong> défini et le membre <strong>cConditionalColumn</strong> de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> est supérieur à zéro).</span><span class="sxs-lookup"><span data-stu-id="b1489-139">A primary index is conditional (<strong>grbit</strong> member of <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> has <strong>JET_bitIndexPrimary</strong> set, and the <strong>cConditionalColumn</strong> member of <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> is greater than zero).</span></span></p></li>
<li><p><span data-ttu-id="b1489-140">S’applique aux versions de Windows à partir de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b1489-140">Applies to versions of Windows starting with Windows Server 2003.</span></span> <span data-ttu-id="b1489-141">Une tentative de création d’un index de tuple avec des limites de tuple a été effectuée, mais sans passer d’informations dans le membre <strong>ptuplelimits</strong> dans <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> (autrement dit, <em>Grbit</em> a <strong>JET_bitIndexTupleLimits</strong> défini, mais le pointeur <strong>ptuplelimits</strong> est null).</span><span class="sxs-lookup"><span data-stu-id="b1489-141">An attempt was made to create a tuple index with tuple limits, but without passing information in the <strong>ptuplelimits</strong> member in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> (that is, <em>grbit</em> has <strong>JET_bitIndexTupleLimits</strong> set, but the <strong>ptuplelimits</strong> pointer is null).</span></span></p></li>
<li><p><span data-ttu-id="b1489-142">Passage d’une définition de clé non valide dans le membre <strong>szKey</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="b1489-142">Passing in an invalid key definition in the <strong>szKey</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure.</span></span> <span data-ttu-id="b1489-143">Pour plus d’informations sur les définitions valides, consultez <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>.</span><span class="sxs-lookup"><span data-stu-id="b1489-143">For information about valid definitions, see <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>.</span></span></p></li>
<li><p><span data-ttu-id="b1489-144">La définition du membre <strong>cbVarSegMac</strong> dans <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> est supérieure à <strong>JET_cbPrimaryKeyMost</strong> (pour un index principal) ou supérieure à <strong>JET_cbSecondaryKeyMost</strong> (pour un index secondaire).</span><span class="sxs-lookup"><span data-stu-id="b1489-144">Setting the <strong>cbVarSegMac</strong> member in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> to be greater than <strong>JET_cbPrimaryKeyMost</strong> (for a primary index) or greater than <strong>JET_cbSecondaryKeyMost</strong> (for a secondary index).</span></span></p></li>
<li><p><span data-ttu-id="b1489-145">Passage d’une combinaison non valide pour un index Unicode défini par l’utilisateur (un qui a le bit <strong>JET_bitIndexUnicode</strong> défini dans le membre <strong>Grbit</strong> de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>).</span><span class="sxs-lookup"><span data-stu-id="b1489-145">Passing an invalid combination for a user-defined Unicode index (one which has the <strong>JET_bitIndexUnicode</strong> bit set in the <strong>grbit</strong> member of <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>).</span></span> <span data-ttu-id="b1489-146">Certaines causes courantes peuvent être que le champ pidxunicode de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> a la valeur null ou que le LCID spécifié dans la structure pidxunicode n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="b1489-146">Some common causes may be that the pidxunicode field of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is null, or the LCID specified in the pidxunicode structure is invalid.</span></span></p></li>
<li><p><span data-ttu-id="b1489-147">Spécification d’une colonne à valeurs multiples pour un index primaire.</span><span class="sxs-lookup"><span data-stu-id="b1489-147">Specifying a multivalued column for a primary index.</span></span></p></li>
<li><p><span data-ttu-id="b1489-148">Tentative d’indexation d’un trop grand nombre de colonnes conditionnelles.</span><span class="sxs-lookup"><span data-stu-id="b1489-148">Trying to index too many conditional columns.</span></span> <span data-ttu-id="b1489-149">Le membre <strong>cConditionalColumn</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ne doit pas être supérieur à <strong>JET_ccolKeyMost</strong>.</span><span class="sxs-lookup"><span data-stu-id="b1489-149">The <strong>cConditionalColumn</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not be greater than <strong>JET_ccolKeyMost</strong>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1489-150">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="b1489-150">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="b1489-151">S’applique aux versions de Windows à partir de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b1489-151">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="b1489-152">Une structure de <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> a été spécifiée et ses limites ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="b1489-152">A <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure was specified, and its limits are not supported.</span></span> <span data-ttu-id="b1489-153">Pour plus d’informations, consultez la section Notes de la structure <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</span><span class="sxs-lookup"><span data-stu-id="b1489-153">For more information, see the remarks section of the <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1489-154">JET_errIndexTuplesNonUniqueOnly</span><span class="sxs-lookup"><span data-stu-id="b1489-154">JET_errIndexTuplesNonUniqueOnly</span></span></p></td>
<td><p><span data-ttu-id="b1489-155">S’applique aux versions de Windows à partir de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b1489-155">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="b1489-156">Un index de tuple ne peut pas être unique (<em>Grbit</em> ne doit pas avoir à la fois <strong>JET_bitIndexTuples</strong> et <strong>JET_bitIndexUnique</strong> défini).</span><span class="sxs-lookup"><span data-stu-id="b1489-156">A tuple index cannot be unique (<em>grbit</em> must not have both <strong>JET_bitIndexTuples</strong> and <strong>JET_bitIndexUnique</strong> set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1489-157">JET_errIndexTuplesOneColumnOnly</span><span class="sxs-lookup"><span data-stu-id="b1489-157">JET_errIndexTuplesOneColumnOnly</span></span></p></td>
<td><p><span data-ttu-id="b1489-158">S’applique aux versions de Windows à partir de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b1489-158">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="b1489-159">Un index de tuple ne peut être que sur une seule colonne (autrement dit, le membre <strong>Grbit</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> a <strong>JET_bitIndexTuples</strong> jeu et le membre <strong>szKey</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> spécifie plusieurs colonnes).</span><span class="sxs-lookup"><span data-stu-id="b1489-159">A tuple index can only be over a single column (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has <strong>JET_bitIndexTuples</strong> set, and the <strong>szKey</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure specifies more than one column).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1489-160">JET_errIndexTuplesSecondaryIndexOnly</span><span class="sxs-lookup"><span data-stu-id="b1489-160">JET_errIndexTuplesSecondaryIndexOnly</span></span></p></td>
<td><p><span data-ttu-id="b1489-161">S’applique aux versions de Windows à partir de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b1489-161">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="b1489-162">Un index de tuple ne peut pas être un index primaire (autrement dit, le membre <strong>Grbit</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ne doit pas avoir <strong>JET_bitIndexPrimary</strong> et <strong>JET_bitIndexTuples</strong> défini).</span><span class="sxs-lookup"><span data-stu-id="b1489-162">A tuple index cannot be a primary index (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not have both <strong>JET_bitIndexPrimary</strong> and <strong>JET_bitIndexTuples</strong> set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1489-163">JET_errIndexTuplesTextColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="b1489-163">JET_errIndexTuplesTextColumnsOnly</span></span></p></td>
<td><p><span data-ttu-id="b1489-164">S’applique aux versions de Windows à partir de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b1489-164">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="b1489-165">Un index de tuple ne peut être que sur une colonne de type texte ou Unicode.</span><span class="sxs-lookup"><span data-stu-id="b1489-165">A tuple index can only be on a text or Unicode column.</span></span> <span data-ttu-id="b1489-166">Si vous tentez d’indexer d’autres colonnes (par exemple, des colonnes binaires), <strong>JET_errIndexTuplesTextColumnsOnly</strong>.</span><span class="sxs-lookup"><span data-stu-id="b1489-166">An attempt to index other columns (for example, binary columns) will result in <strong>JET_errIndexTuplesTextColumnsOnly</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1489-167">JET_errIndexTuplesVarSegMacNotAllowed</span><span class="sxs-lookup"><span data-stu-id="b1489-167">JET_errIndexTuplesVarSegMacNotAllowed</span></span></p></td>
<td><p><span data-ttu-id="b1489-168">S’applique aux versions de Windows à partir de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b1489-168">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="b1489-169">Un index de tuple n’autorise pas la définition du membre <strong>cbVarSegMac</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="b1489-169">A tuple index does not allow the <strong>cbVarSegMac</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure to be set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1489-170">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="b1489-170">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="b1489-171">Une tentative de création d’un index sans informations de version a été effectuée dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="b1489-171">An attempt was made to create an index without version information while in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1489-172">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="b1489-172">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="b1489-173">La définition de l’index n’est pas valide, car le membre <strong>Grbit</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> contient des valeurs incohérentes.</span><span class="sxs-lookup"><span data-stu-id="b1489-173">The index definition is invalid because the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure contains inconsistent values.</span></span> <span data-ttu-id="b1489-174">Voici quelques raisons possibles :</span><span class="sxs-lookup"><span data-stu-id="b1489-174">The following are some possible reasons:</span></span></p>
<ul>
<li><p><span data-ttu-id="b1489-175">Un index principal avait un bit ignore spécifié (JET_bitIndexPrimary a été passé avec l’un des <strong>JET_bitIndexIgnoreNull</strong>, <strong>JET_bitIndexIgnoreAnyNull</strong>ou <strong>JET_bitIndexIgnoreFirstNull</strong>).</span><span class="sxs-lookup"><span data-stu-id="b1489-175">A primary index had an ignore bit specified (JET_bitIndexPrimary was passed with one of <strong>JET_bitIndexIgnoreNull</strong>, <strong>JET_bitIndexIgnoreAnyNull</strong>, or <strong>JET_bitIndexIgnoreFirstNull</strong>).</span></span></p></li>
<li><p><span data-ttu-id="b1489-176">Un index vide n’ignore aucun champ null (autrement dit, le membre <strong>Grbit</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> n’a <strong>JET_bitIndexEmpty</strong> défini, mais n’a pas de <strong>JET_bitIndexIgnoreAnyNull</strong> défini).</span><span class="sxs-lookup"><span data-stu-id="b1489-176">An empty index does not ignore any null fields (that is, <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has <strong>JET_bitIndexEmpty</strong> set, but does not have <strong>JET_bitIndexIgnoreAnyNull</strong> set).</span></span></p></li>
<li><p><span data-ttu-id="b1489-177">Passage d’une structure <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> avec un membre <strong>Grbit</strong> non valide.</span><span class="sxs-lookup"><span data-stu-id="b1489-177">Passing in a <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> structure with an invalid <strong>grbit</strong> member.</span></span> <span data-ttu-id="b1489-178">Consultez <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>.</span><span class="sxs-lookup"><span data-stu-id="b1489-178">See <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>.</span></span></p></li>
</ul>
<p><span data-ttu-id="b1489-179">Lors de la création de plusieurs index à la fois (autrement dit, si le paramètre <em>cIndexCreate</em> est supérieur à un), aucun des index ne peut contenir l’un des bits suivants :</span><span class="sxs-lookup"><span data-stu-id="b1489-179">When creating several indexes at once (that is, if the <em>cIndexCreate</em> parameter is greater than one), none of the indexes may contain any of the following bits:</span></span></p>
<ul>
<li><p><span data-ttu-id="b1489-180"><strong>JET_bitIndexPrimary</strong></span><span class="sxs-lookup"><span data-stu-id="b1489-180"><strong>JET_bitIndexPrimary</strong></span></span></p></li>
<li><p><span data-ttu-id="b1489-181"><strong>JET_bitIndexUnversioned</strong></span><span class="sxs-lookup"><span data-stu-id="b1489-181"><strong>JET_bitIndexUnversioned</strong></span></span></p></li>
<li><p><span data-ttu-id="b1489-182"><strong>JET_bitIndexEmpty</strong></span><span class="sxs-lookup"><span data-stu-id="b1489-182"><strong>JET_bitIndexEmpty</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1489-183">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="b1489-183">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="b1489-184">Un ID de paramètres régionaux (LCID) non valide a été passé (par le biais du membre <strong>LCID</strong> dans la structure <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> , que le membre <strong>pidxunicode</strong> dans la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> contient un pointeur vers ou via le membre <strong>LCID</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ).</span><span class="sxs-lookup"><span data-stu-id="b1489-184">An invalid Locale ID (LCID) was passed in (either through the <strong>lcid</strong> member in the <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> structure, which the <strong>pidxunicode</strong> member in the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure contains a pointer to, or through the <strong>lcid</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1489-185">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="b1489-185">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="b1489-186">Un nom d’index non valide a été spécifié.</span><span class="sxs-lookup"><span data-stu-id="b1489-186">An invalid index name was specified.</span></span> <span data-ttu-id="b1489-187">Pour plus d’informations, consultez <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="b1489-187">See <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> for more details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1489-188">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="b1489-188">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="b1489-189">Un paramètre non valide a été passé dans l’API.</span><span class="sxs-lookup"><span data-stu-id="b1489-189">An invalid parameter was passed into the API.</span></span> <span data-ttu-id="b1489-190">Voici quelques raisons pour lesquelles cette erreur peut être retournée :</span><span class="sxs-lookup"><span data-stu-id="b1489-190">The following are some reasons why this error may be returned:</span></span></p>
<ul>
<li><p><span data-ttu-id="b1489-191">Le champ <strong>cbKey</strong> d’une structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> a la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="b1489-191">The <strong>cbKey</strong> field of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is set to zero.</span></span></p></li>
<li><p><span data-ttu-id="b1489-192">Le membre <strong>cbStruct</strong> d’une structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> n’a pas la valeur sizeof (JET_INDEXCREATE2).</span><span class="sxs-lookup"><span data-stu-id="b1489-192">The <strong>cbStruct</strong> member of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is not set to sizeof(JET_INDEXCREATE2).</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1489-193">JET_errUnicodeTranslationFail</span><span class="sxs-lookup"><span data-stu-id="b1489-193">JET_errUnicodeTranslationFail</span></span></p></td>
<td><p><span data-ttu-id="b1489-194">Une erreur s’est produite lors de la normalisation d’une colonne Unicode.</span><span class="sxs-lookup"><span data-stu-id="b1489-194">An error occurred while trying to normalize a Unicode column.</span></span> <span data-ttu-id="b1489-195">Cela peut être dû à un manque de ressources système.</span><span class="sxs-lookup"><span data-stu-id="b1489-195">This can be caused by running out of system resources.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1489-196">JET_errSpaceHintsInvalid</span><span class="sxs-lookup"><span data-stu-id="b1489-196">JET_errSpaceHintsInvalid</span></span></p></td>
<td><p><span data-ttu-id="b1489-197">Un élément de la structure d’indicateurs d’espace JET n’est pas correct ou n’est pas exploitable.</span><span class="sxs-lookup"><span data-stu-id="b1489-197">An element of the JET space hints structure was not correct or actionable.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="b1489-198">Notes</span><span class="sxs-lookup"><span data-stu-id="b1489-198">Remarks</span></span>

<span data-ttu-id="b1489-199">La fonction **JetCreateIndex4W** itère au sein des index fournis dans le paramètre *pindexcreate* et s’arrête parfois lors du premier échec.</span><span class="sxs-lookup"><span data-stu-id="b1489-199">The **JetCreateIndex4W** function iterates through the indexes given in the *pindexcreate* parameter, and will sometimes abort on the first failure.</span></span> <span data-ttu-id="b1489-200">Les index qui suivent le premier index avec une erreur n’ont peut-être pas été tentés, même si le membre **Err** de la structure [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) contient des JET_errSuccess.</span><span class="sxs-lookup"><span data-stu-id="b1489-200">Any indexes after the first index with an error may not have been attempted, even though the **err** member of the [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) structure contains JET_errSuccess.</span></span>

#### <a name="requirements"></a><span data-ttu-id="b1489-201">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b1489-201">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b1489-202"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="b1489-202"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="b1489-203">Requiert Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b1489-203">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1489-204"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="b1489-204"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="b1489-205">Requiert Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="b1489-205">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1489-206"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="b1489-206"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="b1489-207">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="b1489-207">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1489-208"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="b1489-208"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="b1489-209">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="b1489-209">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1489-210"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="b1489-210"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="b1489-211">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="b1489-211">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="b1489-212">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b1489-212">See also</span></span>

[<span data-ttu-id="b1489-213">JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="b1489-213">JET_CONDITIONALCOLUMN</span></span>](./jet-conditionalcolumn-structure.md)  
[<span data-ttu-id="b1489-214">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="b1489-214">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="b1489-215">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="b1489-215">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="b1489-216">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="b1489-216">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="b1489-217">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="b1489-217">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="b1489-218">JET_INDEXCREATE2</span><span class="sxs-lookup"><span data-stu-id="b1489-218">JET_INDEXCREATE2</span></span>](./jet-indexcreate2-structure.md)  
[<span data-ttu-id="b1489-219">JetCreateIndex</span><span class="sxs-lookup"><span data-stu-id="b1489-219">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="b1489-220">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="b1489-220">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="b1489-221">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="b1489-221">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)  
[<span data-ttu-id="b1489-222">JET_SPACEHINTS</span><span class="sxs-lookup"><span data-stu-id="b1489-222">JET_SPACEHINTS</span></span>](./jet-spacehints-structure.md)
