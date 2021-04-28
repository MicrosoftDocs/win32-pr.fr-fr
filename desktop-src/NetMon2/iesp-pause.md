---
description: IESP ::P méthode ause-la méthode pause interrompt la capture en cours.
ms.assetid: efbc8947-b9fe-4dbd-8097-375b5f99845e
title: IESP ::P méthode ause (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Pause
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 486c7aedc7092e0dd0f9f68cc1ea2ccad08d9438
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084237"
---
# <a name="iesppause-method"></a><span data-ttu-id="0aa7f-103">IESP ::P méthode ause</span><span class="sxs-lookup"><span data-stu-id="0aa7f-103">IESP::Pause method</span></span>

<span data-ttu-id="0aa7f-104">La méthode **Pause** interrompt la capture en cours.</span><span class="sxs-lookup"><span data-stu-id="0aa7f-104">The **Pause** method pauses the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="0aa7f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0aa7f-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Pause(
   LPSTATISTICS lpStats
);
```



## <a name="parameters"></a><span data-ttu-id="0aa7f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0aa7f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0aa7f-107">*lpStats*</span><span class="sxs-lookup"><span data-stu-id="0aa7f-107">*lpStats*</span></span> 
</dt> <dd>

<span data-ttu-id="0aa7f-108">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="0aa7f-108">Obsolete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0aa7f-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0aa7f-109">Return value</span></span>

<span data-ttu-id="0aa7f-110">Si la méthode réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="0aa7f-110">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="0aa7f-111">Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :</span><span class="sxs-lookup"><span data-stu-id="0aa7f-111">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="0aa7f-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="0aa7f-112">Return code</span></span>                                                                                           | <span data-ttu-id="0aa7f-113">Description</span><span class="sxs-lookup"><span data-stu-id="0aa7f-113">Description</span></span>                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0aa7f-114"><dt>**\_capture NMERR \_ suspendue**</dt></span><span class="sxs-lookup"><span data-stu-id="0aa7f-114"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="0aa7f-115">La capture est déjà suspendue.</span><span class="sxs-lookup"><span data-stu-id="0aa7f-115">The capture is already paused.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="0aa7f-116"><dt>**NMERR \_ pas de \_ capture**</dt></span><span class="sxs-lookup"><span data-stu-id="0aa7f-116"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>  | <span data-ttu-id="0aa7f-117">Le NPP ne capture pas de données.</span><span class="sxs-lookup"><span data-stu-id="0aa7f-117">The NPP is not capturing data.</span></span> <span data-ttu-id="0aa7f-118">Appelez [IESP :: Start](iesp-start.md) pour démarrer la capture.</span><span class="sxs-lookup"><span data-stu-id="0aa7f-118">Call [IESP::Start](iesp-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="0aa7f-119"><dt>**NMERR \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="0aa7f-119"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="0aa7f-120">Le NPP n’est pas connecté au réseau.</span><span class="sxs-lookup"><span data-stu-id="0aa7f-120">The NPP is not connected to the network.</span></span> <span data-ttu-id="0aa7f-121">Appelez [IESP :: Connect](iesp-connect.md) pour connecter le NPP au réseau.</span><span class="sxs-lookup"><span data-stu-id="0aa7f-121">Call [IESP::Connect](iesp-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="0aa7f-122"><dt>**NMERR \_ non \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="0aa7f-122"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>        | <span data-ttu-id="0aa7f-123">Le NPP est connecté au réseau, mais pas avec la méthode [IESP :: Connect](iesp-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="0aa7f-123">The NPP is connected to the network but not with the [IESP::Connect](iesp-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="0aa7f-124">Notes </span><span class="sxs-lookup"><span data-stu-id="0aa7f-124">Remarks</span></span>

<span data-ttu-id="0aa7f-125">Lorsque la capture est dans un état suspendu, les nouvelles données ne sont pas ajoutées au [*fichier de capture*](c.md) actuel tant que vous n’avez pas appelé la méthode [IESP :: Resume](iesp-resume.md) pour redémarrer la capture.</span><span class="sxs-lookup"><span data-stu-id="0aa7f-125">While the capture is in a paused state, new data is not added to the current [*capture file*](c.md) until you call the [IESP::Resume](iesp-resume.md) method to restart the capture.</span></span> <span data-ttu-id="0aa7f-126">Lorsque l' **interruption** et la **reprise** sont utilisées pour arrêter et redémarrer la capture, toutes les informations capturées sont placées dans le même fichier de capture.</span><span class="sxs-lookup"><span data-stu-id="0aa7f-126">When **Pause** and **Resume** are used to stop and restart the capture, all captured information is put in the same capture file.</span></span>

<span data-ttu-id="0aa7f-127">Lorsque vous utilisez les méthodes **IESP ::P ause** et **IESP :: Resume** pour contrôler la capture, moniteur réseau continue à ajouter des [*statistiques de conversation*](c.md) chaque fois que la capture est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="0aa7f-127">When you use the **IESP::Pause** and **IESP::Resume** methods to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) whenever the capture is running.</span></span>

<span data-ttu-id="0aa7f-128">Pour redémarrer la capture, appelez [IESP :: Resume](iesp-resume.md).</span><span class="sxs-lookup"><span data-stu-id="0aa7f-128">To restart the capture, call [IESP::Resume](iesp-resume.md).</span></span> <span data-ttu-id="0aa7f-129">Pour arrêter la capture, appelez [IESP :: Stop](iesp-stop.md).</span><span class="sxs-lookup"><span data-stu-id="0aa7f-129">To stop the capture, call [IESP::Stop](iesp-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0aa7f-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0aa7f-130">Requirements</span></span>



| <span data-ttu-id="0aa7f-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0aa7f-131">Requirement</span></span> | <span data-ttu-id="0aa7f-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="0aa7f-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0aa7f-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0aa7f-133">Minimum supported client</span></span><br/> | <span data-ttu-id="0aa7f-134">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0aa7f-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="0aa7f-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0aa7f-135">Minimum supported server</span></span><br/> | <span data-ttu-id="0aa7f-136">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0aa7f-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="0aa7f-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="0aa7f-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="0aa7f-138"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="0aa7f-138"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="0aa7f-139">DLL</span><span class="sxs-lookup"><span data-stu-id="0aa7f-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0aa7f-140"><dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0aa7f-140"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0aa7f-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0aa7f-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0aa7f-142">IESP</span><span class="sxs-lookup"><span data-stu-id="0aa7f-142">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="0aa7f-143">IESP :: Connect</span><span class="sxs-lookup"><span data-stu-id="0aa7f-143">IESP::Connect</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="0aa7f-144">IESP :: Resume</span><span class="sxs-lookup"><span data-stu-id="0aa7f-144">IESP::Resume</span></span>](iesp-resume.md)
</dt> <dt>

[<span data-ttu-id="0aa7f-145">IESP :: Start</span><span class="sxs-lookup"><span data-stu-id="0aa7f-145">IESP::Start</span></span>](iesp-start.md)
</dt> <dt>

[<span data-ttu-id="0aa7f-146">IESP :: Stop</span><span class="sxs-lookup"><span data-stu-id="0aa7f-146">IESP::Stop</span></span>](iesp-stop.md)
</dt> </dl>

 

 




