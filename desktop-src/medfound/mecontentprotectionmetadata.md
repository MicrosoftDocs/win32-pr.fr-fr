---
description: Le flux de médias utilise cet événement pour envoyer des métadonnées spécifiques du système de protection au décodeur.
ms.assetid: 249446CA-AEF7-41A1-98EB-0B9392AE4AD8
title: Événement MEContentProtectionMetadata (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dd72289a900b9c9b96fe9a64d427dab13110d66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863178"
---
# <a name="mecontentprotectionmetadata-event"></a><span data-ttu-id="95f15-103">Événement MEContentProtectionMetadata</span><span class="sxs-lookup"><span data-stu-id="95f15-103">MEContentProtectionMetadata event</span></span>

<span data-ttu-id="95f15-104">Le flux de médias utilise cet événement pour envoyer des métadonnées spécifiques du système de protection au décodeur.</span><span class="sxs-lookup"><span data-stu-id="95f15-104">Media Stream uses this event to send protection system specific metadata to the decoder.</span></span>

## <a name="event-values"></a><span data-ttu-id="95f15-105">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="95f15-105">Event values</span></span>

<span data-ttu-id="95f15-106">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="95f15-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="95f15-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="95f15-107">VARTYPE</span></span>              | <span data-ttu-id="95f15-108">Description</span><span class="sxs-lookup"><span data-stu-id="95f15-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="95f15-109">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="95f15-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="95f15-110">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="95f15-110">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="95f15-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="95f15-111">Attributes</span></span>

<span data-ttu-id="95f15-112">Les attributs suivants sont définis pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="95f15-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="95f15-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="95f15-113">Attribute</span></span>                                                                                              | <span data-ttu-id="95f15-114">Description</span><span class="sxs-lookup"><span data-stu-id="95f15-114">Description</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="95f15-115">\_keyData \_ de \_ métadonnées de flux d’événements MF \_</span><span class="sxs-lookup"><span data-stu-id="95f15-115">MF\_EVENT\_STREAM\_METADATA\_KEYDATA</span></span>](mf-event-stream-metadata-keydata.md)<br/>                | <span data-ttu-id="95f15-116">Il s’agit d’un attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="95f15-116">This is an optional attribute.</span></span> <span data-ttu-id="95f15-117">Données spécifiques au système de protection.</span><span class="sxs-lookup"><span data-stu-id="95f15-117">Protection system specific data.</span></span><br/> <br/>              |
| [<span data-ttu-id="95f15-118">\_contenu des \_ métadonnées du flux d’événements MF \_ \_ \_ KEYIDS</span><span class="sxs-lookup"><span data-stu-id="95f15-118">MF\_EVENT\_STREAM\_METADATA\_CONTENT\_KEYIDS</span></span>](mf-event-stream-metadata-content-keyids.md)<br/> | <span data-ttu-id="95f15-119">ID de la clé de contenu à laquelle l’événement est associé.</span><span class="sxs-lookup"><span data-stu-id="95f15-119">Content key IDs which the event is associated with.</span></span><br/> <br/>                          |
| [<span data-ttu-id="95f15-120">\_métadonnées de flux d’événements MF \_ \_ \_ SYSTEMID</span><span class="sxs-lookup"><span data-stu-id="95f15-120">MF\_EVENT\_STREAM\_METADATA\_SYSTEMID</span></span>](mf-event-stream-metadata-systemid.md)<br/>              | <span data-ttu-id="95f15-121">Il s’agit d’un attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="95f15-121">This is an optional attribute.</span></span> <span data-ttu-id="95f15-122">ID système pour lequel les données de clé sont destinées.</span><span class="sxs-lookup"><span data-stu-id="95f15-122">System ID for which the key data is intended.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="95f15-123">Notes</span><span class="sxs-lookup"><span data-stu-id="95f15-123">Remarks</span></span>

<span data-ttu-id="95f15-124">Cet événement est utilisé, par exemple, pour l’événement de rotation de clé communiquant.</span><span class="sxs-lookup"><span data-stu-id="95f15-124">This event is used, for example, for communicating key rotation event.</span></span> <span data-ttu-id="95f15-125">Dans ce cas, il doit être envoyé le plus tôt possible pour permettre au décodeur de se préparer avant même que les échantillons chiffrés avec le nouvel ID de clé commencent à arriver.</span><span class="sxs-lookup"><span data-stu-id="95f15-125">In this case it should be sent as early as possible to give the decoder time to prepare itself before samples encrypted with the new key ID start arriving.</span></span>

## <a name="requirements"></a><span data-ttu-id="95f15-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="95f15-126">Requirements</span></span>



| <span data-ttu-id="95f15-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="95f15-127">Requirement</span></span> | <span data-ttu-id="95f15-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="95f15-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95f15-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="95f15-129">Minimum supported client</span></span><br/> | <span data-ttu-id="95f15-130">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="95f15-130">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="95f15-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="95f15-131">Minimum supported server</span></span><br/> | <span data-ttu-id="95f15-132">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="95f15-132">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="95f15-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="95f15-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="95f15-134"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="95f15-134"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95f15-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="95f15-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95f15-136">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="95f15-136">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




