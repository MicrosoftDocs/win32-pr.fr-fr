---
description: Contient un pointeur vers l’objet proxy pour le descripteur de présentation des applications.
ms.assetid: 0cd83204-0d32-417c-8911-1d3358eb0802
title: Attribut MF_PD_PMPHOST_CONTEXT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70e8903e438a4649ae43d7aa2072e5a5146e3126
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104393704"
---
# <a name="mf_pd_pmphost_context-attribute"></a><span data-ttu-id="66eb9-103">\_Attribut de contexte MF PD \_ PMPHOST \_</span><span class="sxs-lookup"><span data-stu-id="66eb9-103">MF\_PD\_PMPHOST\_CONTEXT attribute</span></span>

<span data-ttu-id="66eb9-104">Contient un pointeur vers l’objet proxy pour le descripteur de présentation de l’application.</span><span class="sxs-lookup"><span data-stu-id="66eb9-104">Contains a pointer to the proxy object for the application's presentation descriptor.</span></span>

## <a name="data-type"></a><span data-ttu-id="66eb9-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="66eb9-105">Data type</span></span>

<span data-ttu-id="66eb9-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="66eb9-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="66eb9-107">Notes</span><span class="sxs-lookup"><span data-stu-id="66eb9-107">Remarks</span></span>

<span data-ttu-id="66eb9-108">L’hôte PMP (Protected Media Path) utilise cet attribut pour stocker le descripteur de présentation de l’application sur le descripteur de présentation distant.</span><span class="sxs-lookup"><span data-stu-id="66eb9-108">The Protected Media Path (PMP) host uses this attribute to store the application's presentation descriptor on the remote presentation descriptor.</span></span> <span data-ttu-id="66eb9-109">La valeur de l’attribut est un pointeur vers l’interface [_ *IMFRemoteProxy* \*](/windows/desktop/api/mfidl/nn-mfidl-imfremoteproxy) .</span><span class="sxs-lookup"><span data-stu-id="66eb9-109">The attribute value is a pointer to the [_ *IMFRemoteProxy*\*](/windows/desktop/api/mfidl/nn-mfidl-imfremoteproxy) interface.</span></span>

<span data-ttu-id="66eb9-110">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="66eb9-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="66eb9-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="66eb9-111">Requirements</span></span>



| <span data-ttu-id="66eb9-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="66eb9-112">Requirement</span></span> | <span data-ttu-id="66eb9-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="66eb9-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="66eb9-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66eb9-114">Minimum supported client</span></span><br/> | <span data-ttu-id="66eb9-115">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="66eb9-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="66eb9-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66eb9-116">Minimum supported server</span></span><br/> | <span data-ttu-id="66eb9-117">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="66eb9-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="66eb9-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="66eb9-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="66eb9-119"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="66eb9-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66eb9-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="66eb9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66eb9-121">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="66eb9-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="66eb9-122">**IMFAttributes::GetUnknown**</span><span class="sxs-lookup"><span data-stu-id="66eb9-122">**IMFAttributes::GetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[<span data-ttu-id="66eb9-123">**IMFAttributes :: Setunknown,**</span><span class="sxs-lookup"><span data-stu-id="66eb9-123">**IMFAttributes::SetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[<span data-ttu-id="66eb9-124">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="66eb9-124">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="66eb9-125">Attributs du descripteur de présentation</span><span class="sxs-lookup"><span data-stu-id="66eb9-125">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




