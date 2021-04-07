---
description: Spécifie l’état d’une tentative de résolution d’une topologie.
ms.assetid: 7c2410ce-e70b-4303-9dbc-caff4a355d6b
title: Attribut MF_TOPOLOGY_RESOLUTION_STATUS (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddb98db0de67e228606d9f37216d1ea13cbc2f87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863578"
---
# <a name="mf_topology_resolution_status-attribute"></a><span data-ttu-id="ee081-103">\_Attribut état de la résolution de la topologie MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="ee081-103">MF\_TOPOLOGY\_RESOLUTION\_STATUS attribute</span></span>

<span data-ttu-id="ee081-104">Spécifie l’état d’une tentative de résolution d’une topologie.</span><span class="sxs-lookup"><span data-stu-id="ee081-104">Specifies the status of an attempt to resolve a topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="ee081-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="ee081-105">Data type</span></span>

<span data-ttu-id="ee081-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="ee081-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="ee081-107">Notes</span><span class="sxs-lookup"><span data-stu-id="ee081-107">Remarks</span></span>

<span data-ttu-id="ee081-108">Le chargeur de topologie ou la session de média peut définir cet attribut sur une topologie.</span><span class="sxs-lookup"><span data-stu-id="ee081-108">The topology loader or the Media Session might set this attribute on a topology.</span></span> <span data-ttu-id="ee081-109">La valeur de cet attribut est **une opération or au niveau du bit** de l’énumération d' [**indicateurs d’état de \_ résolution de topologie \_ \_ \_ MF**](/windows/desktop/api/mfidl/ne-mfidl-mf_topology_resolution_status_flags) .</span><span class="sxs-lookup"><span data-stu-id="ee081-109">The value of this attribute is a bitwise **OR** of flags from the [**MF\_TOPOLOGY\_RESOLUTION\_STATUS\_FLAGS**](/windows/desktop/api/mfidl/ne-mfidl-mf_topology_resolution_status_flags) enumeration.</span></span>

<span data-ttu-id="ee081-110">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="ee081-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee081-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ee081-111">Requirements</span></span>



| <span data-ttu-id="ee081-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ee081-112">Requirement</span></span> | <span data-ttu-id="ee081-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="ee081-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ee081-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ee081-114">Minimum supported client</span></span><br/> | <span data-ttu-id="ee081-115">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ee081-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ee081-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ee081-116">Minimum supported server</span></span><br/> | <span data-ttu-id="ee081-117">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ee081-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ee081-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="ee081-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee081-119"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee081-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee081-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ee081-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee081-121">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ee081-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ee081-122">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="ee081-122">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="ee081-123">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="ee081-123">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="ee081-124">**IMFTopology**</span><span class="sxs-lookup"><span data-stu-id="ee081-124">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)
</dt> <dt>

[<span data-ttu-id="ee081-125">Attributs de topologie</span><span class="sxs-lookup"><span data-stu-id="ee081-125">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 




