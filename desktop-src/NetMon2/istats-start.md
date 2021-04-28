---
description: 'IStats :: Start, méthode-la méthode start démarre une capture.'
ms.assetid: d4086e30-e5ed-4f29-90f0-d65125d9af6d
title: 'IStats :: Start, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Start
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 64f02529ba10d98092eb30a1bcc350d5c72049fc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094547"
---
# <a name="istatsstart-method"></a><span data-ttu-id="0845c-103">IStats :: Start, méthode</span><span class="sxs-lookup"><span data-stu-id="0845c-103">IStats::Start method</span></span>

<span data-ttu-id="0845c-104">La méthode **Start** démarre une capture.</span><span class="sxs-lookup"><span data-stu-id="0845c-104">The **Start** method starts a capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="0845c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0845c-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Start();
```



## <a name="parameters"></a><span data-ttu-id="0845c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0845c-106">Parameters</span></span>

<span data-ttu-id="0845c-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="0845c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0845c-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0845c-108">Return value</span></span>

<span data-ttu-id="0845c-109">Si la méthode réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="0845c-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="0845c-110">Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :</span><span class="sxs-lookup"><span data-stu-id="0845c-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="0845c-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="0845c-111">Return code</span></span>                                                                                            | <span data-ttu-id="0845c-112">Description</span><span class="sxs-lookup"><span data-stu-id="0845c-112">Description</span></span>                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0845c-113"><dt>**\_capture NMERR \_ suspendue**</dt></span><span class="sxs-lookup"><span data-stu-id="0845c-113"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl>  | <span data-ttu-id="0845c-114">La capture a été suspendue et doit être arrêtée avant de pouvoir être redémarrée.</span><span class="sxs-lookup"><span data-stu-id="0845c-114">The capture has paused and must be stopped before it can be restarted.</span></span> <span data-ttu-id="0845c-115">Appelez la méthode [IStats :: Stop](istats-stop.md) pour arrêter la capture.</span><span class="sxs-lookup"><span data-stu-id="0845c-115">Call the [IStats::Stop](istats-stop.md) method to stop the capture.</span></span><br/> |
| <dl> <span data-ttu-id="0845c-116"><dt>**\_capture NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="0845c-116"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>        | <span data-ttu-id="0845c-117">La capture a déjà démarré.</span><span class="sxs-lookup"><span data-stu-id="0845c-117">The capture has already started.</span></span><br/>                                                                                                            |
| <dl> <span data-ttu-id="0845c-118"><dt>**NMERR \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="0845c-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>   | <span data-ttu-id="0845c-119">Le NPP n’est pas connecté au réseau.</span><span class="sxs-lookup"><span data-stu-id="0845c-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="0845c-120">Appelez la méthode [IStats :: Connect](istats-connect.md) pour connecter le NPP au réseau.</span><span class="sxs-lookup"><span data-stu-id="0845c-120">Call the [IStats::Connect](istats-connect.md) method to connect the NPP to the network.</span></span><br/>           |
| <dl> <span data-ttu-id="0845c-121"><dt>**NMERR \_ non \_ stats \_ uniquement**</dt></span><span class="sxs-lookup"><span data-stu-id="0845c-121"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="0845c-122">Le NPP est connecté au réseau, mais pas avec la méthode [IStats :: Connect](istats-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="0845c-122">The NPP is connected to the network but not with the [IStats::Connect](istats-connect.md) method.</span></span><br/>                                          |



 

## <a name="remarks"></a><span data-ttu-id="0845c-123">Notes </span><span class="sxs-lookup"><span data-stu-id="0845c-123">Remarks</span></span>

<span data-ttu-id="0845c-124">Lors du redémarrage de la capture à l’aide des méthodes IStats :: Start et [IStats :: Stop](istats-stop.md) , vous devez appeler la méthode [IStats :: configure](istats-configure.md) pour reconfigurer la connexion chaque fois que vous appelez IStats :: Start pour redémarrer la capture de données.</span><span class="sxs-lookup"><span data-stu-id="0845c-124">When restarting the capture by using the IStats::Start and [IStats::Stop](istats-stop.md) methods, you must call the [IStats::Configure](istats-configure.md) method to reconfigure the connection each time you call IStats::Start to restart the data capture.</span></span>

> [!Note]  
> <span data-ttu-id="0845c-125">Vous pouvez également démarrer et arrêter la capture à l’aide des méthodes [IStats ::P ause](istats-pause.md) et [IStats :: Resume](istats-resume.md) .</span><span class="sxs-lookup"><span data-stu-id="0845c-125">You can also start and stop the capture by using the [IStats::Pause](istats-pause.md) and [IStats::Resume](istats-resume.md) methods.</span></span> <span data-ttu-id="0845c-126">Lorsque vous utilisez ces méthodes, les données capturées sont stockées dans le même fichier de capture.</span><span class="sxs-lookup"><span data-stu-id="0845c-126">When you use these methods, the captured data is stored in the same capture file.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0845c-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0845c-127">Requirements</span></span>



| <span data-ttu-id="0845c-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0845c-128">Requirement</span></span> | <span data-ttu-id="0845c-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="0845c-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0845c-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0845c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="0845c-131">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0845c-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="0845c-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0845c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="0845c-133">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0845c-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="0845c-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="0845c-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="0845c-135"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="0845c-135"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="0845c-136">DLL</span><span class="sxs-lookup"><span data-stu-id="0845c-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0845c-137"><dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0845c-137"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0845c-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0845c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0845c-139">IStats</span><span class="sxs-lookup"><span data-stu-id="0845c-139">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="0845c-140">IStats :: configure</span><span class="sxs-lookup"><span data-stu-id="0845c-140">IStats::Configure</span></span>](istats-configure.md)
</dt> <dt>

[<span data-ttu-id="0845c-141">IStats :: Connect</span><span class="sxs-lookup"><span data-stu-id="0845c-141">IStats::Connect</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="0845c-142">IStats ::P ause</span><span class="sxs-lookup"><span data-stu-id="0845c-142">IStats::Pause</span></span>](istats-pause.md)
</dt> <dt>

[<span data-ttu-id="0845c-143">IStats :: Resume</span><span class="sxs-lookup"><span data-stu-id="0845c-143">IStats::Resume</span></span>](istats-resume.md)
</dt> <dt>

[<span data-ttu-id="0845c-144">IStats :: Stop</span><span class="sxs-lookup"><span data-stu-id="0845c-144">IStats::Stop</span></span>](istats-stop.md)
</dt> </dl>

 

 




