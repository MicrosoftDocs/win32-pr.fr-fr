---
description: 'IStats :: Resume, méthode-la méthode Resume redémarre une capture suspendue.'
ms.assetid: 128e38c4-7459-4376-a3d7-2c6944fcf535
title: 'IStats :: Resume, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Resume
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: ee7818da3d8a02e41488d473d3cf26607d3b84ff
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114617"
---
# <a name="istatsresume-method"></a><span data-ttu-id="af6b0-103">IStats :: Resume, méthode</span><span class="sxs-lookup"><span data-stu-id="af6b0-103">IStats::Resume method</span></span>

<span data-ttu-id="af6b0-104">La méthode **Resume** redémarre une capture suspendue.</span><span class="sxs-lookup"><span data-stu-id="af6b0-104">The **Resume** method restarts a paused capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="af6b0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="af6b0-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a><span data-ttu-id="af6b0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="af6b0-106">Parameters</span></span>

<span data-ttu-id="af6b0-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="af6b0-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="af6b0-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="af6b0-108">Return value</span></span>

<span data-ttu-id="af6b0-109">Si la méthode réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="af6b0-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="af6b0-110">Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :</span><span class="sxs-lookup"><span data-stu-id="af6b0-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="af6b0-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="af6b0-111">Return code</span></span>                                                                                                | <span data-ttu-id="af6b0-112">Description</span><span class="sxs-lookup"><span data-stu-id="af6b0-112">Description</span></span>                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="af6b0-113"><dt>**NMERR \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="af6b0-113"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>       | <span data-ttu-id="af6b0-114">Le NPP n’est pas connecté au réseau.</span><span class="sxs-lookup"><span data-stu-id="af6b0-114">The NPP is not connected to the network.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="af6b0-115"><dt>**\_capture NMERR \_ non \_ suspendue**</dt></span><span class="sxs-lookup"><span data-stu-id="af6b0-115"><dt>**NMERR\_CAPTURE\_NOT\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="af6b0-116">La capture n’est pas suspendue.</span><span class="sxs-lookup"><span data-stu-id="af6b0-116">The capture is not paused.</span></span> <span data-ttu-id="af6b0-117">Appelez la méthode [IStats ::P ause](istats-pause.md) pour arrêter temporairement la capture.</span><span class="sxs-lookup"><span data-stu-id="af6b0-117">Call the [IStats::Pause](istats-pause.md) method to temporarily stop the capture.</span></span><br/>                     |
| <dl> <span data-ttu-id="af6b0-118"><dt>**NMERR \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="af6b0-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>       | <span data-ttu-id="af6b0-119">Le NPP n’est pas connecté au réseau.</span><span class="sxs-lookup"><span data-stu-id="af6b0-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="af6b0-120">Appelez la méthode [IStats :: Connect](istats-connect.md) pour connecter le NPP au réseau.</span><span class="sxs-lookup"><span data-stu-id="af6b0-120">Call the [IStats::Connect](istats-connect.md) method to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="af6b0-121"><dt>**NMERR \_ non \_ stats \_ uniquement**</dt></span><span class="sxs-lookup"><span data-stu-id="af6b0-121"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl>     | <span data-ttu-id="af6b0-122">Le NPP est connecté au réseau, mais pas avec la méthode [IStats :: Connect](istats-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="af6b0-122">The NPP is connected to the network but not with the [IStats::Connect](istats-connect.md) method.</span></span><br/>                                |



 

## <a name="remarks"></a><span data-ttu-id="af6b0-123">Notes </span><span class="sxs-lookup"><span data-stu-id="af6b0-123">Remarks</span></span>

<span data-ttu-id="af6b0-124">Lorsque la capture est dans un état suspendu, les nouvelles données ne sont pas capturées tant que la méthode IStats :: Resume n’est pas appelée pour redémarrer la capture.</span><span class="sxs-lookup"><span data-stu-id="af6b0-124">While the capture is in a paused state, new data is not captured until the IStats::Resume method is called to restart the capture.</span></span>

<span data-ttu-id="af6b0-125">Lorsque vous utilisez les méthodes **Pause** et **Resume** pour contrôler la capture, moniteur réseau continue à ajouter des [*statistiques de conversation*](c.md) aux statistiques existantes pour la capture en cours.</span><span class="sxs-lookup"><span data-stu-id="af6b0-125">When using the **Pause** and **Resume** methods to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) to the existing statistics for the current capture.</span></span>

<span data-ttu-id="af6b0-126">Pour arrêter la capture, appelez [IStats :: Stop](istats-stop.md).</span><span class="sxs-lookup"><span data-stu-id="af6b0-126">To stop the capture, call [IStats::Stop](istats-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="af6b0-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="af6b0-127">Requirements</span></span>



| <span data-ttu-id="af6b0-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="af6b0-128">Requirement</span></span> | <span data-ttu-id="af6b0-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="af6b0-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af6b0-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af6b0-130">Minimum supported client</span></span><br/> | <span data-ttu-id="af6b0-131">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="af6b0-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="af6b0-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af6b0-132">Minimum supported server</span></span><br/> | <span data-ttu-id="af6b0-133">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="af6b0-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="af6b0-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="af6b0-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="af6b0-135"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="af6b0-135"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="af6b0-136">DLL</span><span class="sxs-lookup"><span data-stu-id="af6b0-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af6b0-137"><dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af6b0-137"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af6b0-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af6b0-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af6b0-139">IStats</span><span class="sxs-lookup"><span data-stu-id="af6b0-139">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="af6b0-140">IStats :: Connect</span><span class="sxs-lookup"><span data-stu-id="af6b0-140">IStats::Connect</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="af6b0-141">IStats ::P ause</span><span class="sxs-lookup"><span data-stu-id="af6b0-141">IStats::Pause</span></span>](istats-pause.md)
</dt> <dt>

[<span data-ttu-id="af6b0-142">IStats :: Stop</span><span class="sxs-lookup"><span data-stu-id="af6b0-142">IStats::Stop</span></span>](istats-stop.md)
</dt> </dl>

 

 




