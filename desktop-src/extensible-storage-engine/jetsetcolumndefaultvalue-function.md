---
description: 'En savoir plus sur : fonction JetSetColumnDefaultValue'
title: JetSetColumnDefaultValue fonction)
TOCTitle: JetSetColumnDefaultValue Function
ms:assetid: 74bfaf50-6c2e-4907-b931-d50ad314b552
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269295(v=EXCHG.10)
ms:contentKeyID: 32765587
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetColumnDefaultValue
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9f50d30b2edeca716895d8dd2339d659f0e1382f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862197"
---
# <a name="jetsetcolumndefaultvalue-function"></a><span data-ttu-id="65549-103">JetSetColumnDefaultValue fonction)</span><span class="sxs-lookup"><span data-stu-id="65549-103">JetSetColumnDefaultValue Function</span></span>


<span data-ttu-id="65549-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="65549-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetcolumndefaultvalue-function"></a><span data-ttu-id="65549-105">JetSetColumnDefaultValue fonction)</span><span class="sxs-lookup"><span data-stu-id="65549-105">JetSetColumnDefaultValue Function</span></span>

<span data-ttu-id="65549-106">La fonction **JetSetColumnDefaultValue** peut être utilisée pour modifier la valeur par défaut d’une colonne existante.</span><span class="sxs-lookup"><span data-stu-id="65549-106">The **JetSetColumnDefaultValue** function can be used to change the default value of an existing column.</span></span>

```cpp
    JET_ERR JET_API JetSetColumnDefaultValue(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          JET_PCSTR szTableName,
      __in          JET_PCSTR szColumnName,
      __in          const void* pvData,
      __in          const unsigned long cbData,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="65549-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="65549-107">Parameters</span></span>

<span data-ttu-id="65549-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="65549-108">*sesid*</span></span>

<span data-ttu-id="65549-109">Session à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="65549-109">The session to use for this call.</span></span>

<span data-ttu-id="65549-110">*dbid*</span><span class="sxs-lookup"><span data-stu-id="65549-110">*dbid*</span></span>

<span data-ttu-id="65549-111">Base de données à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="65549-111">The database to use for this call.</span></span>

<span data-ttu-id="65549-112">*szTableName*</span><span class="sxs-lookup"><span data-stu-id="65549-112">*szTableName*</span></span>

<span data-ttu-id="65549-113">Nom de la table contenant la colonne qui sera affectée.</span><span class="sxs-lookup"><span data-stu-id="65549-113">The name of the table containing the column that will be affected.</span></span>

<span data-ttu-id="65549-114">*szColumnName*</span><span class="sxs-lookup"><span data-stu-id="65549-114">*szColumnName*</span></span>

<span data-ttu-id="65549-115">Nom de la colonne dont la valeur par défaut sera modifiée.</span><span class="sxs-lookup"><span data-stu-id="65549-115">The name of the column whose default value will be changed.</span></span>

<span data-ttu-id="65549-116">*pvData*</span><span class="sxs-lookup"><span data-stu-id="65549-116">*pvData*</span></span>

<span data-ttu-id="65549-117">Mémoire tampon d’entrée contenant la nouvelle valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="65549-117">The input buffer containing the new default value.</span></span>

<span data-ttu-id="65549-118">*cbData*</span><span class="sxs-lookup"><span data-stu-id="65549-118">*cbData*</span></span>

<span data-ttu-id="65549-119">Taille de la mémoire tampon d’entrée contenant la nouvelle valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="65549-119">The size of the input buffer containing the new default value.</span></span>

<span data-ttu-id="65549-120">*grbit*</span><span class="sxs-lookup"><span data-stu-id="65549-120">*grbit*</span></span>

<span data-ttu-id="65549-121">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="65549-121">Reserved for future use.</span></span>

### <a name="return-value"></a><span data-ttu-id="65549-122">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="65549-122">Return Value</span></span>

<span data-ttu-id="65549-123">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="65549-123">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="65549-124">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="65549-124">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="65549-125">Code de retour</span><span class="sxs-lookup"><span data-stu-id="65549-125">Return code</span></span></p></th>
<th><p><span data-ttu-id="65549-126">Description</span><span class="sxs-lookup"><span data-stu-id="65549-126">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="65549-127">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="65549-127">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="65549-128">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="65549-128">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65549-129">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="65549-129">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="65549-130">Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="65549-130">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65549-131">JET_errColumnIllegalNull</span><span class="sxs-lookup"><span data-stu-id="65549-131">JET_errColumnIllegalNull</span></span></p></td>
<td><p><span data-ttu-id="65549-132">Identique à JET_errNullInvalid.</span><span class="sxs-lookup"><span data-stu-id="65549-132">Same as JET_errNullInvalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65549-133">JET_errColumnInUse</span><span class="sxs-lookup"><span data-stu-id="65549-133">JET_errColumnInUse</span></span></p></td>
<td><p><span data-ttu-id="65549-134">Cette colonne spécifiée est actuellement utilisée par un index.</span><span class="sxs-lookup"><span data-stu-id="65549-134">This specified column is currently in use by an index.</span></span></p>
<p><span data-ttu-id="65549-135"><strong>JetSetColumnDefaultValue</strong> ne peut pas modifier la valeur par défaut d’une colonne référencée dans la définition d’un index.</span><span class="sxs-lookup"><span data-stu-id="65549-135"><strong>JetSetColumnDefaultValue</strong> cannot change the default value of a column that is referenced in the definition of an index.</span></span> <span data-ttu-id="65549-136">Cela est dû au fait que cela peut modifier le contenu de l’index.</span><span class="sxs-lookup"><span data-stu-id="65549-136">This is because doing so could change the contents of the index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65549-137">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="65549-137">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="65549-138">La colonne spécifiée n’existe pas pour cette table.</span><span class="sxs-lookup"><span data-stu-id="65549-138">This specified column does not exist for this table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65549-139">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="65549-139">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="65549-140">Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="65549-140">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="65549-141">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="65549-141">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65549-142">JET_errInvalidDatabaseId</span><span class="sxs-lookup"><span data-stu-id="65549-142">JET_errInvalidDatabaseId</span></span></p></td>
<td><p><span data-ttu-id="65549-143">L’ID de base de données spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="65549-143">The specified database ID was invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65549-144">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="65549-144">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="65549-145">L’un des noms d’objets spécifiés n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="65549-145">One of the specified object names was invalid.</span></span> <span data-ttu-id="65549-146">Tous les noms d’objets doivent être conformes au même ensemble de règles.</span><span class="sxs-lookup"><span data-stu-id="65549-146">All object names must conform to the same set of rules.</span></span> <span data-ttu-id="65549-147">Ces règles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="65549-147">These rules are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="65549-148">Les noms d’objets doivent être composés de caractères ASCII.</span><span class="sxs-lookup"><span data-stu-id="65549-148">Object names must be composed of ASCII characters.</span></span></p></li>
<li><p><span data-ttu-id="65549-149">Les noms d’objets doivent comporter au moins un caractère.</span><span class="sxs-lookup"><span data-stu-id="65549-149">Object names must be at least one character in length.</span></span></p></li>
<li><p><span data-ttu-id="65549-150">Les noms d’objets ne peuvent pas dépasser JET_cbNameMost (64) caractères.</span><span class="sxs-lookup"><span data-stu-id="65549-150">Object names may not exceed JET_cbNameMost (64) characters in length.</span></span></p></li>
<li><p><span data-ttu-id="65549-151">Les noms d’objets ne peuvent pas commencer par un espace.</span><span class="sxs-lookup"><span data-stu-id="65549-151">Object names may not begin with a space.</span></span></p></li>
<li><p><span data-ttu-id="65549-152">Les noms d’objets ne peuvent pas contenir de caractères de contrôle ASCII (0x00 à 0x1F).</span><span class="sxs-lookup"><span data-stu-id="65549-152">Object names may not contain ASCII control characters (0x00 through 0x1F).</span></span></p></li>
<li><p><span data-ttu-id="65549-153">Les noms d’objets ne peuvent pas contenir de point d’exclamation ( !), de point (.), de crochet gauche ([) ou de crochet droit (]).</span><span class="sxs-lookup"><span data-stu-id="65549-153">Object names may not contain an exclamation point (!), period (.), left bracket ([), or right bracket (]) character.</span></span></p></li>
<li><p><span data-ttu-id="65549-154">Une fois validée, seule la partie de la chaîne jusqu’au premier espace (le cas échéant) sera utilisée pour le nom de l’objet.</span><span class="sxs-lookup"><span data-stu-id="65549-154">Once validated, only the portion of the string up to the first space (if any) will be used for the object name.</span></span> <span data-ttu-id="65549-155">Cela signifie que les noms d’objets ne peuvent pas non plus contenir d’espace.</span><span class="sxs-lookup"><span data-stu-id="65549-155">This means that object names may not contain a space either.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65549-156">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="65549-156">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="65549-157">Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="65549-157">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65549-158">JET_errNullInvalid</span><span class="sxs-lookup"><span data-stu-id="65549-158">JET_errNullInvalid</span></span></p></td>
<td><p><span data-ttu-id="65549-159">La colonne n’a pas pu être définie sur NULL.</span><span class="sxs-lookup"><span data-stu-id="65549-159">The column could not be set to NULL.</span></span> <span data-ttu-id="65549-160">Cela se produit pour <strong>JetSetColumnDefaultValue</strong> dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="65549-160">This happens for <strong>JetSetColumnDefaultValue</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="65549-161"><em>cbData</em> est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="65549-161"><em>cbData</em> is zero.</span></span></p></li>
<li><p><span data-ttu-id="65549-162"><strong>pvData</strong> a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="65549-162"><strong>pvData</strong> is NULL.</span></span></p></li>
</ul>
<p><span data-ttu-id="65549-163">Par conséquent, il n’est pas possible de définir la valeur par défaut d’une colonne (arrière) sur NULL ou sur une valeur de longueur nulle.</span><span class="sxs-lookup"><span data-stu-id="65549-163">Therefore, it is not possible to set the default value of a column (back) to NULL or to a zero length value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65549-164">JET_errObjectNotFound</span><span class="sxs-lookup"><span data-stu-id="65549-164">JET_errObjectNotFound</span></span></p></td>
<td><p><span data-ttu-id="65549-165">La table spécifiée n’existe pas pour cette base de données.</span><span class="sxs-lookup"><span data-stu-id="65549-165">This specified table does not exist for this database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65549-166">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="65549-166">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="65549-167">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="65549-167">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65549-168">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="65549-168">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="65549-169">La même session ne peut pas être utilisée simultanément pour plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="65549-169">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="65549-170">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="65549-170">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65549-171">JET_errTableInUse</span><span class="sxs-lookup"><span data-stu-id="65549-171">JET_errTableInUse</span></span></p></td>
<td><p><span data-ttu-id="65549-172">Cette table spécifiée est utilisée par une autre session.</span><span class="sxs-lookup"><span data-stu-id="65549-172">This specified table is in use by another session.</span></span></p>
<p><span data-ttu-id="65549-173"><strong>JetSetColumnDefaultValue</strong> requiert un accès exclusif à une table afin de modifier la valeur par défaut de la colonne pour les versions antérieures à Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="65549-173"><strong>JetSetColumnDefaultValue</strong> requires exclusive access to a table in order to change the default value of the column for releases prior to Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65549-174">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="65549-174">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="65549-175">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="65549-175">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65549-176">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="65549-176">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="65549-177">Il n’est pas autorisé de tenter une mise à jour dans l’étendue d’une transaction en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="65549-177">It is illegal to attempt an update when inside the scope of a read only transaction.</span></span> <span data-ttu-id="65549-178">Une transaction en lecture seule est une transaction qui a été démarrée à l’aide d’un appel à <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> avec JET_bitTransactionReadOnly.</span><span class="sxs-lookup"><span data-stu-id="65549-178">A read only transaction is a transaction that has been started using a call to <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> with JET_bitTransactionReadOnly.</span></span> <span data-ttu-id="65549-179">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="65549-179">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65549-180">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="65549-180">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="65549-181">Une autre session a déjà verrouillé l’enregistrement pour la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="65549-181">Another session has previously locked the record for update.</span></span> <span data-ttu-id="65549-182">La mise à jour tentée par cette session échoue.</span><span class="sxs-lookup"><span data-stu-id="65549-182">The update attempted by this session will fail.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="65549-183">En cas de réussite, la valeur par défaut de la colonne spécifiée dans la table donnée dans la base de données donnée est remplacée définitivement par la nouvelle valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="65549-183">On success, the default value of the specified column in the given table in the given database is permanently changed to the new default value.</span></span>

<span data-ttu-id="65549-184">En cas d’échec, aucune modification de l’état de la base de données ne se produit.</span><span class="sxs-lookup"><span data-stu-id="65549-184">On failure, no change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="65549-185">Notes</span><span class="sxs-lookup"><span data-stu-id="65549-185">Remarks</span></span>

<span data-ttu-id="65549-186">Il n’est pas possible de modifier la valeur par défaut d’une colonne dans une table de modèle.</span><span class="sxs-lookup"><span data-stu-id="65549-186">It is not possible to change the default value of a column in a template table.</span></span>

<span data-ttu-id="65549-187">Le moteur de base de données tronque en mode silencieux la valeur par défaut d’une colonne à 255 octets pour les colonnes de type long text et long Binary.</span><span class="sxs-lookup"><span data-stu-id="65549-187">The database engine will silently truncate the default value of a column to 255 bytes for long text and long binary columns.</span></span>

#### <a name="requirements"></a><span data-ttu-id="65549-188">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="65549-188">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="65549-189"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="65549-189"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="65549-190">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="65549-190">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65549-191"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="65549-191"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="65549-192">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="65549-192">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65549-193"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="65549-193"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="65549-194">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="65549-194">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65549-195"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="65549-195"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="65549-196">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="65549-196">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65549-197"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="65549-197"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="65549-198">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="65549-198">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65549-199"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="65549-199"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="65549-200">Implémenté en tant que <strong>JetSetColumnDefaultValueW</strong> (Unicode) et <strong>JetSetColumnDefaultValueA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="65549-200">Implemented as <strong>JetSetColumnDefaultValueW</strong> (Unicode) and <strong>JetSetColumnDefaultValueA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="65549-201">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65549-201">See Also</span></span>

[<span data-ttu-id="65549-202">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="65549-202">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="65549-203">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="65549-203">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="65549-204">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="65549-204">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="65549-205">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="65549-205">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="65549-206">JetBeginTransaction2</span><span class="sxs-lookup"><span data-stu-id="65549-206">JetBeginTransaction2</span></span>](./jetbegintransaction2-function.md)  
[<span data-ttu-id="65549-207">JetStopService</span><span class="sxs-lookup"><span data-stu-id="65549-207">JetStopService</span></span>](./jetstopservice-function.md)
