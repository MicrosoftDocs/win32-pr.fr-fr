---
description: Contient un pointeur vers le descripteur de présentation pour la source du média.
ms.assetid: 4f2c1ad8-fda9-482f-b82a-9838d15d2785
title: Attribut MF_TOPONODE_PRESENTATION_DESCRIPTOR (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0d95fae4f2c4d4a482c2a62d57e0835ea4f1c36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753157"
---
# <a name="mf_toponode_presentation_descriptor-attribute"></a><span data-ttu-id="b5e91-103">\_Attribut de \_ descripteur de présentation TOPONODE MF \_</span><span class="sxs-lookup"><span data-stu-id="b5e91-103">MF\_TOPONODE\_PRESENTATION\_DESCRIPTOR attribute</span></span>

<span data-ttu-id="b5e91-104">Contient un pointeur vers le descripteur de présentation pour la source du média.</span><span class="sxs-lookup"><span data-stu-id="b5e91-104">Contains a pointer to the presentation descriptor for the media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="b5e91-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="b5e91-105">Data type</span></span>

<span data-ttu-id="b5e91-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="b5e91-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="b5e91-107">Notes</span><span class="sxs-lookup"><span data-stu-id="b5e91-107">Remarks</span></span>

<span data-ttu-id="b5e91-108">Cet attribut s’applique aux nœuds sources (_ \* MF \_ Topology \_ SOURCESTREAM \_ node \* \*).</span><span class="sxs-lookup"><span data-stu-id="b5e91-108">This attribute applies to source nodes (_\*MF\_TOPOLOGY\_SOURCESTREAM\_NODE\*\*).</span></span>

<span data-ttu-id="b5e91-109">La valeur de l’attribut est un pointeur vers l’interface [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) du descripteur de présentation.</span><span class="sxs-lookup"><span data-stu-id="b5e91-109">The value of the attribute is a pointer to the presentation descriptor's [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) interface.</span></span> <span data-ttu-id="b5e91-110">Cet attribut est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="b5e91-110">This attribute is required.</span></span>

<span data-ttu-id="b5e91-111">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="b5e91-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5e91-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b5e91-112">Requirements</span></span>



| <span data-ttu-id="b5e91-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b5e91-113">Requirement</span></span> | <span data-ttu-id="b5e91-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5e91-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b5e91-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5e91-115">Minimum supported client</span></span><br/> | <span data-ttu-id="b5e91-116">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b5e91-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b5e91-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5e91-117">Minimum supported server</span></span><br/> | <span data-ttu-id="b5e91-118">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b5e91-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b5e91-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="b5e91-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5e91-120"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5e91-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5e91-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5e91-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5e91-122">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b5e91-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b5e91-123">**IMFAttributes::GetUnknown**</span><span class="sxs-lookup"><span data-stu-id="b5e91-123">**IMFAttributes::GetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[<span data-ttu-id="b5e91-124">**IMFAttributes :: Setunknown,**</span><span class="sxs-lookup"><span data-stu-id="b5e91-124">**IMFAttributes::SetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[<span data-ttu-id="b5e91-125">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="b5e91-125">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="b5e91-126">Attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b5e91-126">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 




