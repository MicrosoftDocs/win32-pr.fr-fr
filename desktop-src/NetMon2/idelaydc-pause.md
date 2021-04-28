---
description: IDelaydC ::P méthode ause-la méthode pause interrompt la capture en cours.
ms.assetid: 9d5e11d1-8c45-4cf5-9fea-10c9e7a6fe86
title: IDelaydC ::P méthode ause (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Pause
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 21b4cd7b6cb921f7bd71b8670a37da12b2239b92
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098497"
---
# <a name="idelaydcpause-method"></a><span data-ttu-id="a7f46-103">IDelaydC ::P méthode ause</span><span class="sxs-lookup"><span data-stu-id="a7f46-103">IDelaydC::Pause method</span></span>

<span data-ttu-id="a7f46-104">La méthode **Pause** interrompt la capture en cours.</span><span class="sxs-lookup"><span data-stu-id="a7f46-104">The **Pause** method pauses the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7f46-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a7f46-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Pause();
```



## <a name="parameters"></a><span data-ttu-id="a7f46-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a7f46-106">Parameters</span></span>

<span data-ttu-id="a7f46-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="a7f46-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a7f46-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a7f46-108">Return value</span></span>

<span data-ttu-id="a7f46-109">Si la méthode réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="a7f46-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="a7f46-110">Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :</span><span class="sxs-lookup"><span data-stu-id="a7f46-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="a7f46-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="a7f46-111">Return code</span></span>                                                                                           | <span data-ttu-id="a7f46-112">Description</span><span class="sxs-lookup"><span data-stu-id="a7f46-112">Description</span></span>                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a7f46-113"><dt>**\_capture NMERR \_ suspendue**</dt></span><span class="sxs-lookup"><span data-stu-id="a7f46-113"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="a7f46-114">La capture est déjà dans un état suspendu.</span><span class="sxs-lookup"><span data-stu-id="a7f46-114">The capture is already in a paused state.</span></span><br/>                                                                                  |
| <dl> <span data-ttu-id="a7f46-115"><dt>**NMERR \_ pas de \_ capture**</dt></span><span class="sxs-lookup"><span data-stu-id="a7f46-115"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>  | <span data-ttu-id="a7f46-116">Le NPP ne capture pas de données.</span><span class="sxs-lookup"><span data-stu-id="a7f46-116">The NPP is not capturing data.</span></span> <span data-ttu-id="a7f46-117">Appelez [IDelaydC :: Start](idelaydc-start.md) pour démarrer la capture.</span><span class="sxs-lookup"><span data-stu-id="a7f46-117">Call [IDelaydC::Start](idelaydc-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="a7f46-118"><dt>**NMERR \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="a7f46-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="a7f46-119">Le NPP n’est pas connecté au réseau.</span><span class="sxs-lookup"><span data-stu-id="a7f46-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="a7f46-120">Appelez [IDelaydC :: Connect](idelaydc-connect.md) pour connecter le NPP au réseau.</span><span class="sxs-lookup"><span data-stu-id="a7f46-120">Call [IDelaydC::Connect](idelaydc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="a7f46-121"><dt>**NMERR \_ non \_ retardé**</dt></span><span class="sxs-lookup"><span data-stu-id="a7f46-121"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>    | <span data-ttu-id="a7f46-122">Le NPP est connecté au réseau, mais pas avec la méthode [IDelaydC :: Connect](idelaydc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="a7f46-122">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="a7f46-123">Notes </span><span class="sxs-lookup"><span data-stu-id="a7f46-123">Remarks</span></span>

<span data-ttu-id="a7f46-124">Lorsque la capture est dans un état suspendu, les nouvelles données ne sont pas ajoutées au [*fichier de capture*](c.md) actuel tant que la méthode **IDelaydC :: Resume** n’est pas appelée pour redémarrer la capture.</span><span class="sxs-lookup"><span data-stu-id="a7f46-124">While the capture is in a paused state, new data is not added to the current [*capture file*](c.md) until the **IDelaydC::Resume** method is called to restart the capture.</span></span> <span data-ttu-id="a7f46-125">Lorsque l' **interruption** et la **reprise** sont utilisées pour arrêter et redémarrer la capture, toutes les informations capturées sont placées dans le même fichier de capture.</span><span class="sxs-lookup"><span data-stu-id="a7f46-125">When **Pause** and **Resume** are used to stop and restart the capture, all captured information is put in the same capture file.</span></span>

<span data-ttu-id="a7f46-126">Quand vous utilisez **IDelaydC ::P ause** et **IDelaydC :: Resume** pour contrôler la capture, moniteur réseau continue à ajouter des [*statistiques de conversation*](c.md) chaque fois que la capture est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="a7f46-126">When using **IDelaydC::Pause** and **IDelaydC::Resume** to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) whenever the capture is running.</span></span>

<span data-ttu-id="a7f46-127">Pour redémarrer la capture, appelez [IDelaydC :: Resume](idelaydc-resume.md).</span><span class="sxs-lookup"><span data-stu-id="a7f46-127">To restart the capture, call [IDelaydC::Resume](idelaydc-resume.md).</span></span>

<span data-ttu-id="a7f46-128">Pour arrêter la capture, appelez [IDelaydC :: Stop](idelaydc-stop.md).</span><span class="sxs-lookup"><span data-stu-id="a7f46-128">To stop the capture, call [IDelaydC::Stop](idelaydc-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a7f46-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a7f46-129">Requirements</span></span>



| <span data-ttu-id="a7f46-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a7f46-130">Requirement</span></span> | <span data-ttu-id="a7f46-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="a7f46-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7f46-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a7f46-132">Minimum supported client</span></span><br/> | <span data-ttu-id="a7f46-133">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a7f46-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="a7f46-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a7f46-134">Minimum supported server</span></span><br/> | <span data-ttu-id="a7f46-135">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a7f46-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="a7f46-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="a7f46-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7f46-137"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7f46-137"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="a7f46-138">DLL</span><span class="sxs-lookup"><span data-stu-id="a7f46-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7f46-139"><dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7f46-139"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7f46-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a7f46-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7f46-141">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="a7f46-141">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="a7f46-142">IDelaydC :: Connect</span><span class="sxs-lookup"><span data-stu-id="a7f46-142">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="a7f46-143">IDelaydC :: Resume</span><span class="sxs-lookup"><span data-stu-id="a7f46-143">IDelaydC::Resume</span></span>](idelaydc-resume.md)
</dt> <dt>

[<span data-ttu-id="a7f46-144">IDelaydC :: Start</span><span class="sxs-lookup"><span data-stu-id="a7f46-144">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="a7f46-145">IDelaydC :: Stop</span><span class="sxs-lookup"><span data-stu-id="a7f46-145">IDelaydC::Stop</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




