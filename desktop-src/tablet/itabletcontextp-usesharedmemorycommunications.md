---
description: Fournit l’accès à la mémoire partagée entre les Tablet threads.
ms.assetid: 047ff598-7d20-49d7-bdd3-498fe5c778c6
title: 'ITabletContextP :: UseSharedMemoryCommunications, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP.UseSharedMemoryCommunications
api_type:
- COM
api_location:
- Wisptis.exe
- Wisptis.exe.dll
ms.openlocfilehash: d7880e1d0377d9d0140a0c82509abd31182c724e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518944"
---
# <a name="itabletcontextpusesharedmemorycommunications-method"></a><span data-ttu-id="45280-103">ITabletContextP :: UseSharedMemoryCommunications, méthode</span><span class="sxs-lookup"><span data-stu-id="45280-103">ITabletContextP::UseSharedMemoryCommunications method</span></span>

<span data-ttu-id="45280-104">Fournit l’accès à la mémoire partagée entre les Tablet threads.</span><span class="sxs-lookup"><span data-stu-id="45280-104">Provides access to memory shared between tablet threads.</span></span>

## <a name="syntax"></a><span data-ttu-id="45280-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="45280-105">Syntax</span></span>


```C++
HRESULT UseSharedMemoryCommunications(
  [in]  DWORD pid,
  [out] DWORD *phEventMoreData,
  [out] DWORD *phEventClientReady,
  [out] DWORD *phMutexAccess,
  [out] DWORD *phFileMapping
);
```



## <a name="parameters"></a><span data-ttu-id="45280-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="45280-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45280-107">*PID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="45280-107">*pid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45280-108">ID de processus.</span><span class="sxs-lookup"><span data-stu-id="45280-108">Process id.</span></span>

</dd> <dt>

<span data-ttu-id="45280-109">*phEventMoreData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="45280-109">*phEventMoreData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="45280-110">Handle d’événement qui signale le moment où de nouvelles données sont disponibles pour être traitées.</span><span class="sxs-lookup"><span data-stu-id="45280-110">Event handle that signals when new data is available to be processed.</span></span>

</dd> <dt>

<span data-ttu-id="45280-111">*phEventClientReady* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="45280-111">*phEventClientReady* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="45280-112">Handle d’événement retourné utilisé pour signaler que le client est prêt à recevoir des données.</span><span class="sxs-lookup"><span data-stu-id="45280-112">Returned event handle used to signal that the client is ready to receive data.</span></span> <span data-ttu-id="45280-113">Signalé après le traitement de nouvelles données.</span><span class="sxs-lookup"><span data-stu-id="45280-113">Signaled after processing new data.</span></span>

</dd> <dt>

<span data-ttu-id="45280-114">*phMutexAccess* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="45280-114">*phMutexAccess* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="45280-115">Mutex accordant l’accès à la mémoire partagée.</span><span class="sxs-lookup"><span data-stu-id="45280-115">The mutex granting access to shared memory.</span></span>

</dd> <dt>

<span data-ttu-id="45280-116">*phFileMapping* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="45280-116">*phFileMapping* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="45280-117">Pointeur vers le bloc de mémoire partagée.</span><span class="sxs-lookup"><span data-stu-id="45280-117">Pointer to the shared memory block.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45280-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="45280-118">Return value</span></span>

<span data-ttu-id="45280-119">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="45280-119">This method can return one of these values.</span></span>



| <span data-ttu-id="45280-120">Code de retour</span><span class="sxs-lookup"><span data-stu-id="45280-120">Return code</span></span>                                                                            | <span data-ttu-id="45280-121">Description</span><span class="sxs-lookup"><span data-stu-id="45280-121">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="45280-122"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="45280-122"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="45280-123">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="45280-123">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="45280-124"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="45280-124"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="45280-125">Une erreur non spécifiée s'est produite.</span><span class="sxs-lookup"><span data-stu-id="45280-125">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="45280-126">Notes</span><span class="sxs-lookup"><span data-stu-id="45280-126">Remarks</span></span>

<span data-ttu-id="45280-127">La méthode **UseSharedMemoryCommunications** est utilisée dans le cadre du protocole de mémoire partagée du Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="45280-127">The **UseSharedMemoryCommunications** method is used as part of the Tablet PC shared memory protocol.</span></span> <span data-ttu-id="45280-128">Étant donné que le service wisptis a un niveau d’intégrité élevé (IL), il peut stocker les données stockées dans la mémoire partagée et y accéder sans avoir à élever ses privilèges.</span><span class="sxs-lookup"><span data-stu-id="45280-128">Since the Wisptis service has a high integrity level (IL), it can store and access data stored in shared memory without needing to elevate its privileges.</span></span>

<span data-ttu-id="45280-129">La structure d' [**\_ en-tête SHAREDMEMORY**](sharedmemory-header.md) est convertie à partir des données référencées par le mappage de fichier et les données de paquets brutes suivent l' **\_ en-tête SHAREDMEMORY**.</span><span class="sxs-lookup"><span data-stu-id="45280-129">The [**SHAREDMEMORY\_HEADER**](sharedmemory-header.md) structure is cast from the data referenced by the file mapping and the raw packet data follows the **SHAREDMEMORY\_HEADER**.</span></span> <span data-ttu-id="45280-130">Les données de paquets brutes peuvent être lues à partir de la mémoire partagée lorsque l’événement référencé par *pdwEventClientReady* est déclenché.</span><span class="sxs-lookup"><span data-stu-id="45280-130">Raw packet data can be read off of the shared memory when the event referenced by *pdwEventClientReady* is raised.</span></span>

<span data-ttu-id="45280-131">La liste suivante décrit la séquence d’événements pour l’accès à et l’utilisation de la mémoire partagée.</span><span class="sxs-lookup"><span data-stu-id="45280-131">The following list describes the sequence of events for accessing and using shared memory.</span></span>

-   <span data-ttu-id="45280-132">Le client définit l’événement clientReady.</span><span class="sxs-lookup"><span data-stu-id="45280-132">The client sets the clientReady event.</span></span>
-   <span data-ttu-id="45280-133">Le client attend l’événement moreData.</span><span class="sxs-lookup"><span data-stu-id="45280-133">The client waits for the moreData event.</span></span>
-   <span data-ttu-id="45280-134">Le client acquiert le mutex.</span><span class="sxs-lookup"><span data-stu-id="45280-134">The client acquires the mutex.</span></span>
-   <span data-ttu-id="45280-135">Le client lit les données de paquets à partir de la section de la mémoire partagée après l’en-tête et les numéros de série après les paquets.</span><span class="sxs-lookup"><span data-stu-id="45280-135">The client reads packet data from the section of shared memory after the header and serial numbers after the packets.</span></span>
-   <span data-ttu-id="45280-136">Le client gère les données en fonction de la valeur de **dwEvent**.</span><span class="sxs-lookup"><span data-stu-id="45280-136">The client handles data depending on the value of **dwEvent**.</span></span>
-   <span data-ttu-id="45280-137">Le client écrit-1 (0xFFFFFFFF) dans **dwEvent**.</span><span class="sxs-lookup"><span data-stu-id="45280-137">The client writes -1 (0xFFFFFFFF) into **dwEvent**.</span></span>
-   <span data-ttu-id="45280-138">Le client libère le mutex.</span><span class="sxs-lookup"><span data-stu-id="45280-138">The client releases the mutex.</span></span>
-   <span data-ttu-id="45280-139">Le client définit l’événement clientReady.</span><span class="sxs-lookup"><span data-stu-id="45280-139">The client sets the clientReady event.</span></span>

## <a name="requirements"></a><span data-ttu-id="45280-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="45280-140">Requirements</span></span>



| <span data-ttu-id="45280-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="45280-141">Requirement</span></span> | <span data-ttu-id="45280-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="45280-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="45280-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="45280-143">Minimum supported client</span></span><br/> | <span data-ttu-id="45280-144">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="45280-144">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="45280-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="45280-145">Minimum supported server</span></span><br/> | <span data-ttu-id="45280-146">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="45280-146">None supported</span></span><br/>                                                              |
| <span data-ttu-id="45280-147">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="45280-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="45280-148"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="45280-148"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45280-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="45280-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45280-150">**Interface ITabletContextP**</span><span class="sxs-lookup"><span data-stu-id="45280-150">**ITabletContextP Interface**</span></span>](itabletcontextp.md)
</dt> <dt>

[<span data-ttu-id="45280-151">**UseNamedSharedMemoryCommunications**</span><span class="sxs-lookup"><span data-stu-id="45280-151">**UseNamedSharedMemoryCommunications**</span></span>](itabletcontextp-usenamedsharedmemorycommunications.md)
</dt> </dl>

 

 




