---
description: Spécifie les caractéristiques actuelles de la source du média.
ms.assetid: af2a2b75-cd4e-453c-876e-3be2db695e4e
title: Attribut MF_EVENT_SOURCE_CHARACTERISTICS (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b8c775c0d3471d3d3442e565879ba8b42e07a61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106540827"
---
# <a name="mf_event_source_characteristics-attribute"></a><span data-ttu-id="c15ff-103">Attribut des caractéristiques de la \_ source d’événement MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="c15ff-103">MF\_EVENT\_SOURCE\_CHARACTERISTICS attribute</span></span>

<span data-ttu-id="c15ff-104">Spécifie les caractéristiques actuelles de la source du média.</span><span class="sxs-lookup"><span data-stu-id="c15ff-104">Specifies the current characteristics of the media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="c15ff-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="c15ff-105">Data type</span></span>

<span data-ttu-id="c15ff-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="c15ff-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="c15ff-107">Notes</span><span class="sxs-lookup"><span data-stu-id="c15ff-107">Remarks</span></span>

<span data-ttu-id="c15ff-108">La valeur de cet attribut est **une opération or au niveau du bit** des indicateurs de l’énumération des [**\_ caractéristiques MFMEDIASOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) .</span><span class="sxs-lookup"><span data-stu-id="c15ff-108">The value of this attribute is a bitwise **OR** of flags from the [**MFMEDIASOURCE\_CHARACTERISTICS**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) enumeration.</span></span>

<span data-ttu-id="c15ff-109">Cet attribut est utilisé avec l’événement [MESourceCharacteristicsChanged](mesourcecharacteristicschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="c15ff-109">This attribute is used with the [MESourceCharacteristicsChanged](mesourcecharacteristicschanged.md) event.</span></span>

<span data-ttu-id="c15ff-110">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="c15ff-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="c15ff-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c15ff-111">Requirements</span></span>



| <span data-ttu-id="c15ff-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c15ff-112">Requirement</span></span> | <span data-ttu-id="c15ff-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="c15ff-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c15ff-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c15ff-114">Minimum supported client</span></span><br/> | <span data-ttu-id="c15ff-115">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c15ff-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c15ff-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c15ff-116">Minimum supported server</span></span><br/> | <span data-ttu-id="c15ff-117">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c15ff-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c15ff-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="c15ff-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="c15ff-119"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c15ff-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c15ff-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c15ff-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c15ff-121">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c15ff-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c15ff-122">Attributs d'événement</span><span class="sxs-lookup"><span data-stu-id="c15ff-122">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="c15ff-123">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="c15ff-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="c15ff-124">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="c15ff-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




