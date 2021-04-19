---
description: La méthode Resume redémarre une capture suspendue.
ms.assetid: 047ea5f8-de3d-40db-ada3-fc0ef4deccef
title: 'IESP :: Resume, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Resume
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 01bbb748fc91bcc5a78b281ec9ebdd2a6d479888
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536109"
---
# <a name="iespresume-method"></a><span data-ttu-id="44263-103">IESP :: Resume, méthode</span><span class="sxs-lookup"><span data-stu-id="44263-103">IESP::Resume method</span></span>

<span data-ttu-id="44263-104">La méthode **Resume** redémarre une capture suspendue.</span><span class="sxs-lookup"><span data-stu-id="44263-104">The **Resume** method restarts a paused capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="44263-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="44263-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a><span data-ttu-id="44263-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="44263-106">Parameters</span></span>

<span data-ttu-id="44263-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="44263-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="44263-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="44263-108">Return value</span></span>

<span data-ttu-id="44263-109">Si la méthode réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="44263-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="44263-110">Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :</span><span class="sxs-lookup"><span data-stu-id="44263-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="44263-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="44263-111">Return code</span></span>                                                                                                | <span data-ttu-id="44263-112">Description</span><span class="sxs-lookup"><span data-stu-id="44263-112">Description</span></span>                                                                                                               |
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="44263-113"><dt>**\_capture NMERR \_ non \_ suspendue**</dt></span><span class="sxs-lookup"><span data-stu-id="44263-113"><dt>**NMERR\_CAPTURE\_NOT\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="44263-114">La capture n’est pas suspendue.</span><span class="sxs-lookup"><span data-stu-id="44263-114">The capture is not paused.</span></span> <span data-ttu-id="44263-115">Appelez [**IESP ::P ause**](iesp-pause.md) pour suspendre la capture.</span><span class="sxs-lookup"><span data-stu-id="44263-115">Call [**IESP::Pause**](iesp-pause.md) to pause the capture.</span></span><br/>                        |
| <dl> <span data-ttu-id="44263-116"><dt>**NMERR \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="44263-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>       | <span data-ttu-id="44263-117">Le NPP n’est pas connecté au réseau.</span><span class="sxs-lookup"><span data-stu-id="44263-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="44263-118">Appelez [**IESP :: Connect**](iesp-connect.md) pour vous connecter au réseau.</span><span class="sxs-lookup"><span data-stu-id="44263-118">Call [**IESP::Connect**](iesp-connect.md) to connect to the network.</span></span><br/> |
| <dl> <span data-ttu-id="44263-119"><dt>**NMERR \_ non \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="44263-119"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>             | <span data-ttu-id="44263-120">Le NPP est connecté au réseau, mais pas avec la méthode [**IESP :: Connect**](iesp-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="44263-120">The NPP is connected to the network, but not with the [**IESP::Connect**](iesp-connect.md) method.</span></span><br/>            |



 

## <a name="remarks"></a><span data-ttu-id="44263-121">Notes</span><span class="sxs-lookup"><span data-stu-id="44263-121">Remarks</span></span>

<span data-ttu-id="44263-122">Lorsque la capture est dans un état suspendu, les nouvelles données ne sont pas ajoutées au [*fichier de capture*](c.md) actuel tant que **IESP :: Resume** n’est pas appelé pour redémarrer la capture.</span><span class="sxs-lookup"><span data-stu-id="44263-122">While the capture is in a paused state, new data is not added to the current [*capture file*](c.md) until **IESP::Resume** is called to restart the capture.</span></span> <span data-ttu-id="44263-123">Lorsque l' **interruption** et la **reprise** sont utilisées pour arrêter et redémarrer la capture, toutes les informations capturées sont placées dans le même fichier de capture.</span><span class="sxs-lookup"><span data-stu-id="44263-123">When **Pause** and **Resume** are used to stop and restart the capture, all captured information is put in the same capture file.</span></span>

<span data-ttu-id="44263-124">Lorsque vous utilisez **suspendre** et **reprendre** pour contrôler la capture, moniteur réseau continue à ajouter des [*statistiques de conversation*](c.md) aux statistiques existantes pour la capture actuelle.</span><span class="sxs-lookup"><span data-stu-id="44263-124">When using **Pause** and **Resume** to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) to the existing statistics for the current capture.</span></span>

<span data-ttu-id="44263-125">Pour arrêter la capture, appelez [**IESP :: Stop**](iesp-stop.md).</span><span class="sxs-lookup"><span data-stu-id="44263-125">To stop the capture, call [**IESP::Stop**](iesp-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="44263-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="44263-126">Requirements</span></span>



| <span data-ttu-id="44263-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="44263-127">Requirement</span></span> | <span data-ttu-id="44263-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="44263-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44263-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="44263-129">Minimum supported client</span></span><br/> | <span data-ttu-id="44263-130">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="44263-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="44263-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="44263-131">Minimum supported server</span></span><br/> | <span data-ttu-id="44263-132">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="44263-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="44263-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="44263-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="44263-134"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="44263-134"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="44263-135">DLL</span><span class="sxs-lookup"><span data-stu-id="44263-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44263-136"><dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44263-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44263-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="44263-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44263-138">IESP</span><span class="sxs-lookup"><span data-stu-id="44263-138">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="44263-139">**IESP :: Connect**</span><span class="sxs-lookup"><span data-stu-id="44263-139">**IESP::Connect**</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="44263-140">**IESP ::P ause**</span><span class="sxs-lookup"><span data-stu-id="44263-140">**IESP::Pause**</span></span>](iesp-pause.md)
</dt> <dt>

[<span data-ttu-id="44263-141">**IESP :: Stop**</span><span class="sxs-lookup"><span data-stu-id="44263-141">**IESP::Stop**</span></span>](iesp-stop.md)
</dt> </dl>

 

 




