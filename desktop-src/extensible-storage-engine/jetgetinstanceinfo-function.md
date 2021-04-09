---
description: 'En savoir plus sur : fonction JetGetInstanceInfo'
title: JetGetInstanceInfo fonction)
TOCTitle: JetGetInstanceInfo Function
ms:assetid: ffccdac0-3631-4753-876a-90ddfdd0252f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294149(v=EXCHG.10)
ms:contentKeyID: 32765763
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetInstanceInfoW
- JetGetInstanceInfo
- JetGetInstanceInfoA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b8c8e9a279f536622cfdfccb8bc8882914aeee64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866825"
---
# <a name="jetgetinstanceinfo-function"></a><span data-ttu-id="44fa0-103">JetGetInstanceInfo fonction)</span><span class="sxs-lookup"><span data-stu-id="44fa0-103">JetGetInstanceInfo Function</span></span>


<span data-ttu-id="44fa0-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="44fa0-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetinstanceinfo-function"></a><span data-ttu-id="44fa0-105">JetGetInstanceInfo fonction)</span><span class="sxs-lookup"><span data-stu-id="44fa0-105">JetGetInstanceInfo Function</span></span>

<span data-ttu-id="44fa0-106">La fonction **JetGetInstanceInfo** récupère des informations sur les instances qui sont en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="44fa0-106">The **JetGetInstanceInfo** function retrieves information about the instances that are running.</span></span>

<span data-ttu-id="44fa0-107">**Windows XP : JetGetInstanceInfo** est introduit dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="44fa0-107">**Windows XP:  JetGetInstanceInfo** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetGetInstanceInfo(
      __out         unsigned long* pcInstanceInfo,
      __out         JET_INSTANCE_INFO** paInstanceInfo
    );
```

### <a name="parameters"></a><span data-ttu-id="44fa0-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="44fa0-108">Parameters</span></span>

<span data-ttu-id="44fa0-109">*pcInstanceInfo*</span><span class="sxs-lookup"><span data-stu-id="44fa0-109">*pcInstanceInfo*</span></span>

<span data-ttu-id="44fa0-110">Pointeur vers une mémoire tampon qui reçoit le nombre d’éléments stockés dans *paInstanceInfo*.</span><span class="sxs-lookup"><span data-stu-id="44fa0-110">A pointer to a buffer which will receive the number of elements stored in *paInstanceInfo*.</span></span>

<span data-ttu-id="44fa0-111">*paInstanceInfo*</span><span class="sxs-lookup"><span data-stu-id="44fa0-111">*paInstanceInfo*</span></span>

<span data-ttu-id="44fa0-112">Pointeur vers une mémoire tampon qui reçoit l’adresse du premier élément d’un tableau de structures.</span><span class="sxs-lookup"><span data-stu-id="44fa0-112">A pointer to a buffer which will receive the address of the first element of an array of structures.</span></span>

### <a name="return-value"></a><span data-ttu-id="44fa0-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="44fa0-113">Return Value</span></span>

<span data-ttu-id="44fa0-114">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="44fa0-114">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="44fa0-115">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="44fa0-115">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="44fa0-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="44fa0-116">Return code</span></span></p></th>
<th><p><span data-ttu-id="44fa0-117">Description</span><span class="sxs-lookup"><span data-stu-id="44fa0-117">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="44fa0-118">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="44fa0-118">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="44fa0-119">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="44fa0-119">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44fa0-120">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="44fa0-120">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="44fa0-121">L’un des paramètres fournis contenait une valeur inattendue ou contenait une valeur qui n’a pas de sens lorsqu’elle était associée à la valeur d’un autre paramètre.</span><span class="sxs-lookup"><span data-stu-id="44fa0-121">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="44fa0-122">Cette erreur est retournée par <strong>JetGetInstanceInfo</strong> quand :</span><span class="sxs-lookup"><span data-stu-id="44fa0-122">This error will be returned by <strong>JetGetInstanceInfo</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="44fa0-123"><em>pcInstanceInfo</em> ou <em>paInstanceInfo</em> ont la valeur null.</span><span class="sxs-lookup"><span data-stu-id="44fa0-123"><em>pcInstanceInfo</em> or <em>paInstanceInfo</em> are NULL.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44fa0-124">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="44fa0-124">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="44fa0-125">La mémoire est insuffisante pour traiter la demande.</span><span class="sxs-lookup"><span data-stu-id="44fa0-125">There is insufficient memory to process the request.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="44fa0-126">Notes</span><span class="sxs-lookup"><span data-stu-id="44fa0-126">Remarks</span></span>

<span data-ttu-id="44fa0-127">Le moteur de base de données alloue un tableau de structures de [JET_INSTANCE_INFO](./jet-instance-info-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="44fa0-127">The database engine will allocate an array of [JET_INSTANCE_INFO](./jet-instance-info-structure.md) structures.</span></span> <span data-ttu-id="44fa0-128">L’appelant est chargé de libérer cette mémoire avec [JetFreeBuffer](./jetfreebuffer-function.md).</span><span class="sxs-lookup"><span data-stu-id="44fa0-128">The caller is responsible for freeing this memory with [JetFreeBuffer](./jetfreebuffer-function.md).</span></span>

<span data-ttu-id="44fa0-129">S’il n’y a aucune instance active, **JetGetInstanceInfo** retourne JET_errSuccess et *pcInstanceInfo* reçoit la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="44fa0-129">If there are no active instances, **JetGetInstanceInfo** will return JET_errSuccess, and *pcInstanceInfo* will receive a value of 0.</span></span>

#### <a name="requirements"></a><span data-ttu-id="44fa0-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="44fa0-130">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="44fa0-131"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="44fa0-131"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="44fa0-132">Nécessite Windows Vista ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="44fa0-132">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44fa0-133"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="44fa0-133"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="44fa0-134">Requiert Windows Server 2008 ou Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="44fa0-134">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44fa0-135"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="44fa0-135"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="44fa0-136">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="44fa0-136">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44fa0-137"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="44fa0-137"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="44fa0-138">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="44fa0-138">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44fa0-139"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="44fa0-139"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="44fa0-140">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="44fa0-140">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44fa0-141"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="44fa0-141"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="44fa0-142">Implémenté en tant que <strong>JetGetInstanceInfoW</strong> (Unicode) et <strong>JetGetInstanceInfoA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="44fa0-142">Implemented as <strong>JetGetInstanceInfoW</strong> (Unicode) and <strong>JetGetInstanceInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="44fa0-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="44fa0-143">See Also</span></span>

[<span data-ttu-id="44fa0-144">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="44fa0-144">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="44fa0-145">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="44fa0-145">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="44fa0-146">JET_INSTANCE_INFO</span><span class="sxs-lookup"><span data-stu-id="44fa0-146">JET_INSTANCE_INFO</span></span>](./jet-instance-info-structure.md)  
[<span data-ttu-id="44fa0-147">JetFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="44fa0-147">JetFreeBuffer</span></span>](./jetfreebuffer-function.md)
