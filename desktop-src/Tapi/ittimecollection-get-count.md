---
description: La \_ méthode obtenir le nombre obtient le nombre d’éléments dans la collection.
ms.assetid: 9fe96af3-bb7b-4f6c-8df2-85bf7850c527
title: 'ITTimeCollection :: get_Count, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a385c8fa3120cbeaa4b876a8af4f60e0df5cb48
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542528"
---
# <a name="ittimecollectionget_count-method"></a><span data-ttu-id="5f68a-103">ITTimeCollection :: obten, \_ méthode Count</span><span class="sxs-lookup"><span data-stu-id="5f68a-103">ITTimeCollection::get\_Count method</span></span>

<span data-ttu-id="5f68a-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="5f68a-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="5f68a-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="5f68a-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="5f68a-106">La méthode **obtenir le \_ nombre** obtient le nombre d’éléments dans la collection.</span><span class="sxs-lookup"><span data-stu-id="5f68a-106">The **get\_Count** method gets the number of items in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f68a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5f68a-107">Syntax</span></span>


```C++
HRESULT get_Count(
  [out] LONG *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="5f68a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5f68a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f68a-109">*pval* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5f68a-109">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5f68a-110">Pointeur vers le nombre d’éléments dans la collection.</span><span class="sxs-lookup"><span data-stu-id="5f68a-110">Pointer to the number of items in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f68a-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5f68a-111">Return value</span></span>

<span data-ttu-id="5f68a-112">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="5f68a-112">This method can return one of these values.</span></span>



| <span data-ttu-id="5f68a-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="5f68a-113">Return code</span></span>                                                                                   | <span data-ttu-id="5f68a-114">Description</span><span class="sxs-lookup"><span data-stu-id="5f68a-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="5f68a-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5f68a-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="5f68a-116">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="5f68a-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="5f68a-117"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="5f68a-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="5f68a-118">Le paramètre *pval* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="5f68a-118">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="5f68a-119"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="5f68a-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="5f68a-120">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="5f68a-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="5f68a-121"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="5f68a-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="5f68a-122">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="5f68a-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="5f68a-123"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="5f68a-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="5f68a-124">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="5f68a-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="5f68a-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5f68a-125">Requirements</span></span>



| <span data-ttu-id="5f68a-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5f68a-126">Requirement</span></span> | <span data-ttu-id="5f68a-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="5f68a-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5f68a-128">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="5f68a-128">TAPI version</span></span><br/> | <span data-ttu-id="5f68a-129">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="5f68a-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="5f68a-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="5f68a-130">Header</span></span><br/>       | <dl> <span data-ttu-id="5f68a-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f68a-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="5f68a-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5f68a-132">Library</span></span><br/>      | <dl> <span data-ttu-id="5f68a-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5f68a-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="5f68a-134">DLL</span><span class="sxs-lookup"><span data-stu-id="5f68a-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="5f68a-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f68a-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f68a-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5f68a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f68a-137">**ITTimeCollection**</span><span class="sxs-lookup"><span data-stu-id="5f68a-137">**ITTimeCollection**</span></span>](ittimecollection.md)
</dt> <dt>

[<span data-ttu-id="5f68a-138">**ITTime**</span><span class="sxs-lookup"><span data-stu-id="5f68a-138">**ITTime**</span></span>](ittime.md)
</dt> </dl>

 

 




