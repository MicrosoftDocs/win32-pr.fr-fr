---
description: 'En savoir plus sur : fonction JetRegisterCallback'
title: Fonction JetRegisterCallback
TOCTitle: JetRegisterCallback Function
ms:assetid: 04c82fac-ffa2-477f-b4dd-59bbf1dde3c8
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269175(v=EXCHG.10)
ms:contentKeyID: 32765478
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRegisterCallback
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 26ca7559488182f2d687d5c678639e108792f413
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529117"
---
# <a name="jetregistercallback-function"></a><span data-ttu-id="a6b7f-103">Fonction JetRegisterCallback</span><span class="sxs-lookup"><span data-stu-id="a6b7f-103">JetRegisterCallback Function</span></span>


<span data-ttu-id="a6b7f-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="a6b7f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetregistercallback-function"></a><span data-ttu-id="a6b7f-105">Fonction JetRegisterCallback</span><span class="sxs-lookup"><span data-stu-id="a6b7f-105">JetRegisterCallback Function</span></span>

<span data-ttu-id="a6b7f-106">La fonction **JetRegisterCallback** permet à l’application de configurer le moteur de base de données pour émettre des notifications à l’application pour des événements spécifiques.</span><span class="sxs-lookup"><span data-stu-id="a6b7f-106">The **JetRegisterCallback** function allows the application to configure the database engine to issue notifications to the application for specific events.</span></span> <span data-ttu-id="a6b7f-107">Ces notifications sont associées à une table spécifique et restent effectives uniquement jusqu’à ce que l’instance contenant la table soit arrêtée à l’aide de [JetTerm](./jetterm-function.md).</span><span class="sxs-lookup"><span data-stu-id="a6b7f-107">These notifications are associated with a specific table and remain in effect only until the instance containing the table is shut down using [JetTerm](./jetterm-function.md).</span></span>

<span data-ttu-id="a6b7f-108">**Windows XP : JetRegisterCallback** est introduit dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a6b7f-108">**Windows XP:  JetRegisterCallback** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetRegisterCallback(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_CBTYP cbtyp,
      __in          JET_CALLBACK pCallback,
      __in          void* pvContext,
      __out         JET_HANDLE* phCallbackId
    );
```

### <a name="parameters"></a><span data-ttu-id="a6b7f-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a6b7f-109">Parameters</span></span>

<span data-ttu-id="a6b7f-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="a6b7f-110">*sesid*</span></span>

<span data-ttu-id="a6b7f-111">Session à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="a6b7f-111">The session to use for this call.</span></span>

<span data-ttu-id="a6b7f-112">*TableID*</span><span class="sxs-lookup"><span data-stu-id="a6b7f-112">*tableid*</span></span>

<span data-ttu-id="a6b7f-113">Curseur à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="a6b7f-113">The cursor to use for this call.</span></span>

<span data-ttu-id="a6b7f-114">*cbtyp*</span><span class="sxs-lookup"><span data-stu-id="a6b7f-114">*cbtyp*</span></span>

<span data-ttu-id="a6b7f-115">Masque de bits composé des raisons de rappel pour lesquelles l’application souhaite recevoir des notifications.</span><span class="sxs-lookup"><span data-stu-id="a6b7f-115">A bit mask composed of the callback reasons for which the application wishes to receive notifications.</span></span>

<span data-ttu-id="a6b7f-116">Pour créer ce masque de bits, tout simplement ou ensemble des raisons de rappel valides à partir de l’énumération [JET_CBTYP](./jet-cbtyp.md) .</span><span class="sxs-lookup"><span data-stu-id="a6b7f-116">To create this bit mask, simply or together valid callback reasons from the [JET_CBTYP](./jet-cbtyp.md) enumeration.</span></span>

<span data-ttu-id="a6b7f-117">*pCallback*</span><span class="sxs-lookup"><span data-stu-id="a6b7f-117">*pCallback*</span></span>

<span data-ttu-id="a6b7f-118">Pointeur de fonction vers la fonction de rappel pour l’application.</span><span class="sxs-lookup"><span data-stu-id="a6b7f-118">The function pointer to the callback function for the application.</span></span>

<span data-ttu-id="a6b7f-119">*pvContext*</span><span class="sxs-lookup"><span data-stu-id="a6b7f-119">*pvContext*</span></span>

<span data-ttu-id="a6b7f-120">Spécifie un pointeur de contexte qui sera attribué à la fonction de rappel pour l’application.</span><span class="sxs-lookup"><span data-stu-id="a6b7f-120">Specifies a context pointer that will be given to the callback function for the application.</span></span>

<span data-ttu-id="a6b7f-121">*phCallbackId*</span><span class="sxs-lookup"><span data-stu-id="a6b7f-121">*phCallbackId*</span></span>

<span data-ttu-id="a6b7f-122">Retourne un handle qui peut être utilisé ultérieurement pour annuler l’inscription de la fonction de rappel donnée à l’aide de [JetUnregisterCallback](./jetunregistercallback-function.md).</span><span class="sxs-lookup"><span data-stu-id="a6b7f-122">Returns a handle that can later be used to cancel the registration of the given callback function using [JetUnregisterCallback](./jetunregistercallback-function.md).</span></span>

### <a name="return-value"></a><span data-ttu-id="a6b7f-123">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a6b7f-123">Return Value</span></span>

<span data-ttu-id="a6b7f-124">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="a6b7f-124">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="a6b7f-125">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="a6b7f-125">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a6b7f-126">Code de retour</span><span class="sxs-lookup"><span data-stu-id="a6b7f-126">Return code</span></span></p></th>
<th><p><span data-ttu-id="a6b7f-127">Description</span><span class="sxs-lookup"><span data-stu-id="a6b7f-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a6b7f-128">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="a6b7f-128">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="a6b7f-129">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="a6b7f-129">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6b7f-130">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="a6b7f-130">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="a6b7f-131">Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="a6b7f-131">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6b7f-132">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="a6b7f-132">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="a6b7f-133">Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="a6b7f-133">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="a6b7f-134">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="a6b7f-134">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6b7f-135">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="a6b7f-135">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="a6b7f-136">L’un des paramètres fournis contenait une valeur inattendue ou contenait une valeur qui n’a pas de sens lorsqu’elle était associée à la valeur d’un autre paramètre.</span><span class="sxs-lookup"><span data-stu-id="a6b7f-136">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="a6b7f-137">Cette erreur est retournée par <strong>JetRegisterCallback</strong> quand :</span><span class="sxs-lookup"><span data-stu-id="a6b7f-137">This error will be returned by <strong>JetRegisterCallback</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="a6b7f-138"><em>cbtyp</em> est égal à zéro,</span><span class="sxs-lookup"><span data-stu-id="a6b7f-138"><em>cbtyp</em> is zero,</span></span></p></li>
<li><p><span data-ttu-id="a6b7f-139"><em>pCallback</em> a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="a6b7f-139"><em>pCallback</em> is NULL.</span></span></p></li>
<li><p><span data-ttu-id="a6b7f-140"><em>phCallbackId</em> a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="a6b7f-140"><em>phCallbackId</em> is NULL.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6b7f-141">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="a6b7f-141">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="a6b7f-142">Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="a6b7f-142">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6b7f-143">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="a6b7f-143">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="a6b7f-144">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="a6b7f-144">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6b7f-145">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="a6b7f-145">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="a6b7f-146">La même session ne peut pas être utilisée simultanément pour plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="a6b7f-146">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="a6b7f-147">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="a6b7f-147">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6b7f-148">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="a6b7f-148">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="a6b7f-149">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="a6b7f-149">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a6b7f-150">En cas de réussite, le rappel spécifié sera inscrit pour les raisons de rappel données avec la table associée au curseur donné.</span><span class="sxs-lookup"><span data-stu-id="a6b7f-150">On success, the specified callback will be registered for the given callback reasons with the table associated with the given cursor.</span></span> <span data-ttu-id="a6b7f-151">Aucune modification de l’état de la base de données ne se produit.</span><span class="sxs-lookup"><span data-stu-id="a6b7f-151">No change to the database state will occur.</span></span>

<span data-ttu-id="a6b7f-152">En cas d’échec, le rappel n’est pas inscrit.</span><span class="sxs-lookup"><span data-stu-id="a6b7f-152">On failure, the callback will not be registered.</span></span> <span data-ttu-id="a6b7f-153">Aucune modification de l’état de la base de données ne se produit.</span><span class="sxs-lookup"><span data-stu-id="a6b7f-153">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="a6b7f-154">Notes</span><span class="sxs-lookup"><span data-stu-id="a6b7f-154">Remarks</span></span>

<span data-ttu-id="a6b7f-155">Cette méthode permet à l’application d’associer des rappels volatiles à une table dans une base de données.</span><span class="sxs-lookup"><span data-stu-id="a6b7f-155">This method provides a means for the application to associate volatile callbacks with a table in a database.</span></span> <span data-ttu-id="a6b7f-156">Si l’application souhaite associer les rappels rendus persistants à une table dans la base de données, elle doit passer le rappel à [JET_TABLECREATE](./jet-tablecreate-structure.md) à l’aide de [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span><span class="sxs-lookup"><span data-stu-id="a6b7f-156">If the application wishes to associate persisted callbacks with a table in the database then it should pass the callback to [JET_TABLECREATE](./jet-tablecreate-structure.md) using [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="a6b7f-157">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a6b7f-157">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a6b7f-158"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="a6b7f-158"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a6b7f-159">Nécessite Windows Vista ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a6b7f-159">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6b7f-160"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="a6b7f-160"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a6b7f-161">Requiert Windows Server 2008 ou Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a6b7f-161">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6b7f-162"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="a6b7f-162"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a6b7f-163">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="a6b7f-163">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6b7f-164"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="a6b7f-164"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="a6b7f-165">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="a6b7f-165">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6b7f-166"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="a6b7f-166"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="a6b7f-167">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="a6b7f-167">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="a6b7f-168">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a6b7f-168">See Also</span></span>

[<span data-ttu-id="a6b7f-169">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="a6b7f-169">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)  
[<span data-ttu-id="a6b7f-170">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="a6b7f-170">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="a6b7f-171">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="a6b7f-171">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="a6b7f-172">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="a6b7f-172">JET_HANDLE</span></span>](./jet-handle.md)  
[<span data-ttu-id="a6b7f-173">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="a6b7f-173">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="a6b7f-174">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="a6b7f-174">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="a6b7f-175">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="a6b7f-175">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="a6b7f-176">JetTerm</span><span class="sxs-lookup"><span data-stu-id="a6b7f-176">JetTerm</span></span>](./jetterm-function.md)  
[<span data-ttu-id="a6b7f-177">JetUnregisterCallback</span><span class="sxs-lookup"><span data-stu-id="a6b7f-177">JetUnregisterCallback</span></span>](./jetunregistercallback-function.md)
