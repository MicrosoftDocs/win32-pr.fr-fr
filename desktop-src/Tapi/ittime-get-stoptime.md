---
description: La \_ méthode obtenir StopTime obtient la valeur de l’heure de fin du protocole NTP (Network Time Protocol). Si l’heure de fin est égale à zéro, la session n’est pas limitée.
ms.assetid: f18042c0-e41d-43b3-a75d-6ab161afde6e
title: 'ITTime :: get_StopTime, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b55ac03c4701884b5a4b7716cb2758887b6160bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525205"
---
# <a name="ittimeget_stoptime-method"></a><span data-ttu-id="b245b-104">ITTime :: \_ StopTime, méthode</span><span class="sxs-lookup"><span data-stu-id="b245b-104">ITTime::get\_StopTime method</span></span>

<span data-ttu-id="b245b-105">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="b245b-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b245b-106">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="b245b-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="b245b-107">La méthode **obtenir \_ StopTime** obtient la valeur de l’heure de fin du protocole NTP (Network Time Protocol).</span><span class="sxs-lookup"><span data-stu-id="b245b-107">The **get\_StopTime** method gets the NTP (Network Time Protocol) ending time value.</span></span> <span data-ttu-id="b245b-108">Si l’heure de fin est égale à zéro, la session n’est pas limitée.</span><span class="sxs-lookup"><span data-stu-id="b245b-108">If the end time is zero, the session is not bounded.</span></span>

## <a name="syntax"></a><span data-ttu-id="b245b-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b245b-109">Syntax</span></span>


```C++
HRESULT get_StopTime(
  [out] DOUBLE *pTime
);
```



## <a name="parameters"></a><span data-ttu-id="b245b-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b245b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b245b-111">*pTime* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b245b-111">*pTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b245b-112">Pointeur désignant l’heure d’arrêt de la session.</span><span class="sxs-lookup"><span data-stu-id="b245b-112">Pointer to the stop time for the session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b245b-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b245b-113">Return value</span></span>

<span data-ttu-id="b245b-114">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="b245b-114">This method can return one of these values.</span></span>



| <span data-ttu-id="b245b-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="b245b-115">Return code</span></span>                                                                                   | <span data-ttu-id="b245b-116">Description</span><span class="sxs-lookup"><span data-stu-id="b245b-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="b245b-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b245b-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="b245b-118">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="b245b-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="b245b-119"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="b245b-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="b245b-120">Le paramètre *pTime* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="b245b-120">The *pTime* parameter is not a valid pointer.</span></span><br/>        |
| <dl> <span data-ttu-id="b245b-121"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="b245b-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="b245b-122">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="b245b-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="b245b-123"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="b245b-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="b245b-124">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="b245b-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="b245b-125"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="b245b-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="b245b-126">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="b245b-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="b245b-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b245b-127">Requirements</span></span>



| <span data-ttu-id="b245b-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b245b-128">Requirement</span></span> | <span data-ttu-id="b245b-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="b245b-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b245b-130">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="b245b-130">TAPI version</span></span><br/> | <span data-ttu-id="b245b-131">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="b245b-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="b245b-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="b245b-132">Header</span></span><br/>       | <dl> <span data-ttu-id="b245b-133"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="b245b-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="b245b-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b245b-134">Library</span></span><br/>      | <dl> <span data-ttu-id="b245b-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b245b-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="b245b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="b245b-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="b245b-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b245b-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b245b-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b245b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b245b-139">**ITTime**</span><span class="sxs-lookup"><span data-stu-id="b245b-139">**ITTime**</span></span>](ittime.md)
</dt> <dt>

[<span data-ttu-id="b245b-140">**ITTime ::p ut \_ StopTime**</span><span class="sxs-lookup"><span data-stu-id="b245b-140">**ITTime::put\_StopTime**</span></span>](ittime-put-stoptime.md)
</dt> </dl>

 

 




