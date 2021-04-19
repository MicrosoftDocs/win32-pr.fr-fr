---
description: 'En savoir plus sur : fonction JetCreateTable'
title: Fonction JetCreateTable
TOCTitle: JetCreateTable Function
ms:assetid: 28455b8b-0000-4bd5-a3ca-e1ef0446ee07
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269210(v=EXCHG.10)
ms:contentKeyID: 32765513
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateTableW
- JetCreateTable
- JetCreateTableA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6f385cfd668af934bfde2669277db7ed048a1fa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522224"
---
# <a name="jetcreatetable-function"></a><span data-ttu-id="b5e46-103">Fonction JetCreateTable</span><span class="sxs-lookup"><span data-stu-id="b5e46-103">JetCreateTable Function</span></span>


<span data-ttu-id="b5e46-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="b5e46-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreatetable-function"></a><span data-ttu-id="b5e46-105">Fonction JetCreateTable</span><span class="sxs-lookup"><span data-stu-id="b5e46-105">JetCreateTable Function</span></span>

<span data-ttu-id="b5e46-106">La fonction **JetCreateTable** crée une table vide dans une base de données ESE.</span><span class="sxs-lookup"><span data-stu-id="b5e46-106">The **JetCreateTable** function creates an empty table in an ESE database.</span></span>

```cpp
    JET_ERR JET_API JetCreateTable(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName,
      __in          unsigned long lPages,
      __in          unsigned long lDensity,
      __out         JET_TABLEID* ptableid
    );
```

### <a name="parameters"></a><span data-ttu-id="b5e46-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b5e46-107">Parameters</span></span>

<span data-ttu-id="b5e46-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="b5e46-108">*sesid*</span></span>

<span data-ttu-id="b5e46-109">Contexte de la session de base de données à utiliser.</span><span class="sxs-lookup"><span data-stu-id="b5e46-109">The database session context to use.</span></span>

<span data-ttu-id="b5e46-110">*dbid*</span><span class="sxs-lookup"><span data-stu-id="b5e46-110">*dbid*</span></span>

<span data-ttu-id="b5e46-111">Identificateur de base de données à utiliser.</span><span class="sxs-lookup"><span data-stu-id="b5e46-111">The database identifier to use.</span></span>

<span data-ttu-id="b5e46-112">*szTableName*</span><span class="sxs-lookup"><span data-stu-id="b5e46-112">*szTableName*</span></span>

<span data-ttu-id="b5e46-113">Nom de l’index à créer.</span><span class="sxs-lookup"><span data-stu-id="b5e46-113">The name of the index to create.</span></span>

<span data-ttu-id="b5e46-114">Le nom doit être mis en forme conformément aux règles suivantes :</span><span class="sxs-lookup"><span data-stu-id="b5e46-114">The name must be formatted according to the following rules:</span></span>

  - <span data-ttu-id="b5e46-115">Être inférieur à JET_cbNameMost, à l’exclusion de la valeur NULL de fin.</span><span class="sxs-lookup"><span data-stu-id="b5e46-115">Be less than JET_cbNameMost, not including the terminating NULL.</span></span>

  - <span data-ttu-id="b5e46-116">Être constitué du jeu de caractères suivant : de 0 à 9, de A à Z, de a à z et de tous les autres signes de ponctuation, à l’exception de « \! »</span><span class="sxs-lookup"><span data-stu-id="b5e46-116">Be made of the following set of characters: 0 through 9, A through Z, a through z, and all other punctuation except for "\!"</span></span> <span data-ttu-id="b5e46-117">(point d’exclamation), « , » (virgule), « \[ » (crochet ouvrant) et « \] » (crochet fermant), c’est-à-dire les caractères ASCII 0x20, 0X22 à 0x2D, 0x2F à 0x5A, 0x5c, 0x5d à 0x7F.</span><span class="sxs-lookup"><span data-stu-id="b5e46-117">(exclamation point), "," (comma), "\[" (opening bracket), and "\]" (closing bracket) — that is, ASCII characters 0x20, 0x22 through 0x2d, 0x2f through 0x5a, 0x5c, 0x5d through 0x7f.</span></span>

  - <span data-ttu-id="b5e46-118">Ne commence pas par un espace.</span><span class="sxs-lookup"><span data-stu-id="b5e46-118">Not begin with a space.</span></span>

  - <span data-ttu-id="b5e46-119">Être constitué d’au moins un caractère autre qu’un espace.</span><span class="sxs-lookup"><span data-stu-id="b5e46-119">Be made of at least one non-space character.</span></span>

<span data-ttu-id="b5e46-120">*lPages*</span><span class="sxs-lookup"><span data-stu-id="b5e46-120">*lPages*</span></span>

<span data-ttu-id="b5e46-121">Nombre initial de pages de base de données à allouer pour la table.</span><span class="sxs-lookup"><span data-stu-id="b5e46-121">The initial number of database pages to allocate for the table.</span></span> <span data-ttu-id="b5e46-122">La spécification d’un nombre supérieur à un peut réduire la fragmentation si de nombreuses lignes sont insérées dans cette table.</span><span class="sxs-lookup"><span data-stu-id="b5e46-122">Specifying a number larger than one can reduce fragmentation if many rows are inserted into this table.</span></span>

<span data-ttu-id="b5e46-123">*lDensity*</span><span class="sxs-lookup"><span data-stu-id="b5e46-123">*lDensity*</span></span>

<span data-ttu-id="b5e46-124">Densité de la table, en points de pourcentage.</span><span class="sxs-lookup"><span data-stu-id="b5e46-124">The table density, in percentage points.</span></span> <span data-ttu-id="b5e46-125">Le nombre doit être égal à 0 ou compris entre 20 et 100.</span><span class="sxs-lookup"><span data-stu-id="b5e46-125">The number must be either 0 or in the range of 20 through 100.</span></span> <span data-ttu-id="b5e46-126">Le passage de 0 signifie que la valeur par défaut doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="b5e46-126">Passing 0 means that the default value should be used.</span></span> <span data-ttu-id="b5e46-127">La valeur par défaut est 80.</span><span class="sxs-lookup"><span data-stu-id="b5e46-127">The default is 80.</span></span>

<span data-ttu-id="b5e46-128">*pTableID*</span><span class="sxs-lookup"><span data-stu-id="b5e46-128">*ptableid*</span></span>

<span data-ttu-id="b5e46-129">En cas de réussite, l’identificateur de table est retourné dans ce champ.</span><span class="sxs-lookup"><span data-stu-id="b5e46-129">On success, the table identifier is returned in this field.</span></span> <span data-ttu-id="b5e46-130">La valeur n’est pas définie si l’API ne retourne pas JET_errSuccess.</span><span class="sxs-lookup"><span data-stu-id="b5e46-130">The value is undefined if the API does not return JET_errSuccess.</span></span>

### <a name="return-value"></a><span data-ttu-id="b5e46-131">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b5e46-131">Return Value</span></span>

<span data-ttu-id="b5e46-132">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="b5e46-132">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="b5e46-133">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="b5e46-133">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b5e46-134">Code de retour</span><span class="sxs-lookup"><span data-stu-id="b5e46-134">Return code</span></span></p></th>
<th><p><span data-ttu-id="b5e46-135">Description</span><span class="sxs-lookup"><span data-stu-id="b5e46-135">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b5e46-136">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="b5e46-136">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="b5e46-137">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="b5e46-137">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5e46-138">JET_errCallbackNotResolved</span><span class="sxs-lookup"><span data-stu-id="b5e46-138">JET_errCallbackNotResolved</span></span></p></td>
<td><p><span data-ttu-id="b5e46-139">La fonction de rappel n’a pas pu être résolue.</span><span class="sxs-lookup"><span data-stu-id="b5e46-139">The callback function could not be resolved.</span></span> <span data-ttu-id="b5e46-140">La DLL n’a peut-être pas été trouvée, ou la fonction dans la DLL n’a peut-être pas été trouvée.</span><span class="sxs-lookup"><span data-stu-id="b5e46-140">The DLL might not have been found, or the function in the DLL might not have been found.</span></span> <span data-ttu-id="b5e46-141">Une fois la journalisation suffisante activée, le journal des événements fournit plus de détails.</span><span class="sxs-lookup"><span data-stu-id="b5e46-141">With sufficient logging enabled, the event log will provide more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5e46-142">JET_errCannotIndex</span><span class="sxs-lookup"><span data-stu-id="b5e46-142">JET_errCannotIndex</span></span></p></td>
<td><p><span data-ttu-id="b5e46-143">Une tentative d’indexation sur une colonne de dépôt/mise à jour ou SLV (Notez que les colonnes SLV sont dépréciées) a été tentée.</span><span class="sxs-lookup"><span data-stu-id="b5e46-143">An attempt was made to index over an escrow-update or SLV column (note that SLV columns are deprecated).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5e46-144">JET_errCannotNestDDL</span><span class="sxs-lookup"><span data-stu-id="b5e46-144">JET_errCannotNestDDL</span></span></p></td>
<td><p><span data-ttu-id="b5e46-145">Si ptablecreate- &gt; Grbit spécifie JET_bitTableCreateTemplateTable, mais ptablecreate- &gt; szTemplateTableName a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="b5e46-145">If ptablecreate-&gt;grbit specifies JET_bitTableCreateTemplateTable, but ptablecreate-&gt;szTemplateTableName is set to NULL.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5e46-146">JET_errColumnDuplicate</span><span class="sxs-lookup"><span data-stu-id="b5e46-146">JET_errColumnDuplicate</span></span></p></td>
<td><p><span data-ttu-id="b5e46-147">Une colonne existe déjà.</span><span class="sxs-lookup"><span data-stu-id="b5e46-147">A column already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5e46-148">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="b5e46-148">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="b5e46-149">Une tentative d’indexation sur une colonne inexistante a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="b5e46-149">An attempt was made to index over a non-existent column.</span></span> <span data-ttu-id="b5e46-150">Toute tentative d’indexation conditionnelle sur une colonne inexistante peut également générer cette erreur.</span><span class="sxs-lookup"><span data-stu-id="b5e46-150">Attempting to conditionally index over a non-existent column can also produce this error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5e46-151">JET_errColumnRedundant</span><span class="sxs-lookup"><span data-stu-id="b5e46-151">JET_errColumnRedundant</span></span></p></td>
<td><p><span data-ttu-id="b5e46-152">Une tentative d’ajout d’une colonne redondante a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="b5e46-152">An attempt was made to add a redundant column.</span></span> <span data-ttu-id="b5e46-153">Il ne doit y avoir qu’une seule colonne AutoIncrement et pas plus d’une colonne version par table.</span><span class="sxs-lookup"><span data-stu-id="b5e46-153">There should be no more than one autoincrement column, and no more than one version column per table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5e46-154">JET_errDensityInvalid</span><span class="sxs-lookup"><span data-stu-id="b5e46-154">JET_errDensityInvalid</span></span></p></td>
<td><p><span data-ttu-id="b5e46-155">Une densité non valide a été transmise dans le membre <em>ulDensity</em> de la structure <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> ou <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="b5e46-155">An invalid density was passed in the <em>ulDensity</em> member in the <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5e46-156">JET_errDDLNotInheritable</span><span class="sxs-lookup"><span data-stu-id="b5e46-156">JET_errDDLNotInheritable</span></span></p></td>
<td><p><span data-ttu-id="b5e46-157">Signifie que la table nommée dans le membre <strong>szTemplateTableName</strong> de la structure <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> n’était pas marquée comme table de modèle (autrement dit, cette table n’avait pas de JET_bitTableCreateTemplateTable définie).</span><span class="sxs-lookup"><span data-stu-id="b5e46-157">Signifies that the table named in the <strong>szTemplateTableName</strong> member of the <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> structure was not a marked as a template table (that is, that table did not have JET_bitTableCreateTemplateTable set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5e46-158">JET_errIndexDuplicate</span><span class="sxs-lookup"><span data-stu-id="b5e46-158">JET_errIndexDuplicate</span></span></p></td>
<td><p><span data-ttu-id="b5e46-159">Une tentative de définition de deux index identiques a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="b5e46-159">An attempt was made to define two identical indexes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5e46-160">JET_errIndexHasPrimary</span><span class="sxs-lookup"><span data-stu-id="b5e46-160">JET_errIndexHasPrimary</span></span></p></td>
<td><p><span data-ttu-id="b5e46-161">Une tentative a été effectuée pour spécifier plusieurs index primaires pour une table.</span><span class="sxs-lookup"><span data-stu-id="b5e46-161">An attempt was made to specify more than one primary index for a table.</span></span> <span data-ttu-id="b5e46-162">Une table doit avoir un seul index primaire.</span><span class="sxs-lookup"><span data-stu-id="b5e46-162">A table must have exactly one primary index.</span></span> <span data-ttu-id="b5e46-163">Si aucun index primaire n’est spécifié, le moteur de base de données en crée un en toute transparence.</span><span class="sxs-lookup"><span data-stu-id="b5e46-163">If no primary index is specified, the database engine will transparently create one.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5e46-164">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="b5e46-164">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="b5e46-165">Une définition d’index non valide a été spécifiée.</span><span class="sxs-lookup"><span data-stu-id="b5e46-165">An invalid index definition was specified.</span></span> <span data-ttu-id="b5e46-166">Voici quelques-unes des raisons possibles de la réception de cette erreur :</span><span class="sxs-lookup"><span data-stu-id="b5e46-166">Some of the possible reasons for receiving this error are:</span></span></p>
<ul>
<li><p><span data-ttu-id="b5e46-167">Un index principal est conditionnel (autrement dit, le membre <strong>Grbit</strong> de la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> a JET_bitIndexPrimary jeu et le membre <strong>cConditionalColumn</strong> de la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> est supérieur à zéro).</span><span class="sxs-lookup"><span data-stu-id="b5e46-167">A primary index is conditional (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexPrimary set, and <strong>cConditionalColumn</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is greater than zero).</span></span></p></li>
<li><p><span data-ttu-id="b5e46-168">Windows Server 2003 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="b5e46-168">Windows Server 2003 and later.</span></span> <span data-ttu-id="b5e46-169">La tentative de création d’un index de tuple avec des limites de tuple, mais sans passer le membre <strong>ptuplelimits</strong> dans la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> (autrement dit, le membre <strong>Grbit</strong> de la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> a JET_bitIndexTupleLimits défini, mais le pointeur <strong>ptuplelimits</strong> a la valeur null).</span><span class="sxs-lookup"><span data-stu-id="b5e46-169">Attempting to create a tuple index with tuple limits, but without passing the <strong>ptuplelimits</strong> member in the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexTupleLimits set, but the <strong>ptuplelimits</strong> pointer is NULL).</span></span></p></li>
<li><p><span data-ttu-id="b5e46-170">Passage d’une définition de clé non valide dans le membre <strong>szKey</strong> de la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="b5e46-170">Passing in an invalid key definition in the <strong>szKey</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure.</span></span> <span data-ttu-id="b5e46-171">Pour plus d’informations sur les définitions valides, consultez <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="b5e46-171">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for a discussion of valid definitions.</span></span></p></li>
<li><p><span data-ttu-id="b5e46-172">La définition du membre <strong>cbVarSegMac</strong> dans <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> est supérieure à JET_cbPrimaryKeyMost (pour un index principal) ou supérieure à JET_cbSecondaryKeyMost (pour un index secondaire).</span><span class="sxs-lookup"><span data-stu-id="b5e46-172">Setting the <strong>cbVarSegMac</strong> member in <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> to be greater than JET_cbPrimaryKeyMost (for a primary index) or greater than JET_cbSecondaryKeyMost (for a secondary index).</span></span></p></li>
<li><p><span data-ttu-id="b5e46-173">Passage d’une combinaison non valide pour un index Unicode défini par l’utilisateur (un qui a le bit JET_bitIndexUnicode défini dans le membre <strong>Grbit</strong> de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>).</span><span class="sxs-lookup"><span data-stu-id="b5e46-173">Passing an invalid combination for a user-defined Unicode index (one which has the JET_bitIndexUnicode bit set in the <strong>grbit</strong> member of <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>).</span></span> <span data-ttu-id="b5e46-174">Certaines causes courantes incluent le membre <strong>pidxunicode</strong> de la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> a la valeur null, ou le LCID spécifié dans la structure <strong>pidxunicode</strong> n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="b5e46-174">Some common causes include the <strong>pidxunicode</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is NULL, or the LCID specified in the <strong>pidxunicode</strong> structure is invalid.</span></span></p></li>
<li><p><span data-ttu-id="b5e46-175">Spécification d’une colonne à valeurs multiples pour un index primaire.</span><span class="sxs-lookup"><span data-stu-id="b5e46-175">Specifying a multi-valued column for a primary index.</span></span></p></li>
<li><p><span data-ttu-id="b5e46-176">Tentative d’indexation d’un trop grand nombre de colonnes conditionnelles.</span><span class="sxs-lookup"><span data-stu-id="b5e46-176">Trying to index too many conditional columns.</span></span> <span data-ttu-id="b5e46-177">Le membre <strong>cConditionalColumn</strong> de la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ne doit pas être supérieur à JET_ccolKeyMost.</span><span class="sxs-lookup"><span data-stu-id="b5e46-177">The <strong>cConditionalColumn</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure must not be greater than JET_ccolKeyMost.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5e46-178">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="b5e46-178">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="b5e46-179">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="b5e46-179">Windows XP and later.</span></span> <span data-ttu-id="b5e46-180">Une structure de <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> a été spécifiée et ses limites ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="b5e46-180">A <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure was specified, and its limits are not supported.</span></span> <span data-ttu-id="b5e46-181">Consultez la section Notes de la structure <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</span><span class="sxs-lookup"><span data-stu-id="b5e46-181">See the remarks section of the <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5e46-182">JET_errIndexTuplesNonUniqueOnly</span><span class="sxs-lookup"><span data-stu-id="b5e46-182">JET_errIndexTuplesNonUniqueOnly</span></span></p></td>
<td><p><span data-ttu-id="b5e46-183">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="b5e46-183">Windows XP and later.</span></span> <span data-ttu-id="b5e46-184">Un index de tuple ne peut pas être unique (autrement dit, le membre <em>Grbit</em> de la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ne doit pas avoir JET_bitIndexPrimary et JET_bitIndexUnique défini).</span><span class="sxs-lookup"><span data-stu-id="b5e46-184">A tuple index cannot be unique (that is, the <em>grbit</em> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexUnique set).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5e46-185">JET_errIndexTuplesOneColumnOnly</span><span class="sxs-lookup"><span data-stu-id="b5e46-185">JET_errIndexTuplesOneColumnOnly</span></span></p></td>
<td><p><span data-ttu-id="b5e46-186">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="b5e46-186">Windows XP and later.</span></span> <span data-ttu-id="b5e46-187">Un index de tuple ne peut être que sur une seule colonne (autrement dit, si le membre <strong>Grbit</strong> de la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> a JET_bitIndexTuples jeu et que le membre <strong>szKey</strong> de la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> spécifie plusieurs colonnes).</span><span class="sxs-lookup"><span data-stu-id="b5e46-187">A tuple index can only be over a single column (that is, if the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexTuples set, and the <strong>szKey</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure specifies more than one column).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5e46-188">JET_errIndexTuplesSecondaryIndexOnly</span><span class="sxs-lookup"><span data-stu-id="b5e46-188">JET_errIndexTuplesSecondaryIndexOnly</span></span></p></td>
<td><p><span data-ttu-id="b5e46-189">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="b5e46-189">Windows XP and later.</span></span> <span data-ttu-id="b5e46-190">Un index de tuple ne peut pas être un index primaire (autrement dit, le membre <strong>Grbit</strong> de la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ne doit pas avoir JET_bitIndexPrimary et JET_bitIndexTuples défini).</span><span class="sxs-lookup"><span data-stu-id="b5e46-190">A tuple index cannot be a primary index (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexTuples set).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5e46-191">JET_errIndexTuplesVarSegMacNotAllowed</span><span class="sxs-lookup"><span data-stu-id="b5e46-191">JET_errIndexTuplesVarSegMacNotAllowed</span></span></p></td>
<td><p><span data-ttu-id="b5e46-192">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="b5e46-192">Windows XP and later.</span></span> <span data-ttu-id="b5e46-193">Un index de tuple n’autorise pas la définition du membre <strong>cbVarSegMac</strong> de la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="b5e46-193">A tuple index does not allow the <strong>cbVarSegMac</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure to be set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5e46-194">JET_errIndexTuplesTextColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="b5e46-194">JET_errIndexTuplesTextColumnsOnly</span></span></p></td>
<td><p><span data-ttu-id="b5e46-195">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="b5e46-195">Windows XP and later.</span></span> <span data-ttu-id="b5e46-196">Un index de tuple ne peut être que sur une colonne de type texte ou Unicode.</span><span class="sxs-lookup"><span data-stu-id="b5e46-196">A tuple index can only be on a text or Unicode column.</span></span> <span data-ttu-id="b5e46-197">Toute tentative d’index d’autres colonnes (telles que des colonnes binaires) entraîne JET_errIndexTuplesTextColumnsOnly.</span><span class="sxs-lookup"><span data-stu-id="b5e46-197">An attempt to index other columns (such as binary columns) will result in JET_errIndexTuplesTextColumnsOnly.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5e46-198">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="b5e46-198">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="b5e46-199">Une tentative de création d’un index sans informations de version a été effectuée dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="b5e46-199">An attempt was made to create an index without version information while in a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5e46-200">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="b5e46-200">JET_errInvalidCodePage</span></span></p></td>
<td><p><span data-ttu-id="b5e46-201">Le membre <strong>CP</strong> de la structure <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> n’a pas été défini sur une page de codes valide.</span><span class="sxs-lookup"><span data-stu-id="b5e46-201">The <strong>cp</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure was not set to a valid code page.</span></span> <span data-ttu-id="b5e46-202">Les seules valeurs valides pour les colonnes de texte sont l’anglais (1252) et Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="b5e46-202">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="b5e46-203">La valeur 0 signifie que la valeur par défaut sera utilisée (anglais, 1252).</span><span class="sxs-lookup"><span data-stu-id="b5e46-203">A value of 0 means the default will be used (English, 1252).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5e46-204">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="b5e46-204">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="b5e46-205">Le membre <strong>coltyp</strong> de la structure <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> n’a pas été défini sur un type de colonne valide.</span><span class="sxs-lookup"><span data-stu-id="b5e46-205">The <strong>coltyp</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure was not set to a valid column type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5e46-206">JET_errInvalidCreateIndex</span><span class="sxs-lookup"><span data-stu-id="b5e46-206">JET_errInvalidCreateIndex</span></span></p></td>
<td><p><span data-ttu-id="b5e46-207">Cette erreur peut se produire pour les raisons suivantes :</span><span class="sxs-lookup"><span data-stu-id="b5e46-207">Some of the reasons this error may occur:</span></span></p>
<ul>
<li><p><span data-ttu-id="b5e46-208">Le membre <strong>rgindexcreate</strong> de la structure <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="b5e46-208">The <strong>rgindexcreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was set to NULL.</span></span></p></li>
<li><p><span data-ttu-id="b5e46-209">Le membre <strong>rgcolumncreate</strong> de la structure <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="b5e46-209">The <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was set to NULL.</span></span></p></li>
<li><p><span data-ttu-id="b5e46-210">Le membre <strong>cbStruct</strong> d’une structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> n’a pas été défini sur une valeur valide.</span><span class="sxs-lookup"><span data-stu-id="b5e46-210">The <strong>cbStruct</strong> member of a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure was not set to a valid value.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5e46-211">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="b5e46-211">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="b5e46-212">Une combinaison de membres <strong>Grbit</strong> non valide a été spécifiée dans <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> ou <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>.</span><span class="sxs-lookup"><span data-stu-id="b5e46-212">An invalid combination of <strong>grbit</strong> members was specified in <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>.</span></span></p>
<p><span data-ttu-id="b5e46-213">La définition de l’index n’est pas valide, car le membre <strong>Grbit</strong> contient des valeurs incohérentes.</span><span class="sxs-lookup"><span data-stu-id="b5e46-213">The index definition is invalid because the <strong>grbit</strong> member contains inconsistent values.</span></span> <span data-ttu-id="b5e46-214">Voici quelques raisons possibles :</span><span class="sxs-lookup"><span data-stu-id="b5e46-214">Some possible reasons are:</span></span></p>
<ul>
<li><p><span data-ttu-id="b5e46-215">Un index primaire a un bit ignore spécifié (autrement dit, JET_bitIndexPrimary a été passé avec JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull ou JET_bitIndexIgnoreFirstNull).</span><span class="sxs-lookup"><span data-stu-id="b5e46-215">A primary index had an ignore bit specified (that is, JET_bitIndexPrimary was passed with JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull, or JET_bitIndexIgnoreFirstNull).</span></span></p></li>
<li><p><span data-ttu-id="b5e46-216">Un index vide n’ignore pas les membres NULL (autrement dit, le membre <strong>Grbit</strong> de la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> n’a JET_bitIndexEmpty défini, mais n’a pas de JET_bitIndexIgnoreAnyNull défini).</span><span class="sxs-lookup"><span data-stu-id="b5e46-216">An empty index does not ignore any NULL members (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexEmpty set, but does not have JET_bitIndexIgnoreAnyNull set).</span></span></p></li>
<li><p><span data-ttu-id="b5e46-217">Passage d’une structure <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> avec un membre <strong>Grbit</strong> non valide.</span><span class="sxs-lookup"><span data-stu-id="b5e46-217">Passing in a <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> structure with an invalid <strong>grbit</strong> member.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5e46-218">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="b5e46-218">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="b5e46-219">Un ID de paramètres régionaux (LCID) non valide a été transmis (par le biais du membre <strong>LCID</strong> de la structure <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> qui est référencée par le membre <strong>pidxunicode</strong> dans la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ou par le champ <strong>LCID</strong> de la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ).</span><span class="sxs-lookup"><span data-stu-id="b5e46-219">An invalid Locale ID (LCID) was passed in (either through the <strong>lcid</strong> member of the <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> structure which is pointed to by the <strong>pidxunicode</strong> member in the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure, or through the <strong>lcid</strong> field of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5e46-220">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="b5e46-220">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="b5e46-221">Un paramètre non valide a été spécifié.</span><span class="sxs-lookup"><span data-stu-id="b5e46-221">An invalid parameter was given.</span></span> <span data-ttu-id="b5e46-222">Voici quelques raisons possibles :</span><span class="sxs-lookup"><span data-stu-id="b5e46-222">Some possible reasons are:</span></span></p>
<ul>
<li><p><span data-ttu-id="b5e46-223">Le membre <strong>rgcolumncreate</strong> de la structure <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="b5e46-223">The <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure is NULL.</span></span></p></li>
<li><p><span data-ttu-id="b5e46-224">Le membre <strong>cbStruct</strong> de l’une des structures <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> données dans le membre <strong>rgcolumncreate</strong> de la structure <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> n’a pas la valeur sizeof (JET_COLUMNCREATE).</span><span class="sxs-lookup"><span data-stu-id="b5e46-224">The <strong>cbStruct</strong> member of one of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structures given in the <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was not set to sizeof( JET_COLUMNCREATE ).</span></span></p></li>
<li><p><span data-ttu-id="b5e46-225">Le membre <strong>cbKey</strong> d’une structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> a la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="b5e46-225">The <strong>cbKey</strong> member of a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is set to zero.</span></span></p></li>
<li><p><span data-ttu-id="b5e46-226">Le membre <strong>cbStruct</strong> d’une structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> n’a pas la valeur sizeof (JET_INDEXCREATE).</span><span class="sxs-lookup"><span data-stu-id="b5e46-226">The <strong>cbStruct</strong> member of a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is not set to sizeof( JET_INDEXCREATE ).</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5e46-227">JET_errRecordTooBig</span><span class="sxs-lookup"><span data-stu-id="b5e46-227">JET_errRecordTooBig</span></span></p></td>
<td><p><span data-ttu-id="b5e46-228">L’enregistrement est trop volumineux.</span><span class="sxs-lookup"><span data-stu-id="b5e46-228">The record is too big.</span></span> <span data-ttu-id="b5e46-229">La somme du membre <strong>cbMax</strong> de la structure <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> pour toutes les colonnes fixes ne doit pas dépasser une certaine valeur.</span><span class="sxs-lookup"><span data-stu-id="b5e46-229">The sum of the <strong>cbMax</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure for all fixed columns must not exceed a certain value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5e46-230">JET_errTableDuplicate</span><span class="sxs-lookup"><span data-stu-id="b5e46-230">JET_errTableDuplicate</span></span></p></td>
<td><p><span data-ttu-id="b5e46-231">La table existe déjà.</span><span class="sxs-lookup"><span data-stu-id="b5e46-231">The table already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5e46-232">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="b5e46-232">JET_errTooManyColumns</span></span></p></td>
<td><p><span data-ttu-id="b5e46-233">Une tentative d’ajout d’un trop grand nombre de colonnes à la table a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="b5e46-233">An attempt was made to add too many columns to the table.</span></span> <span data-ttu-id="b5e46-234">Une table ne peut pas comporter plus de JET_ccolFixedMost colonnes fixes, ni plus de JET_ccolVarMost colonnes de longueur variable, ni plus de JET_ccolTaggedMost colonnes avec balises.</span><span class="sxs-lookup"><span data-stu-id="b5e46-234">A table can have no more than JET_ccolFixedMost fixed columns, no more than JET_ccolVarMost variable-length columns, and no more than JET_ccolTaggedMost tagged columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5e46-235">JET_errUnicodeTranslationFail</span><span class="sxs-lookup"><span data-stu-id="b5e46-235">JET_errUnicodeTranslationFail</span></span></p></td>
<td><p><span data-ttu-id="b5e46-236">Une erreur s’est produite lors de la normalisation d’une colonne Unicode.</span><span class="sxs-lookup"><span data-stu-id="b5e46-236">An error occurred attempting to normalize a Unicode column.</span></span> <span data-ttu-id="b5e46-237">Cela peut être dû à un manque de ressources système.</span><span class="sxs-lookup"><span data-stu-id="b5e46-237">This can be caused by running out of system resources.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="b5e46-238">Notes</span><span class="sxs-lookup"><span data-stu-id="b5e46-238">Remarks</span></span>

<span data-ttu-id="b5e46-239">**JetCreateTable** crée une table qui ne contient aucune colonne.</span><span class="sxs-lookup"><span data-stu-id="b5e46-239">**JetCreateTable** creates a table which does not contain any columns.</span></span> <span data-ttu-id="b5e46-240">Pour ajouter des colonnes, consultez [JetAddColumn](./jetaddcolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="b5e46-240">To add columns, see [JetAddColumn](./jetaddcolumn-function.md).</span></span>

<span data-ttu-id="b5e46-241">En interne, **JetCreateTable** appelle [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md), en remplissant une structure [JET_TABLECREATE2](./jet-tablecreate2-structure.md) avec :</span><span class="sxs-lookup"><span data-stu-id="b5e46-241">Internally, **JetCreateTable** calls [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md), filling in a [JET_TABLECREATE2](./jet-tablecreate2-structure.md) structure with:</span></span>

  - <span data-ttu-id="b5e46-242">JET_TABLECREATE2. cbStruct = sizeof (JET_TABLECREATE2)</span><span class="sxs-lookup"><span data-stu-id="b5e46-242">JET_TABLECREATE2.cbStruct = sizeof( JET_TABLECREATE2 )</span></span>

  - <span data-ttu-id="b5e46-243">JET_TABLECREATE2. szTableName = szTableName</span><span class="sxs-lookup"><span data-stu-id="b5e46-243">JET_TABLECREATE2.szTableName = szTableName</span></span>

  - <span data-ttu-id="b5e46-244">JET_TABLECREATE2. ulPages = lPage</span><span class="sxs-lookup"><span data-stu-id="b5e46-244">JET_TABLECREATE2.ulPages = lPage</span></span>

  - <span data-ttu-id="b5e46-245">JET_TABLECREATE2. ulDensity = lDensity</span><span class="sxs-lookup"><span data-stu-id="b5e46-245">JET_TABLECREATE2.ulDensity = lDensity</span></span>

  - <span data-ttu-id="b5e46-246">JET_TABLECREATE2. TableId = JET_tableidNil</span><span class="sxs-lookup"><span data-stu-id="b5e46-246">JET_TABLECREATE2.tableid = JET_tableidNil</span></span>

<span data-ttu-id="b5e46-247">Tous les autres champs de la structure interne [JET_TABLECREATE2](./jet-tablecreate2-structure.md) sont définis sur zéro ou null.</span><span class="sxs-lookup"><span data-stu-id="b5e46-247">All the other fields of the internal [JET_TABLECREATE2](./jet-tablecreate2-structure.md) structure are set to zero or NULL.</span></span> <span data-ttu-id="b5e46-248">Lors de la sortie, *pTableID* est défini sur JET_TABLECREATE2. TableId.</span><span class="sxs-lookup"><span data-stu-id="b5e46-248">On output, *ptableid* will be set to JET_TABLECREATE2.tableid.</span></span>

<span data-ttu-id="b5e46-249">Pour plus d’informations, consultez [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md) .</span><span class="sxs-lookup"><span data-stu-id="b5e46-249">See [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md) for more details.</span></span>

<span data-ttu-id="b5e46-250">Comme [JetOpenTable](./jetopentable-function.md), lorsque l’application est effectuée à l’aide du membre **TableID** renvoyé à partir de la structure [JET_TABLECREATE2](./jet-tablecreate2-structure.md) , elle doit généralement être fermée avec [JetCloseTable](./jetclosetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="b5e46-250">Like [JetOpenTable](./jetopentable-function.md), when the application is done using the returned **tableid** member from the [JET_TABLECREATE2](./jet-tablecreate2-structure.md) structure, it should usually be closed with [JetCloseTable](./jetclosetable-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="b5e46-251">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b5e46-251">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b5e46-252"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="b5e46-252"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="b5e46-253">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="b5e46-253">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5e46-254"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="b5e46-254"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="b5e46-255">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="b5e46-255">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5e46-256"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="b5e46-256"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="b5e46-257">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="b5e46-257">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5e46-258"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="b5e46-258"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="b5e46-259">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="b5e46-259">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5e46-260"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="b5e46-260"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="b5e46-261">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="b5e46-261">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5e46-262"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="b5e46-262"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="b5e46-263">Implémenté en tant que <strong>JetCreateTableW</strong> (Unicode) et <strong>JetCreateTableA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="b5e46-263">Implemented as <strong>JetCreateTableW</strong> (Unicode) and <strong>JetCreateTableA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="b5e46-264">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5e46-264">See Also</span></span>

[<span data-ttu-id="b5e46-265">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="b5e46-265">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="b5e46-266">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="b5e46-266">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="b5e46-267">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="b5e46-267">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="b5e46-268">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="b5e46-268">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="b5e46-269">JET_TABLECREATE2</span><span class="sxs-lookup"><span data-stu-id="b5e46-269">JET_TABLECREATE2</span></span>](./jet-tablecreate2-structure.md)  
[<span data-ttu-id="b5e46-270">JetAddColumn</span><span class="sxs-lookup"><span data-stu-id="b5e46-270">JetAddColumn</span></span>](./jetaddcolumn-function.md)  
[<span data-ttu-id="b5e46-271">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="b5e46-271">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="b5e46-272">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="b5e46-272">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)
