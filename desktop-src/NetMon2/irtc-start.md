---
description: La méthode start démarre la capture.
ms.assetid: 1f676e19-18ff-4c34-a83f-2723ff356be2
title: 'IRTC :: Start, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Start
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 3ee30112baf7813c983230fb90cd15ea7f52e2bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864065"
---
# <a name="irtcstart-method"></a><span data-ttu-id="5a857-103">IRTC :: Start, méthode</span><span class="sxs-lookup"><span data-stu-id="5a857-103">IRTC::Start method</span></span>

<span data-ttu-id="5a857-104">La méthode **Start** démarre la capture.</span><span class="sxs-lookup"><span data-stu-id="5a857-104">The **Start** method starts the capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a857-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5a857-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Start();
```



## <a name="parameters"></a><span data-ttu-id="5a857-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5a857-106">Parameters</span></span>

<span data-ttu-id="5a857-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="5a857-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5a857-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5a857-108">Return value</span></span>

<span data-ttu-id="5a857-109">Si la méthode réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="5a857-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="5a857-110">Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :</span><span class="sxs-lookup"><span data-stu-id="5a857-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="5a857-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="5a857-111">Return code</span></span>                                                                                           | <span data-ttu-id="5a857-112">Description</span><span class="sxs-lookup"><span data-stu-id="5a857-112">Description</span></span>                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5a857-113"><dt>**\_capture NMERR \_ suspendue**</dt></span><span class="sxs-lookup"><span data-stu-id="5a857-113"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="5a857-114">La capture est dans un état suspendu et doit être arrêtée avant de pouvoir être redémarrée.</span><span class="sxs-lookup"><span data-stu-id="5a857-114">The capture is in a paused state and must be stopped before it can be restarted.</span></span> <span data-ttu-id="5a857-115">Appelez [IRTC :: Stop](idelaydc-stop.md) pour arrêter la capture.</span><span class="sxs-lookup"><span data-stu-id="5a857-115">Call [IRTC::Stop](idelaydc-stop.md) to stop the capture.</span></span><br/> |
| <dl> <span data-ttu-id="5a857-116"><dt>**\_capture NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="5a857-116"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>       | <span data-ttu-id="5a857-117">La capture a déjà démarré.</span><span class="sxs-lookup"><span data-stu-id="5a857-117">The capture is already started.</span></span><br/>                                                                                                            |
| <dl> <span data-ttu-id="5a857-118"><dt>**NMERR \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="5a857-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="5a857-119">Le NPP n’est pas connecté au réseau.</span><span class="sxs-lookup"><span data-stu-id="5a857-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="5a857-120">Appelez [IRTC :: Connect](irtc-connect.md) pour connecter le NPP au réseau.</span><span class="sxs-lookup"><span data-stu-id="5a857-120">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/>                         |
| <dl> <span data-ttu-id="5a857-121"><dt>**NMERR \_ pas de \_ temps réel**</dt></span><span class="sxs-lookup"><span data-stu-id="5a857-121"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>   | <span data-ttu-id="5a857-122">Le NPP est connecté au réseau, mais pas avec la méthode [IRTC :: Connect](irtc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="5a857-122">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="5a857-123">Notes</span><span class="sxs-lookup"><span data-stu-id="5a857-123">Remarks</span></span>

<span data-ttu-id="5a857-124">Lorsque vous redémarrez la capture à l’aide des méthodes IRTC :: Start et [IRTC :: Stop](irtc-stop.md) , vous devez appeler la méthode [IRTC :: configure](irtc-configure.md) pour reconfigurer la connexion chaque fois que vous appelez IRTC :: Start pour redémarrer la capture de données.</span><span class="sxs-lookup"><span data-stu-id="5a857-124">When you restart the capture by using the IRTC::Start and [IRTC::Stop](irtc-stop.md) methods, you must call the [IRTC::Configure](irtc-configure.md) method to reconfigure the connection each time you call IRTC::Start to restart the data capture.</span></span>

> [!Note]  
> <span data-ttu-id="5a857-125">Vous pouvez également démarrer et arrêter la capture à l’aide des méthodes [IRTC ::P ause](irtc-pause.md) et [IRTC :: Resume](irtc-resume.md) .</span><span class="sxs-lookup"><span data-stu-id="5a857-125">You can also start and stop the capture by using the [IRTC::Pause](irtc-pause.md) and [IRTC::Resume](irtc-resume.md) methods.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5a857-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5a857-126">Requirements</span></span>



| <span data-ttu-id="5a857-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5a857-127">Requirement</span></span> | <span data-ttu-id="5a857-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="5a857-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a857-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a857-129">Minimum supported client</span></span><br/> | <span data-ttu-id="5a857-130">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5a857-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="5a857-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a857-131">Minimum supported server</span></span><br/> | <span data-ttu-id="5a857-132">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5a857-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="5a857-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="5a857-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a857-134"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a857-134"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="5a857-135">DLL</span><span class="sxs-lookup"><span data-stu-id="5a857-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a857-136"><dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a857-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a857-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5a857-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a857-138">IRTC</span><span class="sxs-lookup"><span data-stu-id="5a857-138">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="5a857-139">IRTC :: configure</span><span class="sxs-lookup"><span data-stu-id="5a857-139">IRTC::Configure</span></span>](irtc-configure.md)
</dt> <dt>

[<span data-ttu-id="5a857-140">IRTC :: Connect</span><span class="sxs-lookup"><span data-stu-id="5a857-140">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="5a857-141">IRTC ::P ause</span><span class="sxs-lookup"><span data-stu-id="5a857-141">IRTC::Pause</span></span>](irtc-pause.md)
</dt> <dt>

[<span data-ttu-id="5a857-142">IRTC :: Resume</span><span class="sxs-lookup"><span data-stu-id="5a857-142">IRTC::Resume</span></span>](irtc-resume.md)
</dt> <dt>

[<span data-ttu-id="5a857-143">IRTC :: Stop</span><span class="sxs-lookup"><span data-stu-id="5a857-143">IRTC::Stop</span></span>](irtc-stop.md)
</dt> </dl>

 

 




