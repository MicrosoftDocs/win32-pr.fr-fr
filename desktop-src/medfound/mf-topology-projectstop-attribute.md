---
description: Spécifie l’heure de début d’une topologie, par rapport au début de la première topologie dans la séquence.
ms.assetid: 1ca3709e-88ea-40ca-8da4-c2259365122b
title: Attribut MF_TOPOLOGY_PROJECTSTOP (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5730791440131cd9efdbbb94ce15a598051f1e71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528233"
---
# <a name="mf_topology_projectstop-attribute"></a><span data-ttu-id="acbd9-103">\_Attribut PROJECTSTOP de la topologie MF \_</span><span class="sxs-lookup"><span data-stu-id="acbd9-103">MF\_TOPOLOGY\_PROJECTSTOP attribute</span></span>

<span data-ttu-id="acbd9-104">Spécifie l’heure de début d’une topologie, par rapport au début de la première topologie dans la séquence.</span><span class="sxs-lookup"><span data-stu-id="acbd9-104">Specifies the start time for a topology, relative to the start of the first topology in the sequence.</span></span>

## <a name="data-type"></a><span data-ttu-id="acbd9-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="acbd9-105">Data type</span></span>

<span data-ttu-id="acbd9-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="acbd9-106">**UINT64**</span></span>

<span data-ttu-id="acbd9-107">Traiter en tant que valeur **LongLong** .</span><span class="sxs-lookup"><span data-stu-id="acbd9-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="acbd9-108">Notes</span><span class="sxs-lookup"><span data-stu-id="acbd9-108">Remarks</span></span>

<span data-ttu-id="acbd9-109">La valeur est donnée en unités de nanosecondes de 100.</span><span class="sxs-lookup"><span data-stu-id="acbd9-109">The value is given in units of 100 nanoseconds.</span></span>

<span data-ttu-id="acbd9-110">Si la session multimédia a été créée avec l’attribut d' [**\_ \_ \_ heure globale de session MF**](mf-session-global-time-attribute.md) de la **valeur true**, toutes les topologies doivent contenir l’attribut **\_ \_ PROJECTSTOP de topologie MF** .</span><span class="sxs-lookup"><span data-stu-id="acbd9-110">If the Media Session was created with the [**MF\_SESSION\_GLOBAL\_TIME**](mf-session-global-time-attribute.md) attribute equal to **TRUE**, all topologies must contain the **MF\_TOPOLOGY\_PROJECTSTOP** attribute.</span></span> <span data-ttu-id="acbd9-111">Dans le cas contraire, les topologies ne doivent pas contenir l’attribut **\_ \_ PROJECTSTOP** de topologie MF.</span><span class="sxs-lookup"><span data-stu-id="acbd9-111">Otherwise, topologies must not contain the **MF\_TOPOLOGY\_PROJECTSTOP** attribute.</span></span> <span data-ttu-id="acbd9-112">Pour plus d’informations, consultez [durée de présentation des séquences](sequence-presentation-times.md).</span><span class="sxs-lookup"><span data-stu-id="acbd9-112">For more information, see [Sequence Presentation Times](sequence-presentation-times.md).</span></span>

<span data-ttu-id="acbd9-113">Cet attribut est une valeur signée, bien qu’il soit stocké en tant que **UINT64**.</span><span class="sxs-lookup"><span data-stu-id="acbd9-113">This attribute is a signed value, although it is stored as a **UINT64**.</span></span>

<span data-ttu-id="acbd9-114">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="acbd9-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="acbd9-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="acbd9-115">Requirements</span></span>



| <span data-ttu-id="acbd9-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="acbd9-116">Requirement</span></span> | <span data-ttu-id="acbd9-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="acbd9-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="acbd9-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="acbd9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="acbd9-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="acbd9-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="acbd9-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="acbd9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="acbd9-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="acbd9-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="acbd9-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="acbd9-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="acbd9-123"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="acbd9-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="acbd9-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="acbd9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acbd9-125">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="acbd9-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="acbd9-126">Durée des présentations de séquence</span><span class="sxs-lookup"><span data-stu-id="acbd9-126">Sequence Presentation Times</span></span>](sequence-presentation-times.md)
</dt> <dt>

[<span data-ttu-id="acbd9-127">Attributs de topologie</span><span class="sxs-lookup"><span data-stu-id="acbd9-127">Topology Attributes</span></span>](topology-attributes.md)
</dt> <dt>

[<span data-ttu-id="acbd9-128">**IMFAttributes::GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="acbd9-128">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="acbd9-129">**IMFAttributes::SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="acbd9-129">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="acbd9-130">**\_PROJECTSTART de topologie \_ MF**</span><span class="sxs-lookup"><span data-stu-id="acbd9-130">**MF\_TOPOLOGY\_PROJECTSTART**</span></span>](mf-topology-projectstart-attribute.md)
</dt> </dl>

 

 




