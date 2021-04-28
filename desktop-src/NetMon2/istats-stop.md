---
description: 'IStats :: Stop, méthode : la méthode Stop arrête la capture en cours.'
ms.assetid: 3aeeb29e-e174-46a2-82bb-44c466b8db98
title: 'IStats :: Stop, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Stop
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: ef51aff870a3193963b3802332112c51f1024826
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114607"
---
# <a name="istatsstop-method"></a><span data-ttu-id="98b73-103">IStats :: Stop, méthode</span><span class="sxs-lookup"><span data-stu-id="98b73-103">IStats::Stop method</span></span>

<span data-ttu-id="98b73-104">La méthode **Stop** arrête la capture en cours.</span><span class="sxs-lookup"><span data-stu-id="98b73-104">The **Stop** method stops the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="98b73-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="98b73-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Stop();
```



## <a name="parameters"></a><span data-ttu-id="98b73-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="98b73-106">Parameters</span></span>

<span data-ttu-id="98b73-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="98b73-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="98b73-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="98b73-108">Return value</span></span>

<span data-ttu-id="98b73-109">Si la méthode réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="98b73-109">If the method is successful the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="98b73-110">Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :</span><span class="sxs-lookup"><span data-stu-id="98b73-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="98b73-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="98b73-111">Return code</span></span>                                                                                            | <span data-ttu-id="98b73-112">Description</span><span class="sxs-lookup"><span data-stu-id="98b73-112">Description</span></span>                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="98b73-113"><dt>**NMERR \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="98b73-113"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>   | <span data-ttu-id="98b73-114">Le NPP n’est pas connecté au réseau.</span><span class="sxs-lookup"><span data-stu-id="98b73-114">The NPP is not connected to the network.</span></span> <span data-ttu-id="98b73-115">Appelez la méthode [IStats :: Connect](istats-connect.md) pour connecter le NPP au réseau.</span><span class="sxs-lookup"><span data-stu-id="98b73-115">Call the [IStats::Connect](istats-connect.md) method to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="98b73-116"><dt>**NMERR \_ pas de \_ capture**</dt></span><span class="sxs-lookup"><span data-stu-id="98b73-116"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>   | <span data-ttu-id="98b73-117">Le NPP ne capture pas de données.</span><span class="sxs-lookup"><span data-stu-id="98b73-117">The NPP is not capturing data.</span></span> <span data-ttu-id="98b73-118">Appelez la méthode [IStats :: Start](istats-start.md) pour démarrer la capture.</span><span class="sxs-lookup"><span data-stu-id="98b73-118">Call the [IStats::Start](istats-start.md) method to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="98b73-119"><dt>**NMERR \_ non \_ stats \_ uniquement**</dt></span><span class="sxs-lookup"><span data-stu-id="98b73-119"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="98b73-120">Le NPP est connecté au réseau, mais pas avec la méthode [IStats :: Connect](istats-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="98b73-120">The NPP is connected to the network but not with the [IStats::Connect](istats-connect.md) method.</span></span><br/>                                |



 

## <a name="remarks"></a><span data-ttu-id="98b73-121">Notes </span><span class="sxs-lookup"><span data-stu-id="98b73-121">Remarks</span></span>

<span data-ttu-id="98b73-122">Lors du redémarrage de la capture après l’appel de **IStats :: Stop** , veillez à appeler la méthode [IStats :: configure](istats-configure.md) chaque fois que vous appelez [IStats :: Start](istats-start.md) pour redémarrer la capture.</span><span class="sxs-lookup"><span data-stu-id="98b73-122">When restarting the capture after **IStats::Stop** has been called, make sure you call the [IStats::Configure](istats-configure.md) method each time you call [IStats::Start](istats-start.md) to restart the capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="98b73-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="98b73-123">Requirements</span></span>



| <span data-ttu-id="98b73-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="98b73-124">Requirement</span></span> | <span data-ttu-id="98b73-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="98b73-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98b73-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="98b73-126">Minimum supported client</span></span><br/> | <span data-ttu-id="98b73-127">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="98b73-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="98b73-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="98b73-128">Minimum supported server</span></span><br/> | <span data-ttu-id="98b73-129">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="98b73-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="98b73-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="98b73-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="98b73-131"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="98b73-131"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="98b73-132">DLL</span><span class="sxs-lookup"><span data-stu-id="98b73-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98b73-133"><dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98b73-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98b73-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98b73-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98b73-135">IStats</span><span class="sxs-lookup"><span data-stu-id="98b73-135">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="98b73-136">IStats :: Connect</span><span class="sxs-lookup"><span data-stu-id="98b73-136">IStats::Connect</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="98b73-137">IStats :: configure</span><span class="sxs-lookup"><span data-stu-id="98b73-137">IStats::Configure</span></span>](istats-configure.md)
</dt> <dt>

[<span data-ttu-id="98b73-138">IStats :: Start</span><span class="sxs-lookup"><span data-stu-id="98b73-138">IStats::Start</span></span>](istats-start.md)
</dt> </dl>

 

 




