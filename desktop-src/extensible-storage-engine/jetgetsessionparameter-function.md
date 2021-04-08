---
description: 'En savoir plus sur : fonction JetGetSessionParameter'
title: JetGetSessionParameter fonction)
TOCTitle: JetGetSessionParameter Function
ms:assetid: 36fbcc06-a72d-4bfb-976b-1b705487732a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835039(v=EXCHG.10)
ms:contentKeyID: 49894661
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetGetSessionParameter
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f0ac02142d48009d668d903b39163b425d738b55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861933"
---
# <a name="jetgetsessionparameter-function"></a><span data-ttu-id="8a93b-103">JetGetSessionParameter fonction)</span><span class="sxs-lookup"><span data-stu-id="8a93b-103">JetGetSessionParameter Function</span></span>


<span data-ttu-id="8a93b-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="8a93b-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="8a93b-105">La fonction **JetGetSessionParameter** lit le paramètre de session pour la session donnée.</span><span class="sxs-lookup"><span data-stu-id="8a93b-105">The **JetGetSessionParameter** function reads the session parameter for the given session.</span></span>

<span data-ttu-id="8a93b-106">La fonction **JetGetSessionParameter** a été introduite dans le système d’exploitation Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8a93b-106">The **JetGetSessionParameter** function was introduced in the Windows 8 operating system.</span></span>

``` c++
JET_ERR JET_API JetGetSessionParameter (
  __in_opt      JET_SESID sesid,
  __in          unsigned long sesparamid,
  __out_cap_post_count_(cbParamMax, *pcbParamActual)  void* pvParam,
  __in          unsigned long cbParamMax,
  __out_opt_    unsigned long pcbParamActual
);
```

### <a name="parameters"></a><span data-ttu-id="8a93b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8a93b-107">Parameters</span></span>

<span data-ttu-id="8a93b-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="8a93b-108">*sesid*</span></span>

<span data-ttu-id="8a93b-109">Session à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="8a93b-109">The session to use for this call.</span></span>

<span data-ttu-id="8a93b-110">Lorsqu’il est spécifié, l’instance spécifiée est ignorée et l’instance associée à la session est utilisée.</span><span class="sxs-lookup"><span data-stu-id="8a93b-110">When specified, the specified instance is ignored and the instance associated with the session will be used.</span></span>

<span data-ttu-id="8a93b-111">*sesparamid*</span><span class="sxs-lookup"><span data-stu-id="8a93b-111">*sesparamid*</span></span>

<span data-ttu-id="8a93b-112">ID du paramètre de session à définir.</span><span class="sxs-lookup"><span data-stu-id="8a93b-112">The ID of the session parameter to set.</span></span>

<span data-ttu-id="8a93b-113">*pvParam*</span><span class="sxs-lookup"><span data-stu-id="8a93b-113">*pvParam*</span></span>

<span data-ttu-id="8a93b-114">Données dans ce paramètre de session.</span><span class="sxs-lookup"><span data-stu-id="8a93b-114">Data in this session parameter.</span></span>

<span data-ttu-id="8a93b-115">*cbParamMax*</span><span class="sxs-lookup"><span data-stu-id="8a93b-115">*cbParamMax*</span></span>

<span data-ttu-id="8a93b-116">Taille maximale du jeu de données dans ce paramètre de session.</span><span class="sxs-lookup"><span data-stu-id="8a93b-116">The maximum size of the data set in this session parameter.</span></span>

<span data-ttu-id="8a93b-117">*pcbParamActual*</span><span class="sxs-lookup"><span data-stu-id="8a93b-117">*pcbParamActual*</span></span>

<span data-ttu-id="8a93b-118">Taille réelle du jeu de données dans ce paramètre de session.</span><span class="sxs-lookup"><span data-stu-id="8a93b-118">The actual size of the data set in this session parameter.</span></span>

### <a name="return-value"></a><span data-ttu-id="8a93b-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8a93b-119">Return value</span></span>

<span data-ttu-id="8a93b-120">En cas de réussite, la mémoire tampon de sortie appropriée pour le paramètre de session demandé sera définie sur la valeur de ce paramètre de session.</span><span class="sxs-lookup"><span data-stu-id="8a93b-120">On success, the output buffer appropriate for the requested session parameter will be set to the value of that session parameter.</span></span>

<span data-ttu-id="8a93b-121">En cas d’échec, l’état des mémoires tampons de sortie n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="8a93b-121">On failure, the state of the output buffers will be undefined.</span></span>

#### <a name="remarks"></a><span data-ttu-id="8a93b-122">Notes</span><span class="sxs-lookup"><span data-stu-id="8a93b-122">Remarks</span></span>

<span data-ttu-id="8a93b-123">Le paramètre de session est utilisé pour la durée de vie de la session ou jusqu’à ce que la valeur soit réinitialisée.</span><span class="sxs-lookup"><span data-stu-id="8a93b-123">The session parameter is used for the lifetime of the session or until the value is reset.</span></span>

#### <a name="requirements"></a><span data-ttu-id="8a93b-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8a93b-124">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8a93b-125"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="8a93b-125"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="8a93b-126">Requiert Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8a93b-126">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8a93b-127"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="8a93b-127"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="8a93b-128">Requiert Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="8a93b-128">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8a93b-129"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="8a93b-129"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="8a93b-130">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="8a93b-130">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8a93b-131"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="8a93b-131"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="8a93b-132">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="8a93b-132">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8a93b-133"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="8a93b-133"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="8a93b-134">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="8a93b-134">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="8a93b-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a93b-135">See also</span></span>

[<span data-ttu-id="8a93b-136">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="8a93b-136">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="8a93b-137">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="8a93b-137">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="8a93b-138">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="8a93b-138">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="8a93b-139">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="8a93b-139">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="8a93b-140">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="8a93b-140">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="8a93b-141">JetInit</span><span class="sxs-lookup"><span data-stu-id="8a93b-141">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="8a93b-142">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="8a93b-142">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="8a93b-143">JetStopService</span><span class="sxs-lookup"><span data-stu-id="8a93b-143">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="8a93b-144">Paramètres système</span><span class="sxs-lookup"><span data-stu-id="8a93b-144">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
