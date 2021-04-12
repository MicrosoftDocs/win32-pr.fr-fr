---
description: 'En savoir plus sur : fonction JetResetSessionContext'
title: JetResetSessionContext fonction)
TOCTitle: JetResetSessionContext Function
ms:assetid: 537a4753-b804-457a-9a13-53e8d1056eab
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269250(v=EXCHG.10)
ms:contentKeyID: 32765552
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetResetSessionContext
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1ee02050a9583aa67f50fbe53d710c352c196048
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203132"
---
# <a name="jetresetsessioncontext-function"></a><span data-ttu-id="aee10-103">JetResetSessionContext fonction)</span><span class="sxs-lookup"><span data-stu-id="aee10-103">JetResetSessionContext Function</span></span>


<span data-ttu-id="aee10-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="aee10-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetresetsessioncontext-function"></a><span data-ttu-id="aee10-105">JetResetSessionContext fonction)</span><span class="sxs-lookup"><span data-stu-id="aee10-105">JetResetSessionContext Function</span></span>

<span data-ttu-id="aee10-106">La fonction **JetResetSessionContext** dissocie une session du thread actuel.</span><span class="sxs-lookup"><span data-stu-id="aee10-106">The **JetResetSessionContext** function disassociates a session from the current thread.</span></span>

```cpp
    JET_ERR JET_API JetResetSessionContext(
      __in          JET_SESID sesid
    );
```

### <a name="parameters"></a><span data-ttu-id="aee10-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aee10-107">Parameters</span></span>

<span data-ttu-id="aee10-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="aee10-108">*sesid*</span></span>

<span data-ttu-id="aee10-109">Session à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="aee10-109">The session to use for this call.</span></span>

### <a name="return-value"></a><span data-ttu-id="aee10-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="aee10-110">Return Value</span></span>

<span data-ttu-id="aee10-111">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="aee10-111">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="aee10-112">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="aee10-112">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="aee10-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="aee10-113">Return code</span></span></p></th>
<th><p><span data-ttu-id="aee10-114">Description</span><span class="sxs-lookup"><span data-stu-id="aee10-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aee10-115">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="aee10-115">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="aee10-116">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="aee10-116">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aee10-117">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="aee10-117">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="aee10-118">Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="aee10-118">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="aee10-119">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="aee10-119">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aee10-120">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="aee10-120">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="aee10-121">Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="aee10-121">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aee10-122">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="aee10-122">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="aee10-123">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="aee10-123">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aee10-124">JET_errSessionContextNotSetByThisThread</span><span class="sxs-lookup"><span data-stu-id="aee10-124">JET_errSessionContextNotSetByThisThread</span></span></p></td>
<td><p><span data-ttu-id="aee10-125">La session n’a pas pu être dissociée du thread actuel, car elle est associée à un thread différent.</span><span class="sxs-lookup"><span data-stu-id="aee10-125">The session could not be disassociated from the current thread because it is associated with a different thread.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aee10-126">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="aee10-126">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="aee10-127">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="aee10-127">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="aee10-128">En cas de réussite, la session est dissociée du thread actuel.</span><span class="sxs-lookup"><span data-stu-id="aee10-128">On success, the session will be disassociated from the current thread.</span></span> <span data-ttu-id="aee10-129">Aucune modification de l’état de la base de données ne se produit.</span><span class="sxs-lookup"><span data-stu-id="aee10-129">No change to the database state will occur.</span></span>

<span data-ttu-id="aee10-130">En cas d’échec, l’état de la session reste inchangé.</span><span class="sxs-lookup"><span data-stu-id="aee10-130">On failure, the session state will remain unchanged.</span></span> <span data-ttu-id="aee10-131">Aucune modification de l’état de la base de données ne se produit.</span><span class="sxs-lookup"><span data-stu-id="aee10-131">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="aee10-132">Notes</span><span class="sxs-lookup"><span data-stu-id="aee10-132">Remarks</span></span>

<span data-ttu-id="aee10-133">**JetResetSessionContext** doit être appelé sur le même thread que celui qui a appelé [JetSetSessionContext](./jetsetsessioncontext-function.md) pour une session donnée.</span><span class="sxs-lookup"><span data-stu-id="aee10-133">**JetResetSessionContext** must be called on the same thread that called [JetSetSessionContext](./jetsetsessioncontext-function.md) for a given session.</span></span>

#### <a name="requirements"></a><span data-ttu-id="aee10-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aee10-134">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aee10-135"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="aee10-135"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="aee10-136">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="aee10-136">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aee10-137"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="aee10-137"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="aee10-138">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="aee10-138">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aee10-139"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="aee10-139"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="aee10-140">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="aee10-140">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aee10-141"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="aee10-141"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="aee10-142">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="aee10-142">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aee10-143"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="aee10-143"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="aee10-144">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="aee10-144">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="aee10-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aee10-145">See Also</span></span>

[<span data-ttu-id="aee10-146">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="aee10-146">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="aee10-147">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="aee10-147">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="aee10-148">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="aee10-148">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="aee10-149">JetSetSessionContext</span><span class="sxs-lookup"><span data-stu-id="aee10-149">JetSetSessionContext</span></span>](./jetsetsessioncontext-function.md)
