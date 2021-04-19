---
description: La \_ méthode obtenir la bande passante obtient la valeur de la bande passante.
ms.assetid: d9020443-d061-4a60-9d54-191144def110
title: 'ITConnection :: get_Bandwidth, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 563ff4d5902a3434839167ffd28fad2b7552e5c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541770"
---
# <a name="itconnectionget_bandwidth-method"></a><span data-ttu-id="f5a57-103">ITConnection :: obtient \_ la méthode de bande passante</span><span class="sxs-lookup"><span data-stu-id="f5a57-103">ITConnection::get\_Bandwidth method</span></span>

<span data-ttu-id="f5a57-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="f5a57-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f5a57-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="f5a57-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="f5a57-106">La méthode **obtenir la \_ bande passante** obtient la valeur de la bande passante.</span><span class="sxs-lookup"><span data-stu-id="f5a57-106">The **get\_Bandwidth** method gets the bandwidth value.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5a57-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f5a57-107">Syntax</span></span>


```C++
HRESULT get_Bandwidth(
  [out] DOUBLE *pBandwidth
);
```



## <a name="parameters"></a><span data-ttu-id="f5a57-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f5a57-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5a57-109">*pBandwidth* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f5a57-109">*pBandwidth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f5a57-110">Valeur de la bande passante.</span><span class="sxs-lookup"><span data-stu-id="f5a57-110">Bandwidth value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5a57-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f5a57-111">Return value</span></span>

<span data-ttu-id="f5a57-112">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="f5a57-112">This method can return one of these values.</span></span>



| <span data-ttu-id="f5a57-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="f5a57-113">Return code</span></span>                                                                                   | <span data-ttu-id="f5a57-114">Description</span><span class="sxs-lookup"><span data-stu-id="f5a57-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="f5a57-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f5a57-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f5a57-116">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="f5a57-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="f5a57-117"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="f5a57-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="f5a57-118">Le paramètre *pBandwidth* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="f5a57-118">The *pBandwidth* parameter is not a valid pointer.</span></span><br/>   |
| <dl> <span data-ttu-id="f5a57-119"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="f5a57-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f5a57-120">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="f5a57-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="f5a57-121"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="f5a57-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="f5a57-122">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f5a57-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="f5a57-123"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="f5a57-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="f5a57-124">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="f5a57-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="f5a57-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f5a57-125">Requirements</span></span>



| <span data-ttu-id="f5a57-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f5a57-126">Requirement</span></span> | <span data-ttu-id="f5a57-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="f5a57-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f5a57-128">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="f5a57-128">TAPI version</span></span><br/> | <span data-ttu-id="f5a57-129">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="f5a57-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="f5a57-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="f5a57-130">Header</span></span><br/>       | <dl> <span data-ttu-id="f5a57-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5a57-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="f5a57-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f5a57-132">Library</span></span><br/>      | <dl> <span data-ttu-id="f5a57-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f5a57-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="f5a57-134">DLL</span><span class="sxs-lookup"><span data-stu-id="f5a57-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="f5a57-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5a57-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5a57-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5a57-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5a57-137">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="f5a57-137">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

 




