---
title: Message MOM_POSITIONCB (mmsystem. h)
description: Le \_ message de position MOM est envoyé lorsqu’un \_ \_ événement de rappel MEVT F est atteint dans le flux de sortie MIDI.
ms.assetid: 0464d74d-7d1f-4aab-a9e7-03397872f3c0
keywords:
- Message MOM_POSITIONCB Windows Multimedia
topic_type:
- apiref
api_name:
- MOM_POSITIONCB
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e5c9528e8f91778c53ed4761c98bb67d405ec14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743356"
---
# <a name="mom_positioncb-message"></a><span data-ttu-id="2e7bb-104">\_Message MOM POSITIONCB</span><span class="sxs-lookup"><span data-stu-id="2e7bb-104">MOM\_POSITIONCB message</span></span>

<span data-ttu-id="2e7bb-105">Le message de **\_ position MOM** est envoyé lorsqu’un événement de **\_ \_ rappel MEVT F** est atteint dans le flux de sortie MIDI.</span><span class="sxs-lookup"><span data-stu-id="2e7bb-105">The **MOM\_POSITION** message is sent when an **MEVT\_F\_CALLBACK** event is reached in the MIDI output stream.</span></span>

## <a name="parameters"></a><span data-ttu-id="2e7bb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2e7bb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e7bb-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="2e7bb-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="2e7bb-108">Pointeur vers une structure [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) identifiant la mémoire tampon d’entrée.</span><span class="sxs-lookup"><span data-stu-id="2e7bb-108">A pointer to a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure identifying the input buffer.</span></span>

</dd> <dt>

<span data-ttu-id="2e7bb-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="2e7bb-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="2e7bb-110">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="2e7bb-110">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e7bb-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2e7bb-111">Return Value</span></span>

<span data-ttu-id="2e7bb-112">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="2e7bb-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e7bb-113">Notes</span><span class="sxs-lookup"><span data-stu-id="2e7bb-113">Remarks</span></span>

<span data-ttu-id="2e7bb-114">La lecture de la mémoire tampon de flux continue même pendant l’exécution de la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="2e7bb-114">Playback of the stream buffer continues even while the callback function is executing.</span></span> <span data-ttu-id="2e7bb-115">Les événements qui se trouvent après l’événement de **\_ \_ rappel MEVT F** dans la mémoire tampon sont planifiés et envoyés à temps, quel que soit le temps passé dans la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="2e7bb-115">Any events after the **MEVT\_F\_CALLBACK** event in the buffer will be scheduled and sent on time regardless of how much time is spent in the callback function.</span></span>

<span data-ttu-id="2e7bb-116">Si les rappels de position sont générés plus rapidement que votre application ne peut les traiter, le membre **dwOffset** de la structure [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) peut faire référence à un événement que votre application n’a pas encore traitée.</span><span class="sxs-lookup"><span data-stu-id="2e7bb-116">If position callbacks are being generated more quickly than your application can process them, the **dwOffset** member of the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure might refer to an event your application has not yet processed.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e7bb-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2e7bb-117">Requirements</span></span>



| <span data-ttu-id="2e7bb-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2e7bb-118">Requirement</span></span> | <span data-ttu-id="2e7bb-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="2e7bb-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e7bb-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e7bb-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2e7bb-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2e7bb-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="2e7bb-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e7bb-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2e7bb-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2e7bb-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="2e7bb-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="2e7bb-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e7bb-125"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2e7bb-125"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e7bb-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2e7bb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e7bb-127">Messages MIDI</span><span class="sxs-lookup"><span data-stu-id="2e7bb-127">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

