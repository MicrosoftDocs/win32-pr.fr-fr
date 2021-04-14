---
description: 'En savoir plus sur : fonction JetUnregisterCallback'
title: JetUnregisterCallback fonction)
TOCTitle: JetUnregisterCallback Function
ms:assetid: de5c7afa-07e1-4687-989b-b56125a9712e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294116(v=EXCHG.10)
ms:contentKeyID: 32765730
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetUnregisterCallback
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b342bab655e3cf1e3c1a5967410edb1c971af87b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393471"
---
# <a name="jetunregistercallback-function"></a><span data-ttu-id="8499f-103">JetUnregisterCallback fonction)</span><span class="sxs-lookup"><span data-stu-id="8499f-103">JetUnregisterCallback Function</span></span>


<span data-ttu-id="8499f-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="8499f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetunregistercallback-function"></a><span data-ttu-id="8499f-105">JetUnregisterCallback fonction)</span><span class="sxs-lookup"><span data-stu-id="8499f-105">JetUnregisterCallback Function</span></span>

<span data-ttu-id="8499f-106">La fonction **JetUnregisterCallback** permet à l’application de configurer le moteur de base de données pour arrêter l’émission de notifications à l’application, comme demandé précédemment via [JetRegisterCallback](./jetregistercallback-function.md).</span><span class="sxs-lookup"><span data-stu-id="8499f-106">The **JetUnregisterCallback** function enables the application to configure the database engine to stop issuing notifications to the application as previously requested through [JetRegisterCallback](./jetregistercallback-function.md).</span></span>

<span data-ttu-id="8499f-107">**Windows XP :**  **JetUnregisterCallback** est introduit dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8499f-107">**Windows XP:**  **JetUnregisterCallback** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetUnregisterCallback(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_CBTYP cbtyp,
      __in          JET_HANDLE hCallbackId
    );
```

### <a name="parameters"></a><span data-ttu-id="8499f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8499f-108">Parameters</span></span>

<span data-ttu-id="8499f-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="8499f-109">*sesid*</span></span>

<span data-ttu-id="8499f-110">Session à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="8499f-110">The session to use for this call.</span></span>

<span data-ttu-id="8499f-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="8499f-111">*tableid*</span></span>

<span data-ttu-id="8499f-112">Curseur à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="8499f-112">The cursor to use for this call.</span></span>

<span data-ttu-id="8499f-113">*cbtyp*</span><span class="sxs-lookup"><span data-stu-id="8499f-113">*cbtyp*</span></span>

<span data-ttu-id="8499f-114">Masque de masque composé des raisons de rappel pour lesquelles l’application ne souhaite plus recevoir de notifications.</span><span class="sxs-lookup"><span data-stu-id="8499f-114">A bitmask composed of the callback reasons that the application no longer wishes to receive notifications.</span></span>

<span data-ttu-id="8499f-115">Pour créer ce masque de masque, il suffit ou ensemble des raisons de rappel valides de l’énumération [JET_CBTYP](./jet-cbtyp.md) .</span><span class="sxs-lookup"><span data-stu-id="8499f-115">To create this bitmask, simply or together valid callback reasons from the [JET_CBTYP](./jet-cbtyp.md) enumeration.</span></span>

<span data-ttu-id="8499f-116">*hCallbackId*</span><span class="sxs-lookup"><span data-stu-id="8499f-116">*hCallbackId*</span></span>

<span data-ttu-id="8499f-117">Handle du rappel inscrit qui a été retourné par [JetRegisterCallback](./jetregistercallback-function.md).</span><span class="sxs-lookup"><span data-stu-id="8499f-117">The handle of the registered callback that was returned by [JetRegisterCallback](./jetregistercallback-function.md).</span></span>

### <a name="return-value"></a><span data-ttu-id="8499f-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8499f-118">Return Value</span></span>

<span data-ttu-id="8499f-119">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="8499f-119">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="8499f-120">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="8499f-120">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8499f-121">Code de retour</span><span class="sxs-lookup"><span data-stu-id="8499f-121">Return code</span></span></p></th>
<th><p><span data-ttu-id="8499f-122">Description</span><span class="sxs-lookup"><span data-stu-id="8499f-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8499f-123">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="8499f-123">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="8499f-124">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="8499f-124">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8499f-125">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="8499f-125">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="8499f-126">Impossible d’effectuer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="8499f-126">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8499f-127">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="8499f-127">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="8499f-128">Impossible d’effectuer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="8499f-128">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="8499f-129"><strong>Windows XP :</strong>  Cette valeur de retour est introduite dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8499f-129"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8499f-130">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="8499f-130">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="8499f-131">Impossible d’effectuer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="8499f-131">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8499f-132">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="8499f-132">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="8499f-133">Impossible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="8499f-133">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8499f-134">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="8499f-134">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="8499f-135">La même session ne peut pas être utilisée simultanément pour plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="8499f-135">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="8499f-136"><strong>Windows XP :</strong>  Cette valeur de retour est introduite dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8499f-136"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8499f-137">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="8499f-137">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="8499f-138">L’opération ne peut pas se terminer car l’instance qui est associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="8499f-138">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8499f-139">Si cette fonction réussit, le rappel spécifié sera désinscrit pour les raisons de rappel données avec la table associée au curseur donné.</span><span class="sxs-lookup"><span data-stu-id="8499f-139">If this function succeeds, the specified callback will be unregistered for the given callback reasons with the table that is associated with the given cursor.</span></span> <span data-ttu-id="8499f-140">Aucune modification de l’état de la base de données ne se produit.</span><span class="sxs-lookup"><span data-stu-id="8499f-140">No change to the database state will occur.</span></span>

<span data-ttu-id="8499f-141">Si cette fonction échoue, le rappel spécifié n’est pas annulé.</span><span class="sxs-lookup"><span data-stu-id="8499f-141">If this function fails, the specified callback will not be unregistered.</span></span> <span data-ttu-id="8499f-142">Aucune modification de l’état de la base de données ne se produit.</span><span class="sxs-lookup"><span data-stu-id="8499f-142">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="8499f-143">Notes</span><span class="sxs-lookup"><span data-stu-id="8499f-143">Remarks</span></span>

<span data-ttu-id="8499f-144">Le masque de masque donné doit correspondre exactement au masque de données spécifié lors de l’inscription du rappel.</span><span class="sxs-lookup"><span data-stu-id="8499f-144">The given bitmask should exactly match the bitmask that is specified when registering the callback.</span></span> <span data-ttu-id="8499f-145">Le moteur de base de données ne prend pas actuellement en charge la suppression d’un sous-ensemble de ces notifications et ne renvoie pas d’erreur lorsque cette tentative est effectuée.</span><span class="sxs-lookup"><span data-stu-id="8499f-145">The database engine does not currently support removing a subset of these notifications and it does not return an error when this is attempted.</span></span>

#### <a name="requirements"></a><span data-ttu-id="8499f-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8499f-146">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8499f-147"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="8499f-147"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="8499f-148">Nécessite Windows Vista ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8499f-148">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8499f-149"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="8499f-149"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="8499f-150">Requiert Windows Server 2008 ou Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="8499f-150">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8499f-151"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="8499f-151"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="8499f-152">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="8499f-152">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8499f-153"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="8499f-153"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="8499f-154">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="8499f-154">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8499f-155"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="8499f-155"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="8499f-156">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="8499f-156">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="8499f-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8499f-157">See Also</span></span>

[<span data-ttu-id="8499f-158">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="8499f-158">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="8499f-159">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="8499f-159">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="8499f-160">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="8499f-160">JET_HANDLE</span></span>](./jet-handle.md)  
[<span data-ttu-id="8499f-161">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="8499f-161">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="8499f-162">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="8499f-162">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="8499f-163">JetRegisterCallback</span><span class="sxs-lookup"><span data-stu-id="8499f-163">JetRegisterCallback</span></span>](./jetregistercallback-function.md)  
[<span data-ttu-id="8499f-164">JetStopService</span><span class="sxs-lookup"><span data-stu-id="8499f-164">JetStopService</span></span>](./jetstopservice-function.md)
