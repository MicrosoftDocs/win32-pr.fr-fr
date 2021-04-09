---
description: 'En savoir plus sur : fonction JetIdle'
title: JetIdle fonction)
TOCTitle: JetIdle Function
ms:assetid: 77e036eb-b894-4ff7-b14f-1564bf21873f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269301(v=EXCHG.10)
ms:contentKeyID: 32765593
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetIdle
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0adf2845997b97eb93b39b779da4ad19bb9ee066
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866821"
---
# <a name="jetidle-function"></a><span data-ttu-id="d4412-103">JetIdle fonction)</span><span class="sxs-lookup"><span data-stu-id="d4412-103">JetIdle Function</span></span>


<span data-ttu-id="d4412-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="d4412-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetidle-function"></a><span data-ttu-id="d4412-105">JetIdle fonction)</span><span class="sxs-lookup"><span data-stu-id="d4412-105">JetIdle Function</span></span>

<span data-ttu-id="d4412-106">La fonction **JetIdle** est défunte et ne doit être utilisée qu’à des fins de test.</span><span class="sxs-lookup"><span data-stu-id="d4412-106">The **JetIdle** function is defunct, and should only be used for testing purposes.</span></span> <span data-ttu-id="d4412-107">**JetIdle** peut être utilisé pour effectuer des tâches de nettoyage inactives ou vérifier l’état de la Banque des versions dans le moteur ESE.</span><span class="sxs-lookup"><span data-stu-id="d4412-107">**JetIdle** can be used to perform idle cleanup tasks or check the version store status in ESE.</span></span>

```cpp
    JET_ERR JET_API JetIdle(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="d4412-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d4412-108">Parameters</span></span>

<span data-ttu-id="d4412-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="d4412-109">*sesid*</span></span>

<span data-ttu-id="d4412-110">Session qui sera utilisée pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="d4412-110">The session that will be used for this call.</span></span>

<span data-ttu-id="d4412-111">*grbit*</span><span class="sxs-lookup"><span data-stu-id="d4412-111">*grbit*</span></span>

<span data-ttu-id="d4412-112">Groupe de bits qui contiennent les options à utiliser pour cet appel, qui incluent zéro, un ou plusieurs des bits suivants :</span><span class="sxs-lookup"><span data-stu-id="d4412-112">A group of bits that contain the options to be used for this call, which include zero or more of the following bits:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d4412-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4412-113">Value</span></span></p></th>
<th><p><span data-ttu-id="d4412-114">Signification</span><span class="sxs-lookup"><span data-stu-id="d4412-114">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d4412-115">JET_bitIdleCompact</span><span class="sxs-lookup"><span data-stu-id="d4412-115">JET_bitIdleCompact</span></span></p></td>
<td><p><span data-ttu-id="d4412-116">Déclenche le nettoyage de la Banque des versions.</span><span class="sxs-lookup"><span data-stu-id="d4412-116">Triggers cleanup of the version store.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4412-117">JET_bitIdleFlushBuffers</span><span class="sxs-lookup"><span data-stu-id="d4412-117">JET_bitIdleFlushBuffers</span></span></p></td>
<td><p><span data-ttu-id="d4412-118">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="d4412-118">Reserved for future use.</span></span> <span data-ttu-id="d4412-119">Si cet indicateur est spécifié, l’API retourne JET_errInvalidgrbit.</span><span class="sxs-lookup"><span data-stu-id="d4412-119">If this flag is specified, the API will return JET_errInvalidgrbit.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4412-120">JET_bitIdleStatus</span><span class="sxs-lookup"><span data-stu-id="d4412-120">JET_bitIdleStatus</span></span></p></td>
<td><p><span data-ttu-id="d4412-121">Retourne JET_wrnIdleFull si la Banque des versions est supérieure à la moitié complète.</span><span class="sxs-lookup"><span data-stu-id="d4412-121">Returns JET_wrnIdleFull if version store is more than half full.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="d4412-122">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d4412-122">Return Value</span></span>

<span data-ttu-id="d4412-123">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="d4412-123">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="d4412-124">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="d4412-124">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d4412-125">Code de retour</span><span class="sxs-lookup"><span data-stu-id="d4412-125">Return code</span></span></p></th>
<th><p><span data-ttu-id="d4412-126">Description</span><span class="sxs-lookup"><span data-stu-id="d4412-126">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d4412-127">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="d4412-127">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="d4412-128">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="d4412-128">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4412-129">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="d4412-129">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="d4412-130">Un paramètre <em>Grbit</em> fourni à l’API n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="d4412-130">A <em>grbit</em> parameter that was provided to the API was not valid.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d4412-131">Si cette fonction a la valeur, l’opération appropriée est déclenchée, ou un code d’erreur indiquant la totalité de la Banque des versions dépend du *Grbit* fourni.</span><span class="sxs-lookup"><span data-stu-id="d4412-131">If this function succeeds, the appropriate operation will be triggered, or an error code indicating how full the version store is depending on the *grbit* provided.</span></span>

<span data-ttu-id="d4412-132">Si cette fonction échoue, l’opération demandée ne s’est pas terminée correctement.</span><span class="sxs-lookup"><span data-stu-id="d4412-132">If this function fails, the requested operation will not have completed successfully.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d4412-133">Notes</span><span class="sxs-lookup"><span data-stu-id="d4412-133">Remarks</span></span>

<span data-ttu-id="d4412-134">La Banque des versions gère le mécanisme d’isolation d’instantané de ESE.</span><span class="sxs-lookup"><span data-stu-id="d4412-134">The version store maintains ESE's snapshot isolation mechanism.</span></span> <span data-ttu-id="d4412-135">Si la Banque des versions est plus de moitié complète, le programme peut fermer des transactions de longue durée.</span><span class="sxs-lookup"><span data-stu-id="d4412-135">If the version store is more than half full, the program might close long-running transactions.</span></span> <span data-ttu-id="d4412-136">Si une transaction de longue durée épuise la Banque des versions, il cesse d’autoriser les opérations d’écriture dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="d4412-136">If a long-running transaction exhausts the version store, ESE will stop allowing write operations to the database.</span></span>

#### <a name="requirements"></a><span data-ttu-id="d4412-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d4412-137">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d4412-138"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="d4412-138"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="d4412-139">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="d4412-139">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4412-140"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="d4412-140"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d4412-141">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="d4412-141">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4412-142"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="d4412-142"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="d4412-143">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="d4412-143">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4412-144"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="d4412-144"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="d4412-145">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="d4412-145">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4412-146"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="d4412-146"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="d4412-147">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="d4412-147">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="d4412-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d4412-148">See Also</span></span>

[<span data-ttu-id="d4412-149">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="d4412-149">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="d4412-150">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="d4412-150">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="d4412-151">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="d4412-151">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="d4412-152">JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="d4412-152">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)
