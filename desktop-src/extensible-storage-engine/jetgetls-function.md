---
description: 'En savoir plus sur : fonction JetGetLS'
title: JetGetLS fonction)
TOCTitle: JetGetLS Function
ms:assetid: 411baf34-d167-4633-81af-be4886f4a646
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269234(v=EXCHG.10)
ms:contentKeyID: 32765536
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetLS
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b7a89cf4e20798a2c412ba6eb39b08f99a60a464
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520755"
---
# <a name="jetgetls-function"></a><span data-ttu-id="d279c-103">JetGetLS fonction)</span><span class="sxs-lookup"><span data-stu-id="d279c-103">JetGetLS Function</span></span>


<span data-ttu-id="d279c-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="d279c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetls-function"></a><span data-ttu-id="d279c-105">JetGetLS fonction)</span><span class="sxs-lookup"><span data-stu-id="d279c-105">JetGetLS Function</span></span>

<span data-ttu-id="d279c-106">La fonction **JetGetLS** permet à l’application de récupérer le descripteur de contexte appelé stockage local qui est associé à un curseur ou la table associée à ce curseur.</span><span class="sxs-lookup"><span data-stu-id="d279c-106">The **JetGetLS** function enables the application to retrieve the context handle known as Local Storage that is associated with a cursor or the table associated with that cursor.</span></span> <span data-ttu-id="d279c-107">Ce descripteur de contexte doit avoir été défini précédemment à l’aide de [JetSetLS](./jetsetls-function.md).</span><span class="sxs-lookup"><span data-stu-id="d279c-107">This context handle must have been previously set using [JetSetLS](./jetsetls-function.md).</span></span> <span data-ttu-id="d279c-108">**JetGetLS** peut également être utilisé pour extraire simultanément le descripteur de contexte actuel d’un curseur ou d’une table et réinitialiser ce handle de contexte.</span><span class="sxs-lookup"><span data-stu-id="d279c-108">**JetGetLS** can also be used to simultaneously fetch the current context handle for a cursor or table and reset that context handle.</span></span>

<span data-ttu-id="d279c-109">**Windows XP : JetGetLS** est introduit dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d279c-109">**Windows XP:  JetGetLS** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetGetLS(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_LS* pls,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="d279c-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d279c-110">Parameters</span></span>

<span data-ttu-id="d279c-111">*sesid*</span><span class="sxs-lookup"><span data-stu-id="d279c-111">*sesid*</span></span>

<span data-ttu-id="d279c-112">Session à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="d279c-112">The session to use for this call.</span></span>

<span data-ttu-id="d279c-113">*TableID*</span><span class="sxs-lookup"><span data-stu-id="d279c-113">*tableid*</span></span>

<span data-ttu-id="d279c-114">Curseur à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="d279c-114">The cursor to use for this call.</span></span>

<span data-ttu-id="d279c-115">*pls*</span><span class="sxs-lookup"><span data-stu-id="d279c-115">*pls*</span></span>

<span data-ttu-id="d279c-116">Mémoire tampon de sortie qui reçoit le handle de contexte actuellement associé au curseur ou à la table.</span><span class="sxs-lookup"><span data-stu-id="d279c-116">The output buffer that receives the context handle currently associated with the cursor or table.</span></span>

<span data-ttu-id="d279c-117">*grbit*</span><span class="sxs-lookup"><span data-stu-id="d279c-117">*grbit*</span></span>

<span data-ttu-id="d279c-118">Groupe de bits spécifiant zéro ou plusieurs des options suivantes.</span><span class="sxs-lookup"><span data-stu-id="d279c-118">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d279c-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="d279c-119">Value</span></span></p></th>
<th><p><span data-ttu-id="d279c-120">Signification</span><span class="sxs-lookup"><span data-stu-id="d279c-120">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d279c-121">JET_bitLSCursor</span><span class="sxs-lookup"><span data-stu-id="d279c-121">JET_bitLSCursor</span></span></p></td>
<td><p><span data-ttu-id="d279c-122">Indique que le handle de contexte associé au curseur donné doit être récupéré.</span><span class="sxs-lookup"><span data-stu-id="d279c-122">Indicates that the context handle associated with the given cursor should be retrieved.</span></span></p>
<p><span data-ttu-id="d279c-123">Si ni JET_bitLSCursor ni JET_bitLSTable n’est spécifié, JET_bitLSCursor est présumé.</span><span class="sxs-lookup"><span data-stu-id="d279c-123">If neither JET_bitLSCursor nor JET_bitLSTable is specified then JET_bitLSCursor is presumed.</span></span></p>
<p><span data-ttu-id="d279c-124">Cette option ne peut pas être utilisée avec JET_bitLSTable.</span><span class="sxs-lookup"><span data-stu-id="d279c-124">This option cannot be used with JET_bitLSTable.</span></span> <span data-ttu-id="d279c-125">L’opération échouera avec JET_errInvalidgrbit si cette tentative est effectuée.</span><span class="sxs-lookup"><span data-stu-id="d279c-125">The operation will fail with JET_errInvalidgrbit if this is attempted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d279c-126">JET_bitLSTable</span><span class="sxs-lookup"><span data-stu-id="d279c-126">JET_bitLSTable</span></span></p></td>
<td><p><span data-ttu-id="d279c-127">Indique que le handle de contexte associé à la table qui contient le curseur donné doit être récupéré.</span><span class="sxs-lookup"><span data-stu-id="d279c-127">Indicates that the context handle associated to the table that contains the given cursor should be retrieved.</span></span> <span data-ttu-id="d279c-128">L’utilisation de cette option avec JET_bitLSCursor n’est pas autorisée.</span><span class="sxs-lookup"><span data-stu-id="d279c-128">It is illegal to use this option with JET_bitLSCursor.</span></span> <span data-ttu-id="d279c-129">L’opération échouera avec JET_errInvalidgrbit si cette tentative est effectuée.</span><span class="sxs-lookup"><span data-stu-id="d279c-129">The operation will fail with JET_errInvalidgrbit if this is attempted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d279c-130">JET_bitLSReset</span><span class="sxs-lookup"><span data-stu-id="d279c-130">JET_bitLSReset</span></span></p></td>
<td><p><span data-ttu-id="d279c-131">Indique que le handle de contexte pour l’objet choisi doit être réinitialisé à JET_LSNil.</span><span class="sxs-lookup"><span data-stu-id="d279c-131">Indicates that the context handle for the chosen object should be reset to JET_LSNil.</span></span> <span data-ttu-id="d279c-132">La valeur actuelle du handle de contexte est retournée dans la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="d279c-132">The current value of the context handle is returned in the output buffer.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="d279c-133">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d279c-133">Return Value</span></span>

<span data-ttu-id="d279c-134">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="d279c-134">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="d279c-135">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="d279c-135">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d279c-136">Code de retour</span><span class="sxs-lookup"><span data-stu-id="d279c-136">Return code</span></span></p></th>
<th><p><span data-ttu-id="d279c-137">Description</span><span class="sxs-lookup"><span data-stu-id="d279c-137">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d279c-138">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="d279c-138">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="d279c-139">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="d279c-139">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d279c-140">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="d279c-140">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="d279c-141">Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="d279c-141">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d279c-142">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="d279c-142">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="d279c-143">Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="d279c-143">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="d279c-144">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d279c-144">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d279c-145">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="d279c-145">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="d279c-146">L’une des options demandées n’est pas valide, utilisée de manière non conforme ou non implémentée.</span><span class="sxs-lookup"><span data-stu-id="d279c-146">One of the options requested was invalid, used in an illegal manner, or not implemented.</span></span></p>
<p><span data-ttu-id="d279c-147">Cela peut se produire pour <strong>JetGetLS</strong> quand les JET_bitLSCursor et les JET_bitLSTable sont définis.</span><span class="sxs-lookup"><span data-stu-id="d279c-147">This can happen for <strong>JetGetLS</strong> when both JET_bitLSCursor and JET_bitLSTable are set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d279c-148">JET_errLSNotSet</span><span class="sxs-lookup"><span data-stu-id="d279c-148">JET_errLSNotSet</span></span></p></td>
<td><p><span data-ttu-id="d279c-149">Impossible de retourner le descripteur de contexte, car aucun descripteur de contexte n’est actuellement associé à l’objet demandé.</span><span class="sxs-lookup"><span data-stu-id="d279c-149">The context handle could not be returned because no context handle is currently associated with the requested object.</span></span></p>
<p><span data-ttu-id="d279c-150"><strong>Remarque  </strong> Cette erreur n’est pas renvoyée si JET_bitLSReset est spécifié mais qu’aucun handle de contexte n’a été associé à l’objet demandé.</span><span class="sxs-lookup"><span data-stu-id="d279c-150"><strong>Note  </strong> This error is not returned if JET_bitLSReset is specified yet no context handle was associated with the requested object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d279c-151">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="d279c-151">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="d279c-152">Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="d279c-152">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d279c-153">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="d279c-153">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="d279c-154">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="d279c-154">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d279c-155">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="d279c-155">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="d279c-156">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="d279c-156">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d279c-157">En cas de réussite, le handle de contexte a été récupéré à partir de l’objet demandé.</span><span class="sxs-lookup"><span data-stu-id="d279c-157">On success, the context handle was successfully retrieved from the requested object.</span></span> <span data-ttu-id="d279c-158">Si JET_bitLSReset a été spécifié, ce handle de contexte a également été correctement supprimé de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d279c-158">If JET_bitLSReset was specified then that context handle was also successfully removed from the object.</span></span> <span data-ttu-id="d279c-159">Aucune modification de l’état de la base de données ne se produit.</span><span class="sxs-lookup"><span data-stu-id="d279c-159">No change to the database state will occur.</span></span>

<span data-ttu-id="d279c-160">En cas d’échec, aucune modification de l’état de l’objet demandé n’est survenue.</span><span class="sxs-lookup"><span data-stu-id="d279c-160">On failure, no change to the state of the requested object has occurred.</span></span> <span data-ttu-id="d279c-161">Aucune modification de l’état de la base de données ne se produit.</span><span class="sxs-lookup"><span data-stu-id="d279c-161">No change to the database state will occur.</span></span>

#### <a name="requirements"></a><span data-ttu-id="d279c-162">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d279c-162">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d279c-163"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="d279c-163"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="d279c-164">Nécessite Windows Vista ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d279c-164">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d279c-165"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="d279c-165"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d279c-166">Requiert Windows Server 2008 ou Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d279c-166">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d279c-167"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="d279c-167"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="d279c-168">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="d279c-168">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d279c-169"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="d279c-169"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="d279c-170">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="d279c-170">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d279c-171"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="d279c-171"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="d279c-172">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="d279c-172">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="d279c-173">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d279c-173">See Also</span></span>

[<span data-ttu-id="d279c-174">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="d279c-174">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="d279c-175">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="d279c-175">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="d279c-176">JET_LS</span><span class="sxs-lookup"><span data-stu-id="d279c-176">JET_LS</span></span>](./jet-ls.md)  
[<span data-ttu-id="d279c-177">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="d279c-177">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="d279c-178">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="d279c-178">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="d279c-179">JetSetLS</span><span class="sxs-lookup"><span data-stu-id="d279c-179">JetSetLS</span></span>](./jetsetls-function.md)
