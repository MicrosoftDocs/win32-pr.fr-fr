---
description: La \_ méthode put StartTime définit la valeur de l’heure de début du protocole NTP (Network Time Protocol) 32 bits. La session est considérée comme active à partir de cette heure.
ms.assetid: c7c96265-4588-4f05-83b6-6ef54f02650b
title: ITTime ::p ut_StartTime, méthode (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a5b574f7c90d7cc2f92204e3a045b33e6fb8480
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540404"
---
# <a name="ittimeput_starttime-method"></a><span data-ttu-id="a5bf1-104">ITTime ::p ut \_ StartTime, méthode</span><span class="sxs-lookup"><span data-stu-id="a5bf1-104">ITTime::put\_StartTime method</span></span>

<span data-ttu-id="a5bf1-105">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="a5bf1-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a5bf1-106">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="a5bf1-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="a5bf1-107">La méthode **put \_ StartTime** définit la valeur de l’heure de début du protocole NTP (Network Time Protocol) 32 bits.</span><span class="sxs-lookup"><span data-stu-id="a5bf1-107">The **put\_StartTime** method sets the 32-bit NTP (Network Time Protocol) starting time value.</span></span> <span data-ttu-id="a5bf1-108">La session est considérée comme active à partir de cette heure.</span><span class="sxs-lookup"><span data-stu-id="a5bf1-108">The session is considered active from this time.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5bf1-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a5bf1-109">Syntax</span></span>


```C++
HRESULT put_StartTime(
  [in] DOUBLE Time
);
```



## <a name="parameters"></a><span data-ttu-id="a5bf1-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a5bf1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5bf1-111">*Heure* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a5bf1-111">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5bf1-112">Heure de début de la session.</span><span class="sxs-lookup"><span data-stu-id="a5bf1-112">Start time for the session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5bf1-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a5bf1-113">Return value</span></span>

<span data-ttu-id="a5bf1-114">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="a5bf1-114">This method can return one of these values.</span></span>



| <span data-ttu-id="a5bf1-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="a5bf1-115">Return code</span></span>                                                                                   | <span data-ttu-id="a5bf1-116">Description</span><span class="sxs-lookup"><span data-stu-id="a5bf1-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="a5bf1-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a5bf1-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a5bf1-118">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="a5bf1-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="a5bf1-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a5bf1-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="a5bf1-120">Le paramètre *Tim* e n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="a5bf1-120">The *Tim* e parameter is not valid.</span></span><br/>                   |
| <dl> <span data-ttu-id="a5bf1-121"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="a5bf1-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="a5bf1-122">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="a5bf1-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="a5bf1-123"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="a5bf1-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="a5bf1-124">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="a5bf1-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="a5bf1-125"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="a5bf1-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="a5bf1-126">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="a5bf1-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="a5bf1-127">Notes</span><span class="sxs-lookup"><span data-stu-id="a5bf1-127">Remarks</span></span>

<span data-ttu-id="a5bf1-128">Cette fonction peut envoyer des données sur le réseau sous une forme non chiffrée ; par conséquent, une personne malveillante sur le réseau peut être en mesure de lire les données.</span><span class="sxs-lookup"><span data-stu-id="a5bf1-128">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="a5bf1-129">Les risques de sécurité liés à l’envoi des données en texte clair doivent être pris en compte avant d’utiliser cette méthode.</span><span class="sxs-lookup"><span data-stu-id="a5bf1-129">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5bf1-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a5bf1-130">Requirements</span></span>



| <span data-ttu-id="a5bf1-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a5bf1-131">Requirement</span></span> | <span data-ttu-id="a5bf1-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="a5bf1-132">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a5bf1-133">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="a5bf1-133">TAPI version</span></span><br/> | <span data-ttu-id="a5bf1-134">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="a5bf1-134">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="a5bf1-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="a5bf1-135">Header</span></span><br/>       | <dl> <span data-ttu-id="a5bf1-136"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5bf1-136"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="a5bf1-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a5bf1-137">Library</span></span><br/>      | <dl> <span data-ttu-id="a5bf1-138"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a5bf1-138"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="a5bf1-139">DLL</span><span class="sxs-lookup"><span data-stu-id="a5bf1-139">DLL</span></span><br/>          | <dl> <span data-ttu-id="a5bf1-140"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5bf1-140"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5bf1-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5bf1-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5bf1-142">**ITTime**</span><span class="sxs-lookup"><span data-stu-id="a5bf1-142">**ITTime**</span></span>](ittime.md)
</dt> <dt>

[<span data-ttu-id="a5bf1-143">**ITTime :: obtient \_ StartTime**</span><span class="sxs-lookup"><span data-stu-id="a5bf1-143">**ITTime::get\_StartTime**</span></span>](ittime-get-starttime.md)
</dt> </dl>

 

 




