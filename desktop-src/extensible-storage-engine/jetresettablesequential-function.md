---
description: 'En savoir plus sur : fonction JetResetTableSequential'
title: JetResetTableSequential fonction)
TOCTitle: JetResetTableSequential Function
ms:assetid: 5fe9daf2-5ef1-46d6-b0c3-ef92fb57d8bb
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269261(v=EXCHG.10)
ms:contentKeyID: 32765563
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetResetTableSequential
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 86de80ac935af81fd2b4e8fdfef8b20dbb8d27d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106527516"
---
# <a name="jetresettablesequential-function"></a><span data-ttu-id="2ef14-103">JetResetTableSequential fonction)</span><span class="sxs-lookup"><span data-stu-id="2ef14-103">JetResetTableSequential Function</span></span>


<span data-ttu-id="2ef14-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="2ef14-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetresettablesequential-function"></a><span data-ttu-id="2ef14-105">JetResetTableSequential fonction)</span><span class="sxs-lookup"><span data-stu-id="2ef14-105">JetResetTableSequential Function</span></span>

<span data-ttu-id="2ef14-106">La fonction **JetResetTableSequential** informe le moteur de base de données que l’application n’analyse plus la totalité de l’index actuel contenant un curseur donné.</span><span class="sxs-lookup"><span data-stu-id="2ef14-106">The **JetResetTableSequential** function notifies the database engine that the application is no longer scanning the entire current index containing a given cursor.</span></span> <span data-ttu-id="2ef14-107">Cet appel inverse une notification envoyée par [JetSetTableSequential](./jetsettablesequential-function.md).</span><span class="sxs-lookup"><span data-stu-id="2ef14-107">This call reverses a notification sent by [JetSetTableSequential](./jetsettablesequential-function.md).</span></span>

<span data-ttu-id="2ef14-108">**Windows XP :**   **JetResetTableSequential** est introduit dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2ef14-108">**Windows XP:**   **JetResetTableSequential** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetResetTableSequential(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="2ef14-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2ef14-109">Parameters</span></span>

<span data-ttu-id="2ef14-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="2ef14-110">*sesid*</span></span>

<span data-ttu-id="2ef14-111">Session à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="2ef14-111">The session to use for this call.</span></span>

<span data-ttu-id="2ef14-112">*TableID*</span><span class="sxs-lookup"><span data-stu-id="2ef14-112">*tableid*</span></span>

<span data-ttu-id="2ef14-113">Curseur à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="2ef14-113">The cursor to use for this call.</span></span>

<span data-ttu-id="2ef14-114">*grbit*</span><span class="sxs-lookup"><span data-stu-id="2ef14-114">*grbit*</span></span>

<span data-ttu-id="2ef14-115">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="2ef14-115">Reserved for future use.</span></span>

### <a name="return-value"></a><span data-ttu-id="2ef14-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2ef14-116">Return Value</span></span>

<span data-ttu-id="2ef14-117">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="2ef14-117">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="2ef14-118">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="2ef14-118">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2ef14-119">Code de retour</span><span class="sxs-lookup"><span data-stu-id="2ef14-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="2ef14-120">Description</span><span class="sxs-lookup"><span data-stu-id="2ef14-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2ef14-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="2ef14-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="2ef14-122">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="2ef14-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2ef14-123">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="2ef14-123">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="2ef14-124">Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="2ef14-124">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2ef14-125">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="2ef14-125">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="2ef14-126">Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="2ef14-126">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="2ef14-127">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="2ef14-127">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2ef14-128">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="2ef14-128">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="2ef14-129">Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="2ef14-129">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2ef14-130">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="2ef14-130">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="2ef14-131">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="2ef14-131">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2ef14-132">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="2ef14-132">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="2ef14-133">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="2ef14-133">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2ef14-134">En cas de réussite, l’index actuel du curseur n’est plus optimisé pour une analyse séquentielle de la totalité de l’index.</span><span class="sxs-lookup"><span data-stu-id="2ef14-134">On success, the current index of the cursor is no longer optimized for a sequential scan of the entire index.</span></span> <span data-ttu-id="2ef14-135">Aucune modification de l’état de la base de données ne se produit.</span><span class="sxs-lookup"><span data-stu-id="2ef14-135">No change to the database state will occur.</span></span>

<span data-ttu-id="2ef14-136">En cas d’échec, aucune modification de la configuration du curseur ne se produit.</span><span class="sxs-lookup"><span data-stu-id="2ef14-136">On failure, no change to the configuration of the cursor will occur.</span></span> <span data-ttu-id="2ef14-137">Aucune modification de l’état de la base de données ne se produit.</span><span class="sxs-lookup"><span data-stu-id="2ef14-137">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="2ef14-138">Notes</span><span class="sxs-lookup"><span data-stu-id="2ef14-138">Remarks</span></span>

<span data-ttu-id="2ef14-139">Il est possible d’effectuer cet appel sur un curseur qui n’a pas été précédemment configuré par un appel à [JetSetTableSequential](./jetsettablesequential-function.md).</span><span class="sxs-lookup"><span data-stu-id="2ef14-139">It is safe to make this call against a cursor that has not been previously configured by a call to [JetSetTableSequential](./jetsettablesequential-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="2ef14-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2ef14-140">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2ef14-141"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="2ef14-141"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="2ef14-142">Nécessite Windows Vista ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2ef14-142">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2ef14-143"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="2ef14-143"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="2ef14-144">Requiert Windows Server 2008 ou Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="2ef14-144">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2ef14-145"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="2ef14-145"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="2ef14-146">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="2ef14-146">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2ef14-147"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="2ef14-147"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="2ef14-148">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="2ef14-148">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2ef14-149"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="2ef14-149"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="2ef14-150">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="2ef14-150">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="2ef14-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2ef14-151">See Also</span></span>

[<span data-ttu-id="2ef14-152">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="2ef14-152">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="2ef14-153">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="2ef14-153">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="2ef14-154">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="2ef14-154">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="2ef14-155">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="2ef14-155">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="2ef14-156">JetSetTableSequential</span><span class="sxs-lookup"><span data-stu-id="2ef14-156">JetSetTableSequential</span></span>](./jetsettablesequential-function.md)  
[<span data-ttu-id="2ef14-157">JetStopService</span><span class="sxs-lookup"><span data-stu-id="2ef14-157">JetStopService</span></span>](./jetstopservice-function.md)
