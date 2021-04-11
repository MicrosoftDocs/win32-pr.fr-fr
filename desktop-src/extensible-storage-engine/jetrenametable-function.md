---
description: 'En savoir plus sur : fonction JetRenameTable'
title: JetRenameTable fonction)
TOCTitle: JetRenameTable Function
ms:assetid: face9341-58e3-450b-980d-08eb1dc3e9d2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294142(v=EXCHG.10)
ms:contentKeyID: 32765756
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRenameTableW
- JetRenameTableA
- JetRenameTable
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 624b194a1cad836b8927e6e7e4b8490fcad250b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320482"
---
# <a name="jetrenametable-function"></a><span data-ttu-id="cf4af-103">JetRenameTable fonction)</span><span class="sxs-lookup"><span data-stu-id="cf4af-103">JetRenameTable Function</span></span>


<span data-ttu-id="cf4af-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="cf4af-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetrenametable-function"></a><span data-ttu-id="cf4af-105">JetRenameTable fonction)</span><span class="sxs-lookup"><span data-stu-id="cf4af-105">JetRenameTable Function</span></span>

<span data-ttu-id="cf4af-106">La fonction **JetRenameTable** peut être utilisée pour modifier le nom d’une table existante.</span><span class="sxs-lookup"><span data-stu-id="cf4af-106">The **JetRenameTable** function can be used to change the name of an existing table.</span></span>

```cpp
    JET_ERR JET_API JetRenameTable(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szName,
      __in          const tchar* szNameNew
    );
```

### <a name="parameters"></a><span data-ttu-id="cf4af-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cf4af-107">Parameters</span></span>

<span data-ttu-id="cf4af-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="cf4af-108">*sesid*</span></span>

<span data-ttu-id="cf4af-109">Session à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="cf4af-109">The session to use for this call.</span></span>

<span data-ttu-id="cf4af-110">*dbid*</span><span class="sxs-lookup"><span data-stu-id="cf4af-110">*dbid*</span></span>

<span data-ttu-id="cf4af-111">Base de données à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="cf4af-111">The database to use for this call.</span></span>

<span data-ttu-id="cf4af-112">*szName*</span><span class="sxs-lookup"><span data-stu-id="cf4af-112">*szName*</span></span>

<span data-ttu-id="cf4af-113">Nom actuel de la table qui sera renommée.</span><span class="sxs-lookup"><span data-stu-id="cf4af-113">The current name of the table that will be renamed.</span></span>

<span data-ttu-id="cf4af-114">*szNameNew*</span><span class="sxs-lookup"><span data-stu-id="cf4af-114">*szNameNew*</span></span>

<span data-ttu-id="cf4af-115">Nouveau nom de la table qui sera renommé.</span><span class="sxs-lookup"><span data-stu-id="cf4af-115">The new name for the table that will be renamed.</span></span>

### <a name="return-value"></a><span data-ttu-id="cf4af-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="cf4af-116">Return Value</span></span>

<span data-ttu-id="cf4af-117">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="cf4af-117">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="cf4af-118">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="cf4af-118">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cf4af-119">Code de retour</span><span class="sxs-lookup"><span data-stu-id="cf4af-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="cf4af-120">Description</span><span class="sxs-lookup"><span data-stu-id="cf4af-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cf4af-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="cf4af-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="cf4af-122">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="cf4af-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf4af-123">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="cf4af-123">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="cf4af-124">Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="cf4af-124">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf4af-125">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="cf4af-125">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="cf4af-126">Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="cf4af-126">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="cf4af-127">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="cf4af-127">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf4af-128">JET_errInvalidDatabase</span><span class="sxs-lookup"><span data-stu-id="cf4af-128">JET_errInvalidDatabase</span></span></p></td>
<td><p><span data-ttu-id="cf4af-129">La base de données spécifiée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="cf4af-129">The specified database was invalid.</span></span></p>
<p><span data-ttu-id="cf4af-130">Cette erreur est renvoyée uniquement dans Windows 2000 lorsqu’une opération de modification de nom de table est tentée sur la base de données temporaire.</span><span class="sxs-lookup"><span data-stu-id="cf4af-130">This error is only returned in Windows 2000 when a table rename operation is attempted on the temporary database.</span></span> <span data-ttu-id="cf4af-131">JET_errInvalidDatabaseId est retourné dans ce cas dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="cf4af-131">JET_errInvalidDatabaseId is returned for this case in later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf4af-132">JET_errInvalidDatabaseId</span><span class="sxs-lookup"><span data-stu-id="cf4af-132">JET_errInvalidDatabaseId</span></span></p></td>
<td><p><span data-ttu-id="cf4af-133">L’ID de base de données spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="cf4af-133">The specified database ID was invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf4af-134">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="cf4af-134">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="cf4af-135">L’un des noms d’objets spécifiés n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="cf4af-135">One of the specified object names was invalid.</span></span> <span data-ttu-id="cf4af-136">Tous les noms d’objets doivent être conformes au même ensemble de règles.</span><span class="sxs-lookup"><span data-stu-id="cf4af-136">All object names must conform to the same set of rules.</span></span> <span data-ttu-id="cf4af-137">Ces règles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="cf4af-137">These rules are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="cf4af-138">Les noms d’objets doivent être composés de caractères ASCII.</span><span class="sxs-lookup"><span data-stu-id="cf4af-138">Object names must be composed of ASCII characters.</span></span></p></li>
<li><p><span data-ttu-id="cf4af-139">Les noms d’objets doivent comporter au moins un caractère.</span><span class="sxs-lookup"><span data-stu-id="cf4af-139">Object names must be at least one character in length.</span></span></p></li>
<li><p><span data-ttu-id="cf4af-140">Les noms d’objets ne peuvent pas dépasser JET_cbNameMost (64) caractères.</span><span class="sxs-lookup"><span data-stu-id="cf4af-140">Object names may not exceed JET_cbNameMost (64) characters in length.</span></span></p></li>
<li><p><span data-ttu-id="cf4af-141">Les noms d’objets ne peuvent pas commencer par un espace.</span><span class="sxs-lookup"><span data-stu-id="cf4af-141">Object names may not begin with a space.</span></span></p></li>
<li><p><span data-ttu-id="cf4af-142">Les noms d’objets ne peuvent pas contenir de caractères de contrôle ASCII (0x00 à 0x1F).</span><span class="sxs-lookup"><span data-stu-id="cf4af-142">Object names may not contain ASCII control characters (0x00 through 0x1F).</span></span></p></li>
<li><p><span data-ttu-id="cf4af-143">Les noms d’objets ne peuvent pas contenir un point d’exclamation ( !), un point (.), un crochet gauche ([) ou un crochet droit (]), une fois validés, seule la partie de la chaîne jusqu’au premier espace (le cas échéant) sera utilisée pour le nom de l’objet.</span><span class="sxs-lookup"><span data-stu-id="cf4af-143">Object names may not contain an exclamation point (!), period (.), left bracket ([), or right bracket (]) character - once validated, only the portion of the string up to the first space (if any) will be used for the object name.</span></span> <span data-ttu-id="cf4af-144">Cela signifie que les noms d’objets ne peuvent pas non plus contenir d’espace.</span><span class="sxs-lookup"><span data-stu-id="cf4af-144">This effectively means that object names may not contain a space either.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf4af-145">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="cf4af-145">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="cf4af-146">L’un des paramètres fournis contenait une valeur inattendue ou contenait une valeur qui n’a pas de sens lorsqu’elle était associée à la valeur d’un autre paramètre.</span><span class="sxs-lookup"><span data-stu-id="cf4af-146">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="cf4af-147">Cela peut se produire pour <strong>JetRenameTable</strong> dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="cf4af-147">This can happen for <strong>JetRenameTable</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="cf4af-148"><em>szName</em> a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="cf4af-148"><em>szName</em> is NULL.</span></span></p></li>
<li><p><span data-ttu-id="cf4af-149"><em>szNameNew</em> a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="cf4af-149"><em>szNameNew</em> is NULL.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf4af-150">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="cf4af-150">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="cf4af-151">Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="cf4af-151">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf4af-152">JET_errObjectNotFound</span><span class="sxs-lookup"><span data-stu-id="cf4af-152">JET_errObjectNotFound</span></span></p></td>
<td><p><span data-ttu-id="cf4af-153">La table spécifiée n’existe pas pour cette base de données.</span><span class="sxs-lookup"><span data-stu-id="cf4af-153">This specified table does not exist for this database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf4af-154">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="cf4af-154">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="cf4af-155">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="cf4af-155">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf4af-156">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="cf4af-156">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="cf4af-157">La même session ne peut pas être utilisée simultanément pour plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="cf4af-157">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="cf4af-158">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="cf4af-158">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf4af-159">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="cf4af-159">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="cf4af-160">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="cf4af-160">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf4af-161">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="cf4af-161">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="cf4af-162">Une mise à jour ne peut pas être effectuée dans l’étendue d’une transaction en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="cf4af-162">An update cannot be done while inside the scope of a read-only transaction.</span></span> <span data-ttu-id="cf4af-163">Une transaction en lecture seule est une transaction qui a été démarrée à l’aide d’un appel à <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> avec JET_bitTransactionReadOnly.</span><span class="sxs-lookup"><span data-stu-id="cf4af-163">A read-only transaction is a transaction that has been started using a call to <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> with JET_bitTransactionReadOnly.</span></span></p>
<p><span data-ttu-id="cf4af-164">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="cf4af-164">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cf4af-165">En cas de réussite, le nom de la table spécifiée dans la base de données spécifiée est remplacé définitivement par le nouveau nom.</span><span class="sxs-lookup"><span data-stu-id="cf4af-165">On success, the name of the specified table in the given database is permanently changed to the new name.</span></span>

<span data-ttu-id="cf4af-166">En cas d’échec, aucune modification de l’état de la base de données ne se produit.</span><span class="sxs-lookup"><span data-stu-id="cf4af-166">On failure, no change to the database state will occur.</span></span>

#### <a name="requirements"></a><span data-ttu-id="cf4af-167">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cf4af-167">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cf4af-168"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="cf4af-168"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="cf4af-169">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="cf4af-169">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf4af-170"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="cf4af-170"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="cf4af-171">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="cf4af-171">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf4af-172"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="cf4af-172"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="cf4af-173">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="cf4af-173">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf4af-174"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="cf4af-174"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="cf4af-175">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="cf4af-175">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf4af-176"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="cf4af-176"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="cf4af-177">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="cf4af-177">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf4af-178"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="cf4af-178"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="cf4af-179">Implémenté en tant que <strong>JetRenameTableW</strong> (Unicode) et <strong>JetRenameTableA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="cf4af-179">Implemented as <strong>JetRenameTableW</strong> (Unicode) and <strong>JetRenameTableA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="cf4af-180">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cf4af-180">See Also</span></span>

[<span data-ttu-id="cf4af-181">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="cf4af-181">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="cf4af-182">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="cf4af-182">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="cf4af-183">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="cf4af-183">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="cf4af-184">JetBeginTransaction2</span><span class="sxs-lookup"><span data-stu-id="cf4af-184">JetBeginTransaction2</span></span>](./jetbegintransaction2-function.md)
