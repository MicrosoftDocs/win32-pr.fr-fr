---
description: 'IDelaydC :: QueryStatus, méthode-la méthode QueryStatus récupère l’état du NPP.'
ms.assetid: b035d495-a078-4436-9501-0a30fbfa7268
title: 'IDelaydC :: QueryStatus, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.QueryStatus
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 13d1e34b57302d263b81ed64df0b136dc01177b2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118457"
---
# <a name="idelaydcquerystatus-method"></a><span data-ttu-id="d4c4c-103">IDelaydC :: QueryStatus, méthode</span><span class="sxs-lookup"><span data-stu-id="d4c4c-103">IDelaydC::QueryStatus method</span></span>

<span data-ttu-id="d4c4c-104">La méthode **QueryStatus** récupère l’état du NPP.</span><span class="sxs-lookup"><span data-stu-id="d4c4c-104">The **QueryStatus** method retrieves the status of the NPP.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4c4c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d4c4c-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE QueryStatus(
  [out] NETWORKSTATUS *pNetworkStatus
);
```



## <a name="parameters"></a><span data-ttu-id="d4c4c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d4c4c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4c4c-107">*pNetworkStatus* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d4c4c-107">*pNetworkStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d4c4c-108">Pointeur vers une structure [NETWORKSTATUS](networkstatus.md) retournée qui indique l’état actuel (capture, pause, arrêtée, etc.) du NPP.</span><span class="sxs-lookup"><span data-stu-id="d4c4c-108">Pointer to a returned [NETWORKSTATUS](networkstatus.md) structure that indicates the current state (capturing, paused, stopped, and so on) of the NPP.</span></span> <span data-ttu-id="d4c4c-109">Il vous incombe d’allouer et de libérer la mémoire associée à la structure **NETWORKSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="d4c4c-109">It is your responsibility to allocate and free the memory associated with the **NETWORKSTATUS** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4c4c-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d4c4c-110">Return value</span></span>

<span data-ttu-id="d4c4c-111">Si la méthode réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="d4c4c-111">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="d4c4c-112">Si la méthode échoue, la valeur de retour est le code d’erreur suivant :</span><span class="sxs-lookup"><span data-stu-id="d4c4c-112">If the method is unsuccessful, the return value is the following error code:</span></span>



| <span data-ttu-id="d4c4c-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="d4c4c-113">Return code</span></span>                                                                                              | <span data-ttu-id="d4c4c-114">Description</span><span class="sxs-lookup"><span data-stu-id="d4c4c-114">Description</span></span>                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d4c4c-115"><dt>**\_paramètre NMERR non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d4c4c-115"><dt>**NMERR\_INVALID\_PARAMETER**</dt></span></span> </dl> | <span data-ttu-id="d4c4c-116">Le paramètre *pNetworkStatus* ne pointe pas vers une structure [NETWORKSTATUS](networkstatus.md) valide.</span><span class="sxs-lookup"><span data-stu-id="d4c4c-116">The *pNetworkStatus* parameter is not pointing to a valid [NETWORKSTATUS](networkstatus.md) structure.</span></span> <span data-ttu-id="d4c4c-117">Allouez de la mémoire pour cette structure et rappelez la méthode **IDelaydC :: QueryStatus** .</span><span class="sxs-lookup"><span data-stu-id="d4c4c-117">Allocate memory for this structure and call the **IDelaydC::QueryStatus** method again.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d4c4c-118">Notes </span><span class="sxs-lookup"><span data-stu-id="d4c4c-118">Remarks</span></span>

<span data-ttu-id="d4c4c-119">Cette méthode peut être appelée à tout moment après l’appel de [CreateNPPInterface](createnppinterface.md) .</span><span class="sxs-lookup"><span data-stu-id="d4c4c-119">This method can be called at any time after [CreateNPPInterface](createnppinterface.md) is called.</span></span> <span data-ttu-id="d4c4c-120">Il peut être appelé pour déterminer si le NPP est connecté au réseau, pour déterminer l’état de la capture en cours et pour déterminer si des déclencheurs sont en attente.</span><span class="sxs-lookup"><span data-stu-id="d4c4c-120">It can be called to see if the NPP is connected to the network, to find out the status of the current capture, and to see if any triggers are pending.</span></span>

<span data-ttu-id="d4c4c-121">Avant d’appeler cette méthode, vous devez allouer la mémoire nécessaire à la structure [NETWORKSTATUS](networkstatus.md) et libérer cette mémoire lorsque la structure n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="d4c4c-121">Before calling this method, you must allocate the memory needed for the [NETWORKSTATUS](networkstatus.md) structure and free that memory when the structure is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4c4c-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d4c4c-122">Requirements</span></span>



| <span data-ttu-id="d4c4c-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d4c4c-123">Requirement</span></span> | <span data-ttu-id="d4c4c-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4c4c-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4c4c-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d4c4c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d4c4c-126">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d4c4c-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="d4c4c-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d4c4c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d4c4c-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d4c4c-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="d4c4c-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="d4c4c-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4c4c-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4c4c-130"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="d4c4c-131">DLL</span><span class="sxs-lookup"><span data-stu-id="d4c4c-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4c4c-132"><dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4c4c-132"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4c4c-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d4c4c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4c4c-134">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="d4c4c-134">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="d4c4c-135">CreateNPPInterface</span><span class="sxs-lookup"><span data-stu-id="d4c4c-135">CreateNPPInterface</span></span>](createnppinterface.md)
</dt> <dt>

[<span data-ttu-id="d4c4c-136">NETWORKSTATUS</span><span class="sxs-lookup"><span data-stu-id="d4c4c-136">NETWORKSTATUS</span></span>](networkstatus.md)
</dt> </dl>

 

 




