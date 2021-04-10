---
description: 'En savoir plus sur : fonction de rappel JET_PFNREALLOC'
title: JET_PFNREALLOC fonction de rappel
TOCTitle: JET_PFNREALLOC Callback Function
ms:assetid: 443d0b7e-1c3b-4584-9bc3-938724527313
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269237(v=EXCHG.10)
ms:contentKeyID: 32765539
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
ms.openlocfilehash: 032c1edcfd18166b79f4c8b2868d53d0b84434d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210842"
---
# <a name="jet_pfnrealloc-callback-function"></a><span data-ttu-id="f5280-103">JET_PFNREALLOC fonction de rappel</span><span class="sxs-lookup"><span data-stu-id="f5280-103">JET_PFNREALLOC Callback Function</span></span>


<span data-ttu-id="f5280-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="f5280-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_pfnrealloc-callback-function"></a><span data-ttu-id="f5280-105">JET_PFNREALLOC fonction de rappel</span><span class="sxs-lookup"><span data-stu-id="f5280-105">JET_PFNREALLOC Callback Function</span></span>

<span data-ttu-id="f5280-106">La fonction JET_PFNREALLOC est un rappel compatible [réalloué](/cpp/c-runtime-library/reference/realloc?view=vs-2019) utilisé par [JetEnumerateColumns](./jetenumeratecolumns-function.md) pour allouer de la mémoire pour ses mémoires tampons de sortie.</span><span class="sxs-lookup"><span data-stu-id="f5280-106">The JET_PFNREALLOC function is a [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback used by [JetEnumerateColumns](./jetenumeratecolumns-function.md) to allocate memory for its output buffers.</span></span>

```cpp
    void * JET_API JET_PFNREALLOC(
      [in]                 void* pvContext,
      [in]                 void* pv,
      [in]                 unsigned long cb
    );
```

### <a name="parameters"></a><span data-ttu-id="f5280-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f5280-107">Parameters</span></span>

<span data-ttu-id="f5280-108">*pvContext*</span><span class="sxs-lookup"><span data-stu-id="f5280-108">*pvContext*</span></span>

<span data-ttu-id="f5280-109">Pointeur de contexte donné à [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="f5280-109">The context pointer given to [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span> <span data-ttu-id="f5280-110">Ce pointeur de contexte peut être utilisé pour communiquer l’état de l’appelant de [JetEnumerateColumns](./jetenumeratecolumns-function.md) à l’implémentation de ce rappel.</span><span class="sxs-lookup"><span data-stu-id="f5280-110">This context pointer can be used to convey state from the caller of [JetEnumerateColumns](./jetenumeratecolumns-function.md) to the implementation of this callback.</span></span>

<span data-ttu-id="f5280-111">*va*</span><span class="sxs-lookup"><span data-stu-id="f5280-111">*pv*</span></span>

<span data-ttu-id="f5280-112">Si la valeur est non NULL, spécifie un pointeur vers un bloc de mémoire précédemment alloué par ce rappel.</span><span class="sxs-lookup"><span data-stu-id="f5280-112">If non-NULL, specifies a pointer to a memory block previously allocated by this callback.</span></span> <span data-ttu-id="f5280-113">Si la valeur est NULL, un nouveau bloc de mémoire de la taille demandée sera alloué.</span><span class="sxs-lookup"><span data-stu-id="f5280-113">If NULL, a new memory block of the requested size will be allocated.</span></span>

<span data-ttu-id="f5280-114">*libéré*</span><span class="sxs-lookup"><span data-stu-id="f5280-114">*cb*</span></span>

<span data-ttu-id="f5280-115">Nouvelle taille du bloc de mémoire en octets.</span><span class="sxs-lookup"><span data-stu-id="f5280-115">The new size of the memory block in bytes.</span></span> <span data-ttu-id="f5280-116">Si ce paramètre a la valeur 0 (zéro) et qu’un bloc de mémoire est spécifié, ce bloc de mémoire est libéré.</span><span class="sxs-lookup"><span data-stu-id="f5280-116">If this parameter is 0 (zero) and a memory block is specified, that memory block will be freed.</span></span>

### <a name="return-value"></a><span data-ttu-id="f5280-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f5280-117">Return Value</span></span>

<span data-ttu-id="f5280-118">Le système peut générer des codes de réussite ou d’échec à la suite d’un appel à cette fonction.</span><span class="sxs-lookup"><span data-stu-id="f5280-118">The system may generate success or failure codes as a result of a call to this function.</span></span> <span data-ttu-id="f5280-119">Pour plus d’informations sur la façon de renvoyer ces codes en tant que HRESULT, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md).</span><span class="sxs-lookup"><span data-stu-id="f5280-119">For information about how to return these codes as HRESULTs, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f5280-120">Code de retour</span><span class="sxs-lookup"><span data-stu-id="f5280-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="f5280-121">Description</span><span class="sxs-lookup"><span data-stu-id="f5280-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f5280-122">Succès</span><span class="sxs-lookup"><span data-stu-id="f5280-122">Success</span></span></p></td>
<td><p><span data-ttu-id="f5280-123">Si un bloc de mémoire précédemment alloué a été spécifié et qu’une nouvelle taille de zéro a été spécifiée, ce bloc est libéré et la valeur NULL est retournée.</span><span class="sxs-lookup"><span data-stu-id="f5280-123">If a previously allocated memory block was specified and a new size of zero was specified then that block is freed and NULL will be returned.</span></span> <span data-ttu-id="f5280-124">Si un bloc de mémoire précédemment alloué a été spécifié et qu’une nouvelle taille différente de zéro a été spécifiée, le bloc de mémoire réalloué est retourné.</span><span class="sxs-lookup"><span data-stu-id="f5280-124">If a previously allocated memory block was specified and a non-zero new size was specified then the reallocated memory block is returned.</span></span> <span data-ttu-id="f5280-125">Si aucun bloc de mémoire n’a été spécifié, un bloc de mémoire nouvellement alloué de la taille spécifiée est retourné.</span><span class="sxs-lookup"><span data-stu-id="f5280-125">If no memory block was specified then a newly allocated memory block of the specified size is returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5280-126">Échec</span><span class="sxs-lookup"><span data-stu-id="f5280-126">Failure</span></span></p></td>
<td><p><span data-ttu-id="f5280-127">La valeur NULL est retournée.</span><span class="sxs-lookup"><span data-stu-id="f5280-127">NULL will be returned.</span></span> <span data-ttu-id="f5280-128">Si un bloc de mémoire précédemment alloué a été fourni, ce bloc restera alloué.</span><span class="sxs-lookup"><span data-stu-id="f5280-128">If a previously allocated memory block was provided then that block will remain allocated.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="f5280-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f5280-129">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f5280-130"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="f5280-130"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f5280-131">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="f5280-131">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5280-132"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="f5280-132"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f5280-133">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="f5280-133">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5280-134"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="f5280-134"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f5280-135">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="f5280-135">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="f5280-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5280-136">See Also</span></span>

[<span data-ttu-id="f5280-137">JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="f5280-137">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)
