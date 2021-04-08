---
description: Événement de traçage réseau Winsock pour l’opération de fermeture du Socket.
ms.assetid: C59B2B51-288A-46C9-B390-26A18DB0C2FB
title: Événement AFD_EVENT_CLOSE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AFD_EVENT_CLOSE
api_type:
- NA
api_location: ''
ms.openlocfilehash: fbc6c63a3084db6a9be0a4b4ea7672d84881a29a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751485"
---
# <a name="afd_event_close-event"></a><span data-ttu-id="accfa-103">Événement de fermeture d' \_ événement AFD \_</span><span class="sxs-lookup"><span data-stu-id="accfa-103">AFD\_EVENT\_CLOSE event</span></span>

<span data-ttu-id="accfa-104">L’événement de **\_ \_ fermeture d’événement AFD** est un événement de traçage réseau Winsock pour l’opération de fermeture de Socket.</span><span class="sxs-lookup"><span data-stu-id="accfa-104">The **AFD\_EVENT\_CLOSE** event is a Winsock network tracing event for socket close operation.</span></span>


```C++
const EVENT_DESCRIPTOR AFD_EVENT_CLOSE = {0x3e9, 0x0, 0x10, 0x4, 0xf, 0x3e9, 0x8000000000000004};
```



## <a name="parameters"></a><span data-ttu-id="accfa-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="accfa-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="accfa-106">*EnterExit*</span><span class="sxs-lookup"><span data-stu-id="accfa-106">*EnterExit*</span></span> 
</dt> <dd>

<span data-ttu-id="accfa-107">Informations sur cet événement.</span><span class="sxs-lookup"><span data-stu-id="accfa-107">Information on this event.</span></span>

<span data-ttu-id="accfa-108">Le tableau suivant répertorie les valeurs possibles pour le paramètre *EnterExit* :</span><span class="sxs-lookup"><span data-stu-id="accfa-108">The following table lists the possible values for the *EnterExit* parameter:</span></span>



| <span data-ttu-id="accfa-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="accfa-109">Value</span></span>                                                                        | <span data-ttu-id="accfa-110">Signification</span><span class="sxs-lookup"><span data-stu-id="accfa-110">Meaning</span></span>                                                                                              |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="accfa-111"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="accfa-111"><dt>0</dt></span></span> </dl> | <span data-ttu-id="accfa-112">Début d’une demande Winsock.</span><span class="sxs-lookup"><span data-stu-id="accfa-112">The start of a Winsock request.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="accfa-113"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="accfa-113"><dt>1</dt></span></span> </dl> | <span data-ttu-id="accfa-114">La demande Winsock est terminée.</span><span class="sxs-lookup"><span data-stu-id="accfa-114">The Winsock request completed.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="accfa-115"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="accfa-115"><dt>2</dt></span></span> </dl> | <span data-ttu-id="accfa-116">Le pilote AFD Winsock a effectué une action interne (en abandonnant une connexion, par exemple).</span><span class="sxs-lookup"><span data-stu-id="accfa-116">The Winsock AFD driver took an internal action (aborting a connection, for example).</span></span><br/>      |
| <dl> <span data-ttu-id="accfa-117"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="accfa-117"><dt>3</dt></span></span> </dl> | <span data-ttu-id="accfa-118">Le pilote TCP/IP a entraîné l’apparition de cet événement.</span><span class="sxs-lookup"><span data-stu-id="accfa-118">The TCP/IP driver caused this event to occur.</span></span> <span data-ttu-id="accfa-119">Cela indique généralement une notification de données.</span><span class="sxs-lookup"><span data-stu-id="accfa-119">This usually indicates a data notification.</span></span><br/> |
| <dl> <span data-ttu-id="accfa-120"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="accfa-120"><dt>4</dt></span></span> </dl> | <span data-ttu-id="accfa-121">Le pilote AFD Winsock a entraîné l’apparition de cet événement (par exemple, la définition d’une option de socket).</span><span class="sxs-lookup"><span data-stu-id="accfa-121">The Winsock AFD driver caused this event to occur (setting a socket option, for example).</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="accfa-122">*Lieu*</span><span class="sxs-lookup"><span data-stu-id="accfa-122">*Location*</span></span> 
</dt> <dd>

<span data-ttu-id="accfa-123">Champ privé utilisé en interne.</span><span class="sxs-lookup"><span data-stu-id="accfa-123">A private field used internally.</span></span>

</dd> <dt>

<span data-ttu-id="accfa-124">*Processus*</span><span class="sxs-lookup"><span data-stu-id="accfa-124">*Process*</span></span> 
</dt> <dd>

<span data-ttu-id="accfa-125">Adresse [EPROCESS](/windows-hardware/drivers/kernel/eprocess) du processus qui possède le socket associé.</span><span class="sxs-lookup"><span data-stu-id="accfa-125">The [EPROCESS](/windows-hardware/drivers/kernel/eprocess) address of the process that owns the related socket.</span></span> <span data-ttu-id="accfa-126">Il s’agit d’une structure opaque qui sert d’objet de processus pour un processus.</span><span class="sxs-lookup"><span data-stu-id="accfa-126">This is an opaque structure that serves as the process object for a process.</span></span> <span data-ttu-id="accfa-127">Pour plus d’informations, consultez la documentation du kit de pilotes Windows pour la structure [EPROCESS](/windows-hardware/drivers/kernel/eprocess) .</span><span class="sxs-lookup"><span data-stu-id="accfa-127">For more information, see the Windows Driver Kit documentation for the [EPROCESS](/windows-hardware/drivers/kernel/eprocess) structure.</span></span>

</dd> <dt>

<span data-ttu-id="accfa-128">*Point de terminaison*</span><span class="sxs-lookup"><span data-stu-id="accfa-128">*Endpoint*</span></span> 
</dt> <dd>

<span data-ttu-id="accfa-129">\_Adresse du point de terminaison AFD du Socket.</span><span class="sxs-lookup"><span data-stu-id="accfa-129">The AFD\_ENDPOINT address of the socket.</span></span>

</dd> <dt>

<span data-ttu-id="accfa-130">*État*</span><span class="sxs-lookup"><span data-stu-id="accfa-130">*Status*</span></span> 
</dt> <dd>

<span data-ttu-id="accfa-131">Code NTSTATUS pour l’opération.</span><span class="sxs-lookup"><span data-stu-id="accfa-131">The NTSTATUS code for the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="accfa-132">Notes</span><span class="sxs-lookup"><span data-stu-id="accfa-132">Remarks</span></span>

<span data-ttu-id="accfa-133">L’événement de **\_ \_ fermeture d’événement AFD** est suivi pour qu’une opération réseau Winsock ferme un Socket.</span><span class="sxs-lookup"><span data-stu-id="accfa-133">The **AFD\_EVENT\_CLOSE** event is traced for a Winsock network operation to close a socket.</span></span> <span data-ttu-id="accfa-134">Le canal de cet événement est Winsock-AFD.</span><span class="sxs-lookup"><span data-stu-id="accfa-134">The channel for this event is Winsock-AFD.</span></span> <span data-ttu-id="accfa-135">Le niveau de cet événement est informatif.</span><span class="sxs-lookup"><span data-stu-id="accfa-135">The level for this event is informational.</span></span>

## <a name="requirements"></a><span data-ttu-id="accfa-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="accfa-136">Requirements</span></span>



| <span data-ttu-id="accfa-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="accfa-137">Requirement</span></span> | <span data-ttu-id="accfa-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="accfa-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="accfa-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="accfa-139">Minimum supported client</span></span><br/> | <span data-ttu-id="accfa-140">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="accfa-140">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="accfa-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="accfa-141">Minimum supported server</span></span><br/> | <span data-ttu-id="accfa-142">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="accfa-142">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="accfa-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="accfa-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="accfa-144">Contrôle du suivi Winsock</span><span class="sxs-lookup"><span data-stu-id="accfa-144">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="accfa-145">**descripteur d’événement \_**</span><span class="sxs-lookup"><span data-stu-id="accfa-145">**EVENT\_DESCRIPTOR**</span></span>](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor)
</dt> <dt>

[<span data-ttu-id="accfa-146">Suivi Winsock</span><span class="sxs-lookup"><span data-stu-id="accfa-146">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="accfa-147">Niveaux de suivi Winsock</span><span class="sxs-lookup"><span data-stu-id="accfa-147">Winsock Tracing Levels</span></span>](winsock-tracing-levels.md)
</dt> <dt>

[<span data-ttu-id="accfa-148">Détails du suivi de modification du catalogue Winsock</span><span class="sxs-lookup"><span data-stu-id="accfa-148">Winsock Catalog Change Tracing Details</span></span>](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

