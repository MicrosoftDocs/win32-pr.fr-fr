---
description: 'En savoir plus sur : fonction JetSetColumns'
title: Fonction JetSetColumns
TOCTitle: JetSetColumns Function
ms:assetid: a5b011dc-0da6-44bf-aaf5-352d8a57e5bf
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294050(v=EXCHG.10)
ms:contentKeyID: 32765649
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetColumns
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cfd4535b66064c19257f4bb7b51b059453660916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112043"
---
# <a name="jetsetcolumns-function"></a><span data-ttu-id="8b775-103">Fonction JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="8b775-103">JetSetColumns Function</span></span>


<span data-ttu-id="8b775-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="8b775-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetcolumns-function"></a><span data-ttu-id="8b775-105">Fonction JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="8b775-105">JetSetColumns Function</span></span>

<span data-ttu-id="8b775-106">Le comportement de la fonction **JetSetColumns** est similaire à celui de [JetSetColumn](./jetsetcolumn-function.md) , mais permet à une application de définir plusieurs valeurs de colonne en une seule opération.</span><span class="sxs-lookup"><span data-stu-id="8b775-106">The **JetSetColumns** function is similar in behavior to [JetSetColumn](./jetsetcolumn-function.md) but allows an application to set multiple column values in a single operation.</span></span> <span data-ttu-id="8b775-107">Un tableau de structures de [JET_SETCOLUMN](./jet-setcolumn-structure.md) est utilisé pour décrire l’ensemble des valeurs de colonne à définir, et pour décrire les mémoires tampons d’entrée pour chaque valeur de colonne à définir.</span><span class="sxs-lookup"><span data-stu-id="8b775-107">An array of [JET_SETCOLUMN](./jet-setcolumn-structure.md) structures is used to describe the set of column values to be set, and to describe input buffers for each column value to be set.</span></span>

```cpp
    JET_ERR JET_API JetSetColumns(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_out_opt  JET_SETCOLUMN* psetcolumn,
      __in          unsigned long csetcolumn
    );
```

### <a name="parameters"></a><span data-ttu-id="8b775-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8b775-108">Parameters</span></span>

<span data-ttu-id="8b775-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="8b775-109">*sesid*</span></span>

<span data-ttu-id="8b775-110">Session à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="8b775-110">The session to use for this call.</span></span>

<span data-ttu-id="8b775-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="8b775-111">*tableid*</span></span>

<span data-ttu-id="8b775-112">Curseur à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="8b775-112">The cursor to use for this call.</span></span>

<span data-ttu-id="8b775-113">*psetcolumn*</span><span class="sxs-lookup"><span data-stu-id="8b775-113">*psetcolumn*</span></span>

<span data-ttu-id="8b775-114">Pointeur vers un tableau d’une ou plusieurs structures de [JET_SETCOLUMN](./jet-setcolumn-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="8b775-114">A pointer to an array of one or more [JET_SETCOLUMN](./jet-setcolumn-structure.md) structures.</span></span> <span data-ttu-id="8b775-115">Chaque structure comprend des descriptions de la valeur de colonne à définir et de l’emplacement où les données de colonne doivent être définies.</span><span class="sxs-lookup"><span data-stu-id="8b775-115">Each structure includes descriptions of which column value to set and from where to get column data to set.</span></span>

<span data-ttu-id="8b775-116">*csetcolumn*</span><span class="sxs-lookup"><span data-stu-id="8b775-116">*csetcolumn*</span></span>

<span data-ttu-id="8b775-117">Nombre de structures de [JET_SETCOLUMN](./jet-setcolumn-structure.md) dans le tableau donné par *psetcolumn*.</span><span class="sxs-lookup"><span data-stu-id="8b775-117">The number of [JET_SETCOLUMN](./jet-setcolumn-structure.md) structures in the array given by *psetcolumn*.</span></span>

### <a name="return-value"></a><span data-ttu-id="8b775-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8b775-118">Return Value</span></span>

<span data-ttu-id="8b775-119">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="8b775-119">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="8b775-120">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="8b775-120">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8b775-121">Code de retour</span><span class="sxs-lookup"><span data-stu-id="8b775-121">Return code</span></span></p></th>
<th><p><span data-ttu-id="8b775-122">Description</span><span class="sxs-lookup"><span data-stu-id="8b775-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8b775-123">JET_errBadColumnId</span><span class="sxs-lookup"><span data-stu-id="8b775-123">JET_errBadColumnId</span></span></p></td>
<td><p><span data-ttu-id="8b775-124">L’ID de colonne indiqué est en dehors des limites autorisées d’un ID de colonne.</span><span class="sxs-lookup"><span data-stu-id="8b775-124">The column ID given is outside the legal limits of a column ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b775-125">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="8b775-125">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="8b775-126">Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="8b775-126">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b775-127">JET_errColumnIllegalNull</span><span class="sxs-lookup"><span data-stu-id="8b775-127">JET_errColumnIllegalNull</span></span></p></td>
<td><p><span data-ttu-id="8b775-128">Identique à JET_errNullInvalid.</span><span class="sxs-lookup"><span data-stu-id="8b775-128">Same as JET_errNullInvalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b775-129">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="8b775-129">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="8b775-130">La colonne décrite par le <em>ColumnID</em> donné n’existe pas dans la table.</span><span class="sxs-lookup"><span data-stu-id="8b775-130">The column described by the given <em>columnid</em> does not exist in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b775-131">JET_errColumnNotUpdatable</span><span class="sxs-lookup"><span data-stu-id="8b775-131">JET_errColumnNotUpdatable</span></span></p></td>
<td><p><span data-ttu-id="8b775-132">Une tentative non conforme a été effectuée pour mettre à jour une valeur long pendant une opération de mise à jour d’origine de la suppression d’une copie Insert.</span><span class="sxs-lookup"><span data-stu-id="8b775-132">An illegal attempt was made to update a long value during a insert copy delete original update operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b775-133">JET_errColumnTooBig</span><span class="sxs-lookup"><span data-stu-id="8b775-133">JET_errColumnTooBig</span></span></p></td>
<td><p><span data-ttu-id="8b775-134">Les données de la valeur de colonne donnée dans la mémoire tampon d’entrée dépassent la limite de taille naturelle pour une colonne de longueur fixe ou configurée pour le texte de longueur fixe ou les colonnes binaires.</span><span class="sxs-lookup"><span data-stu-id="8b775-134">The given column value data given in the input buffer exceeds the size limitation either natural for a fixed length column or configured for fixed length text or binary columns.</span></span> <span data-ttu-id="8b775-135">Cette erreur est également retournée lors du passage de plus de 1024 octets de données pour une longue colonne et de la définition de l’indicateur de JET_bitSetIntrinsicLV.</span><span class="sxs-lookup"><span data-stu-id="8b775-135">This error is also returned when passing more than 1024 bytes of data for a long column and setting the JET_bitSetIntrinsicLV flag.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b775-136">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="8b775-136">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="8b775-137">Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="8b775-137">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="8b775-138">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="8b775-138">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b775-139">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="8b775-139">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="8b775-140">La taille de données de la valeur de colonne donnée ne correspond pas à ce qui est naturel pour le type de données de longueur fixe.</span><span class="sxs-lookup"><span data-stu-id="8b775-140">The given column value data size does not match what is natural for the fixed length data type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b775-141">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="8b775-141">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="8b775-142">Une tentative non conforme a été effectuée pour mettre à jour une colonne à incrémentation automatique pendant une opération d’insertion ou de mise à jour, ou pour mettre à jour une colonne de version pendant une opération de remplacement.</span><span class="sxs-lookup"><span data-stu-id="8b775-142">An illegal attempt was made to update an auto-increment column either during an insert or update operation, or to update a version column during a replace operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b775-143">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="8b775-143">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="8b775-144">Les options fournies sont inconnues ou une combinaison non conforme de paramètres de bits connus.</span><span class="sxs-lookup"><span data-stu-id="8b775-144">The options supplied are unknown or an illegal combination of known bit settings.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b775-145">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="8b775-145">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="8b775-146">Le psetinfo- &gt; cbStruct donné n’est pas une taille valide pour la structure <a href="gg294090(v=exchg.10).md">JET_SETINFO</a> .</span><span class="sxs-lookup"><span data-stu-id="8b775-146">The given psetinfo-&gt;cbStruct is not a valid size for the <a href="gg294090(v=exchg.10).md">JET_SETINFO</a> structure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b775-147">JET_errMultiValuedDuplicate</span><span class="sxs-lookup"><span data-stu-id="8b775-147">JET_errMultiValuedDuplicate</span></span></p></td>
<td><p><span data-ttu-id="8b775-148">L’opération de définition de colonne a tenté de créer une valeur dupliquée et spécifiée soit JET_bitSetUniqueMultiValues, soit JET_bitSetUniqueNormalizedMultiValues.</span><span class="sxs-lookup"><span data-stu-id="8b775-148">The set column operation attempted to create a duplicate value and specified either JET_bitSetUniqueMultiValues or JET_bitSetUniqueNormalizedMultiValues.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b775-149">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="8b775-149">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="8b775-150">Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="8b775-150">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b775-151">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="8b775-151">JET_errNotInTransaction</span></span></p></td>
<td><p><span data-ttu-id="8b775-152">Une tentative non conforme a été effectuée pour mettre à jour une valeur de colonne longue lorsque la session appelante n’était pas dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="8b775-152">An illegal attempt was made to update a long column value when the calling session was not in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b775-153">JET_errNullInvalid</span><span class="sxs-lookup"><span data-stu-id="8b775-153">JET_errNullInvalid</span></span></p></td>
<td><p><span data-ttu-id="8b775-154">Une tentative non conforme a été effectuée pour définir une colonne non NULL à NULL.</span><span class="sxs-lookup"><span data-stu-id="8b775-154">An illegal attempt was made to set a non-NULL column to NULL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b775-155">JET_errRecordTooBig</span><span class="sxs-lookup"><span data-stu-id="8b775-155">JET_errRecordTooBig</span></span></p></td>
<td><p><span data-ttu-id="8b775-156">La valeur de la colonne n’a pas pu être définie sur la valeur dans la mémoire tampon d’entrée, car elle aurait provoqué un dépassement de la limite de taille liée à la taille de la page de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="8b775-156">The column value could not be set to the value in the input buffer because it would have caused the record to exceed its page size related size limitation.</span></span> <span data-ttu-id="8b775-157">Les colonnes de type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> ou <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> peuvent être stockées séparément des données de l’enregistrement restant.</span><span class="sxs-lookup"><span data-stu-id="8b775-157">Columns of type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> can be stored separately from the remaining record data.</span></span> <span data-ttu-id="8b775-158">Toutefois, les autres colonnes doivent être stockées avec l’enregistrement et peuvent entraîner le dépassement de la limite de taille des enregistrements.</span><span class="sxs-lookup"><span data-stu-id="8b775-158">However, other columns must be stored with the record and can cause the record size limitation to be exceeded.</span></span> <span data-ttu-id="8b775-159">Même les colonnes longues nécessitent 5 octets d’espace dans l’enregistrement en tant que liaison, ce qui peut entraîner des JET_errRecordTooBig retournées.</span><span class="sxs-lookup"><span data-stu-id="8b775-159">Even long columns require 5-bytes of space within the record as a linkage and this too can lead to JET_errRecordTooBig being returned.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b775-160">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="8b775-160">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="8b775-161">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="8b775-161">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b775-162">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="8b775-162">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="8b775-163">La même session ne peut pas être utilisée simultanément pour plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="8b775-163">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="8b775-164">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="8b775-164">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b775-165">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="8b775-165">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="8b775-166">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="8b775-166">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b775-167">JET_errUpdateNotPrepared</span><span class="sxs-lookup"><span data-stu-id="8b775-167">JET_errUpdateNotPrepared</span></span></p></td>
<td><p><span data-ttu-id="8b775-168">Le curseur ne se trouve pas actuellement dans le processus d’insertion d’un nouvel enregistrement ou de mise à jour d’un enregistrement existant.</span><span class="sxs-lookup"><span data-stu-id="8b775-168">The cursor is not currently in the process of either inserting a new record or updating an existing record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b775-169">JET_wrnColumnMaxTruncated</span><span class="sxs-lookup"><span data-stu-id="8b775-169">JET_wrnColumnMaxTruncated</span></span></p></td>
<td><p><span data-ttu-id="8b775-170">La valeur de colonne dans la mémoire tampon d’entrée a dépassé la longueur maximale configurée pour une colonne de longueur variable et a été tronquée.</span><span class="sxs-lookup"><span data-stu-id="8b775-170">The column value in the input buffer exceeded the maximum configured length for a variable length column and was truncated.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8b775-171">En cas de réussite, pour chaque colonne décrite dans psetcolumns, la partie souhaitée de la valeur de colonne est définie avec les données copiées à partir de la mémoire tampon d’entrée.</span><span class="sxs-lookup"><span data-stu-id="8b775-171">On success, for each column described in the psetcolumns, the desired portion of the column value is set with data copied from the input buffer.</span></span> <span data-ttu-id="8b775-172">Le jeu de données de la colonne a peut-être été tronqué s’il dépasse la longueur maximale spécifiée pour une colonne de longueur variable.</span><span class="sxs-lookup"><span data-stu-id="8b775-172">The column data set may have been truncated if it exceeded the maximum length specified for a variable length column.</span></span>

<span data-ttu-id="8b775-173">En cas d’échec, l’emplacement du curseur reste inchangé et aucune donnée de valeur de colonne n’est mise à jour dans le tampon de copie.</span><span class="sxs-lookup"><span data-stu-id="8b775-173">On failure, the cursor location is left unchanged and no column value data is updated in the copy buffer.</span></span>

#### <a name="remarks"></a><span data-ttu-id="8b775-174">Notes</span><span class="sxs-lookup"><span data-stu-id="8b775-174">Remarks</span></span>

<span data-ttu-id="8b775-175">Si une opération de définition de colonne individuelle retourne une erreur, la totalité de l’opération de **JetSetColumns** retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="8b775-175">If any individual set column operation returns an error then the whole **JetSetColumns** operation will return an error.</span></span> <span data-ttu-id="8b775-176">Des avertissements, en général, sont retournés dans l' \> erreur psetcolumns et non dans le code de retour de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="8b775-176">Warnings, in general, are returned in the psetcolumns-\>error and not in the return code from this function.</span></span> <span data-ttu-id="8b775-177">Toutefois, si le dernier jeu de colonnes a un avertissement, cet avertissement est retourné à partir de **JetSetColumns** lui-même.</span><span class="sxs-lookup"><span data-stu-id="8b775-177">However, if the last column set has a warning, then this warning will be returned from **JetSetColumns** itself.</span></span>

#### <a name="requirements"></a><span data-ttu-id="8b775-178">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8b775-178">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8b775-179"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="8b775-179"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="8b775-180">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="8b775-180">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b775-181"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="8b775-181"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="8b775-182">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="8b775-182">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b775-183"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="8b775-183"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="8b775-184">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="8b775-184">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b775-185"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="8b775-185"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="8b775-186">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="8b775-186">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b775-187"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="8b775-187"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="8b775-188">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="8b775-188">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="8b775-189">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b775-189">See Also</span></span>

[<span data-ttu-id="8b775-190">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="8b775-190">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="8b775-191">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="8b775-191">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="8b775-192">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="8b775-192">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="8b775-193">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="8b775-193">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="8b775-194">JET_SETCOLUMN</span><span class="sxs-lookup"><span data-stu-id="8b775-194">JET_SETCOLUMN</span></span>](./jet-setcolumn-structure.md)  
[<span data-ttu-id="8b775-195">JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="8b775-195">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)  
[<span data-ttu-id="8b775-196">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="8b775-196">JetSetColumn</span></span>](./jetsetcolumn-function.md)
