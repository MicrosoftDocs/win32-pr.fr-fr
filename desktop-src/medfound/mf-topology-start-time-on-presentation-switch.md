---
description: Spécifie l’heure de début des présentations mises en file d’attente après la première présentation.
ms.assetid: 087f5d61-b3e6-4fdf-98e6-b018de7b237f
title: Attribut MF_TOPOLOGY_START_TIME_ON_PRESENTATION_SWITCH (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5f4c50271ad2da9682be9d259ad855352e844af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524079"
---
# <a name="mf_topology_start_time_on_presentation_switch-attribute"></a><span data-ttu-id="32783-103">\_ \_ Heure de début de la topologie MF \_ sur l' \_ \_ attribut de commutateur de présentation \_</span><span class="sxs-lookup"><span data-stu-id="32783-103">MF\_TOPOLOGY\_START\_TIME\_ON\_PRESENTATION\_SWITCH attribute</span></span>

<span data-ttu-id="32783-104">Spécifie l’heure de début des présentations mises en file d’attente après la première présentation.</span><span class="sxs-lookup"><span data-stu-id="32783-104">Specifies the start time for presentations that are queued after the first presentation.</span></span>

## <a name="data-type"></a><span data-ttu-id="32783-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="32783-105">Data type</span></span>

<span data-ttu-id="32783-106">**Int64** stocké comme **UINT64**</span><span class="sxs-lookup"><span data-stu-id="32783-106">**INT64** stored as **UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="32783-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="32783-107">Get/set</span></span>

<span data-ttu-id="32783-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span><span class="sxs-lookup"><span data-stu-id="32783-108">To get this attribute, call [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span></span>

<span data-ttu-id="32783-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span><span class="sxs-lookup"><span data-stu-id="32783-109">To set this attribute, call [**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span></span>

## <a name="applies-to"></a><span data-ttu-id="32783-110">S'applique à</span><span class="sxs-lookup"><span data-stu-id="32783-110">Applies To</span></span>

[<span data-ttu-id="32783-111">**IMFTopology**</span><span class="sxs-lookup"><span data-stu-id="32783-111">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="32783-112">Notes</span><span class="sxs-lookup"><span data-stu-id="32783-112">Remarks</span></span>

<span data-ttu-id="32783-113">Lorsque l’application met en file d’attente la première présentation sur la session multimédia, l’application spécifie l’heure de début dans le paramètre *pvarStartPosition* de la méthode [**IMFMediaSession :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) .</span><span class="sxs-lookup"><span data-stu-id="32783-113">When the application queues the first presentation on the Media Session, the application specifies the start time in the *pvarStartPosition* parameter of the [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) method.</span></span> <span data-ttu-id="32783-114">Toutefois, pour toutes les présentations ultérieures, l’heure de début est indiquée par l' \_ \_ heure de début de la topologie MF \_ \_ sur \_ \_ l’attribut de changement de présentation sur la topologie.</span><span class="sxs-lookup"><span data-stu-id="32783-114">For any subsequent presentations, however, the start time is given by the MF\_TOPOLOGY\_START\_TIME\_ON\_PRESENTATION\_SWITCH attribute on the topology.</span></span> <span data-ttu-id="32783-115">L’heure de début est spécifiée en unités de 100 nanosecondes, par rapport au début de la présentation.</span><span class="sxs-lookup"><span data-stu-id="32783-115">The start time is specified in 100-nanosecond units, relative to the beginning of the presentation.</span></span> <span data-ttu-id="32783-116">Par exemple, si la valeur est 50 millions, la lecture démarre 5 secondes dans la présentation.</span><span class="sxs-lookup"><span data-stu-id="32783-116">For example, if the value is 50000000, playback starts 5 seconds into the presentation.</span></span> <span data-ttu-id="32783-117">Si cet attribut n’est pas défini, l’heure de début par défaut est zéro.</span><span class="sxs-lookup"><span data-stu-id="32783-117">If this attribute is not set, the default start time is zero.</span></span>

<span data-ttu-id="32783-118">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="32783-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="32783-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="32783-119">Requirements</span></span>



| <span data-ttu-id="32783-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="32783-120">Requirement</span></span> | <span data-ttu-id="32783-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="32783-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="32783-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="32783-122">Minimum supported client</span></span><br/> | <span data-ttu-id="32783-123">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="32783-123">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="32783-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="32783-124">Minimum supported server</span></span><br/> | <span data-ttu-id="32783-125">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="32783-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="32783-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="32783-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="32783-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="32783-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32783-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="32783-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32783-129">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="32783-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="32783-130">Attributs de topologie</span><span class="sxs-lookup"><span data-stu-id="32783-130">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 




