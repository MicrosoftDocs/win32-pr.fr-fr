---
description: 'En savoir plus sur : fonction de rappel JET_PFNSTATUS'
title: JET_PFNSTATUS fonction de rappel
TOCTitle: JET_PFNSTATUS Callback Function
ms:assetid: 8b0cf5bf-a4ee-4d8f-8dd7-556c35cd269d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269326(v=EXCHG.10)
ms:contentKeyID: 32765616
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c5f3eb374580dc6bed752900434706b66c6623b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203895"
---
# <a name="jet_pfnstatus-callback-function"></a><span data-ttu-id="87f95-103">JET_PFNSTATUS fonction de rappel</span><span class="sxs-lookup"><span data-stu-id="87f95-103">JET_PFNSTATUS Callback Function</span></span>


<span data-ttu-id="87f95-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="87f95-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_pfnstatus-callback-function"></a><span data-ttu-id="87f95-105">JET_PFNSTATUS fonction de rappel</span><span class="sxs-lookup"><span data-stu-id="87f95-105">JET_PFNSTATUS Callback Function</span></span>

<span data-ttu-id="87f95-106">La fonction de rappel **JET_PFNSTATUS** reçoit des informations sur la progression des opérations de longue durée, telles que les opérations de défragmentation, de sauvegarde ou de restauration.</span><span class="sxs-lookup"><span data-stu-id="87f95-106">The **JET_PFNSTATUS** callback function receives information about the progress of long-running operations, such as defragmentation, backup, or restore operations.</span></span> <span data-ttu-id="87f95-107">Pendant ces opérations, le moteur de base de données appelle cette fonction de rappel pour fournir une mise à jour de la progression de l’opération.</span><span class="sxs-lookup"><span data-stu-id="87f95-107">During such operations, the database engine calls this callback function to give an update on the progress of the operation.</span></span>

```cpp
    JET_ERR JET_API JET_PFNSTATUS(
                           JET_SESID  sesid,
                           JET_SNP snp,
                           JET_SNT snt,
                           void* pv
    );
```

### <a name="parameters"></a><span data-ttu-id="87f95-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="87f95-108">Parameters</span></span>

<span data-ttu-id="87f95-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="87f95-109">*sesid*</span></span>

<span data-ttu-id="87f95-110">Session de type [JET_SESID](./jet-sesid.md) avec laquelle la fonction d’exécution longue a été appelée.</span><span class="sxs-lookup"><span data-stu-id="87f95-110">The session of type [JET_SESID](./jet-sesid.md) with which the long-running function was called.</span></span>

<span data-ttu-id="87f95-111">*SNP*</span><span class="sxs-lookup"><span data-stu-id="87f95-111">*snp*</span></span>

<span data-ttu-id="87f95-112">Type d’opération tel que spécifié dans [JET_SNP](./jet-snp.md).</span><span class="sxs-lookup"><span data-stu-id="87f95-112">The type of operation as specified in [JET_SNP](./jet-snp.md).</span></span> <span data-ttu-id="87f95-113">Les types d’opérations incluent la réparation, le compactage, la restauration, la sauvegarde, la mise à jour, le nettoyage et la mise à jour du format d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="87f95-113">Types of operations include repair, compact, restore, backup, update, scrub, and update the record format.</span></span>

<span data-ttu-id="87f95-114">*SNT*</span><span class="sxs-lookup"><span data-stu-id="87f95-114">*snt*</span></span>

<span data-ttu-id="87f95-115">État d’une opération.</span><span class="sxs-lookup"><span data-stu-id="87f95-115">The status of an operation.</span></span> <span data-ttu-id="87f95-116">Les types d’État incluent début, en cours, achèvement ou échec.</span><span class="sxs-lookup"><span data-stu-id="87f95-116">Status types include beginning, in progress, completion, or failure.</span></span> <span data-ttu-id="87f95-117">L’État est spécifié avec le troisième paramètre de type [JET_SNT](./jet-snt.md).</span><span class="sxs-lookup"><span data-stu-id="87f95-117">The status will be specified with the third parameter of type [JET_SNT](./jet-snt.md).</span></span>

<span data-ttu-id="87f95-118">*va*</span><span class="sxs-lookup"><span data-stu-id="87f95-118">*pv*</span></span>

<span data-ttu-id="87f95-119">Pointeur facultatif vers une structure de type [JET_SNPROG](./jet-snprog-structure.md).</span><span class="sxs-lookup"><span data-stu-id="87f95-119">An optional pointer to a structure of type [JET_SNPROG](./jet-snprog-structure.md).</span></span>

### <a name="return-value"></a><span data-ttu-id="87f95-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="87f95-120">Return Value</span></span>

<span data-ttu-id="87f95-121">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des [codes d’erreur du moteur de stockage extensible](./extensible-storage-engine-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="87f95-121">This function returns the [JET_ERR](./jet-err.md) datatype with one of the [Extensible Storage Engine error codes](./extensible-storage-engine-error-codes.md).</span></span> <span data-ttu-id="87f95-122">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="87f95-122">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<span data-ttu-id="87f95-123">En cas de réussite, l’opération qui a émis le rappel peut se poursuivre normalement.</span><span class="sxs-lookup"><span data-stu-id="87f95-123">On success, the operation that issued the callback can proceed normally.</span></span> <span data-ttu-id="87f95-124">Dans certains cas, le rappel peut retourner un avertissement qui influence cette opération.</span><span class="sxs-lookup"><span data-stu-id="87f95-124">In some cases, the callback might return a warning that influences that operation.</span></span>

<span data-ttu-id="87f95-125">En cas d’échec, l’opération qui a émis le rappel peut se poursuivre normalement ou échouer.</span><span class="sxs-lookup"><span data-stu-id="87f95-125">On failure, the operation that issued the callback might proceed normally or might fail.</span></span>

### <a name="remarks"></a><span data-ttu-id="87f95-126">Notes</span><span class="sxs-lookup"><span data-stu-id="87f95-126">Remarks</span></span>

<span data-ttu-id="87f95-127">Cette fonction de rappel sera utilisée dans une notification de progression dans laquelle la structure indiquera l’état actuel de la progression.</span><span class="sxs-lookup"><span data-stu-id="87f95-127">This callback function will be used in a progress notification in which the structure will indicate the current state of the progress.</span></span> <span data-ttu-id="87f95-128">Notez que la fonction de rappel peut être appelée plusieurs fois pour la progression de l’opération.</span><span class="sxs-lookup"><span data-stu-id="87f95-128">Note that the callback function might be called multiple times for the progress of the operation.</span></span>

### <a name="requirements"></a><span data-ttu-id="87f95-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="87f95-129">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="87f95-130"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="87f95-130"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="87f95-131">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="87f95-131">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="87f95-132"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="87f95-132"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="87f95-133">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="87f95-133">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="87f95-134"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="87f95-134"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="87f95-135">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="87f95-135">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="87f95-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87f95-136">See Also</span></span>

[<span data-ttu-id="87f95-137">Codes d’erreur du moteur de stockage extensible</span><span class="sxs-lookup"><span data-stu-id="87f95-137">Extensible Storage Engine error codes</span></span>](./extensible-storage-engine-error-codes.md)  
[<span data-ttu-id="87f95-138">Erreurs du moteur de stockage extensible</span><span class="sxs-lookup"><span data-stu-id="87f95-138">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="87f95-139">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="87f95-139">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="87f95-140">JET_SNP</span><span class="sxs-lookup"><span data-stu-id="87f95-140">JET_SNP</span></span>](./jet-snp.md)  
[<span data-ttu-id="87f95-141">JET_SNPROG</span><span class="sxs-lookup"><span data-stu-id="87f95-141">JET_SNPROG</span></span>](./jet-snprog-structure.md)  
[<span data-ttu-id="87f95-142">JET_SNT</span><span class="sxs-lookup"><span data-stu-id="87f95-142">JET_SNT</span></span>](./jet-snt.md)
