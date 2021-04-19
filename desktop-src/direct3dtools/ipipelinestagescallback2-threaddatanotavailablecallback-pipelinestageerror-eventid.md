---
description: Rappel qui avertit l’hôte que ThreadData n’est pas disponible pour une étape et un événement de pipeline particuliers.
MS-HAID: vspixengine.IPipeLineStagesCallback2\_ThreadDataNotAvailableCallback\_PipeLineStageError\_EventID
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPipeLineStagesCallback2 :: ThreadDataNotAvailableCallback, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 231DC830-5F1A-4DDA-B5D0-C7FBCEDCB2A0
api_name:
- IPipeLineStagesCallback2.ThreadDataNotAvailableCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2a0c9cc0bc32b6d01394be1403e961d7ae37a1d9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106516361"
---
# <a name="span-idvspixengineipipelinestagescallback2_threaddatanotavailablecallback_pipelinestageerror_eventidspanipipelinestagescallback2threaddatanotavailablecallback-method"></a><span data-ttu-id="2793c-103"><span id="vspixengine.ipipelinestagescallback2_threaddatanotavailablecallback_pipelinestageerror_eventid"></span>IPipeLineStagesCallback2 :: ThreadDataNotAvailableCallback, méthode</span><span class="sxs-lookup"><span data-stu-id="2793c-103"><span id="vspixengine.ipipelinestagescallback2_threaddatanotavailablecallback_pipelinestageerror_eventid"></span>IPipeLineStagesCallback2::ThreadDataNotAvailableCallback method</span></span>

<span data-ttu-id="2793c-104">Rappel qui avertit l’hôte que ThreadData n’est pas disponible pour une étape et un événement de pipeline particuliers.</span><span class="sxs-lookup"><span data-stu-id="2793c-104">A callback that notifies the host that ThreadData is unavailable for a particular pipeline stage and event.</span></span>

## <a name="syntax"></a><span data-ttu-id="2793c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2793c-105">Syntax</span></span>


```C++
HRESULT ThreadDataNotAvailableCallback(
   PipeLineStageError error,
   EventID            eid
);
```

## <a name="parameters"></a><span data-ttu-id="2793c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2793c-106">Parameters</span></span>

<span data-ttu-id="2793c-107">*Erreurs* </span><span class="sxs-lookup"><span data-stu-id="2793c-107">*error* </span></span>  
<span data-ttu-id="2793c-108">Erreur d’étape de pipeline.</span><span class="sxs-lookup"><span data-stu-id="2793c-108">The pipeline stage error.</span></span>

<span data-ttu-id="2793c-109">*Numéro* </span><span class="sxs-lookup"><span data-stu-id="2793c-109">*eid* </span></span>  
<span data-ttu-id="2793c-110">Événement représenté dans les résultats.</span><span class="sxs-lookup"><span data-stu-id="2793c-110">The event represented in the results.</span></span>

## <a name="return-value"></a><span data-ttu-id="2793c-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2793c-111">Return value</span></span>

<span data-ttu-id="2793c-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="2793c-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2793c-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2793c-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2793c-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2793c-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="2793c-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="2793c-115">Header</span></span></p></td><td><span data-ttu-id="2793c-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="2793c-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="2793c-117"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2793c-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="2793c-118">**IPipeLineStagesCallback2**</span><span class="sxs-lookup"><span data-stu-id="2793c-118">**IPipeLineStagesCallback2**</span></span>](/windows/desktop/direct3dtools/ipipelinestagescallback2)

 

 
