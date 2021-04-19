---
description: Le \_ message CALLDEVSPECIFIC de la ligne TSPI est envoyé à la fonction de rappel LINEEVENT pour notifier à l’interface TAPI les événements spécifiques à l’appareil qui se produisent lors d’un appel.
ms.assetid: accd753a-3be0-4c7d-bbc7-d294d1381144
title: Message LINE_CALLDEVSPECIFIC (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a48bf8a54a1f326fe7bb27c82349e5575c8bbf6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542586"
---
# <a name="line_calldevspecific-message"></a><span data-ttu-id="2575b-103">\_Message CALLDEVSPECIFIC de ligne</span><span class="sxs-lookup"><span data-stu-id="2575b-103">LINE\_CALLDEVSPECIFIC message</span></span>

<span data-ttu-id="2575b-104">Le message **\_ CALLDEVSPECIFIC** de la ligne TSPI est envoyé à la fonction de rappel [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) pour notifier à l’interface TAPI les événements spécifiques à l’appareil qui se produisent lors d’un appel.</span><span class="sxs-lookup"><span data-stu-id="2575b-104">The TSPI **LINE\_CALLDEVSPECIFIC** message is sent to the [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) callback function to notify TAPI about device-specific events occurring on a call.</span></span> <span data-ttu-id="2575b-105">La signification du message et l’interprétation du *dwParam1* via les paramètres *dwParam3* sont spécifiques à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2575b-105">The meaning of the message and the interpretation of the *dwParam1* through *dwParam3* parameters is device specific.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="2575b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2575b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2575b-107">*htLine*</span><span class="sxs-lookup"><span data-stu-id="2575b-107">*htLine*</span></span> 
</dt> <dd>

<span data-ttu-id="2575b-108">Handle de l’objet opaque TAPI sur le périphérique de ligne.</span><span class="sxs-lookup"><span data-stu-id="2575b-108">The TAPI opaque object handle to the line device.</span></span>

</dd> <dt>

<span data-ttu-id="2575b-109">*htCall*</span><span class="sxs-lookup"><span data-stu-id="2575b-109">*htCall*</span></span> 
</dt> <dd>

<span data-ttu-id="2575b-110">Handle de l’objet opaque TAPI vers l’appareil d’appel.</span><span class="sxs-lookup"><span data-stu-id="2575b-110">The TAPI opaque object handle to the call device.</span></span>

</dd> <dt>

<span data-ttu-id="2575b-111">*dwMsg*</span><span class="sxs-lookup"><span data-stu-id="2575b-111">*dwMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="2575b-112">La ligne de valeur \_ CALLDEVSPECIFIC.</span><span class="sxs-lookup"><span data-stu-id="2575b-112">The value LINE\_CALLDEVSPECIFIC.</span></span>

</dd> <dt>

<span data-ttu-id="2575b-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="2575b-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="2575b-114">Spécifique à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2575b-114">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="2575b-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="2575b-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="2575b-116">Spécifique à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2575b-116">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="2575b-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="2575b-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="2575b-118">Spécifique à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2575b-118">Device specific.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2575b-119">Notes</span><span class="sxs-lookup"><span data-stu-id="2575b-119">Remarks</span></span>

<span data-ttu-id="2575b-120">Le message de **ligne \_ CALLDEVSPECIFIC** est utilisé par un fournisseur de services conjointement avec la fonction [**\_ lineDevSpecific TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecific) .</span><span class="sxs-lookup"><span data-stu-id="2575b-120">The **LINE\_CALLDEVSPECIFIC** message is used by a service provider in conjunction with the [**TSPI\_lineDevSpecific**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecific) function.</span></span> <span data-ttu-id="2575b-121">Sa signification est spécifique à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2575b-121">Its meaning is device specific.</span></span>

<span data-ttu-id="2575b-122">L’interface TAPI envoie le message [**\_ DEVSPECIFIC de ligne**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85)) aux applications en réponse à la réception de ce message d’un fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="2575b-122">TAPI sends the [**LINE\_DEVSPECIFIC**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85)) message to applications in response to receiving this message from a service provider.</span></span> <span data-ttu-id="2575b-123">Les paramètres *htLine* et *htCall* sont traduits dans le *hCall* approprié en tant que paramètre *hDevice* au niveau de l’interface TAPI.</span><span class="sxs-lookup"><span data-stu-id="2575b-123">The *htLine* and *htCall* parameters are translated to the appropriate *hCall* as the *hDevice* parameter at the TAPI level.</span></span> <span data-ttu-id="2575b-124">Les paramètres *dwParam1*, *dwParam2* et *dwParam3* sont transmis sans modification.</span><span class="sxs-lookup"><span data-stu-id="2575b-124">The *dwParam1*, *dwParam2*, and *dwParam3* parameters are passed through unmodified.</span></span>

<span data-ttu-id="2575b-125">Il n’y a aucun message directement correspondant au niveau de l’interface TAPI, bien que ce message soit très similaire à la [**ligne \_ DEVSPECIFIC**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2575b-125">There is no directly corresponding message at the TAPI level, although this message is very similar to [**LINE\_DEVSPECIFIC**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85)).</span></span> <span data-ttu-id="2575b-126">Au niveau de TSPI, les messages spécifiques à l’appareil sont répartis entre les événements de rapport sur les lignes et les adresses, et ces événements de rapport sur les appels.</span><span class="sxs-lookup"><span data-stu-id="2575b-126">At the TSPI level, the device-specific messages are split between those reporting events on lines and addresses, and those reporting events on calls.</span></span>

## <a name="requirements"></a><span data-ttu-id="2575b-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2575b-127">Requirements</span></span>



| <span data-ttu-id="2575b-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2575b-128">Requirement</span></span> | <span data-ttu-id="2575b-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="2575b-129">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="2575b-130">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="2575b-130">TAPI version</span></span><br/> | <span data-ttu-id="2575b-131">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="2575b-131">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="2575b-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="2575b-132">Header</span></span><br/>       | <dl> <span data-ttu-id="2575b-133"><dt>TSPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="2575b-133"><dt>Tspi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2575b-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2575b-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="2575b-135">[**DEVSPECIFIC de ligne \_**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2575b-135">[**LINE\_DEVSPECIFIC**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="2575b-136">**LINEEVENT**</span><span class="sxs-lookup"><span data-stu-id="2575b-136">**LINEEVENT**</span></span>](/windows/win32/api/tspi/nc-tspi-lineevent)
</dt> <dt>

[<span data-ttu-id="2575b-137">**TSPI \_ lineDevSpecific**</span><span class="sxs-lookup"><span data-stu-id="2575b-137">**TSPI\_lineDevSpecific**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecific)
</dt> </dl>

 

