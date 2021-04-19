---
description: La méthode pause arrête temporairement la capture en cours.
ms.assetid: 43176e9e-1502-484c-a8af-4e7bbf5f6474
title: IStats ::P méthode ause (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Pause
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d9e9f04ce3d25399866c711dad7a853f2c43c2ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524744"
---
# <a name="istatspause-method"></a><span data-ttu-id="b4594-103">IStats ::P méthode ause</span><span class="sxs-lookup"><span data-stu-id="b4594-103">IStats::Pause method</span></span>

<span data-ttu-id="b4594-104">La méthode **Pause** arrête temporairement la capture en cours.</span><span class="sxs-lookup"><span data-stu-id="b4594-104">The **Pause** method temporarily stops the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4594-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b4594-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Pause();
```



## <a name="parameters"></a><span data-ttu-id="b4594-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b4594-106">Parameters</span></span>

<span data-ttu-id="b4594-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="b4594-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b4594-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b4594-108">Return value</span></span>

<span data-ttu-id="b4594-109">Si la méthode réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="b4594-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="b4594-110">Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :</span><span class="sxs-lookup"><span data-stu-id="b4594-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="b4594-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="b4594-111">Return code</span></span>                                                                                            | <span data-ttu-id="b4594-112">Description</span><span class="sxs-lookup"><span data-stu-id="b4594-112">Description</span></span>                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b4594-113"><dt>**\_capture NMERR \_ suspendue**</dt></span><span class="sxs-lookup"><span data-stu-id="b4594-113"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl>  | <span data-ttu-id="b4594-114">La capture est déjà suspendue.</span><span class="sxs-lookup"><span data-stu-id="b4594-114">The capture is already paused.</span></span><br/>                                                                                                    |
| <dl> <span data-ttu-id="b4594-115"><dt>**NMERR \_ pas de \_ capture**</dt></span><span class="sxs-lookup"><span data-stu-id="b4594-115"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>   | <span data-ttu-id="b4594-116">Le NPP ne capture pas de données.</span><span class="sxs-lookup"><span data-stu-id="b4594-116">The NPP is not capturing data.</span></span> <span data-ttu-id="b4594-117">Appelez la méthode [IStats :: Start](istats-start.md) pour démarrer la capture.</span><span class="sxs-lookup"><span data-stu-id="b4594-117">Call the [IStats::Start](istats-start.md) method to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="b4594-118"><dt>**NMERR \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="b4594-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>   | <span data-ttu-id="b4594-119">Le NPP n’est pas connecté au réseau.</span><span class="sxs-lookup"><span data-stu-id="b4594-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="b4594-120">Appelez la méthode [IStats :: Connect](istats-connect.md) pour connecter le NPP au réseau.</span><span class="sxs-lookup"><span data-stu-id="b4594-120">Call the [IStats::Connect](istats-connect.md) method to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="b4594-121"><dt>**NMERR \_ non \_ stats \_ uniquement**</dt></span><span class="sxs-lookup"><span data-stu-id="b4594-121"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="b4594-122">Le NPP est connecté au réseau, mais pas avec la méthode [IStats :: Connect](istats-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="b4594-122">The NPP is connected to the network but not with the [IStats::Connect](istats-connect.md) method.</span></span><br/>                                |



 

## <a name="remarks"></a><span data-ttu-id="b4594-123">Notes</span><span class="sxs-lookup"><span data-stu-id="b4594-123">Remarks</span></span>

<span data-ttu-id="b4594-124">Lorsque la capture est suspendue, les nouveaux frames ne sont pas capturés tant qu’un appel à la méthode [IStats :: Resume](istats-resume.md) n’a pas redémarré la capture.</span><span class="sxs-lookup"><span data-stu-id="b4594-124">While the capture is paused, new frames are not captured until a call to the [IStats::Resume](istats-resume.md) method restarts the capture.</span></span>

<span data-ttu-id="b4594-125">Lorsque vous utilisez les méthodes **IStats ::P ause** et **IStats :: Resume** pour contrôler la capture, moniteur réseau continue à ajouter des [*statistiques de conversation*](c.md) chaque fois que la capture est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="b4594-125">When you use the **IStats::Pause** and **IStats::Resume** methods to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) whenever the capture is running.</span></span>

<span data-ttu-id="b4594-126">Pour redémarrer l’appel de capture [IStats :: Resume](istats-resume.md).</span><span class="sxs-lookup"><span data-stu-id="b4594-126">To restart the capture call [IStats::Resume](istats-resume.md).</span></span> <span data-ttu-id="b4594-127">Pour arrêter la capture, appelez [IStats :: Stop](istats-stop.md).</span><span class="sxs-lookup"><span data-stu-id="b4594-127">To stop the capture, call [IStats::Stop](istats-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b4594-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b4594-128">Requirements</span></span>



| <span data-ttu-id="b4594-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b4594-129">Requirement</span></span> | <span data-ttu-id="b4594-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4594-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4594-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4594-131">Minimum supported client</span></span><br/> | <span data-ttu-id="b4594-132">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b4594-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="b4594-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4594-133">Minimum supported server</span></span><br/> | <span data-ttu-id="b4594-134">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b4594-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="b4594-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="b4594-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4594-136"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4594-136"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="b4594-137">DLL</span><span class="sxs-lookup"><span data-stu-id="b4594-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4594-138"><dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4594-138"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4594-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4594-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4594-140">IStats</span><span class="sxs-lookup"><span data-stu-id="b4594-140">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="b4594-141">IStats :: Connect</span><span class="sxs-lookup"><span data-stu-id="b4594-141">IStats::Connect</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="b4594-142">IStats :: Resume</span><span class="sxs-lookup"><span data-stu-id="b4594-142">IStats::Resume</span></span>](istats-resume.md)
</dt> <dt>

[<span data-ttu-id="b4594-143">IStats :: Start</span><span class="sxs-lookup"><span data-stu-id="b4594-143">IStats::Start</span></span>](istats-start.md)
</dt> <dt>

[<span data-ttu-id="b4594-144">IStats :: Stop</span><span class="sxs-lookup"><span data-stu-id="b4594-144">IStats::Stop</span></span>](istats-stop.md)
</dt> </dl>

 

 




