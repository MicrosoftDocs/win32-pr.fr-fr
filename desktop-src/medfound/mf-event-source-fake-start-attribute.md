---
description: Spécifie si la topologie du segment actuel est vide.
ms.assetid: efd497dc-affc-4453-975c-09c5dca06374
title: Attribut MF_EVENT_SOURCE_FAKE_START (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae47bbfdedb7535ff46763ad5bc36f552ffe4780
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869118"
---
# <a name="mf_event_source_fake_start-attribute"></a><span data-ttu-id="8b35c-103">\_Attribut de \_ \_ début factice de source d’événement MF \_</span><span class="sxs-lookup"><span data-stu-id="8b35c-103">MF\_EVENT\_SOURCE\_FAKE\_START attribute</span></span>

<span data-ttu-id="8b35c-104">Spécifie si la topologie du segment actuel est vide.</span><span class="sxs-lookup"><span data-stu-id="8b35c-104">Specifies whether the current segment topology is empty.</span></span>

## <a name="data-type"></a><span data-ttu-id="8b35c-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="8b35c-105">Data type</span></span>

<span data-ttu-id="8b35c-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="8b35c-106">**UINT32**</span></span>

<span data-ttu-id="8b35c-107">Traiter en tant que valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="8b35c-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b35c-108">Notes</span><span class="sxs-lookup"><span data-stu-id="8b35c-108">Remarks</span></span>

<span data-ttu-id="8b35c-109">Cet attribut est utilisé avec l’événement [MESourceStarted](mesourcestarted.md) .</span><span class="sxs-lookup"><span data-stu-id="8b35c-109">This attribute is used with the [MESourceStarted](mesourcestarted.md) event.</span></span>

<span data-ttu-id="8b35c-110">La source de Sequencer affecte la **valeur true** à cet attribut si la topologie du segment actuel est vide.</span><span class="sxs-lookup"><span data-stu-id="8b35c-110">The sequencer source sets this attribute to **TRUE** if the current segment topology is empty.</span></span> <span data-ttu-id="8b35c-111">Si cet attribut a la **valeur true**, la lecture n’a pas encore démarré.</span><span class="sxs-lookup"><span data-stu-id="8b35c-111">If this attribute is **TRUE**, playback has not started yet.</span></span> <span data-ttu-id="8b35c-112">La valeur par défaut de cet attribut est **false**.</span><span class="sxs-lookup"><span data-stu-id="8b35c-112">The default value of this attribute is **FALSE**.</span></span>

<span data-ttu-id="8b35c-113">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="8b35c-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b35c-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8b35c-114">Requirements</span></span>



| <span data-ttu-id="8b35c-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8b35c-115">Requirement</span></span> | <span data-ttu-id="8b35c-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="8b35c-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8b35c-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8b35c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8b35c-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8b35c-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8b35c-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8b35c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8b35c-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8b35c-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8b35c-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="8b35c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b35c-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b35c-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b35c-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b35c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b35c-124">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8b35c-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="8b35c-125">Attributs d'événement</span><span class="sxs-lookup"><span data-stu-id="8b35c-125">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="8b35c-126">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="8b35c-126">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="8b35c-127">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="8b35c-127">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




