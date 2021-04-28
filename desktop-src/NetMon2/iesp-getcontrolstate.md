---
description: 'IESP :: GetControlState, méthode-la méthode GetControlState récupère l’état de la capture, qui indique si la capture est en cours d’exécution ou en pause.'
ms.assetid: 19cc3095-3aa3-4482-95f5-959b19f76cea
title: 'IESP :: GetControlState, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.GetControlState
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: b007eb6824ee3e65cdf8195914bbff3a50c39b2c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114677"
---
# <a name="iespgetcontrolstate-method"></a><span data-ttu-id="062a0-103">IESP :: GetControlState, méthode</span><span class="sxs-lookup"><span data-stu-id="062a0-103">IESP::GetControlState method</span></span>

<span data-ttu-id="062a0-104">La méthode **GetControlState** récupère l’état de la [*capture*](c.md), qui indique si la capture est en cours d’exécution ou en pause.</span><span class="sxs-lookup"><span data-stu-id="062a0-104">The **GetControlState** method retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span>

## <a name="syntax"></a><span data-ttu-id="062a0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="062a0-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetControlState(
  [out] BOOL *IsRunnning,
  [out] BOOL *IsPaused
);
```



## <a name="parameters"></a><span data-ttu-id="062a0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="062a0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="062a0-107">*IsRunnning* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="062a0-107">*IsRunnning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="062a0-108">Indicateur de l’exécution de la capture en cours, y compris si la capture est suspendue.</span><span class="sxs-lookup"><span data-stu-id="062a0-108">Indicator that the current capture is running, including if the capture is paused.</span></span>

</dd> <dt>

<span data-ttu-id="062a0-109">*IsPaused* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="062a0-109">*IsPaused* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="062a0-110">Indicateur signalant que la capture en cours est suspendue.</span><span class="sxs-lookup"><span data-stu-id="062a0-110">Indicator that the current capture is paused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="062a0-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="062a0-111">Return value</span></span>

<span data-ttu-id="062a0-112">Si la méthode réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="062a0-112">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="062a0-113">Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :</span><span class="sxs-lookup"><span data-stu-id="062a0-113">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="062a0-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="062a0-114">Return code</span></span>                                                                                          | <span data-ttu-id="062a0-115">Description</span><span class="sxs-lookup"><span data-stu-id="062a0-115">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="062a0-116"><dt>**NMERR \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="062a0-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="062a0-117">Le NPP n’est pas connecté au réseau.</span><span class="sxs-lookup"><span data-stu-id="062a0-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="062a0-118">Appelez [IESP :: Connect](iesp-connect.md) pour connecter le NPP au réseau.</span><span class="sxs-lookup"><span data-stu-id="062a0-118">Call [IESP::Connect](iesp-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="062a0-119"><dt>**NMERR \_ non \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="062a0-119"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>       | <span data-ttu-id="062a0-120">Le NPP est connecté au réseau, mais pas avec la méthode [IESP :: Connect](iesp-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="062a0-120">The NPP is connected to the network but not with the [IESP::Connect](iesp-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="062a0-121">Notes </span><span class="sxs-lookup"><span data-stu-id="062a0-121">Remarks</span></span>

<span data-ttu-id="062a0-122">Cette méthode peut être appelée chaque fois que le NPP est connecté au réseau.</span><span class="sxs-lookup"><span data-stu-id="062a0-122">This method can be called any time the NPP is connected to the network.</span></span> <span data-ttu-id="062a0-123">Vous pouvez utiliser cette méthode pour déterminer si une capture est en cours d’exécution, si la capture est suspendue ou si la capture a été arrêtée alors que le NPP est toujours connecté.</span><span class="sxs-lookup"><span data-stu-id="062a0-123">You can use this method to find out if a capture is running, if the capture is paused, or if the capture has been stopped but the NPP is still connected.</span></span>

## <a name="requirements"></a><span data-ttu-id="062a0-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="062a0-124">Requirements</span></span>



| <span data-ttu-id="062a0-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="062a0-125">Requirement</span></span> | <span data-ttu-id="062a0-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="062a0-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="062a0-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="062a0-127">Minimum supported client</span></span><br/> | <span data-ttu-id="062a0-128">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="062a0-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="062a0-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="062a0-129">Minimum supported server</span></span><br/> | <span data-ttu-id="062a0-130">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="062a0-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="062a0-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="062a0-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="062a0-132"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="062a0-132"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="062a0-133">DLL</span><span class="sxs-lookup"><span data-stu-id="062a0-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="062a0-134"><dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="062a0-134"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="062a0-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="062a0-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="062a0-136">IESP</span><span class="sxs-lookup"><span data-stu-id="062a0-136">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="062a0-137">IESP :: Connect</span><span class="sxs-lookup"><span data-stu-id="062a0-137">IESP::Connect</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="062a0-138">IESP ::P ause</span><span class="sxs-lookup"><span data-stu-id="062a0-138">IESP::Pause</span></span>](iesp-pause.md)
</dt> <dt>

[<span data-ttu-id="062a0-139">IESP :: Start</span><span class="sxs-lookup"><span data-stu-id="062a0-139">IESP::Start</span></span>](iesp-start.md)
</dt> <dt>

[<span data-ttu-id="062a0-140">IESP :: Stop</span><span class="sxs-lookup"><span data-stu-id="062a0-140">IESP::Stop</span></span>](iesp-stop.md)
</dt> </dl>

 

 




