---
description: La méthode Resume redémarre une capture suspendue.
ms.assetid: 4fa47220-d323-407b-9dae-704969f66bdd
title: 'IDelaydC :: Resume, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Resume
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: ba0deef666c2e9829cb5a71d91e73da9c1b7d780
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750060"
---
# <a name="idelaydcresume-method"></a><span data-ttu-id="7b9e2-103">IDelaydC :: Resume, méthode</span><span class="sxs-lookup"><span data-stu-id="7b9e2-103">IDelaydC::Resume method</span></span>

<span data-ttu-id="7b9e2-104">La méthode **Resume** redémarre une capture suspendue.</span><span class="sxs-lookup"><span data-stu-id="7b9e2-104">The **Resume** method restarts a paused capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b9e2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7b9e2-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a><span data-ttu-id="7b9e2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7b9e2-106">Parameters</span></span>

<span data-ttu-id="7b9e2-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="7b9e2-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7b9e2-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7b9e2-108">Return value</span></span>

<span data-ttu-id="7b9e2-109">Si la méthode réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="7b9e2-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="7b9e2-110">Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :</span><span class="sxs-lookup"><span data-stu-id="7b9e2-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="7b9e2-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="7b9e2-111">Return code</span></span>                                                                                                | <span data-ttu-id="7b9e2-112">Description</span><span class="sxs-lookup"><span data-stu-id="7b9e2-112">Description</span></span>                                                                                                                               |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7b9e2-113"><dt>**\_capture NMERR \_ non \_ suspendue**</dt></span><span class="sxs-lookup"><span data-stu-id="7b9e2-113"><dt>**NMERR\_CAPTURE\_NOT\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="7b9e2-114">La capture n’est pas suspendue.</span><span class="sxs-lookup"><span data-stu-id="7b9e2-114">The capture is not paused.</span></span> <span data-ttu-id="7b9e2-115">Appelez [**IDelaydC ::P ause**](idelaydc-pause.md) pour suspendre la capture.</span><span class="sxs-lookup"><span data-stu-id="7b9e2-115">Call [**IDelaydC::Pause**](idelaydc-pause.md) to pause the capture.</span></span><br/>                                |
| <dl> <span data-ttu-id="7b9e2-116"><dt>**NMERR \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="7b9e2-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>       | <span data-ttu-id="7b9e2-117">Le NPP n’est pas connecté au réseau.</span><span class="sxs-lookup"><span data-stu-id="7b9e2-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="7b9e2-118">Appelez [**IDelaydC :: Connect**](idelaydc-connect.md) pour connecter le NPP au réseau.</span><span class="sxs-lookup"><span data-stu-id="7b9e2-118">Call [**IDelaydC::Connect**](idelaydc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="7b9e2-119"><dt>**NMERR \_ non \_ retardé**</dt></span><span class="sxs-lookup"><span data-stu-id="7b9e2-119"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>         | <span data-ttu-id="7b9e2-120">Le NPP est connecté au réseau, mais pas avec la méthode [**IDelaydC :: Connect**](idelaydc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="7b9e2-120">The NPP is connected to the network but not with the [**IDelaydC::Connect**](idelaydc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="7b9e2-121">Notes</span><span class="sxs-lookup"><span data-stu-id="7b9e2-121">Remarks</span></span>

<span data-ttu-id="7b9e2-122">Lorsque la capture est suspendue, les nouvelles données ne sont pas ajoutées au [*fichier de capture*](c.md) actuel tant que la méthode **IDelaydC :: Resume** n’est pas appelée pour redémarrer la capture.</span><span class="sxs-lookup"><span data-stu-id="7b9e2-122">While the capture is paused, new data is not added to the current [*capture file*](c.md) until the **IDelaydC::Resume** method is called to restart the capture.</span></span> <span data-ttu-id="7b9e2-123">Lorsque l' [**interruption**](idelaydc-pause.md) et la **reprise** sont utilisées pour arrêter et redémarrer la capture, toutes les informations capturées sont placées dans le même fichier de capture.</span><span class="sxs-lookup"><span data-stu-id="7b9e2-123">When [**Pause**](idelaydc-pause.md) and **Resume** are used to stop and restart the capture, all captured information is put in the same capture file.</span></span>

<span data-ttu-id="7b9e2-124">Lorsque vous utilisez [**suspendre**](idelaydc-pause.md) et **reprendre** pour contrôler la capture, moniteur réseau continue à ajouter des [*statistiques de conversation*](c.md) aux statistiques existantes pour la capture actuelle.</span><span class="sxs-lookup"><span data-stu-id="7b9e2-124">When using [**Pause**](idelaydc-pause.md) and **Resume** to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) to the existing statistics for the current capture.</span></span>

<span data-ttu-id="7b9e2-125">Pour arrêter la capture, appelez [**IDelaydC :: Stop**](idelaydc-stop.md).</span><span class="sxs-lookup"><span data-stu-id="7b9e2-125">To stop the capture, call [**IDelaydC::Stop**](idelaydc-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7b9e2-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7b9e2-126">Requirements</span></span>



| <span data-ttu-id="7b9e2-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7b9e2-127">Requirement</span></span> | <span data-ttu-id="7b9e2-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="7b9e2-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b9e2-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7b9e2-129">Minimum supported client</span></span><br/> | <span data-ttu-id="7b9e2-130">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7b9e2-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="7b9e2-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7b9e2-131">Minimum supported server</span></span><br/> | <span data-ttu-id="7b9e2-132">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7b9e2-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="7b9e2-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="7b9e2-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b9e2-134"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b9e2-134"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="7b9e2-135">DLL</span><span class="sxs-lookup"><span data-stu-id="7b9e2-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b9e2-136"><dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b9e2-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b9e2-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b9e2-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b9e2-138">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="7b9e2-138">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="7b9e2-139">**IDelaydC :: Connect**</span><span class="sxs-lookup"><span data-stu-id="7b9e2-139">**IDelaydC::Connect**</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="7b9e2-140">**IDelaydC ::P ause**</span><span class="sxs-lookup"><span data-stu-id="7b9e2-140">**IDelaydC::Pause**</span></span>](idelaydc-pause.md)
</dt> <dt>

[<span data-ttu-id="7b9e2-141">**IDelaydC :: Stop**</span><span class="sxs-lookup"><span data-stu-id="7b9e2-141">**IDelaydC::Stop**</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




