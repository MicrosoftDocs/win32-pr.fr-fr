---
description: 'IStats :: GetControlState, méthode-la méthode GetControlState récupère l’état de la capture, qui indique si la capture est en cours d’exécution ou en pause.'
ms.assetid: 0faf2300-d9ff-4fe0-9d50-18beafd1daea
title: 'IStats :: GetControlState, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.GetControlState
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 25532293335756a872ef5104d5eef66027fe2ae4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098467"
---
# <a name="istatsgetcontrolstate-method"></a><span data-ttu-id="d986f-103">IStats :: GetControlState, méthode</span><span class="sxs-lookup"><span data-stu-id="d986f-103">IStats::GetControlState method</span></span>

<span data-ttu-id="d986f-104">La méthode **GetControlState** récupère l’état de la [*capture*](c.md), qui indique si la capture est en cours d’exécution ou en pause.</span><span class="sxs-lookup"><span data-stu-id="d986f-104">The **GetControlState** method retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span>

## <a name="syntax"></a><span data-ttu-id="d986f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d986f-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetControlState(
  [out] BOOL *IsRunnning,
  [out] BOOL *IsPaused
);
```



## <a name="parameters"></a><span data-ttu-id="d986f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d986f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d986f-107">*IsRunnning* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d986f-107">*IsRunnning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d986f-108">Indicateur de l’exécution de la capture en cours, y compris si la capture est suspendue.</span><span class="sxs-lookup"><span data-stu-id="d986f-108">Indicator that the current capture is running, including if the capture is paused.</span></span>

</dd> <dt>

<span data-ttu-id="d986f-109">*IsPaused* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d986f-109">*IsPaused* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d986f-110">Indicateur signalant que la capture en cours est suspendue.</span><span class="sxs-lookup"><span data-stu-id="d986f-110">Indicator that the current capture is paused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d986f-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d986f-111">Return value</span></span>

<span data-ttu-id="d986f-112">Si la méthode réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="d986f-112">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="d986f-113">Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :</span><span class="sxs-lookup"><span data-stu-id="d986f-113">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="d986f-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="d986f-114">Return code</span></span>                                                                                            | <span data-ttu-id="d986f-115">Description</span><span class="sxs-lookup"><span data-stu-id="d986f-115">Description</span></span>                                                                                                                       |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d986f-116"><dt>**NMERR \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="d986f-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>   | <span data-ttu-id="d986f-117">Le NPP n’est pas connecté au réseau.</span><span class="sxs-lookup"><span data-stu-id="d986f-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="d986f-118">Appelez [IStats :: Connect](istats-connect.md) pour connecter le NPP au réseau.</span><span class="sxs-lookup"><span data-stu-id="d986f-118">Call [IStats::Connect](istats-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="d986f-119"><dt>**NMERR \_ non \_ stats \_ uniquement**</dt></span><span class="sxs-lookup"><span data-stu-id="d986f-119"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="d986f-120">Le NPP est connecté au réseau, mais pas avec la méthode [IStats :: Connect](istats-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="d986f-120">The NPP is connected to the network but not with the [IStats::Connect](istats-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="d986f-121">Notes </span><span class="sxs-lookup"><span data-stu-id="d986f-121">Remarks</span></span>

<span data-ttu-id="d986f-122">Cette méthode peut être appelée chaque fois que le NPP est connecté au réseau.</span><span class="sxs-lookup"><span data-stu-id="d986f-122">This method can be called any time the NPP is connected to the network.</span></span> <span data-ttu-id="d986f-123">Vous pouvez utiliser cette méthode pour déterminer si une capture est en cours d’exécution, si la capture est suspendue ou si la capture a été arrêtée, mais que le NPP n’est pas déconnecté.</span><span class="sxs-lookup"><span data-stu-id="d986f-123">You can use this method to find out if a capture is running, if the capture is paused, or if the capture has been stopped but the NPP is not disconnected.</span></span>

## <a name="requirements"></a><span data-ttu-id="d986f-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d986f-124">Requirements</span></span>



| <span data-ttu-id="d986f-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d986f-125">Requirement</span></span> | <span data-ttu-id="d986f-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="d986f-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d986f-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d986f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d986f-128">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d986f-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="d986f-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d986f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d986f-130">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d986f-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="d986f-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="d986f-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="d986f-132"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d986f-132"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="d986f-133">DLL</span><span class="sxs-lookup"><span data-stu-id="d986f-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d986f-134"><dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d986f-134"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d986f-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d986f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d986f-136">IStats</span><span class="sxs-lookup"><span data-stu-id="d986f-136">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="d986f-137">IStats :: Connect</span><span class="sxs-lookup"><span data-stu-id="d986f-137">IStats::Connect</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="d986f-138">IStats ::P ause</span><span class="sxs-lookup"><span data-stu-id="d986f-138">IStats::Pause</span></span>](istats-pause.md)
</dt> <dt>

[<span data-ttu-id="d986f-139">IStatsC :: Start</span><span class="sxs-lookup"><span data-stu-id="d986f-139">IStatsC::Start</span></span>](istats-start.md)
</dt> <dt>

[<span data-ttu-id="d986f-140">IStatsC :: Stop</span><span class="sxs-lookup"><span data-stu-id="d986f-140">IStatsC::Stop</span></span>](istats-stop.md)
</dt> </dl>

 

 




