---
description: Spécifie les caractéristiques précédentes de la source du média.
ms.assetid: 9779f350-60d5-4129-bada-0c4a58f93e6a
title: Attribut MF_EVENT_SOURCE_CHARACTERISTICS_OLD (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cb19505643de064e3aa54abc9e37649ecd97ff9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521477"
---
# <a name="mf_event_source_characteristics_old-attribute"></a><span data-ttu-id="51b54-103">\_ \_ \_ Attribut ancien des caractéristiques \_ de la source d’événement MF</span><span class="sxs-lookup"><span data-stu-id="51b54-103">MF\_EVENT\_SOURCE\_CHARACTERISTICS\_OLD attribute</span></span>

<span data-ttu-id="51b54-104">Spécifie les caractéristiques précédentes de la source du média.</span><span class="sxs-lookup"><span data-stu-id="51b54-104">Specifies the previous characteristics of the media source.</span></span> <span data-ttu-id="51b54-105">Les données d’attribut sont une **opération or au niveau du bit** des indicateurs de l’énumération des [**\_ caractéristiques MFMEDIASOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) .</span><span class="sxs-lookup"><span data-stu-id="51b54-105">The attribute data is a bitwise **OR** of flags from the [**MFMEDIASOURCE\_CHARACTERISTICS**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) enumeration.</span></span>

## <a name="data-type"></a><span data-ttu-id="51b54-106">Type de données</span><span class="sxs-lookup"><span data-stu-id="51b54-106">Data type</span></span>

<span data-ttu-id="51b54-107">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="51b54-107">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="51b54-108">Notes</span><span class="sxs-lookup"><span data-stu-id="51b54-108">Remarks</span></span>

<span data-ttu-id="51b54-109">Cet attribut est utilisé avec l’événement [MESourceCharacteristicsChanged](mesourcecharacteristicschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="51b54-109">This attribute is used with the [MESourceCharacteristicsChanged](mesourcecharacteristicschanged.md) event.</span></span>

<span data-ttu-id="51b54-110">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="51b54-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="51b54-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="51b54-111">Requirements</span></span>



| <span data-ttu-id="51b54-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="51b54-112">Requirement</span></span> | <span data-ttu-id="51b54-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="51b54-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="51b54-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="51b54-114">Minimum supported client</span></span><br/> | <span data-ttu-id="51b54-115">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="51b54-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="51b54-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="51b54-116">Minimum supported server</span></span><br/> | <span data-ttu-id="51b54-117">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="51b54-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="51b54-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="51b54-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="51b54-119"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="51b54-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51b54-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="51b54-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51b54-121">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="51b54-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="51b54-122">Attributs d'événement</span><span class="sxs-lookup"><span data-stu-id="51b54-122">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="51b54-123">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="51b54-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="51b54-124">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="51b54-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="51b54-125">**IMFMediaSource**</span><span class="sxs-lookup"><span data-stu-id="51b54-125">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
</dt> </dl>

 

 




