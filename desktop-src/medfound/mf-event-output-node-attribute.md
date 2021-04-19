---
description: Identifie le nœud de topologie d’un récepteur de flux.
ms.assetid: 9aa6ca66-5122-4d05-94b9-32be194e9eb3
title: Attribut MF_EVENT_OUTPUT_NODE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02c484ea55841f4057bf0855dd51b90db951acb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518383"
---
# <a name="mf_event_output_node-attribute"></a><span data-ttu-id="05edc-103">\_Attribut de \_ nœud de sortie d’événement MF \_</span><span class="sxs-lookup"><span data-stu-id="05edc-103">MF\_EVENT\_OUTPUT\_NODE attribute</span></span>

<span data-ttu-id="05edc-104">Identifie le nœud de topologie d’un récepteur de flux.</span><span class="sxs-lookup"><span data-stu-id="05edc-104">Identifies the topology node for a stream sink.</span></span>

## <a name="data-type"></a><span data-ttu-id="05edc-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="05edc-105">Data type</span></span>

<span data-ttu-id="05edc-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="05edc-106">**UINT64**</span></span>

<span data-ttu-id="05edc-107">Traiter en tant que [**TOPOID**](topoid.md).</span><span class="sxs-lookup"><span data-stu-id="05edc-107">Treat as [**TOPOID**](topoid.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="05edc-108">Notes</span><span class="sxs-lookup"><span data-stu-id="05edc-108">Remarks</span></span>

<span data-ttu-id="05edc-109">La valeur de cet attribut est un identificateur de nœud pour un nœud de sortie sur la topologie actuelle.</span><span class="sxs-lookup"><span data-stu-id="05edc-109">The value of this attribute is a node identifier for an output node on the current topology.</span></span> <span data-ttu-id="05edc-110">Pour obtenir un pointeur vers le nœud associé, appelez [**IMFTopology :: GetNodeByID**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getnodebyid) sur la topologie.</span><span class="sxs-lookup"><span data-stu-id="05edc-110">To get a pointer to the associated node, call [**IMFTopology::GetNodeByID**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getnodebyid) on the topology.</span></span>

<span data-ttu-id="05edc-111">Cet attribut est utilisé avec les événements suivants :</span><span class="sxs-lookup"><span data-stu-id="05edc-111">This attribute is used with the following events:</span></span>

-   [<span data-ttu-id="05edc-112">MESessionStreamSinkFormatChanged</span><span class="sxs-lookup"><span data-stu-id="05edc-112">MESessionStreamSinkFormatChanged</span></span>](mesessionstreamsinkformatchanged.md)
-   [<span data-ttu-id="05edc-113">MESinkInvalidated</span><span class="sxs-lookup"><span data-stu-id="05edc-113">MESinkInvalidated</span></span>](mesinkinvalidated.md)

<span data-ttu-id="05edc-114">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="05edc-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="05edc-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="05edc-115">Requirements</span></span>



| <span data-ttu-id="05edc-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="05edc-116">Requirement</span></span> | <span data-ttu-id="05edc-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="05edc-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="05edc-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05edc-118">Minimum supported client</span></span><br/> | <span data-ttu-id="05edc-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="05edc-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="05edc-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05edc-120">Minimum supported server</span></span><br/> | <span data-ttu-id="05edc-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="05edc-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="05edc-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="05edc-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="05edc-123"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="05edc-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05edc-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="05edc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05edc-125">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="05edc-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="05edc-126">Attributs d'événement</span><span class="sxs-lookup"><span data-stu-id="05edc-126">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="05edc-127">**IMFAttributes::GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="05edc-127">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="05edc-128">**IMFAttributes::SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="05edc-128">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




