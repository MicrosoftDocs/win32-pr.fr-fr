---
description: La méthode GetControlState récupère l’état de la capture, qui indique si la capture est en cours d’exécution ou en pause.
ms.assetid: ae0cf869-bf5b-4c23-a924-014554053c92
title: 'IRTC :: GetControlState, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.GetControlState
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d437d9463ed3225cd3a474e78220acf1f07af4bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864073"
---
# <a name="irtcgetcontrolstate-method"></a><span data-ttu-id="54684-103">IRTC :: GetControlState, méthode</span><span class="sxs-lookup"><span data-stu-id="54684-103">IRTC::GetControlState method</span></span>

<span data-ttu-id="54684-104">La méthode **GetControlState** récupère l’état de la [*capture*](c.md), qui indique si la capture est en cours d’exécution ou en pause.</span><span class="sxs-lookup"><span data-stu-id="54684-104">The **GetControlState** method retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span>

## <a name="syntax"></a><span data-ttu-id="54684-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="54684-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetControlState(
  [out] BOOL *IsRunnning,
  [out] BOOL *IsPaused
);
```



## <a name="parameters"></a><span data-ttu-id="54684-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="54684-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54684-107">*IsRunnning* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="54684-107">*IsRunnning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="54684-108">Indicateur de l’exécution de la capture en cours, y compris si la capture est suspendue.</span><span class="sxs-lookup"><span data-stu-id="54684-108">Indicator that the current capture is running, including if the capture is paused.</span></span>

</dd> <dt>

<span data-ttu-id="54684-109">*IsPaused* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="54684-109">*IsPaused* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="54684-110">Indicateur signalant que la capture en cours est suspendue.</span><span class="sxs-lookup"><span data-stu-id="54684-110">Indicator that the current capture is paused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54684-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="54684-111">Return value</span></span>

<span data-ttu-id="54684-112">Si la méthode réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="54684-112">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="54684-113">Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :</span><span class="sxs-lookup"><span data-stu-id="54684-113">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="54684-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="54684-114">Return code</span></span>                                                                                          | <span data-ttu-id="54684-115">Description</span><span class="sxs-lookup"><span data-stu-id="54684-115">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="54684-116"><dt>**NMERR \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="54684-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="54684-117">Le NPP n’est pas connecté au réseau.</span><span class="sxs-lookup"><span data-stu-id="54684-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="54684-118">Appelez [IRTC :: Connect](irtc-connect.md) pour connecter le NPP au réseau.</span><span class="sxs-lookup"><span data-stu-id="54684-118">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="54684-119"><dt>**NMERR \_ pas de \_ temps réel**</dt></span><span class="sxs-lookup"><span data-stu-id="54684-119"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>  | <span data-ttu-id="54684-120">Le NPP est connecté au réseau, mais pas avec la méthode [IRTC :: Connect](irtc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="54684-120">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="54684-121">Notes</span><span class="sxs-lookup"><span data-stu-id="54684-121">Remarks</span></span>

<span data-ttu-id="54684-122">Cette méthode peut être appelée chaque fois que le NPP est connecté au réseau.</span><span class="sxs-lookup"><span data-stu-id="54684-122">This method can be called any time the NPP is connected to the network.</span></span> <span data-ttu-id="54684-123">Vous pouvez utiliser cette méthode pour déterminer si une capture est en cours d’exécution, si la capture est suspendue ou si la capture a été arrêtée alors que le NPP est toujours connecté.</span><span class="sxs-lookup"><span data-stu-id="54684-123">You can use this method to find out if a capture is running, if the capture is paused, or if the capture has been stopped but the NPP is still connected.</span></span>

## <a name="requirements"></a><span data-ttu-id="54684-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="54684-124">Requirements</span></span>



| <span data-ttu-id="54684-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="54684-125">Requirement</span></span> | <span data-ttu-id="54684-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="54684-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54684-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="54684-127">Minimum supported client</span></span><br/> | <span data-ttu-id="54684-128">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="54684-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="54684-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="54684-129">Minimum supported server</span></span><br/> | <span data-ttu-id="54684-130">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="54684-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="54684-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="54684-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="54684-132"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="54684-132"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="54684-133">DLL</span><span class="sxs-lookup"><span data-stu-id="54684-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54684-134"><dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54684-134"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54684-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="54684-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54684-136">IRTC</span><span class="sxs-lookup"><span data-stu-id="54684-136">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="54684-137">IRTC :: Connect</span><span class="sxs-lookup"><span data-stu-id="54684-137">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="54684-138">IRTC ::P ause</span><span class="sxs-lookup"><span data-stu-id="54684-138">IRTC::Pause</span></span>](irtc-pause.md)
</dt> <dt>

[<span data-ttu-id="54684-139">IRTC :: Start</span><span class="sxs-lookup"><span data-stu-id="54684-139">IRTC::Start</span></span>](irtc-start.md)
</dt> <dt>

[<span data-ttu-id="54684-140">IRTC :: Stop</span><span class="sxs-lookup"><span data-stu-id="54684-140">IRTC::Stop</span></span>](irtc-stop.md)
</dt> </dl>

 

 




