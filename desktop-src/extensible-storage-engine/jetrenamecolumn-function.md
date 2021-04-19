---
description: 'En savoir plus sur : fonction JetRenameColumn'
title: JetRenameColumn fonction)
TOCTitle: JetRenameColumn Function
ms:assetid: 30967765-355b-417c-b0d6-8b59e677cc98
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269218(v=EXCHG.10)
ms:contentKeyID: 32765521
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRenameColumn
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9ab2dee1895e4148bb2ea0600464d7e9c4a6a358
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534722"
---
# <a name="jetrenamecolumn-function"></a><span data-ttu-id="70c1c-103">JetRenameColumn fonction)</span><span class="sxs-lookup"><span data-stu-id="70c1c-103">JetRenameColumn Function</span></span>


<span data-ttu-id="70c1c-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="70c1c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetrenamecolumn-function"></a><span data-ttu-id="70c1c-105">JetRenameColumn fonction)</span><span class="sxs-lookup"><span data-stu-id="70c1c-105">JetRenameColumn Function</span></span>

<span data-ttu-id="70c1c-106">La fonction **JetRenameColumn** peut être utilisée pour modifier le nom d’une colonne existante sur une table.</span><span class="sxs-lookup"><span data-stu-id="70c1c-106">The **JetRenameColumn** function can be used to change the name of an existing column on a table.</span></span>

<span data-ttu-id="70c1c-107">**Windows XP :**  **JetRenameColumn** est introduit dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="70c1c-107">**Windows XP:**  **JetRenameColumn** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetRenameColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szName,
      __in          JET_PCSTR szNameNew,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="70c1c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="70c1c-108">Parameters</span></span>

<span data-ttu-id="70c1c-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="70c1c-109">*sesid*</span></span>

<span data-ttu-id="70c1c-110">Session à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="70c1c-110">The session to use for this call.</span></span>

<span data-ttu-id="70c1c-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="70c1c-111">*tableid*</span></span>

<span data-ttu-id="70c1c-112">Curseur à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="70c1c-112">The cursor to use for this call.</span></span>

<span data-ttu-id="70c1c-113">*szName*</span><span class="sxs-lookup"><span data-stu-id="70c1c-113">*szName*</span></span>

<span data-ttu-id="70c1c-114">Nom actuel de la colonne qui sera renommée.</span><span class="sxs-lookup"><span data-stu-id="70c1c-114">The current name of the column that will be renamed.</span></span>

<span data-ttu-id="70c1c-115">*szNameNew*</span><span class="sxs-lookup"><span data-stu-id="70c1c-115">*szNameNew*</span></span>

<span data-ttu-id="70c1c-116">Nouveau nom de la colonne qui sera renommée.</span><span class="sxs-lookup"><span data-stu-id="70c1c-116">The new name for the column that will be renamed.</span></span>

<span data-ttu-id="70c1c-117">*grbit*</span><span class="sxs-lookup"><span data-stu-id="70c1c-117">*grbit*</span></span>

<span data-ttu-id="70c1c-118">Ce paramètre doit avoir la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="70c1c-118">This parameter must be 0.</span></span>

### <a name="return-value"></a><span data-ttu-id="70c1c-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="70c1c-119">Return Value</span></span>

<span data-ttu-id="70c1c-120">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="70c1c-120">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="70c1c-121">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="70c1c-121">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="70c1c-122">Code de retour</span><span class="sxs-lookup"><span data-stu-id="70c1c-122">Return code</span></span></p></th>
<th><p><span data-ttu-id="70c1c-123">Description</span><span class="sxs-lookup"><span data-stu-id="70c1c-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="70c1c-124">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="70c1c-124">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="70c1c-125">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="70c1c-125">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70c1c-126">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="70c1c-126">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="70c1c-127">Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="70c1c-127">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70c1c-128">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="70c1c-128">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="70c1c-129">La colonne spécifiée n’existe pas pour cette table.</span><span class="sxs-lookup"><span data-stu-id="70c1c-129">This specified column does not exist for this table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70c1c-130">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="70c1c-130">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="70c1c-131">L’un des noms d’objets spécifiés n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="70c1c-131">One of the specified object names was invalid.</span></span> <span data-ttu-id="70c1c-132">Tous les noms d’objets doivent être conformes au même ensemble de règles.</span><span class="sxs-lookup"><span data-stu-id="70c1c-132">All object names must conform to the same set of rules.</span></span> <span data-ttu-id="70c1c-133">Ces règles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="70c1c-133">These rules are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="70c1c-134">Les noms d’objets doivent être composés de caractères ASCII.</span><span class="sxs-lookup"><span data-stu-id="70c1c-134">Object names must be composed of ASCII characters.</span></span></p></li>
<li><p><span data-ttu-id="70c1c-135">Les noms d’objets doivent comporter au moins un caractère.</span><span class="sxs-lookup"><span data-stu-id="70c1c-135">Object names must be at least one character in length.</span></span></p></li>
<li><p><span data-ttu-id="70c1c-136">Les noms d’objets ne peuvent pas dépasser JET_cbNameMost (64) caractères.</span><span class="sxs-lookup"><span data-stu-id="70c1c-136">Object names may not exceed JET_cbNameMost (64) characters in length.</span></span></p></li>
<li><p><span data-ttu-id="70c1c-137">Les noms d’objets ne peuvent pas commencer par un espace. les noms d’objets ne peuvent pas contenir de caractères de contrôle ASCII (0x00 à 0x1F).</span><span class="sxs-lookup"><span data-stu-id="70c1c-137">Object names may not begin with a space - object names may not contain ASCII control characters (0x00 through 0x1F).</span></span></p></li>
<li><p><span data-ttu-id="70c1c-138">Les noms d’objets ne peuvent pas contenir de point d’exclamation ( !), de point (.), de crochet gauche ([) ou de crochet droit (]).</span><span class="sxs-lookup"><span data-stu-id="70c1c-138">Object names may not contain an exclamation point (!), period (.), left bracket ([), or right bracket (]) character.</span></span></p></li>
<li><p><span data-ttu-id="70c1c-139">Une fois validée, seule la partie de la chaîne jusqu’au premier espace (le cas échéant) sera utilisée pour le nom de l’objet.</span><span class="sxs-lookup"><span data-stu-id="70c1c-139">Once validated, only the portion of the string up to the first space (if any) will be used for the object name.</span></span> <span data-ttu-id="70c1c-140">Cela signifie que les noms d’objets ne peuvent pas non plus contenir d’espace.</span><span class="sxs-lookup"><span data-stu-id="70c1c-140">This effectively means that object names may not contain a space either.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70c1c-141">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="70c1c-141">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="70c1c-142">L’un des paramètres fournis contenait une valeur inattendue ou contenait une valeur qui n’a pas de sens lorsqu’elle était associée à la valeur d’un autre paramètre.</span><span class="sxs-lookup"><span data-stu-id="70c1c-142">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="70c1c-143">Cela peut se produire pour <strong>JetRenameColumn</strong> dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="70c1c-143">This can happen for <strong>JetRenameColumn</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="70c1c-144"><em>szName</em> a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="70c1c-144"><em>szName</em> is NULL.</span></span></p></li>
<li><p><span data-ttu-id="70c1c-145"><em>szNameNew</em> a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="70c1c-145"><em>szNameNew</em> is NULL.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70c1c-146">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="70c1c-146">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="70c1c-147">Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="70c1c-147">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="70c1c-148">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="70c1c-148">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70c1c-149">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="70c1c-149">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="70c1c-150">Cette opération ne peut être effectuée que si la session n’est pas actuellement à l’intérieur d’une transaction.</span><span class="sxs-lookup"><span data-stu-id="70c1c-150">This operation may only be performed when the session is not currently inside a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70c1c-151">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="70c1c-151">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="70c1c-152">Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="70c1c-152">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70c1c-153">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="70c1c-153">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="70c1c-154">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="70c1c-154">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70c1c-155">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="70c1c-155">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="70c1c-156">La même session ne peut pas être utilisée simultanément pour plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="70c1c-156">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="70c1c-157">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="70c1c-157">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70c1c-158">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="70c1c-158">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="70c1c-159">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="70c1c-159">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70c1c-160">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="70c1c-160">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="70c1c-161">Une mise à jour ne peut pas être effectuée dans l’étendue d’une transaction en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="70c1c-161">An update cannot be done while inside the scope of a read-only transaction.</span></span> <span data-ttu-id="70c1c-162">Une transaction en lecture seule est une transaction qui a été démarrée à l’aide d’un appel à <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> avec JET_bitTransactionReadOnly.</span><span class="sxs-lookup"><span data-stu-id="70c1c-162">A read-only transaction is a transaction that has been started using a call to <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> with JET_bitTransactionReadOnly.</span></span> <span data-ttu-id="70c1c-163">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="70c1c-163">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="70c1c-164">En cas de réussite, le nom de la colonne spécifiée dans la table associée au curseur est définitivement remplacé par le nouveau nom.</span><span class="sxs-lookup"><span data-stu-id="70c1c-164">On success, the name of the specified column in the table associated with the cursor is permanently changed to the new name.</span></span> <span data-ttu-id="70c1c-165">Tous les index qui font référence à cette colonne seront également mis à jour.</span><span class="sxs-lookup"><span data-stu-id="70c1c-165">Any indexes that reference that column will also be updated.</span></span>

<span data-ttu-id="70c1c-166">En cas d’échec, aucune modification de l’état de la base de données ne se produit.</span><span class="sxs-lookup"><span data-stu-id="70c1c-166">On failure, no change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="70c1c-167">Notes</span><span class="sxs-lookup"><span data-stu-id="70c1c-167">Remarks</span></span>

<span data-ttu-id="70c1c-168">L’opération de changement de nom de colonne est inhabituelle car, contrairement aux autres opérations de schéma, elle n’est pas exécutée en tant que transaction.</span><span class="sxs-lookup"><span data-stu-id="70c1c-168">The column rename operation is unusual because, unlike other schema operations, it is not carried out as a transaction.</span></span> <span data-ttu-id="70c1c-169">Lorsqu’une colonne d’une table donnée est renommée dans une session, toute autre session utilisant cette table verra immédiatement la modification, même si elle se trouve dans une transaction qui empêche cette session de voir toute autre modification apportée par la session à effectuer l’opération de changement de nom.</span><span class="sxs-lookup"><span data-stu-id="70c1c-169">When a column in a given table is renamed in one session then any other session using that table will see the change immediately, even if they are in a transaction that would prevent that session from seeing any other change made by the session doing the rename operation.</span></span>

<span data-ttu-id="70c1c-170">L’ID de colonne d’une colonne n’est pas affecté par l’opération de changement de nom.</span><span class="sxs-lookup"><span data-stu-id="70c1c-170">The column ID of a column is not affected by the rename operation.</span></span>

#### <a name="requirements"></a><span data-ttu-id="70c1c-171">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="70c1c-171">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="70c1c-172"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="70c1c-172"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="70c1c-173">Nécessite Windows Vista ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="70c1c-173">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70c1c-174"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="70c1c-174"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="70c1c-175">Requiert Windows Server 2008 ou Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="70c1c-175">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70c1c-176"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="70c1c-176"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="70c1c-177">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="70c1c-177">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70c1c-178"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="70c1c-178"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="70c1c-179">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="70c1c-179">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70c1c-180"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="70c1c-180"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="70c1c-181">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="70c1c-181">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70c1c-182"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="70c1c-182"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="70c1c-183">Implémenté en tant que <strong>JetRenameColumnW</strong> (Unicode) et <strong>JetRenameColumnA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="70c1c-183">Implemented as <strong>JetRenameColumnW</strong> (Unicode) and <strong>JetRenameColumnA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="70c1c-184">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="70c1c-184">See Also</span></span>

[<span data-ttu-id="70c1c-185">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="70c1c-185">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="70c1c-186">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="70c1c-186">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="70c1c-187">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="70c1c-187">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="70c1c-188">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="70c1c-188">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="70c1c-189">JetBeginTransaction2</span><span class="sxs-lookup"><span data-stu-id="70c1c-189">JetBeginTransaction2</span></span>](./jetbegintransaction2-function.md)
