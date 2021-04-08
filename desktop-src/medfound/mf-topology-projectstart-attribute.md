---
description: Spécifie l’heure d’arrêt d’une topologie, par rapport au début de la première topologie dans la séquence.
ms.assetid: 7669f97e-87ad-4a64-a2a5-62b8ce450d80
title: Attribut MF_TOPOLOGY_PROJECTSTART (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34a7e3d50bd89e0fdfc032f9854c1a183276f04a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863581"
---
# <a name="mf_topology_projectstart-attribute"></a><span data-ttu-id="02f40-103">\_Attribut PROJECTSTART de la topologie MF \_</span><span class="sxs-lookup"><span data-stu-id="02f40-103">MF\_TOPOLOGY\_PROJECTSTART attribute</span></span>

<span data-ttu-id="02f40-104">Spécifie l’heure d’arrêt d’une topologie, par rapport au début de la première topologie dans la séquence.</span><span class="sxs-lookup"><span data-stu-id="02f40-104">Specifies the stop time for a topology, relative to the start of the first topology in the sequence.</span></span>

## <a name="data-type"></a><span data-ttu-id="02f40-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="02f40-105">Data type</span></span>

<span data-ttu-id="02f40-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="02f40-106">**UINT64**</span></span>

<span data-ttu-id="02f40-107">Traiter en tant que valeur **LongLong** .</span><span class="sxs-lookup"><span data-stu-id="02f40-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="02f40-108">Notes</span><span class="sxs-lookup"><span data-stu-id="02f40-108">Remarks</span></span>

<span data-ttu-id="02f40-109">La valeur est donnée en unités de nanosecondes de 100.</span><span class="sxs-lookup"><span data-stu-id="02f40-109">The value is given in units of 100 nanoseconds.</span></span>

<span data-ttu-id="02f40-110">Si la session multimédia a été créée avec l’attribut d' [**\_ \_ \_ heure globale de session MF**](mf-session-global-time-attribute.md) de la **valeur true**, toutes les topologies doivent contenir l’attribut **\_ \_ PROJECTSTART de topologie MF** .</span><span class="sxs-lookup"><span data-stu-id="02f40-110">If the Media Session was created with the [**MF\_SESSION\_GLOBAL\_TIME**](mf-session-global-time-attribute.md) attribute equal to **TRUE**, all topologies must contain the **MF\_TOPOLOGY\_PROJECTSTART** attribute.</span></span> <span data-ttu-id="02f40-111">Dans le cas contraire, les topologies ne doivent pas contenir l’attribut **\_ \_ PROJECTSTART** de topologie MF.</span><span class="sxs-lookup"><span data-stu-id="02f40-111">Otherwise, topologies must not contain the **MF\_TOPOLOGY\_PROJECTSTART** attribute.</span></span> <span data-ttu-id="02f40-112">Pour plus d’informations, consultez [durée de présentation des séquences](sequence-presentation-times.md).</span><span class="sxs-lookup"><span data-stu-id="02f40-112">For more information, see [Sequence Presentation Times](sequence-presentation-times.md).</span></span>

<span data-ttu-id="02f40-113">Cet attribut est une valeur signée, bien qu’il soit stocké en tant que **UINT64**.</span><span class="sxs-lookup"><span data-stu-id="02f40-113">This attribute is a signed value, although it is stored as a **UINT64**.</span></span>

<span data-ttu-id="02f40-114">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="02f40-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="02f40-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="02f40-115">Requirements</span></span>



| <span data-ttu-id="02f40-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="02f40-116">Requirement</span></span> | <span data-ttu-id="02f40-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="02f40-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="02f40-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="02f40-118">Minimum supported client</span></span><br/> | <span data-ttu-id="02f40-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="02f40-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="02f40-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="02f40-120">Minimum supported server</span></span><br/> | <span data-ttu-id="02f40-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="02f40-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="02f40-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="02f40-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="02f40-123"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="02f40-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02f40-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="02f40-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02f40-125">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="02f40-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="02f40-126">Durée des présentations de séquence</span><span class="sxs-lookup"><span data-stu-id="02f40-126">Sequence Presentation Times</span></span>](sequence-presentation-times.md)
</dt> <dt>

[<span data-ttu-id="02f40-127">Attributs de topologie</span><span class="sxs-lookup"><span data-stu-id="02f40-127">Topology Attributes</span></span>](topology-attributes.md)
</dt> <dt>

[<span data-ttu-id="02f40-128">**IMFAttributes::GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="02f40-128">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="02f40-129">**IMFAttributes::SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="02f40-129">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="02f40-130">**\_PROJECTSTOP de topologie \_ MF**</span><span class="sxs-lookup"><span data-stu-id="02f40-130">**MF\_TOPOLOGY\_PROJECTSTOP**</span></span>](mf-topology-projectstop-attribute.md)
</dt> </dl>

 

 




