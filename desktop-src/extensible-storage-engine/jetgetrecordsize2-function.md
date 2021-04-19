---
description: 'En savoir plus sur : fonction JetGetRecordSize2'
title: JetGetRecordSize2 fonction)
TOCTitle: JetGetRecordSize2 Function
ms:assetid: 803cfb4e-44f3-447a-b642-018e6f2f713f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269314(v=EXCHG.10)
ms:contentKeyID: 32765604
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetRecordSize2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5c68eafaaa53b5b88e6b003bdbafce287035cbc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522239"
---
# <a name="jetgetrecordsize2-function"></a><span data-ttu-id="733c4-103">JetGetRecordSize2 fonction)</span><span class="sxs-lookup"><span data-stu-id="733c4-103">JetGetRecordSize2 Function</span></span>


<span data-ttu-id="733c4-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="733c4-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetrecordsize2-function"></a><span data-ttu-id="733c4-105">JetGetRecordSize2 fonction)</span><span class="sxs-lookup"><span data-stu-id="733c4-105">JetGetRecordSize2 Function</span></span>

<span data-ttu-id="733c4-106">La fonction **JetGetRecordSize2** récupère les informations sur la taille des enregistrements à partir de l’emplacement souhaité.</span><span class="sxs-lookup"><span data-stu-id="733c4-106">The **JetGetRecordSize2** function retrieves record size information from the desired location.</span></span>

<span data-ttu-id="733c4-107">**Windows 7 : JetGetRecordSize2** est introduit dans le système d’exploitation Windows 7.</span><span class="sxs-lookup"><span data-stu-id="733c4-107">**Windows 7:  JetGetRecordSize2** is introduced in the Windows 7 operating system.</span></span>

```cpp
    JET_ERR JET_API JetGetRecordSize2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_RECSIZE2* precsize,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="733c4-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="733c4-108">Parameters</span></span>

<span data-ttu-id="733c4-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="733c4-109">*sesid*</span></span>

<span data-ttu-id="733c4-110">Identifie le contexte de session de base de données qui sera utilisé pour l’appel d’API.</span><span class="sxs-lookup"><span data-stu-id="733c4-110">Identifies the database session context that will be used for the API call.</span></span>

<span data-ttu-id="733c4-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="733c4-111">*tableid*</span></span>

<span data-ttu-id="733c4-112">Identifie la table ou le curseur qui sera utilisé pour l’appel d’API.</span><span class="sxs-lookup"><span data-stu-id="733c4-112">Identifies the table or cursor that will be used for the API call.</span></span> <span data-ttu-id="733c4-113">Le curseur doit être positionné sur un enregistrement ou avoir une mise à jour préparée.</span><span class="sxs-lookup"><span data-stu-id="733c4-113">The cursor must be positioned on a record, or have an update prepared.</span></span>

<span data-ttu-id="733c4-114">*precsize*</span><span class="sxs-lookup"><span data-stu-id="733c4-114">*precsize*</span></span>

<span data-ttu-id="733c4-115">Pointeur vers une mémoire tampon de sortie pour la structure [JET_RECSIZE2](./jet-recsize2-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="733c4-115">A pointer to an output buffer for the [JET_RECSIZE2](./jet-recsize2-structure.md) structure.</span></span>

<span data-ttu-id="733c4-116">*grbit*</span><span class="sxs-lookup"><span data-stu-id="733c4-116">*grbit*</span></span>

<span data-ttu-id="733c4-117">Il s’agit d’une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="733c4-117">This is one or more of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="733c4-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="733c4-118">Value</span></span></p></th>
<th><p><span data-ttu-id="733c4-119">Signification</span><span class="sxs-lookup"><span data-stu-id="733c4-119">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="733c4-120">JET_bitRecordSizeInCopyBuffer</span><span class="sxs-lookup"><span data-stu-id="733c4-120">JET_bitRecordSizeInCopyBuffer</span></span></p></td>
<td><p><span data-ttu-id="733c4-121">Cela récupère la taille de l’enregistrement qui se trouve dans le tampon de copie préparé pour la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="733c4-121">This retrieves the size of the record that is in the copy buffer prepared for update.</span></span> <span data-ttu-id="733c4-122">Dans le cas contraire, l' <em>TableID</em> ou le curseur doit être positionné sur un enregistrement et cet enregistrement sera utilisé.</span><span class="sxs-lookup"><span data-stu-id="733c4-122">Otherwise, the <em>tableid</em> or cursor must be positioned on a record, and that record will be used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="733c4-123">JET_bitRecordSizeRunningTotal</span><span class="sxs-lookup"><span data-stu-id="733c4-123">JET_bitRecordSizeRunningTotal</span></span></p></td>
<td><p><span data-ttu-id="733c4-124">Lorsque ce bit est spécifié, le <a href="gg269174(v=exchg.10).md">JET_RECSIZE2</a> n’est pas mis à zéro avant de remplir le contenu, ce qui agit efficacement comme une accumulation des statistiques pour plusieurs enregistrements visités ou mis à jour.</span><span class="sxs-lookup"><span data-stu-id="733c4-124">When this bit is specified, the <a href="gg269174(v=exchg.10).md">JET_RECSIZE2</a> is not zeroed before filling the contents, effectively acting as an accumulation of the statistics for multiple records visited or updated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="733c4-125">JET_bitRecordSizeLocal</span><span class="sxs-lookup"><span data-stu-id="733c4-125">JET_bitRecordSizeLocal</span></span></p></td>
<td><p><span data-ttu-id="733c4-126">Ainsi, l’API ignore les valeurs longues non intrinsèques.</span><span class="sxs-lookup"><span data-stu-id="733c4-126">This causes the API to ignore non-intrinsic Long Values.</span></span> <span data-ttu-id="733c4-127">Par exemple, seul l’enregistrement local de la page sera utilisé.</span><span class="sxs-lookup"><span data-stu-id="733c4-127">For example, only the local record on the page will be used.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="733c4-128">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="733c4-128">Return Value</span></span>

<span data-ttu-id="733c4-129">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="733c4-129">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="733c4-130">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="733c4-130">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="733c4-131">Code de retour</span><span class="sxs-lookup"><span data-stu-id="733c4-131">Return code</span></span></p></th>
<th><p><span data-ttu-id="733c4-132">Description</span><span class="sxs-lookup"><span data-stu-id="733c4-132">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="733c4-133">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="733c4-133">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="733c4-134">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="733c4-134">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="733c4-135">JET_errInvalidGrbit</span><span class="sxs-lookup"><span data-stu-id="733c4-135">JET_errInvalidGrbit</span></span></p></td>
<td><p><span data-ttu-id="733c4-136">L’une des options demandées n’est pas valide ou n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="733c4-136">One of the requested options was invalid or not implemented.</span></span> <span data-ttu-id="733c4-137">Cette erreur est retournée par la fonction <strong>JetGetRecordSize2</strong> lorsqu’un <em>Grbit</em> illégal est spécifié.</span><span class="sxs-lookup"><span data-stu-id="733c4-137">This error will be returned by the <strong>JetGetRecordSize2</strong> function when an illegal <em>grbit</em> is specified.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="733c4-138">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="733c4-138">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="733c4-139">Impossible de terminer l’opération, car l’instance associée à la session n’a pas été initialisée.</span><span class="sxs-lookup"><span data-stu-id="733c4-139">It is not possible to complete the operation because the instance associated with the session has not been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="733c4-140">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="733c4-140">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="733c4-141">Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="733c4-141">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="733c4-142">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="733c4-142">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="733c4-143">Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="733c4-143">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="733c4-144"><strong>Windows XP :  </strong> JET_errInstanceUnavailable ne sont retournées que par le système d’exploitation Windows XP et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="733c4-144"><strong>Windows XP:  </strong>JET_errInstanceUnavailable will only be returned by the Windows XP operating system and later versions of Windows.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="733c4-145">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="733c4-145">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="733c4-146">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="733c4-146">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="733c4-147">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="733c4-147">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="733c4-148">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="733c4-148">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="733c4-149">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="733c4-149">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="733c4-150">Il n’est pas conforme d’utiliser la même session pour plusieurs threads en même temps.</span><span class="sxs-lookup"><span data-stu-id="733c4-150">It is illegal to use the same session for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="733c4-151"><strong>Windows XP :  </strong> Les JET_errInstanceUnavailable sont retournées uniquement par Windows XP et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="733c4-151"><strong>Windows XP:  </strong>JET_errInstanceUnavailable will only be returned by Windows XP and later versions of Windows.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="733c4-152">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="733c4-152">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="733c4-153">Cela peut se produire si le curseur a été placé de manière incorrecte.</span><span class="sxs-lookup"><span data-stu-id="733c4-153">This can happen if the cursor was positioned incorrectly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="733c4-154">JET_errRecordDeleted</span><span class="sxs-lookup"><span data-stu-id="733c4-154">JET_errRecordDeleted</span></span></p></td>
<td><p><span data-ttu-id="733c4-155">Si le curseur n’est pas positionné dans une transaction, cela peut se produire si un autre thread supprime l’enregistrement de cette session.</span><span class="sxs-lookup"><span data-stu-id="733c4-155">If the cursor was not positioned in a transaction, this can happen if another thread deletes the record out from under this session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="733c4-156">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="733c4-156">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="733c4-157">Peut être retourné si une precsize <strong>null</strong><em></em> a été passée.</span><span class="sxs-lookup"><span data-stu-id="733c4-157">This can be returned if a <strong>NULL</strong><em>precsize</em> was passed.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="733c4-158">Notes</span><span class="sxs-lookup"><span data-stu-id="733c4-158">Remarks</span></span>

<span data-ttu-id="733c4-159">La taille de la clé accumulée dans le champ **cbOverhead** de [JET_RECSIZE2](./jet-recsize2-structure.md)est affectée par JET_bitRecordSizeInCopyBuffer.</span><span class="sxs-lookup"><span data-stu-id="733c4-159">The size of the key accumulated in the **cbOverhead** field of [JET_RECSIZE2](./jet-recsize2-structure.md), is affected by JET_bitRecordSizeInCopyBuffer.</span></span> <span data-ttu-id="733c4-160">Si ce bit est spécifié, la taille de clé accumulée dans le champ **cbOverhead** est la taille de la clé complète.</span><span class="sxs-lookup"><span data-stu-id="733c4-160">If this bit is specified, the key size accumulated in the **cbOverhead** field is the full key size.</span></span> <span data-ttu-id="733c4-161">Si ce bit n’est pas utilisé, la taille cumulée de la clé n’inclut pas la taille enregistrée en raison de la compression de préfixe de clé.</span><span class="sxs-lookup"><span data-stu-id="733c4-161">If this bit is not used, the key size accumulated will not include any size saved due to key prefix compression.</span></span>

#### <a name="requirements"></a><span data-ttu-id="733c4-162">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="733c4-162">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="733c4-163"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="733c4-163"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="733c4-164">Nécessite Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="733c4-164">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="733c4-165"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="733c4-165"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="733c4-166">Requiert Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="733c4-166">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="733c4-167"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="733c4-167"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="733c4-168">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="733c4-168">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="733c4-169"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="733c4-169"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="733c4-170">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="733c4-170">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="733c4-171"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="733c4-171"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="733c4-172">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="733c4-172">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="733c4-173">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="733c4-173">See Also</span></span>

[<span data-ttu-id="733c4-174">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="733c4-174">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="733c4-175">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="733c4-175">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="733c4-176">JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="733c4-176">JET_RECSIZE</span></span>](./jet-recsize-structure.md)  
[<span data-ttu-id="733c4-177">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="733c4-177">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="733c4-178">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="733c4-178">JET_TABLEID</span></span>](./jet-tableid.md)
