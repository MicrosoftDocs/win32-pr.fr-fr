---
description: La méthode GetControlState récupère l’état de la capture, qui indique si la capture est en cours d’exécution ou en pause.
ms.assetid: 21b7faaa-591f-4e15-b4e9-453ea690ab4a
title: 'IDelaydC :: GetControlState, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.GetControlState
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 8f5c3f084db788844f061ba2005d9c3ca38acef0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950953"
---
# <a name="idelaydcgetcontrolstate-method"></a><span data-ttu-id="c0758-103">IDelaydC :: GetControlState, méthode</span><span class="sxs-lookup"><span data-stu-id="c0758-103">IDelaydC::GetControlState method</span></span>

<span data-ttu-id="c0758-104">La méthode **GetControlState** récupère l’état de la [*capture*](c.md), qui indique si la capture est en cours d’exécution ou en pause.</span><span class="sxs-lookup"><span data-stu-id="c0758-104">The **GetControlState** method retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0758-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c0758-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetControlState(
  [out] BOOL *IsRunnning,
  [out] BOOL *IsPaused
);
```



## <a name="parameters"></a><span data-ttu-id="c0758-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c0758-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0758-107">*IsRunnning* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c0758-107">*IsRunnning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c0758-108">Indicateur de l’exécution de la capture en cours, y compris si la capture est suspendue.</span><span class="sxs-lookup"><span data-stu-id="c0758-108">Indicator that the current capture is running, including if the capture is paused.</span></span>

</dd> <dt>

<span data-ttu-id="c0758-109">*IsPaused* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c0758-109">*IsPaused* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c0758-110">Indicateur signalant que la capture en cours est suspendue.</span><span class="sxs-lookup"><span data-stu-id="c0758-110">Indicator that the current capture is paused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0758-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c0758-111">Return value</span></span>

<span data-ttu-id="c0758-112">Si la méthode réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="c0758-112">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="c0758-113">Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :</span><span class="sxs-lookup"><span data-stu-id="c0758-113">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="c0758-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="c0758-114">Return code</span></span>                                                                                          | <span data-ttu-id="c0758-115">Description</span><span class="sxs-lookup"><span data-stu-id="c0758-115">Description</span></span>                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c0758-116"><dt>**NMERR \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="c0758-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="c0758-117">Le NPP n’est pas connecté au réseau.</span><span class="sxs-lookup"><span data-stu-id="c0758-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="c0758-118">Appelez [IDelaydC :: Connect](idelaydc-connect.md) pour connecter le NPP au réseau.</span><span class="sxs-lookup"><span data-stu-id="c0758-118">Call [IDelaydC::Connect](idelaydc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="c0758-119"><dt>**NMERR \_ non \_ retardé**</dt></span><span class="sxs-lookup"><span data-stu-id="c0758-119"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>   | <span data-ttu-id="c0758-120">Le NPP est connecté au réseau, mais pas avec la méthode [IDelaydC :: Connect](idelaydc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="c0758-120">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="c0758-121">Notes</span><span class="sxs-lookup"><span data-stu-id="c0758-121">Remarks</span></span>

<span data-ttu-id="c0758-122">Cette méthode peut être appelée chaque fois que le NPP est connecté au réseau à l’aide de l’interface [IDelaydC](idelaydc.md) .</span><span class="sxs-lookup"><span data-stu-id="c0758-122">This method can be called any time the NPP is connected to the network by using the [IDelaydC](idelaydc.md) interface.</span></span> <span data-ttu-id="c0758-123">Vous pouvez utiliser cette méthode pour déterminer si une capture est en cours d’exécution, si la capture est suspendue ou si la capture a été arrêtée, mais que le NPP n’est pas déconnecté.</span><span class="sxs-lookup"><span data-stu-id="c0758-123">You can use this method to find out if a capture is running, if the capture is paused, or if the capture has been stopped but the NPP is not disconnected.</span></span>

<span data-ttu-id="c0758-124">Les méthodes utilisées pour démarrer, suspendre et arrêter la capture sont répertoriées dans la liste Voir aussi ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="c0758-124">The methods used to start, pause, and, stop the capture are listed in the See Also list below.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0758-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c0758-125">Requirements</span></span>



| <span data-ttu-id="c0758-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c0758-126">Requirement</span></span> | <span data-ttu-id="c0758-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="c0758-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0758-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c0758-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c0758-129">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c0758-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="c0758-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c0758-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c0758-131">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c0758-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="c0758-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="c0758-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0758-133"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0758-133"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="c0758-134">DLL</span><span class="sxs-lookup"><span data-stu-id="c0758-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0758-135"><dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0758-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0758-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0758-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0758-137">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="c0758-137">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="c0758-138">IDelaydC :: Connect</span><span class="sxs-lookup"><span data-stu-id="c0758-138">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="c0758-139">IDelaydC ::P ause</span><span class="sxs-lookup"><span data-stu-id="c0758-139">IDelaydC::Pause</span></span>](idelaydc-pause.md)
</dt> <dt>

[<span data-ttu-id="c0758-140">IDelaydC :: Start</span><span class="sxs-lookup"><span data-stu-id="c0758-140">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="c0758-141">IDelaydC :: Stop</span><span class="sxs-lookup"><span data-stu-id="c0758-141">IDelaydC::Stop</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




