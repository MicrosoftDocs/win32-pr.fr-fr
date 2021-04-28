---
description: IRTC ::P méthode ause-la méthode pause interrompt la capture en cours.
ms.assetid: 8c7b310e-de04-4bd8-9c96-3c5948e610be
title: IRTC ::P méthode ause (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Pause
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d42af1912365a4237889e4e46d0fb3343377c772
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110677"
---
# <a name="irtcpause-method"></a><span data-ttu-id="0b879-103">IRTC ::P méthode ause</span><span class="sxs-lookup"><span data-stu-id="0b879-103">IRTC::Pause method</span></span>

<span data-ttu-id="0b879-104">La méthode **Pause** interrompt la capture en cours.</span><span class="sxs-lookup"><span data-stu-id="0b879-104">The **Pause** method pauses the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b879-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0b879-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Pause();
```



## <a name="parameters"></a><span data-ttu-id="0b879-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0b879-106">Parameters</span></span>

<span data-ttu-id="0b879-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="0b879-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0b879-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0b879-108">Return value</span></span>

<span data-ttu-id="0b879-109">Si la méthode réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="0b879-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="0b879-110">Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :</span><span class="sxs-lookup"><span data-stu-id="0b879-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="0b879-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="0b879-111">Return code</span></span>                                                                                           | <span data-ttu-id="0b879-112">Description</span><span class="sxs-lookup"><span data-stu-id="0b879-112">Description</span></span>                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0b879-113"><dt>**\_capture NMERR \_ suspendue**</dt></span><span class="sxs-lookup"><span data-stu-id="0b879-113"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="0b879-114">La capture est déjà suspendue.</span><span class="sxs-lookup"><span data-stu-id="0b879-114">The capture is already paused.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="0b879-115"><dt>**NMERR \_ pas de \_ capture**</dt></span><span class="sxs-lookup"><span data-stu-id="0b879-115"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>  | <span data-ttu-id="0b879-116">Le NPP ne capture pas de données.</span><span class="sxs-lookup"><span data-stu-id="0b879-116">The NPP is not capturing data.</span></span> <span data-ttu-id="0b879-117">Appelez [IRTC :: Start](irtc-start.md) pour démarrer la capture.</span><span class="sxs-lookup"><span data-stu-id="0b879-117">Call [IRTC::Start](irtc-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="0b879-118"><dt>**NMERR \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="0b879-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="0b879-119">Le NPP n’est pas connecté au réseau.</span><span class="sxs-lookup"><span data-stu-id="0b879-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="0b879-120">Appelez [IRTC :: Connect](irtc-connect.md) pour connecter le NPP au réseau.</span><span class="sxs-lookup"><span data-stu-id="0b879-120">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="0b879-121"><dt>**NMERR \_ pas de \_ temps réel**</dt></span><span class="sxs-lookup"><span data-stu-id="0b879-121"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>   | <span data-ttu-id="0b879-122">Le NPP est connecté au réseau, mais pas avec la méthode [IRTC :: Connect](irtc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="0b879-122">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="0b879-123">Notes </span><span class="sxs-lookup"><span data-stu-id="0b879-123">Remarks</span></span>

<span data-ttu-id="0b879-124">Lorsque la capture est dans un état suspendu, les nouveaux frames ne sont pas capturés jusqu’à ce que la méthode [IRTC :: Resume](irtc-resume.md) soit appelée pour redémarrer la capture.</span><span class="sxs-lookup"><span data-stu-id="0b879-124">While the capture is in a paused state, new frames are not captured until the [IRTC::Resume](irtc-resume.md) method is called to restart the capture.</span></span>

<span data-ttu-id="0b879-125">Lorsque vous utilisez les méthodes **IRTC ::P ause** et **IRTC :: Resume** pour contrôler la capture, moniteur réseau continue à ajouter des [*statistiques de conversation*](c.md) chaque fois que la capture est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="0b879-125">When you use the **IRTC::Pause** and **IRTC::Resume** methods to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) whenever the capture is running.</span></span>

<span data-ttu-id="0b879-126">Pour redémarrer l’appel de capture [IRTC :: Resume](irtc-resume.md).</span><span class="sxs-lookup"><span data-stu-id="0b879-126">To restart the capture call [IRTC::Resume](irtc-resume.md).</span></span> <span data-ttu-id="0b879-127">Pour arrêter la capture, appelez [IRTC :: Stop](irtc-stop.md).</span><span class="sxs-lookup"><span data-stu-id="0b879-127">To stop the capture, call [IRTC::Stop](irtc-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0b879-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0b879-128">Requirements</span></span>



| <span data-ttu-id="0b879-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0b879-129">Requirement</span></span> | <span data-ttu-id="0b879-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="0b879-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b879-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0b879-131">Minimum supported client</span></span><br/> | <span data-ttu-id="0b879-132">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0b879-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="0b879-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0b879-133">Minimum supported server</span></span><br/> | <span data-ttu-id="0b879-134">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0b879-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="0b879-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="0b879-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b879-136"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b879-136"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="0b879-137">DLL</span><span class="sxs-lookup"><span data-stu-id="0b879-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b879-138"><dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b879-138"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b879-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0b879-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b879-140">IRTC</span><span class="sxs-lookup"><span data-stu-id="0b879-140">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="0b879-141">IRTC :: Connect</span><span class="sxs-lookup"><span data-stu-id="0b879-141">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="0b879-142">IRTC :: Resume</span><span class="sxs-lookup"><span data-stu-id="0b879-142">IRTC::Resume</span></span>](irtc-resume.md)
</dt> <dt>

[<span data-ttu-id="0b879-143">IRTC :: Start</span><span class="sxs-lookup"><span data-stu-id="0b879-143">IRTC::Start</span></span>](irtc-start.md)
</dt> <dt>

[<span data-ttu-id="0b879-144">IRTC :: Stop</span><span class="sxs-lookup"><span data-stu-id="0b879-144">IRTC::Stop</span></span>](irtc-stop.md)
</dt> </dl>

 

 




