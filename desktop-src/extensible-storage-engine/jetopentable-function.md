---
description: 'En savoir plus sur : fonction JetOpenTable'
title: Fonction JetOpenTable
TOCTitle: JetOpenTable Function
ms:assetid: ded6348c-a82a-49bc-8a5d-e40ed5d6315c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294118(v=EXCHG.10)
ms:contentKeyID: 32765732
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenTable
- JetOpenTableW
- JetOpenTableA
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7a3ffe9490b75606910c5867d3e8b59d9a8c520d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749708"
---
# <a name="jetopentable-function"></a><span data-ttu-id="400a6-103">Fonction JetOpenTable</span><span class="sxs-lookup"><span data-stu-id="400a6-103">JetOpenTable Function</span></span>


<span data-ttu-id="400a6-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="400a6-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetopentable-function"></a><span data-ttu-id="400a6-105">Fonction JetOpenTable</span><span class="sxs-lookup"><span data-stu-id="400a6-105">JetOpenTable Function</span></span>

<span data-ttu-id="400a6-106">La fonction **JetOpenTable** ouvre un curseur sur une table créée précédemment.</span><span class="sxs-lookup"><span data-stu-id="400a6-106">The **JetOpenTable** function opens a cursor on a previously created table.</span></span>

```cpp
    JET_ERR JET_API JetOpenTable(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName,
      __in_opt      const void* pvParameters,
      __in          unsigned long cbParameters,
      __in          JET_GRBIT grbit,
      __out         JET_TABLEID* ptableid
    );
```

### <a name="parameters"></a><span data-ttu-id="400a6-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="400a6-107">Parameters</span></span>

<span data-ttu-id="400a6-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="400a6-108">*sesid*</span></span>

<span data-ttu-id="400a6-109">Contexte de la session de base de données à utiliser.</span><span class="sxs-lookup"><span data-stu-id="400a6-109">The database session context to use.</span></span>

<span data-ttu-id="400a6-110">*dbid*</span><span class="sxs-lookup"><span data-stu-id="400a6-110">*dbid*</span></span>

<span data-ttu-id="400a6-111">Identificateur de base de données à utiliser pour rechercher la table.</span><span class="sxs-lookup"><span data-stu-id="400a6-111">The database identifier to use to find the table.</span></span>

<span data-ttu-id="400a6-112">*szTableName*</span><span class="sxs-lookup"><span data-stu-id="400a6-112">*szTableName*</span></span>

<span data-ttu-id="400a6-113">Nom de la table à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="400a6-113">The name of the table to open.</span></span>

<span data-ttu-id="400a6-114">*pvParameters*</span><span class="sxs-lookup"><span data-stu-id="400a6-114">*pvParameters*</span></span>

<span data-ttu-id="400a6-115">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="400a6-115">Deprecated.</span></span> <span data-ttu-id="400a6-116">Affectez la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="400a6-116">Set to **NULL**.</span></span>

<span data-ttu-id="400a6-117">*cbParameters*</span><span class="sxs-lookup"><span data-stu-id="400a6-117">*cbParameters*</span></span>

<span data-ttu-id="400a6-118">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="400a6-118">Deprecated.</span></span> <span data-ttu-id="400a6-119">Défini sur 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="400a6-119">Set to 0 (zero).</span></span>

<span data-ttu-id="400a6-120">*grbit*</span><span class="sxs-lookup"><span data-stu-id="400a6-120">*grbit*</span></span>

<span data-ttu-id="400a6-121">Groupe de bits spécifiant zéro ou plusieurs des options suivantes.</span><span class="sxs-lookup"><span data-stu-id="400a6-121">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="400a6-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="400a6-122">Value</span></span></p></th>
<th><p><span data-ttu-id="400a6-123">Signification</span><span class="sxs-lookup"><span data-stu-id="400a6-123">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="400a6-124">JET_bitTableDenyRead</span><span class="sxs-lookup"><span data-stu-id="400a6-124">JET_bitTableDenyRead</span></span></p></td>
<td><p><span data-ttu-id="400a6-125">La table ne peut pas être ouverte pour un accès en lecture par une autre session de base de données.</span><span class="sxs-lookup"><span data-stu-id="400a6-125">The table cannot be opened for read-access by another database session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="400a6-126">JET_bitTableDenyWrite</span><span class="sxs-lookup"><span data-stu-id="400a6-126">JET_bitTableDenyWrite</span></span></p></td>
<td><p><span data-ttu-id="400a6-127">La table ne peut pas être ouverte pour un accès en écriture par une autre session de base de données.</span><span class="sxs-lookup"><span data-stu-id="400a6-127">The table cannot be opened for write-access by another database session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="400a6-128">JET_bitTableNoCache</span><span class="sxs-lookup"><span data-stu-id="400a6-128">JET_bitTableNoCache</span></span></p></td>
<td><p><span data-ttu-id="400a6-129">Ne mettez pas en cache les pages pour cette table.</span><span class="sxs-lookup"><span data-stu-id="400a6-129">Do not cache the pages for this table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="400a6-130">JET_bitTablePermitDDL</span><span class="sxs-lookup"><span data-stu-id="400a6-130">JET_bitTablePermitDDL</span></span></p></td>
<td><p><span data-ttu-id="400a6-131">Autorise la modification DDL sur les tables marquées comme FixedDDL.</span><span class="sxs-lookup"><span data-stu-id="400a6-131">Allows DDL modification on tables flagged as FixedDDL.</span></span> <span data-ttu-id="400a6-132">Cette option doit être utilisée avec l’option JET_bitTableDenyRead.</span><span class="sxs-lookup"><span data-stu-id="400a6-132">This option must be used with the JET_bitTableDenyRead option.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="400a6-133">JET_bitTablePreread</span><span class="sxs-lookup"><span data-stu-id="400a6-133">JET_bitTablePreread</span></span></p></td>
<td><p><span data-ttu-id="400a6-134">Indique que la table n’est probablement pas dans le cache des tampons, et que la prélecture peut être bénéfique pour les performances.</span><span class="sxs-lookup"><span data-stu-id="400a6-134">Provides a hint that the table is probably not in the buffer cache, and that pre-reading may be beneficial to performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="400a6-135">JET_bitTableReadOnly</span><span class="sxs-lookup"><span data-stu-id="400a6-135">JET_bitTableReadOnly</span></span></p></td>
<td><p><span data-ttu-id="400a6-136">Demande l’accès en lecture seule à la table.</span><span class="sxs-lookup"><span data-stu-id="400a6-136">Requests read-only access to the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="400a6-137">JET_bitTableSequential</span><span class="sxs-lookup"><span data-stu-id="400a6-137">JET_bitTableSequential</span></span></p></td>
<td><p><span data-ttu-id="400a6-138">La table doit être préextraite très agressivement du disque, car l’application l’analyse de manière séquentielle.</span><span class="sxs-lookup"><span data-stu-id="400a6-138">The table should be very aggressively prefetched from disk because the application will be scanning it sequentially.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="400a6-139">JET_bitTableUpdatable</span><span class="sxs-lookup"><span data-stu-id="400a6-139">JET_bitTableUpdatable</span></span></p></td>
<td><p><span data-ttu-id="400a6-140">Demande l’accès en écriture à la table.</span><span class="sxs-lookup"><span data-stu-id="400a6-140">Requests write-access to the table.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="400a6-141">*pTableID*</span><span class="sxs-lookup"><span data-stu-id="400a6-141">*ptableid*</span></span>

<span data-ttu-id="400a6-142">En cas de réussite, pointe vers l’identificateur de la table.</span><span class="sxs-lookup"><span data-stu-id="400a6-142">On success, points to the identifier of the table.</span></span> <span data-ttu-id="400a6-143">En cas d’échec, le contenu de *pTableID* n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="400a6-143">On failure, the contents for *ptableid* are undefined.</span></span>

### <a name="return-value"></a><span data-ttu-id="400a6-144">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="400a6-144">Return Value</span></span>

<span data-ttu-id="400a6-145">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="400a6-145">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="400a6-146">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="400a6-146">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="400a6-147">Code de retour</span><span class="sxs-lookup"><span data-stu-id="400a6-147">Return code</span></span></p></th>
<th><p><span data-ttu-id="400a6-148">Description</span><span class="sxs-lookup"><span data-stu-id="400a6-148">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="400a6-149">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="400a6-149">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="400a6-150">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="400a6-150">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="400a6-151">JET_errInvalidDatabaseId</span><span class="sxs-lookup"><span data-stu-id="400a6-151">JET_errInvalidDatabaseId</span></span></p></td>
<td><p><span data-ttu-id="400a6-152"><em>dbid</em> n’est pas un identificateur de base de données valide.</span><span class="sxs-lookup"><span data-stu-id="400a6-152"><em>dbid</em> is not a valid database identifier.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="400a6-153">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="400a6-153">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="400a6-154">Une combinaison incorrecte de <em>Grbit</em> a été transmise.</span><span class="sxs-lookup"><span data-stu-id="400a6-154">A bad combination of <em>grbit</em> was passed in.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="400a6-155">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="400a6-155">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="400a6-156">Le nom donné dans <em>szTableName</em> n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="400a6-156">The name given in <em>szTableName</em> is invalid.</span></span></p>
<p><span data-ttu-id="400a6-157">Pour plus d’informations sur les noms de table valides, consultez le paramètre <em>szTableName</em> dans <a href="gg269210(v=exchg.10).md">JetCreateTable</a>.</span><span class="sxs-lookup"><span data-stu-id="400a6-157">For more information about valid table names, see the <em>szTableName</em> parameter in <a href="gg269210(v=exchg.10).md">JetCreateTable</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="400a6-158">JET_errObjectNotFound</span><span class="sxs-lookup"><span data-stu-id="400a6-158">JET_errObjectNotFound</span></span></p></td>
<td><p><span data-ttu-id="400a6-159">Une tentative d’ouverture d’une table qui n’existe pas dans la base de données a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="400a6-159">An attempt was made to open a table that does not exist in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="400a6-160">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="400a6-160">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="400a6-161">L’opération a échoué, car le moteur ne peut pas allouer les ressources requises pour ouvrir un nouveau curseur.</span><span class="sxs-lookup"><span data-stu-id="400a6-161">The operation failed because the engine cannot allocate the resources required to open a new cursor.</span></span> <span data-ttu-id="400a6-162">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="400a6-162">See the Remarks section.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="400a6-163">JET_errTableInUse</span><span class="sxs-lookup"><span data-stu-id="400a6-163">JET_errTableInUse</span></span></p></td>
<td><p><span data-ttu-id="400a6-164">La table est utilisée par une autre opération de base de données.</span><span class="sxs-lookup"><span data-stu-id="400a6-164">The table is being used by another database operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="400a6-165">JET_wrnTableInUseBySystem</span><span class="sxs-lookup"><span data-stu-id="400a6-165">JET_wrnTableInUseBySystem</span></span></p></td>
<td><p><span data-ttu-id="400a6-166">AVERTISSEMENT récupérable indiquant que la table est en cours d’utilisation par le système.</span><span class="sxs-lookup"><span data-stu-id="400a6-166">A nonfatal warning indicating that the table is being used by the system.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="400a6-167">JET_errTableLocked</span><span class="sxs-lookup"><span data-stu-id="400a6-167">JET_errTableLocked</span></span></p></td>
<td><p><span data-ttu-id="400a6-168">La table est verrouillée par une autre opération de base de données.</span><span class="sxs-lookup"><span data-stu-id="400a6-168">The table is locked by another database operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="400a6-169">JET_errTooManyOpenTables</span><span class="sxs-lookup"><span data-stu-id="400a6-169">JET_errTooManyOpenTables</span></span></p></td>
<td><p><span data-ttu-id="400a6-170">Tentative d’ouverture d’un trop grand nombre de tables uniques à la fois.</span><span class="sxs-lookup"><span data-stu-id="400a6-170">An attempt was made to open too many unique tables at once.</span></span> <span data-ttu-id="400a6-171">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="400a6-171">See the Remarks section.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="400a6-172">Notes</span><span class="sxs-lookup"><span data-stu-id="400a6-172">Remarks</span></span>

<span data-ttu-id="400a6-173">Les tables ouvertes avec **JetOpenTable** doivent généralement être fermées avec [JetCloseTable](./jetclosetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="400a6-173">Tables opened with **JetOpenTable** should usually be closed with [JetCloseTable](./jetclosetable-function.md).</span></span> <span data-ttu-id="400a6-174">L’exception à cette règle se produit lorsque **JetOpenTable** est appelé dans une transaction et que la transaction est restaurée (avec [JetRollback](./jetrollback-function.md)).</span><span class="sxs-lookup"><span data-stu-id="400a6-174">The exception to this rule happens when **JetOpenTable** is called in a transaction and the transaction is rolled back (with [JetRollback](./jetrollback-function.md)).</span></span> <span data-ttu-id="400a6-175">Lors de la restauration d’une transaction, la table est fermée automatiquement.</span><span class="sxs-lookup"><span data-stu-id="400a6-175">When rolling back a transaction, the table is automatically closed.</span></span> <span data-ttu-id="400a6-176">Dans ce cas, il s’agit d’une erreur de fermeture de la table avec [JetCloseTable](./jetclosetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="400a6-176">In this case, it is an error to close the table with [JetCloseTable](./jetclosetable-function.md).</span></span>

<span data-ttu-id="400a6-177">Il est légal d’ouvrir des tables système avec **JetOpenTable** (par exemple, MSysObjects, MSysUnicodeFixup).</span><span class="sxs-lookup"><span data-stu-id="400a6-177">It is legal to open system tables with **JetOpenTable** (for example, MSysObjects, MSysUnicodeFixup).</span></span> <span data-ttu-id="400a6-178">Le schéma des tables système peut changer. par conséquent, l’accès aux tables système est déconseillé.</span><span class="sxs-lookup"><span data-stu-id="400a6-178">The schema of the system tables may change, so accessing system tables is discouraged.</span></span> <span data-ttu-id="400a6-179">Le nombre de tables uniques qui peuvent être ouvertes simultanément est directement affecté par *JET_paramMaxOpenTables*.</span><span class="sxs-lookup"><span data-stu-id="400a6-179">The number of unique tables that can be opened simultaneously is affected directly by *JET_paramMaxOpenTables*.</span></span> <span data-ttu-id="400a6-180">Si la table est actuellement ouverte, un nouveau curseur sera créé sur la table.</span><span class="sxs-lookup"><span data-stu-id="400a6-180">If the table is currently open then a new cursor will be created on the table.</span></span> <span data-ttu-id="400a6-181">Les ressources de curseur sont configurées à l’aide de [JetSetSystemParameter](./jetsetsystemparameter-function.md) avec *JET_paramMaxCursors*.</span><span class="sxs-lookup"><span data-stu-id="400a6-181">Cursor resources are configured using [JetSetSystemParameter](./jetsetsystemparameter-function.md) with *JET_paramMaxCursors*.</span></span> <span data-ttu-id="400a6-182">Voir aussi [JetDupCursor](./jetdupcursor-function.md).</span><span class="sxs-lookup"><span data-stu-id="400a6-182">Also see [JetDupCursor](./jetdupcursor-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="400a6-183">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="400a6-183">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="400a6-184"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="400a6-184"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="400a6-185">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="400a6-185">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="400a6-186"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="400a6-186"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="400a6-187">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="400a6-187">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="400a6-188"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="400a6-188"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="400a6-189">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="400a6-189">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="400a6-190"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="400a6-190"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="400a6-191">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="400a6-191">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="400a6-192"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="400a6-192"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="400a6-193">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="400a6-193">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="400a6-194"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="400a6-194"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="400a6-195">Implémenté en tant que <strong>JetOpenTableW</strong> (Unicode) et <strong>JetOpenTableA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="400a6-195">Implemented as <strong>JetOpenTableW</strong> (Unicode) and <strong>JetOpenTableA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="400a6-196">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="400a6-196">See Also</span></span>

[<span data-ttu-id="400a6-197">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="400a6-197">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="400a6-198">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="400a6-198">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="400a6-199">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="400a6-199">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="400a6-200">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="400a6-200">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="400a6-201">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="400a6-201">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="400a6-202">JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="400a6-202">JetDupCursor</span></span>](./jetdupcursor-function.md)  
[<span data-ttu-id="400a6-203">JetRollback</span><span class="sxs-lookup"><span data-stu-id="400a6-203">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="400a6-204">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="400a6-204">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="400a6-205">Paramètres de ressource</span><span class="sxs-lookup"><span data-stu-id="400a6-205">Resource Parameters</span></span>](./resource-parameters.md)
