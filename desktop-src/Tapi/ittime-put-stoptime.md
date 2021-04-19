---
description: La \_ méthode put StopTime définit la valeur de l’heure de fin NTP (Network Time Protocol). Si l’heure de fin est égale à zéro, la session n’est pas limitée.
ms.assetid: 6f07054c-5fb2-4ee4-9025-3acf9b51ddbd
title: ITTime ::p ut_StopTime, méthode (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53446ea1d7ee93589987c42b005d7a84e7e728ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545427"
---
# <a name="ittimeput_stoptime-method"></a><span data-ttu-id="00610-104">ITTime ::p ut \_ StopTime, méthode</span><span class="sxs-lookup"><span data-stu-id="00610-104">ITTime::put\_StopTime method</span></span>

<span data-ttu-id="00610-105">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="00610-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="00610-106">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="00610-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="00610-107">La méthode **put \_ StopTime** définit la valeur de l’heure de fin NTP (Network Time Protocol).</span><span class="sxs-lookup"><span data-stu-id="00610-107">The **put\_StopTime** method sets the NTP (Network Time Protocol) ending time value.</span></span> <span data-ttu-id="00610-108">Si l’heure de fin est égale à zéro, la session n’est pas limitée.</span><span class="sxs-lookup"><span data-stu-id="00610-108">If the end time is zero, the session is not bounded.</span></span>

## <a name="syntax"></a><span data-ttu-id="00610-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="00610-109">Syntax</span></span>


```C++
HRESULT put_StopTime(
  [in] DOUBLE Time
);
```



## <a name="parameters"></a><span data-ttu-id="00610-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="00610-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00610-111">*Heure* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="00610-111">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00610-112">Heure d’arrêt de la session.</span><span class="sxs-lookup"><span data-stu-id="00610-112">Stop time for the session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00610-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="00610-113">Return value</span></span>

<span data-ttu-id="00610-114">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="00610-114">This method can return one of these values.</span></span>



| <span data-ttu-id="00610-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="00610-115">Return code</span></span>                                                                                   | <span data-ttu-id="00610-116">Description</span><span class="sxs-lookup"><span data-stu-id="00610-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="00610-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="00610-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="00610-118">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="00610-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="00610-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="00610-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="00610-120">Le paramètre de *temps* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="00610-120">The *Time* parameter is not valid.</span></span><br/>                   |
| <dl> <span data-ttu-id="00610-121"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="00610-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="00610-122">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="00610-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="00610-123"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="00610-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="00610-124">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="00610-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="00610-125"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="00610-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="00610-126">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="00610-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="00610-127">Notes</span><span class="sxs-lookup"><span data-stu-id="00610-127">Remarks</span></span>

<span data-ttu-id="00610-128">Cette fonction peut envoyer des données sur le réseau sous une forme non chiffrée ; par conséquent, une personne malveillante sur le réseau peut être en mesure de lire les données.</span><span class="sxs-lookup"><span data-stu-id="00610-128">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="00610-129">Les risques de sécurité liés à l’envoi des données en texte clair doivent être pris en compte avant d’utiliser cette méthode.</span><span class="sxs-lookup"><span data-stu-id="00610-129">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="00610-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="00610-130">Requirements</span></span>



| <span data-ttu-id="00610-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="00610-131">Requirement</span></span> | <span data-ttu-id="00610-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="00610-132">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="00610-133">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="00610-133">TAPI version</span></span><br/> | <span data-ttu-id="00610-134">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="00610-134">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="00610-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="00610-135">Header</span></span><br/>       | <dl> <span data-ttu-id="00610-136"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="00610-136"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="00610-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="00610-137">Library</span></span><br/>      | <dl> <span data-ttu-id="00610-138"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="00610-138"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="00610-139">DLL</span><span class="sxs-lookup"><span data-stu-id="00610-139">DLL</span></span><br/>          | <dl> <span data-ttu-id="00610-140"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00610-140"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00610-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="00610-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00610-142">**ITTime**</span><span class="sxs-lookup"><span data-stu-id="00610-142">**ITTime**</span></span>](ittime.md)
</dt> <dt>

[<span data-ttu-id="00610-143">**ITTime :: obtient \_ StopTime**</span><span class="sxs-lookup"><span data-stu-id="00610-143">**ITTime::get\_StopTime**</span></span>](ittime-get-stoptime.md)
</dt> </dl>

 

 




