---
description: Contient un pointeur vers le descripteur de présentation à partir du chemin d’accès du média protégé (PMP).
ms.assetid: cf12552e-0963-46fa-9a26-44dd601ab68c
title: Attribut MF_PD_APP_CONTEXT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8971ead121407ff1a7793c16b14f6b02d3dd102e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209789"
---
# <a name="mf_pd_app_context-attribute"></a><span data-ttu-id="b530a-103">Attribut de contexte de l' \_ application MF PD \_ \_</span><span class="sxs-lookup"><span data-stu-id="b530a-103">MF\_PD\_APP\_CONTEXT attribute</span></span>

<span data-ttu-id="b530a-104">Contient un pointeur vers le descripteur de présentation à partir du chemin d’accès du média protégé (PMP).</span><span class="sxs-lookup"><span data-stu-id="b530a-104">Contains a pointer to the presentation descriptor from the Protected Media Path (PMP).</span></span>

## <a name="data-type"></a><span data-ttu-id="b530a-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="b530a-105">Data type</span></span>

<span data-ttu-id="b530a-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="b530a-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="b530a-107">Notes</span><span class="sxs-lookup"><span data-stu-id="b530a-107">Remarks</span></span>

<span data-ttu-id="b530a-108">Le proxy de source multimédia, qui est créé dans le processus PMP, utilise cet attribut pour stocker le descripteur de présentation distant sur le descripteur de présentation de l’application.</span><span class="sxs-lookup"><span data-stu-id="b530a-108">The media source proxy, which is created in the PMP process, uses this attribute to store the remote presentation descriptor on the application's presentation descriptor.</span></span>

<span data-ttu-id="b530a-109">La valeur de cet attribut est un pointeur vers l’interface [_ *IMFPresentationDescriptor* \*](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) .</span><span class="sxs-lookup"><span data-stu-id="b530a-109">The value of this attribute is a pointer to the [_ *IMFPresentationDescriptor*\*](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) interface.</span></span>

<span data-ttu-id="b530a-110">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="b530a-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b530a-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b530a-111">Requirements</span></span>



| <span data-ttu-id="b530a-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b530a-112">Requirement</span></span> | <span data-ttu-id="b530a-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="b530a-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b530a-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b530a-114">Minimum supported client</span></span><br/> | <span data-ttu-id="b530a-115">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b530a-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b530a-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b530a-116">Minimum supported server</span></span><br/> | <span data-ttu-id="b530a-117">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b530a-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b530a-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="b530a-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="b530a-119"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b530a-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b530a-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b530a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b530a-121">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b530a-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b530a-122">**IMFAttributes::GetUnknown**</span><span class="sxs-lookup"><span data-stu-id="b530a-122">**IMFAttributes::GetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[<span data-ttu-id="b530a-123">**IMFAttributes :: Setunknown,**</span><span class="sxs-lookup"><span data-stu-id="b530a-123">**IMFAttributes::SetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[<span data-ttu-id="b530a-124">Attributs du descripteur de présentation</span><span class="sxs-lookup"><span data-stu-id="b530a-124">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




