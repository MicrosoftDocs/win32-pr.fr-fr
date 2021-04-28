---
description: 'IRTC :: Resume, méthode-la méthode Resume redémarre une capture suspendue.'
ms.assetid: 685dfdee-3bd0-44b3-ac4f-c9960cf77c5c
title: 'IRTC :: Resume, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Resume
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 55e5cb66eecbee96df9573e9347d1f32e3508d2b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110560"
---
# <a name="irtcresume-method"></a><span data-ttu-id="5798c-103">IRTC :: Resume, méthode</span><span class="sxs-lookup"><span data-stu-id="5798c-103">IRTC::Resume method</span></span>

<span data-ttu-id="5798c-104">La méthode **Resume** redémarre une capture suspendue.</span><span class="sxs-lookup"><span data-stu-id="5798c-104">The **Resume** method restarts a paused capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="5798c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5798c-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a><span data-ttu-id="5798c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5798c-106">Parameters</span></span>

<span data-ttu-id="5798c-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="5798c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5798c-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5798c-108">Return value</span></span>

<span data-ttu-id="5798c-109">Si la méthode réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="5798c-109">If the method is successful the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="5798c-110">Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :</span><span class="sxs-lookup"><span data-stu-id="5798c-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="5798c-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="5798c-111">Return code</span></span>                                                                                                | <span data-ttu-id="5798c-112">Description</span><span class="sxs-lookup"><span data-stu-id="5798c-112">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5798c-113"><dt>**\_capture NMERR \_ non \_ suspendue**</dt></span><span class="sxs-lookup"><span data-stu-id="5798c-113"><dt>**NMERR\_CAPTURE\_NOT\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="5798c-114">La capture n’est pas suspendue.</span><span class="sxs-lookup"><span data-stu-id="5798c-114">The capture is not paused.</span></span> <span data-ttu-id="5798c-115">Appelez [IRTC ::P ause](irtc-pause.md) pour suspendre la capture.</span><span class="sxs-lookup"><span data-stu-id="5798c-115">Call [IRTC::Pause](irtc-pause.md) to pause the capture.</span></span><br/>                                |
| <dl> <span data-ttu-id="5798c-116"><dt>**NMERR \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="5798c-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>       | <span data-ttu-id="5798c-117">Le NPP n’est pas connecté au réseau.</span><span class="sxs-lookup"><span data-stu-id="5798c-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="5798c-118">Appelez [IRTC :: Connect](irtc-connect.md) pour connecter le NPP au réseau.</span><span class="sxs-lookup"><span data-stu-id="5798c-118">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="5798c-119"><dt>**NMERR \_ pas de \_ temps réel**</dt></span><span class="sxs-lookup"><span data-stu-id="5798c-119"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>        | <span data-ttu-id="5798c-120">Le NPP est connecté au réseau, mais pas avec la méthode [IRTC :: Connect](irtc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="5798c-120">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="5798c-121">Notes </span><span class="sxs-lookup"><span data-stu-id="5798c-121">Remarks</span></span>

<span data-ttu-id="5798c-122">Lorsque la capture est dans un état suspendu, les nouvelles données ne sont pas capturées tant qu’un appel à la méthode [IRTC :: Resume](idelaydc-resume.md) n’a pas redémarré la capture.</span><span class="sxs-lookup"><span data-stu-id="5798c-122">While the capture is in a paused state, new data is not captured until a call to the [IRTC::Resume](idelaydc-resume.md) method restarts the capture.</span></span>

<span data-ttu-id="5798c-123">Lorsque vous utilisez les méthodes **Pause** et **Resume** pour contrôler la capture, moniteur réseau continue à ajouter des [*statistiques de conversation*](c.md) aux statistiques existantes pour la capture en cours.</span><span class="sxs-lookup"><span data-stu-id="5798c-123">When using the **Pause** and **Resume** methods to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) to the existing statistics for the current capture.</span></span>

<span data-ttu-id="5798c-124">Pour arrêter la capture, appelez la méthode [IRTC :: Stop](irtc-stop.md) .</span><span class="sxs-lookup"><span data-stu-id="5798c-124">To stop the capture, call the [IRTC::Stop](irtc-stop.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="5798c-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5798c-125">Requirements</span></span>



| <span data-ttu-id="5798c-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5798c-126">Requirement</span></span> | <span data-ttu-id="5798c-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="5798c-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5798c-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5798c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5798c-129">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5798c-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="5798c-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5798c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5798c-131">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5798c-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="5798c-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="5798c-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="5798c-133"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="5798c-133"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="5798c-134">DLL</span><span class="sxs-lookup"><span data-stu-id="5798c-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5798c-135"><dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5798c-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5798c-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5798c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5798c-137">IRTC</span><span class="sxs-lookup"><span data-stu-id="5798c-137">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="5798c-138">IRTC :: Connect</span><span class="sxs-lookup"><span data-stu-id="5798c-138">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="5798c-139">IRTC ::P ause</span><span class="sxs-lookup"><span data-stu-id="5798c-139">IRTC::Pause</span></span>](irtc-pause.md)
</dt> <dt>

[<span data-ttu-id="5798c-140">IRTC :: Stop</span><span class="sxs-lookup"><span data-stu-id="5798c-140">IRTC::Stop</span></span>](irtc-stop.md)
</dt> </dl>

 

 




