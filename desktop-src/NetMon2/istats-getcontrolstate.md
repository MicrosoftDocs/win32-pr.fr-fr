---
description: La méthode GetControlState récupère l’état de la capture, qui indique si la capture est en cours d’exécution ou en pause.
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
ms.openlocfilehash: a83b5d20461b28b7022bfdc3ddbf3d5d92149c26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531230"
---
# <a name="istatsgetcontrolstate-method"></a><span data-ttu-id="84589-103">IStats :: GetControlState, méthode</span><span class="sxs-lookup"><span data-stu-id="84589-103">IStats::GetControlState method</span></span>

<span data-ttu-id="84589-104">La méthode **GetControlState** récupère l’état de la [*capture*](c.md), qui indique si la capture est en cours d’exécution ou en pause.</span><span class="sxs-lookup"><span data-stu-id="84589-104">The **GetControlState** method retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span>

## <a name="syntax"></a><span data-ttu-id="84589-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="84589-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetControlState(
  [out] BOOL *IsRunnning,
  [out] BOOL *IsPaused
);
```



## <a name="parameters"></a><span data-ttu-id="84589-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="84589-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84589-107">*IsRunnning* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="84589-107">*IsRunnning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="84589-108">Indicateur de l’exécution de la capture en cours, y compris si la capture est suspendue.</span><span class="sxs-lookup"><span data-stu-id="84589-108">Indicator that the current capture is running, including if the capture is paused.</span></span>

</dd> <dt>

<span data-ttu-id="84589-109">*IsPaused* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="84589-109">*IsPaused* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="84589-110">Indicateur signalant que la capture en cours est suspendue.</span><span class="sxs-lookup"><span data-stu-id="84589-110">Indicator that the current capture is paused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84589-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="84589-111">Return value</span></span>

<span data-ttu-id="84589-112">Si la méthode réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="84589-112">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="84589-113">Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :</span><span class="sxs-lookup"><span data-stu-id="84589-113">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="84589-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="84589-114">Return code</span></span>                                                                                            | <span data-ttu-id="84589-115">Description</span><span class="sxs-lookup"><span data-stu-id="84589-115">Description</span></span>                                                                                                                       |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="84589-116"><dt>**NMERR \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="84589-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>   | <span data-ttu-id="84589-117">Le NPP n’est pas connecté au réseau.</span><span class="sxs-lookup"><span data-stu-id="84589-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="84589-118">Appelez [IStats :: Connect](istats-connect.md) pour connecter le NPP au réseau.</span><span class="sxs-lookup"><span data-stu-id="84589-118">Call [IStats::Connect](istats-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="84589-119"><dt>**NMERR \_ non \_ stats \_ uniquement**</dt></span><span class="sxs-lookup"><span data-stu-id="84589-119"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="84589-120">Le NPP est connecté au réseau, mais pas avec la méthode [IStats :: Connect](istats-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="84589-120">The NPP is connected to the network but not with the [IStats::Connect](istats-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="84589-121">Notes</span><span class="sxs-lookup"><span data-stu-id="84589-121">Remarks</span></span>

<span data-ttu-id="84589-122">Cette méthode peut être appelée chaque fois que le NPP est connecté au réseau.</span><span class="sxs-lookup"><span data-stu-id="84589-122">This method can be called any time the NPP is connected to the network.</span></span> <span data-ttu-id="84589-123">Vous pouvez utiliser cette méthode pour déterminer si une capture est en cours d’exécution, si la capture est suspendue ou si la capture a été arrêtée, mais que le NPP n’est pas déconnecté.</span><span class="sxs-lookup"><span data-stu-id="84589-123">You can use this method to find out if a capture is running, if the capture is paused, or if the capture has been stopped but the NPP is not disconnected.</span></span>

## <a name="requirements"></a><span data-ttu-id="84589-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="84589-124">Requirements</span></span>



| <span data-ttu-id="84589-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="84589-125">Requirement</span></span> | <span data-ttu-id="84589-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="84589-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84589-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84589-127">Minimum supported client</span></span><br/> | <span data-ttu-id="84589-128">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="84589-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="84589-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84589-129">Minimum supported server</span></span><br/> | <span data-ttu-id="84589-130">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="84589-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="84589-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="84589-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="84589-132"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="84589-132"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="84589-133">DLL</span><span class="sxs-lookup"><span data-stu-id="84589-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84589-134"><dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84589-134"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84589-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="84589-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84589-136">IStats</span><span class="sxs-lookup"><span data-stu-id="84589-136">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="84589-137">IStats :: Connect</span><span class="sxs-lookup"><span data-stu-id="84589-137">IStats::Connect</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="84589-138">IStats ::P ause</span><span class="sxs-lookup"><span data-stu-id="84589-138">IStats::Pause</span></span>](istats-pause.md)
</dt> <dt>

[<span data-ttu-id="84589-139">IStatsC :: Start</span><span class="sxs-lookup"><span data-stu-id="84589-139">IStatsC::Start</span></span>](istats-start.md)
</dt> <dt>

[<span data-ttu-id="84589-140">IStatsC :: Stop</span><span class="sxs-lookup"><span data-stu-id="84589-140">IStatsC::Stop</span></span>](istats-stop.md)
</dt> </dl>

 

 




