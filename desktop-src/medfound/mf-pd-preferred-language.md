---
description: Contient le langage RFC 1766 par défaut de la source du média.
ms.assetid: 30f99804-6aea-473b-9bbf-e8c715501391
title: Attribut MF_PD_PREFERRED_LANGUAGE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81bb121c7181724ef06b3e8fe9239342a140104a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210490"
---
# <a name="mf_pd_preferred_language-attribute"></a><span data-ttu-id="b49bd-103">\_Attribut de \_ langue par défaut MF PD \_</span><span class="sxs-lookup"><span data-stu-id="b49bd-103">MF\_PD\_PREFERRED\_LANGUAGE attribute</span></span>

<span data-ttu-id="b49bd-104">Contient le langage RFC 1766 par défaut de la source du média.</span><span class="sxs-lookup"><span data-stu-id="b49bd-104">Contains the preferred RFC 1766 language of the media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="b49bd-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="b49bd-105">Data type</span></span>

<span data-ttu-id="b49bd-106">**WCHAR**</span><span class="sxs-lookup"><span data-stu-id="b49bd-106">**WCHAR**</span></span>

## <a name="getset"></a><span data-ttu-id="b49bd-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="b49bd-107">Get/set</span></span>

<span data-ttu-id="b49bd-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="b49bd-108">To get this attribute, call [**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="b49bd-109">Pour définir cet attribut, appelez [**IMFAttributes :: Settring**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="b49bd-109">To set this attribute, call [**IMFAttributes::Settring**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="applies-to"></a><span data-ttu-id="b49bd-110">S’applique à</span><span class="sxs-lookup"><span data-stu-id="b49bd-110">Applies to</span></span>

[<span data-ttu-id="b49bd-111">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="b49bd-111">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a><span data-ttu-id="b49bd-112">Notes</span><span class="sxs-lookup"><span data-stu-id="b49bd-112">Remarks</span></span>

<span data-ttu-id="b49bd-113">L' \_ attribut de \_ langue par défaut MF PD \_ est facultatif.</span><span class="sxs-lookup"><span data-stu-id="b49bd-113">The MF\_PD\_PREFERRED\_LANGUAGE attribute is optional.</span></span> <span data-ttu-id="b49bd-114">Une application peut définir cet attribut sur une source de média (par exemple, une source réseau) pour spécifier sa langue par défaut.</span><span class="sxs-lookup"><span data-stu-id="b49bd-114">An application can set this attribute on a media source (such as a network source) to specify its preferred language.</span></span>

<span data-ttu-id="b49bd-115">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="b49bd-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b49bd-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b49bd-116">Requirements</span></span>



| <span data-ttu-id="b49bd-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b49bd-117">Requirement</span></span> | <span data-ttu-id="b49bd-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="b49bd-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b49bd-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b49bd-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b49bd-120">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="b49bd-120">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="b49bd-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b49bd-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b49bd-122">Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="b49bd-122">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="b49bd-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="b49bd-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b49bd-124"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b49bd-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b49bd-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b49bd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b49bd-126">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b49bd-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b49bd-127">Attributs du descripteur de présentation</span><span class="sxs-lookup"><span data-stu-id="b49bd-127">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




